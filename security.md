# Security
This section gives a cyber security risk assessment for the company and recommended security controls.

[Risk Assesment](#risk-assessment) | [Security Controls](#security-controls) | [Plan](./plan.md) | [Network Design](./network.md) | [Cloud Services](./cloud.md) | [Ethics](./ethics.md) | [Reflection](./reflection.md) | [Return to index](./README.md)

---

## Risk Assessment

[View risk assessment spreadsheet](./risk-assessment.xlsx)

A mini cyber security risk assessment was conducted for the Truelec network using a **Threat–Vulnerability–Asset (TVA)** methodology, consistent with the risk assessment process taught in this unit. The assessment was completed using the provided Excel risk assessment template and follows a structured approach that links each threat to a specific vulnerability and affected asset.

### Assets considered
The assessment included assets from **all required asset types**, as documented in the Assets Register sheet of the spreadsheet:

- **Hardware:** HQ Edge Router (HW-01), HQ Core Switch (HW-02), Application Servers (HW-03), Branch Router (HW-04), WiFi Access Points (HW-05), CCTV System (HW-06)  
- **Software:** Booking Application (SW-01), Windows Server OS (SW-02)  
- **Network/Service:** WAN Links (NW-01), Corporate WiFi (NW-02)  
- **People:** IT Administrators (PE-01), Branch Employees (PE-02)  
- **Data (at least four – requirement satisfied):** Customer Booking Data (DA-01), Employee Personal Data (DA-02), Financial Records (DA-03), CCTV Footage (DA-04)

### Threat coverage
The assessment considered **all 12 information security threats** from the unit’s threat catalogue: Malware, Phishing, Ransomware, Insider Misuse, Physical Theft/Damage, Unauthorised Access, Network Failure, Data Leakage, Human Error, Denial of Service (DoS), Hardware Failure, and Software Failure. This exceeds the minimum requirement of eight threats.

### Risk rating method
Each risk was assessed using a **1–5 scale** for both likelihood and impact, as defined in the Risk Rating Scale sheet of the spreadsheet:

- **Likelihood:** Rare (1) → Almost Certain (5)  
- **Impact:** Insignificant (1) → Critical (5)

The overall risk score was calculated as:  
**Risk = Likelihood × Impact**, and classified as Low, Medium, or High accordingly.

### TVA Matrix summary (pre-controls)
The full Threat–Vulnerability–Asset mappings are shown in the **TVA_Matrix** sheet of the spreadsheet. Key high-risk findings included:

- **T1 – Malware infection** affecting Application Servers due to unpatched Windows servers (Risk = 20, High).  
- **T2 – Phishing attacks** affecting Employee Personal Data due to credential disclosure (Risk = 16, High).  
- **T3 – Ransomware** affecting Customer Booking Data due to insufficient backup controls (Risk = 15, High).  
- **T4 – Insider misuse** affecting Financial Records due to excessive user privileges (Risk = 15, High).  
- **T6 – Unauthorised access** affecting the Booking Application due to weak authentication (Risk = 16, High).

*(Insert screenshots of your TVA_Matrix sheet here, linked from your repository.)*

---

## Security Controls

### Highest-risk data asset
Based on the risk assessment, the **highest-risk data asset** is:

> **Customer Booking Data (DA-01)**

This data is critical to Truelec’s operations, contains sensitive client information, and was rated high risk due to exposure to ransomware and potential data loss.

---

### **Control 1 — Access Control (AC)**  
**NIST SP 800-53: Access Control (AC)**

**How this reduces risk:**  
Strict access control limits who can view, modify, or delete Customer Booking Data, reducing the likelihood of insider misuse, unauthorised access, and accidental data corruption.

**How it will be implemented in Truelec’s network:**  
- Implement **Role-Based Access Control (RBAC)** on the booking application and Windows Servers (HW-03).  
- Enforce authentication via **Active Directory** at headquarters.  
- Restrict branch access to Customer Booking Data through the HQ firewall and application server authentication.  
- Apply the **principle of least privilege**, granting users only the minimum access required.

**Specific technologies/approaches:**  
- Active Directory authentication  
- Role-Based Access Control (RBAC)  
- Least privilege access model  

**Disadvantages for users:**  
- Some staff may experience slower access approval processes.  
- Users may initially lose access to data they previously viewed, requiring adjustment to new permissions.

---

### **Control 2 — Encryption (SC)**  
**NIST SP 800-53: System and Communications Protection (SC)**

**How this reduces risk:**  
Encryption protects Customer Booking Data from being read or misused if intercepted or accessed without authorisation, mitigating risks from data leakage and external attacks.

**How it will be implemented in Truelec’s network:**  
- **Data in transit:** Use **TLS 1.3** for all communications between branches and headquarters over the WAN.  
- **Data at rest:** Encrypt databases storing Customer Booking Data on the application servers (HW-03).  
- Apply the same encryption controls whether servers remain on-premise or are migrated to Azure/AWS.

**Specific technologies/approaches:**  
- TLS 1.3 for secure network communications  
- AES-256 encryption for database storage  

**Disadvantages for users:**  
- Slight performance overhead when accessing encrypted data.  
- Possible minor delays in data retrieval during peak usage.

---

### **Control 3 — Backup and Recovery (CP)**  
**NIST SP 800-53: Contingency Planning (CP)**

**How this reduces risk:**  
Regular, secure backups reduce the impact of ransomware and accidental data loss by enabling rapid recovery of Customer Booking Data.

**How it will be implemented in Truelec’s network:**  
- Implement **automated daily backups** of Customer Booking Data from the application servers (HW-03).  
- Store backups in a **separate, secure off-site location or different cloud region**.  
- Conduct **periodic restoration tests** to verify that backups can be successfully recovered.

**Specific technologies/approaches:**  
- Immutable (write-once) backups  
- Off-site or cloud-based backup repository  
- Scheduled automated backup jobs  

**Disadvantages for users:**  
- Backup processes may require short maintenance windows, temporarily affecting system availability.  
- Additional storage and management costs for maintaining secure backups.

---

### Summary of selected controls

| Control | Purpose | Key benefit | Main limitation |
|---|---|---|---|
| Access Control | Restrict who can access data | Reduces insider misuse | Slower access approvals |
| Encryption | Protect data from interception | Prevents data leakage | Slight performance impact |
| Backup & Recovery | Enable data restoration | Protects against ransomware | Requires storage and maintenance |

### Conclusion
The combination of **Access Control, Encryption, and Backup & Recovery** provides layered protection for Customer Booking Data, directly addressing the highest-risk threats identified in the TVA Matrix. These controls reduce both the likelihood and impact of major cyber incidents while remaining practical for Truelec’s operational environment.

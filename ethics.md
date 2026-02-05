# Ethical Issues
This section discusses the different ethical issues that arise in the scenario.

[Data Privacy](#data-privacy-and-security-issues) | [Plan](./plan.md) | [Network Design](./network.md) | [Cloud Services](./cloud.md) | [Security](./security.md) | [Reflections](./reflections.md) | [Return to index](./README.md)

---

## Data Privacy and Security Issues

### 1. Types of Data Collected by Truelec

Truelec collects and processes several categories of data as part of its normal business operations. These include:

**1.1 Customer Data**  
This includes:
- Customer names and contact details  
- Service booking records and project details  
- Site locations and work descriptions  
- Communication records between Truelec and clients  

This data contains personally identifiable information (PII). If mishandled, it could violate customer privacy and trust.

**1.2 Employee Personal Data**  
This includes:
- Employee names, addresses, and identification details  
- Payroll and employment records  
- System login credentials and role-based access details  

This data is sensitive and must be protected to prevent identity theft or misuse.

**1.3 Financial Data**  
This includes:
- Invoices and payment records  
- Accounting and transaction data  
- Internal financial reports  

Unauthorised access to this data could enable fraud, financial manipulation, or business disruption.

**1.4 CCTV and Access Control Data**  
This includes:
- CCTV video recordings from security cameras  
- RFID access logs showing building entry and movement  

This involves surveillance data, which raises significant ethical concerns regarding employee and visitor privacy.

---

### 2. Privacy and Security Concerns in Data Collection, Storage, and Use

**2.1 Data Collection Concerns**  
Truelec must ensure that:
- Only necessary data is collected for legitimate business purposes  
- Customers and employees are clearly informed about how their data is used  
- Data is not collected in an excessive or intrusive manner  

Collecting more data than necessary increases privacy risks and potential legal liability.

**2.2 Data Storage Concerns**  
Currently, most data is stored on on-premise servers at headquarters, with potential migration to cloud services. Key risks include:
- Weak or missing encryption of stored data  
- Poor access controls allowing internal misuse  
- Lack of secure, separate backups  
- Misconfigured cloud storage if migration occurs  

If cloud services are used, Truelec must ensure that data is stored in Australian regions where possible and protected with strong security controls.

**2.3 Data Use Concerns**  
Ethical concerns include:
- Using customer data only for legitimate business purposes  
- Not sharing data with third parties without explicit consent  
- Not retaining personal data longer than necessary  

Using customer or employee data for unauthorised marketing or profiling would be unethical and potentially illegal.

---

### 3. Risks Associated with Unauthorised Access or Data Breaches

**3.1 External Cyber Attacks**  
Possible risks include:
- Hackers accessing customer booking data  
- Ransomware encrypting critical business systems  
- Malware compromising application servers  

Potential consequences:
- Service downtime  
- Financial losses  
- Loss of customer trust  
- Legal penalties  

**3.2 Insider Threats (Internal Misuse)**  
Risks include:
- Employees accessing data beyond their role requirements  
- Misuse of financial or customer information  
- Accidental data leakage due to poor security awareness  

This highlights the need for strict access controls and employee cybersecurity training.

**3.3 Data Leakage and Surveillance Risks**  
If CCTV footage or access logs are accessed without authorisation, it could:
- Violate employee and customer privacy  
- Be misused for unfair monitoring or discrimination  
- Lead to legal complaints or investigations  

---

### 4. Relevant Data Protection Regulations and Implications

**4.1 Australian Privacy Act 1988 (Cth)**  
Truelec is subject to the **Privacy Act 1988 (Cth)** and must comply with the **Australian Privacy Principles (APPs)**, which require:
- Lawful and fair collection of personal information  
- Clear purpose for data collection and use  
- Secure storage and protection of personal data  
- Transparency in how personal data is handled  

**Implications for Truelec:**
- Must implement reasonable security safeguards  
- Must notify affected individuals in case of a serious data breach  
- Must report eligible data breaches to the Office of the Australian Information Commissioner (OAIC)  

Failure to comply may result in:
- Regulatory investigations  
- Financial penalties  
- Legal action by affected individuals  

**Reference:**  
Office of the Australian Information Commissioner (OAIC). *Privacy Act 1988 and Australian Privacy Principles.*  
https://www.oaic.gov.au/privacy/the-privacy-act/

**4.2 Notifiable Data Breaches (NDB) Scheme**  
Under the NDB scheme, Truelec must notify affected individuals and the OAIC if a data breach is likely to cause serious harm.

**Implications:**
- Mandatory incident response processes  
- Increased legal and reputational risk  
- Potential fines for non-compliance  

**Reference:**  
OAIC. *Notifiable Data Breaches scheme.*  
https://www.oaic.gov.au/privacy/notifiable-data-breaches/

---

### 5. Potential Impact of a Data Breach

**5.1 Impact on Customers**  
A data breach could result in:
- Loss of privacy and exposure of personal details  
- Risk of identity theft or financial fraud  
- Loss of trust in Truelec  

**Impact level: High**, as customers rely on Truelec to protect their data.

**5.2 Impact on Employees**  
Employees could experience:
- Exposure of personal information  
- Increased stress and workload during incident response  
- Potential job insecurity if the breach is severe  

**Impact level: Medium to High**, depending on the scale of the breach.

**5.3 Impact on Truelec (Organisation)**  
Truelec could face:
- Financial losses from remediation and legal costs  
- Regulatory fines under the Privacy Act  
- Loss of business contracts and reputation damage  
- Decreased customer confidence  

**Impact level: Critical**, especially if customer data is compromised or core systems are disrupted.

---

### 6. Conclusion

Truelec has significant ethical and legal responsibilities regarding data privacy and security. The company must ensure that customer and employee data is collected, stored, and used responsibly in compliance with the **Privacy Act 1988** and the **Notifiable Data Breaches Scheme**. Strong security controls, clear data governance policies, and transparent communication with stakeholders are essential to minimise risks and maintain trust. A serious data breach would have severe consequences for customers, employees, and the organisation, making robust cybersecurity and privacy management a critical priority.

---

### References

- Office of the Australian Information Commissioner (OAIC). *Privacy Act 1988 and Australian Privacy Principles.*  
  https://www.oaic.gov.au/privacy/the-privacy-act/

- Office of the Australian Information Commissioner (OAIC). *Notifiable Data Breaches scheme.*  
  https://www.oaic.gov.au/privacy/notifiable-data-breaches/

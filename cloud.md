# Cloud Services
This section gives pricing for a cloud setup for the company.

[Cloud VM Provider Comparison](#cloud-vm-provider-comparison) | [Total Cost](#total-cost-of-cloud-vms) | [Plan](./plan.md) | [Network Design](./network.md) | [Security](./security.md) | [Ethics](./ethics.md) | [Reflection](./reflection.md) | [Return to index](./README.md)

---

## Cloud VM Provider Comparison

Truelec currently hosts all servers on-premise using 5-year-old Dell PowerEdge Tower servers. The booking application requires **three servers at headquarters and one server per branch office**. To evaluate whether cloud virtual machines (VMs) are a better option, official pricing calculators from **Microsoft Azure and Amazon Web Services (AWS)** were used, and the same (or very similar) specifications were applied to ensure a fair comparison.

### Standardised VM Specifications (used for both providers)

| Specification | Azure Selection | AWS Equivalent | Justification |
|---|---|---|---|
| Region | Australia Southeast | Asia Pacific (Sydney) | Closest Australian regions with low latency for Truelec operations |
| Operating System | Windows (license included) | Windows | Aligns with Truelec’s enterprise and application environment |
| vCPUs | 4 | 4 (t3.xlarge) | Comparable to existing Dell server performance |
| RAM | 16 GB | 16 GB | Suitable for application workload and future growth |
| Storage | 500 GB Premium SSD (P1) | 500 GB gp3 SSD | High-performance storage; kept identical across providers |
| Pricing model | Pay-as-you-go | On-Demand | Fair, consistent basis for comparison |

### Microsoft Azure (per VM)

The estimate was generated using the official Azure Pricing Calculator and exported to the repository.

- VM Type: **D4s v3 (4 vCPU, 16 GB RAM)**
- Region: **Australia Southeast**
- OS: **Windows (license included)**
- Storage: **500 GB Premium SSD (P1 managed disk)**
- Billing: **Pay-as-you-go (730 hrs/month)**

**Azure monthly cost per VM: AUD 736.82**  
**Azure annual cost per VM: AUD 8,841.84**

### Amazon Web Services (per VM)

The estimate was generated using the official AWS Pricing Calculator and exported to the repository.

- Instance: **t3.xlarge (4 vCPU, 16 GB RAM)**
- Region: **Asia Pacific (Sydney)**
- OS: **Windows**
- Storage: **500 GB gp3 SSD**
- Pricing: **On-Demand (100% utilisation)**

*(AWS monthly cost will be taken directly from your final exported estimate.)*

### Recommended Provider

**Recommended Provider: Microsoft Azure**

Azure is recommended because:
- It provides competitive pricing in Australian regions for this VM configuration.
- It integrates well with Windows-based enterprise environments, which suits Truelec’s IT landscape.
- Azure offers strong networking, security, and redundancy features that support multi-branch connectivity.

---

Links to cloud provider export files:
- [AWS](./aws-estimate.csv)
- [Azure](./azure-estimate.xlsx)

---

## Total Cost of Cloud VMs

### Number of servers required

Based on the project scenario:

- Headquarters: **3 servers**
- Branch offices: **3 servers (1 per branch)**
- **Total cloud VMs required = 6**

### 5-Year cost calculation (using recommended provider: Azure)

**Step 1 — Monthly cost per VM:**  
Azure = **AUD 736.82**

**Step 2 — 5-year cost per VM:**  
736.82 × 12 × 5 = **AUD 44,209.20 per VM**

**Step 3 — Total 5-year cost for all VMs**

| Item | Number of VMs | 5-Year Cost per VM (AUD) | Total 5-Year Cost (AUD) |
|---|---|---|---|
| Cloud VMs | 6 | 44,209.20 | **265,255.20** |

**Total 5-year cloud cost = AUD 265,255.20**

### Cloud VMs vs Physical Servers

**Advantages of Cloud VMs**
- No large upfront hardware purchase  
- Easier maintenance (provider manages hardware)  
- Better scalability (CPU/RAM/storage can be increased)  
- Higher availability with built-in redundancy options  
- Faster deployment compared to buying and installing hardware  

**Disadvantages of Cloud VMs**
- Ongoing monthly costs instead of one-time purchase  
- Dependence on reliable internet connectivity  
- Potential data sovereignty and compliance concerns  
- Less direct control over physical hardware  
- Possible performance variability at peak times  

**Advantages of buying new physical servers**
- One-time capital expenditure  
- Full control over data and hardware  
- No dependence on external cloud provider  
- Potentially cheaper over a very long lifespan  

**Disadvantages of physical servers**
- High initial purchase cost  
- Requires in-house IT maintenance  
- Hardware failures could cause downtime  
- Harder to scale compared to cloud infrastructure  

### Final conclusion

Based on the cost analysis, scalability benefits, and reduced maintenance burden, **migrating Truelec’s booking application servers to Microsoft Azure cloud virtual machines is recommended.** Although cloud services involve ongoing costs, they provide greater flexibility, improved reliability, and easier management compared to maintaining aging on-premise hardware.

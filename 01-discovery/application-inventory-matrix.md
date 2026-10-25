# 📋 Enterprise Application Discovery & Inventory Profiling Matrix

> **Purpose:** Baseline discovery questionnaire used during Phase 1 of the Migration Factory.

---

## Workload Profiling Template

| Parameter | Application Profile |
| :--- | :--- |
| **Application Name** | e.g., Core Payment Gateway / Billing Engine |
| **Business Criticality** | Tier-1 (Mission Critical) / Tier-2 / Tier-3 |
| **Application Owner** | Engineering Director / VP Technology |
| **Current Hosting** | On-Premises VMware vSphere 7.0 / RHEL 8.4 / Windows 2019 |
| **Target Destination** | Azure Spoke Prod VNet (snet-app-prod-01) |
| **Modernization Strategy** | Replatform (Azure App Service / AKS) or Rehost (IaaS VM) |
| **Database Engine** | Oracle 19c RAC (2.4 TB) / Microsoft SQL Server 2019 AlwaysOn |
| **Recovery Time Objective (RTO)** | < 1 Hour |
| **Recovery Point Objective (RPO)** | < 15 Minutes |
| **Compliance Scope** | PCI-DSS v4.0, SOC2 Type II, ISO 27001 |
| **Upstream Dependencies** | Core Banking API, SAP S/4HANA Finance |
| **Downstream Dependencies** | Notification SMS Service, Analytics Data Lake |
| **Cutover Tolerance Window** | Max 4 Hours (Weekend Maintenance Window: Sat 22:00 - Sun 02:00 UTC) |

---
*Created by [Rahul Goyal](https://github.com/rahulgoyaldevops)*
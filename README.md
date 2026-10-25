<div align="center">

# 🔄 Cloud Migration Playbook

[![Azure](https://img.shields.io/badge/Azure-Migration-0078D4?style=for-the-badge&logo=microsoftazure&logoColor=white)](https://azure.microsoft.com/)
[![AWS](https://img.shields.io/badge/AWS-Migration-232F3E?style=for-the-badge&logo=amazonwebservices&logoColor=white)](https://aws.amazon.com/)
[![Enterprise](https://img.shields.io/badge/Enterprise-100%2B_Apps-FF6F00?style=for-the-badge)](https://github.com/rahulgoyaldevops)

**Battle-tested framework for large-scale cloud migrations — from assessment to hypercare. Built from real experience migrating 100+ applications across dev, UAT, and production environments.**

*Not theory. This is how enterprise migration is executed in the trenches.*

</div>

---

## 🎯 What This Playbook Covers

> Migrating a handful of VMs is straightforward. Migrating **100+ applications across multiple subscriptions, from on-premises datacenters to cloud, while maintaining uptime, zero data loss, strict governance, and FinOps targets** — requires an industrialized Migration Factory.

## 🏭 Migration Factory Framework

```
┌──────────────────────────── MIGRATION FACTORY ──────────────────────────────┐
│                                                                             │
│  PHASE 1        PHASE 2        PHASE 3        PHASE 4        PHASE 5       │
│  ┌──────────┐   ┌──────────┐   ┌──────────┐   ┌──────────┐   ┌──────────┐ │
│  │DISCOVERY │──▶│ASSESSMENT│──▶│READINESS │──▶│ MIGRATE  │──▶│HYPERCARE │ │
│  │          │   │          │   │          │   │          │   │          │  │
│  │ Inventory│   │ 6R       │   │ Pre-     │   │ Cutover  │   │ Post-    │  │
│  │ Dependency│  │ Strategy │   │ Checklist│   │ Windows  │   │ Validation│ │
│  │ Mapping  │   │ TCO/ROI  │   │ Network  │   │ Data     │   │ Perf     │  │
│  │ Workload │   │ Risk     │   │ Security │   │ Sync     │   │ Baseline │  │
│  │ Profiling│   │ Analysis │   │ IAM      │   │ DNS      │   │ Sign-off │  │
│  │          │   │          │   │ Backup   │   │ Cutover  │   │ KT       │  │
│  └──────────┘   └──────────┘   └──────────┘   └──────────┘   └──────────┘ │
│                                                                             │
│  ► Workloads: On-Premise Datacenter ──▶ Azure / AWS Landing Zone           │
│  ► Scale: 100+ Applications (Dev, UAT, Production)                         │
│  ► Focus: High Availability, RTO/RPO SLAs, Least Privilege Security        │
└─────────────────────────────────────────────────────────────────────────────┘
```

## 📋 The 6R Migration Strategies

| Strategy | When to Use | Complexity | Cost Impact |
|:--|:--|:--|:--|
| **Rehost** (Lift & Shift) | Urgent migration, data center exit deadline | Low | Neutral |
| **Replatform** (Lift & Reshape) | Adopt managed PaaS (e.g., Azure SQL, App Service) | Medium | Lower OpEx |
| **Refactor** (Re-architect) | Cloud-native microservices, AKS, serverless | High | Max elasticity |
| **Repurchase** | Replace legacy systems with modern SaaS | Low-Med | Operational shift |
| **Retire** | Decommission dead workloads identified in discovery | Zero | Direct savings |
| **Retain** | High latency/regulatory lock-in on-prem | Zero | Deferred |

## 📁 Repository Structure

```
cloud-migration-playbook/
│
├── 01-discovery/               # CMDB audit, dependency discovery, wave grouping
├── 02-assessment/              # 6R decision matrix, TCO & licensing calculator
├── 03-readiness/               # Landing zone validation & pre-migration checklist
├── 04-migration/               # Cutover runbooks, sync verification, rollback plan
├── 05-hypercare/               # Post-cutover monitoring, KT, and SLA baselines
└── README.md
```

## 🚀 Key Artifacts Included
- **[Pre-Migration Checklist](03-readiness/pre-migration-checklist.md)**: 30+ point verification before initiating cutover.
- **[6R Decision Tree](02-assessment/6r-strategy-decision-tree.md)**: Rationalization guide for application modernization.

---

<div align="center">

**Architected by [Rahul Goyal](https://github.com/rahulgoyaldevops)** — Enterprise Cloud Architect | 14+ Years

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Rahul_Goyal-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/rahulgoyaldevops/)

</div>
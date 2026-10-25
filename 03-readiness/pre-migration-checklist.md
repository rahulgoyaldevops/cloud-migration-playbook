# ✅ Pre-Migration Checklist (Enterprise Grade)

> **Execution Protocol:** This checklist must be fully verified and approved by Architecture, Security, and App Owners before cutover window initiation.

---

## 1. Cloud Network & Connectivity
- [ ] Target Landing Zone VNet and Subnets verified with assigned non-overlapping CIDRs.
- [ ] ExpressRoute / Site-to-Site VPN circuits operating within latency SLAs (< 15ms target).
- [ ] Central Azure Firewall / NVA egress inspection routing rules active via UDR.
- [ ] Private DNS Zones linked across Hub and Spoke VNets with autoregistration enabled where required.
- [ ] On-premises DNS conditional forwarders pointing to Azure Private Resolver / Inbound Endpoints.

## 2. Enterprise Governance & Identity
- [ ] Microsoft Entra ID integration confirmed; PIM (Privileged Identity Management) roles assigned.
- [ ] Azure Policy initiatives mapped and exempt list reviewed with enterprise justifications.
- [ ] Key Vault provisioned with RBAC authorization and Private Endpoints enabled.
- [ ] Defender for Cloud posture score assessed and server agent onboarding validated.

## 3. Workload & Data Migration Readiness
- [ ] Source database consistency check executed; full baseline backup archived to cold storage.
- [ ] Continuous data replication / sync engine active (e.g. Azure Migrate, DMS, GoldenGate).
- [ ] DNS TTL reduced to 300 seconds (5 mins) 48 hours in advance to enable rapid propagation.
- [ ] Application dependency mapping cross-checked with Network Security Groups (NSGs).

## 4. Operational & Rollback Framework
- [ ] Validated point-in-time rollback runbook with guaranteed RTO (< 1 hour).
- [ ] Monitoring baseline configured in Azure Monitor & Log Analytics.
- [ ] War room schedule, bridge line, and escalation matrix published.
- [ ] Formal Change Advisory Board (CAB) approval documented.

---
*Authored by [Rahul Goyal](https://github.com/rahulgoyaldevops) — 14+ Years Senior DevOps & Cloud Engineering*
# ⏪ Enterprise Rollback Standard Operating Procedure (SOP)

> **Document Classification:** Confidential & Internal Operations  
> **Author:** Rahul Goyal — Senior DevOps Engineer (14+ Years)  
> **Maximum Allowable Rollback Execution Window:** < 60 Minutes

---

## 1. Rollback Trigger Criteria (No-Go Gate)
A rollback is formally declared by the Incident Commander / Migration Lead if ANY of the following occur during the cutover window:
- [ ] Database row-count validation variance > 0.00% across transactional core tables.
- [ ] Core business API synthetic transactions return 5xx errors for > 15 consecutive minutes.
- [ ] ExpressRoute / Hybrid circuit latency exceeds agreed P99 threshold (> 50ms) with no immediate routing resolution.
- [ ] Database delta synchronization lag cannot be eliminated within the 2-hour maintenance window.

---

## 2. Step-by-Step Rollback Execution Runbook

```
Step 1: DECLARE FORMAL ROLLBACK (T + 0 min)
├── Notify Command Center Bridge, Application Owners, and Executive Stakeholders
└── Freeze all active deployments and data sync streams

Step 2: REDIRECT TRAFFIC BACK TO SOURCE (T + 10 min)
├── Revert internal DNS / Azure Front Door routing to point back to On-Premises VIPs
└── Flush internal and external DNS cache

Step 3: REACTIVATE ON-PREMISES INFRASTRUCTURE (T + 25 min)
├── Remove application workloads from Maintenance / Read-Only mode
├── Start background batch and queuing services (RabbitMQ, Kafka, Windows Services)
└── Validate database write access on on-premises primary instances

Step 4: POST-ROLLBACK VERIFICATION & AUDIT (T + 45 min)
├── Execute synthetic test suite against on-premises endpoints
├── Confirm incoming traffic matches pre-migration baseline
└── Convene root cause analysis (RCA) review board within 24 hours
```

---
*Part of Cloud Migration Playbook by [Rahul Goyal](https://github.com/rahulgoyaldevops)*
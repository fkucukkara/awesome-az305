# Exam Guide: AZ-305

## Official facts (Microsoft)

Source: [AZ-305 study guide](https://learn.microsoft.com/en-us/credentials/certifications/resources/study-guides/az-305), [exam page](https://learn.microsoft.com/en-us/credentials/certifications/exams/az-305/) and [certification page](https://learn.microsoft.com/en-us/credentials/certifications/azure-solutions-architect/). Skills measured as of **April 17, 2026**.

| Item | Detail |
|---|---|
| Exam | AZ-305: Designing Microsoft Azure Infrastructure Solutions |
| Certification | Microsoft Certified: Azure Solutions Architect Expert |
| Level | Expert |
| Certification prerequisite | Microsoft Certified: Azure Administrator Associate (AZ-104), per the certification page |
| Passing score | 700 or greater |
| Duration | Shown when you schedule; not stated on the study guide, so check the Pearson VUE confirmation |
| Delivery | Proctored through Pearson VUE |
| Question types | Can include case studies and interactive components |
| Retake | After 24 hours for the first retake; longer waits after that ([retake policy](https://learn.microsoft.com/en-us/credentials/support/retake-policy)) |
| Renewal | Every 12 months, free online assessment on Microsoft Learn |
| Languages | English, Japanese, Chinese (Simplified), Korean, German, French, Spanish, Portuguese (Brazil), Chinese (Traditional), Italian |
| Preview features | Most questions cover GA features; commonly used preview features may appear |
| Note from Microsoft | The bullets under each skill illustrate how it is assessed; related topics may also appear |

Microsoft does not publish the number of questions. Do not trust sites that claim a fixed number.

## Audience and experience (official)

You design **cloud and hybrid solutions** on Azure covering compute, network, storage, monitoring and security. You advise stakeholders and translate **business requirements into designs** aligned with the **Azure Well-Architected Framework** and the **Cloud Adoption Framework for Azure**. You partner with developers, administrators, security engineers and data engineers.

You should have advanced experience with IT operations (networking, virtualization, identity, security, business continuity, disaster recovery, data platforms, governance), plus experience in Azure administration, Azure development and DevOps processes.

## Domains and weights (official)

| # | Domain | Weight | Guide |
|---|---|---|---|
| 1 | Design identity, governance, and monitoring solutions | 25–30% | [01](01-identity-governance-monitoring/README.md) |
| 2 | Design data storage solutions | 20–25% | [02](02-data-storage/README.md) |
| 3 | Design business continuity solutions | 15–20% | [03](03-business-continuity/README.md) |
| 4 | Design infrastructure solutions | 30–35% | [04](04-infrastructure/README.md) |

Domain 4 is the largest, and compute, network and migration choices appear in every case study. Identity and governance is next. Together they are well over half of the exam.

## What AZ-305 tests differently from AZ-104

| AZ-104 (administrator) | AZ-305 (architect) |
|---|---|
| **How** do I configure it? | **Which** service should I recommend, and **why**? |
| One correct setting | Several valid options; pick the one that fits **all** requirements |
| Portal and CLI steps | **Trade-offs**: cost, ops effort, resilience, security, compliance |
| Single resource | **Whole solution** across identity, network, data, DR |

See [CASE-STUDY-GUIDE.md](CASE-STUDY-GUIDE.md) for the method and [DECISION-MATRICES.md](DECISION-MATRICES.md) for service selection tables.

## Important services (derived from the objectives)

Microsoft Entra ID, Conditional Access, PIM, External ID, Entra Connect/Cloud Sync, Azure RBAC, managed identities, Key Vault, Managed HSM, management groups, Azure Policy, Defender for Cloud, Purview · Azure Monitor, Log Analytics, Application Insights, Sentinel, Event Hubs · Azure SQL (Database, MI, VM), PostgreSQL/MySQL Flexible Server, Cosmos DB, Blob/ADLS Gen2, Azure Files, NetApp Files, Data Factory, Synapse, Fabric, Stream Analytics · Azure Backup, Site Recovery, availability zones, failover groups · VMs, VMSS, AKS, Container Apps, ACI, App Service, Functions, Logic Apps, Batch · Service Bus, Event Grid, API Management, Redis, App Configuration · Azure Migrate, DMS, Data Box, Storage Mover · VNet, Virtual WAN, VPN Gateway, ExpressRoute, Azure Firewall, Private Link, Front Door, Application Gateway, Load Balancer, Traffic Manager.

## Recommended preparation (our advice, not Microsoft's)

1. Read each domain file once, slowly. Do the Quick Checks.
2. Learn the **decision tables** in each topic, then read [DECISION-MATRICES.md](DECISION-MATRICES.md). Most wrong answers come from picking the *second best* service.
3. Practise one **requirement-first** habit: write down constraints (cost, ops effort, RTO/RPO, compliance) before looking at options. See [CASE-STUDY-GUIDE.md](CASE-STUDY-GUIDE.md).
4. Skim the [Azure Architecture Center](https://learn.microsoft.com/en-us/azure/architecture/) and the Well-Architected pillars so the vocabulary is familiar.
5. Take the free Microsoft practice assessment, then read the explanations for every miss.
6. Revise with [QUICK-REVISION.md](QUICK-REVISION.md).
7. Finish with [EXAM-DAY-CHECKLIST.md](EXAM-DAY-CHECKLIST.md).

## Official Microsoft resources

See [references/microsoft-resources.md](references/microsoft-resources.md).

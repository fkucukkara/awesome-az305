# Microsoft Resources and Coverage Map

All links are to official Microsoft sources. Skills measured as of **April 17, 2026**.

## Exam and certification

- [Certification page: Azure Solutions Architect Expert](https://learn.microsoft.com/en-us/credentials/certifications/azure-solutions-architect/)
- [Exam page: AZ-305](https://learn.microsoft.com/en-us/credentials/certifications/exams/az-305/)
- [Exam study guide (skills measured)](https://learn.microsoft.com/en-us/credentials/certifications/resources/study-guides/az-305)
- [Free practice assessment](https://learn.microsoft.com/en-us/credentials/certifications/exams/az-305/practice/assessment?assessment-type=practice&assessmentId=15)
- [Exam sandbox](https://aka.ms/examdemo)
- [Exam scoring and score reports](https://learn.microsoft.com/en-us/credentials/certifications/exam-scoring-reports)
- [Retake policy](https://learn.microsoft.com/en-us/credentials/support/retake-policy)
- [Request accommodations](https://learn.microsoft.com/en-us/credentials/certifications/request-accommodations)
- [Renewal](https://learn.microsoft.com/en-us/credentials/certifications/renew-your-microsoft-certification)
- [Exam Readiness Zone videos](https://learn.microsoft.com/en-us/shows/exam-readiness-zone/?terms=AZ-305)

## Microsoft Learn learning paths

The instructor-led course [AZ-305T00](https://learn.microsoft.com/en-us/training/courses/az-305t00) is built around these paths:

| Path | Matches |
|---|---|
| [AZ-305 Microsoft Azure Architect Design Prerequisites](https://learn.microsoft.com/en-us/training/paths/microsoft-azure-architect-design-prerequisites/) | Background (core architecture, CAF, Well-Architected Framework) |
| [Design identity, governance, and monitor solutions](https://learn.microsoft.com/en-us/training/paths/design-identity-governance-monitor-solutions/) | [Domain 1](../01-identity-governance-monitoring/README.md) |
| [Design data storage solutions](https://learn.microsoft.com/en-us/training/paths/design-data-storage-solutions/) | [Domain 2](../02-data-storage/README.md) |
| [Design business continuity solutions](https://learn.microsoft.com/en-us/training/paths/design-business-continuity-solutions/) | [Domain 3](../03-business-continuity/README.md) |
| [Design infrastructure solutions](https://learn.microsoft.com/en-us/training/paths/design-infranstructure-solutions/) | [Domain 4](../04-infrastructure/README.md) |

## Design frameworks

- [Azure Well-Architected Framework](https://learn.microsoft.com/en-us/azure/well-architected/)
- [Cloud Adoption Framework for Azure](https://learn.microsoft.com/en-us/azure/cloud-adoption-framework/)
- [Azure landing zones](https://learn.microsoft.com/en-us/azure/cloud-adoption-framework/ready/landing-zone/)
- [Azure Architecture Center](https://learn.microsoft.com/en-us/azure/architecture/)
- [Browse Azure architectures](https://learn.microsoft.com/en-us/azure/architecture/browse/)
- [Cloud design patterns](https://learn.microsoft.com/en-us/azure/architecture/patterns/)
- [Architecture decision trees (compute, data store, messaging, load balancing)](https://learn.microsoft.com/en-us/azure/architecture/guide/technology-choices/technology-choices-overview)

## Documentation by service

| Area | Docs |
|---|---|
| Monitoring and logging | [Azure Monitor](https://learn.microsoft.com/en-us/azure/azure-monitor/) · [Log Analytics workspace design](https://learn.microsoft.com/en-us/azure/azure-monitor/logs/workspace-design) · [Diagnostic settings](https://learn.microsoft.com/en-us/azure/azure-monitor/essentials/diagnostic-settings) · [Application Insights](https://learn.microsoft.com/en-us/azure/azure-monitor/app/app-insights-overview) · [Microsoft Sentinel](https://learn.microsoft.com/en-us/azure/sentinel/) |
| Identity | [Microsoft Entra ID](https://learn.microsoft.com/en-us/entra/identity/) · [Conditional Access](https://learn.microsoft.com/en-us/entra/identity/conditional-access/) · [Hybrid identity](https://learn.microsoft.com/en-us/entra/identity/hybrid/) · [Microsoft Entra External ID](https://learn.microsoft.com/en-us/entra/external-id/) · [Application Proxy](https://learn.microsoft.com/en-us/entra/identity/app-proxy/) · [Managed identities](https://learn.microsoft.com/en-us/entra/identity/managed-identities-azure-resources/overview) |
| Authorization | [Azure RBAC](https://learn.microsoft.com/en-us/azure/role-based-access-control/overview) · [Privileged Identity Management](https://learn.microsoft.com/en-us/entra/id-governance/privileged-identity-management/) · [Azure Lighthouse](https://learn.microsoft.com/en-us/azure/lighthouse/) |
| Secrets and keys | [Key Vault](https://learn.microsoft.com/en-us/azure/key-vault/) · [Managed HSM](https://learn.microsoft.com/en-us/azure/key-vault/managed-hsm/overview) · [App Configuration](https://learn.microsoft.com/en-us/azure/azure-app-configuration/) |
| Governance | [Management groups](https://learn.microsoft.com/en-us/azure/governance/management-groups/overview) · [Azure Policy](https://learn.microsoft.com/en-us/azure/governance/policy/overview) · [Tagging strategy](https://learn.microsoft.com/en-us/azure/cloud-adoption-framework/ready/azure-best-practices/resource-tagging) · [Defender for Cloud](https://learn.microsoft.com/en-us/azure/defender-for-cloud/) · [Microsoft Purview](https://learn.microsoft.com/en-us/purview/) · [Entitlement management](https://learn.microsoft.com/en-us/entra/id-governance/entitlement-management-overview) · [Access reviews](https://learn.microsoft.com/en-us/entra/id-governance/access-reviews-overview) |
| Relational data | [Azure SQL](https://learn.microsoft.com/en-us/azure/azure-sql/) · [SQL Managed Instance](https://learn.microsoft.com/en-us/azure/azure-sql/managed-instance/sql-managed-instance-paas-overview) · [Hyperscale](https://learn.microsoft.com/en-us/azure/azure-sql/database/service-tier-hyperscale) · [PostgreSQL Flexible Server](https://learn.microsoft.com/en-us/azure/postgresql/flexible-server/) · [MySQL Flexible Server](https://learn.microsoft.com/en-us/azure/mysql/flexible-server/) |
| NoSQL and storage | [Cosmos DB](https://learn.microsoft.com/en-us/azure/cosmos-db/) · [Consistency levels](https://learn.microsoft.com/en-us/azure/cosmos-db/consistency-levels) · [Storage documentation](https://learn.microsoft.com/en-us/azure/storage/) · [Storage redundancy](https://learn.microsoft.com/en-us/azure/storage/common/storage-redundancy) · [Access tiers](https://learn.microsoft.com/en-us/azure/storage/blobs/access-tiers-overview) · [ADLS Gen2](https://learn.microsoft.com/en-us/azure/storage/blobs/data-lake-storage-introduction) · [Azure Files](https://learn.microsoft.com/en-us/azure/storage/files/) · [NetApp Files](https://learn.microsoft.com/en-us/azure/azure-netapp-files/) |
| Data integration and analytics | [Data Factory](https://learn.microsoft.com/en-us/azure/data-factory/) · [Synapse Analytics](https://learn.microsoft.com/en-us/azure/synapse-analytics/) · [Microsoft Fabric](https://learn.microsoft.com/en-us/fabric/) · [Databricks](https://learn.microsoft.com/en-us/azure/databricks/) · [Stream Analytics](https://learn.microsoft.com/en-us/azure/stream-analytics/) · [Data Explorer](https://learn.microsoft.com/en-us/azure/data-explorer/) |
| Business continuity | [Reliability documentation](https://learn.microsoft.com/en-us/azure/reliability/) · [Availability zones](https://learn.microsoft.com/en-us/azure/reliability/availability-zones-overview) · [Azure Backup](https://learn.microsoft.com/en-us/azure/backup/) · [Site Recovery](https://learn.microsoft.com/en-us/azure/site-recovery/) · [SQL failover groups](https://learn.microsoft.com/en-us/azure/azure-sql/database/failover-group-sql-db) · [Composite SLAs](https://learn.microsoft.com/en-us/azure/well-architected/reliability/metrics) |
| Compute | [Virtual machines](https://learn.microsoft.com/en-us/azure/virtual-machines/) · [VM Scale Sets](https://learn.microsoft.com/en-us/azure/virtual-machine-scale-sets/) · [AKS](https://learn.microsoft.com/en-us/azure/aks/) · [Container Apps](https://learn.microsoft.com/en-us/azure/container-apps/) · [Container Instances](https://learn.microsoft.com/en-us/azure/container-instances/) · [App Service](https://learn.microsoft.com/en-us/azure/app-service/) · [Functions](https://learn.microsoft.com/en-us/azure/azure-functions/) · [Logic Apps](https://learn.microsoft.com/en-us/azure/logic-apps/) · [Batch](https://learn.microsoft.com/en-us/azure/batch/) |
| Application architecture | [Service Bus](https://learn.microsoft.com/en-us/azure/service-bus-messaging/) · [Event Grid](https://learn.microsoft.com/en-us/azure/event-grid/) · [Event Hubs](https://learn.microsoft.com/en-us/azure/event-hubs/) · [Choose a messaging service](https://learn.microsoft.com/en-us/azure/service-bus-messaging/compare-messaging-services) · [API Management](https://learn.microsoft.com/en-us/azure/api-management/) · [Azure Managed Redis](https://learn.microsoft.com/en-us/azure/redis/) · [Bicep](https://learn.microsoft.com/en-us/azure/azure-resource-manager/bicep/overview) · [Deployment Stacks](https://learn.microsoft.com/en-us/azure/azure-resource-manager/bicep/deployment-stacks) |
| Migration | [Azure Migrate](https://learn.microsoft.com/en-us/azure/migrate/) · [Database Migration Service](https://learn.microsoft.com/en-us/azure/dms/) · [Azure Data Box](https://learn.microsoft.com/en-us/azure/databox/) · [Storage Mover](https://learn.microsoft.com/en-us/azure/storage-mover/) · [Azure VMware Solution](https://learn.microsoft.com/en-us/azure/azure-vmware/) · [CAF Migrate](https://learn.microsoft.com/en-us/azure/cloud-adoption-framework/migrate/) |
| Networking | [Virtual Network](https://learn.microsoft.com/en-us/azure/virtual-network/) · [Virtual WAN](https://learn.microsoft.com/en-us/azure/virtual-wan/) · [VPN Gateway](https://learn.microsoft.com/en-us/azure/vpn-gateway/) · [ExpressRoute](https://learn.microsoft.com/en-us/azure/expressroute/) · [Azure Firewall](https://learn.microsoft.com/en-us/azure/firewall/) · [Private Link](https://learn.microsoft.com/en-us/azure/private-link/) · [Front Door](https://learn.microsoft.com/en-us/azure/frontdoor/) · [Application Gateway](https://learn.microsoft.com/en-us/azure/application-gateway/) · [Load Balancer](https://learn.microsoft.com/en-us/azure/load-balancer/) · [Traffic Manager](https://learn.microsoft.com/en-us/azure/traffic-manager/) · [DDoS Protection](https://learn.microsoft.com/en-us/azure/ddos-protection/) · [Load balancing options](https://learn.microsoft.com/en-us/azure/architecture/guide/technology-choices/load-balancing-overview) |

## Coverage map

Every official objective → where it is covered → trap → revision.

Legend: **G** = guide section, **T** = main exam trap, **R** = [QUICK-REVISION](../QUICK-REVISION.md) section.

### Domain 1: Identity, governance, and monitoring (25–30%)

| Official objective | Guide | Main trap | Revision |
|---|---|---|---|
| Recommend a logging solution | [D1 §1](../01-identity-governance-monitoring/README.md) | Diagnostic settings aren't automatic; AMA replaces legacy agent | R1 |
| Recommend a solution for routing logs | D1 §1 | Event Hubs = SIEM stream, Storage = archive | R1 |
| Recommend a monitoring solution | D1 §1 | Metrics vs logs; Sentinel vs Defender for Cloud | R1 |
| Recommend an authentication solution | [D1 §2](../01-identity-governance-monitoring/README.md) | Conditional Access = P1, risk = P2 | R1 |
| Recommend an identity management solution | D1 §2 | B2B vs External ID; federation rarely the answer | R1 |
| Authorizing access to Azure resources | [D1 §3](../01-identity-governance-monitoring/README.md) | Contributor can't assign roles; Global Admin ≠ Owner | R1 |
| Authorizing access to on-premises resources | D1 §3 | Application Proxy for web apps; Entra DS for legacy | R1 |
| Manage secrets, certificates, and keys | [D1 §4](../01-identity-governance-monitoring/README.md) | Purge protection; managed identity over secrets | R1 |
| Structure for management groups, subscriptions, resource groups, and tagging | [D1 §5](../01-identity-governance-monitoring/README.md) | Tags don't inherit; max 6 MG levels | R1 |
| Recommend a solution for managing compliance | [D1 §6](../01-identity-governance-monitoring/README.md) | Policy doesn't fix existing resources; Blueprints deprecated | R1 |
| Recommend a solution for identity governance | [D1 §7](../01-identity-governance-monitoring/README.md) | Entitlement management for external users; PIM for just-in-time | R1 |

### Domain 2: Data storage (20–25%)

| Official objective | Guide | Main trap | Revision |
|---|---|---|---|
| Recommend a solution for storing relational data | [D2 §1](../02-data-storage/README.md) | SQL Agent or cross-DB = MI; OS access = VM | R2 |
| Recommend a database service tier and compute tier | D2 §1 | Serverless cold start; BC vs Hyperscale | R2 |
| Recommend a solution for database scalability | D2 §1 | Elastic pool, read scale-out, sharding | R2 |
| Recommend a solution for data protection | D2 §1 | TDE vs Always Encrypted; PITR vs LTR | R2 |
| Recommend a solution for storing semi-structured data | [D2 §2](../02-data-storage/README.md) | Lowest sufficient consistency; partition key | R2 |
| Recommend a solution for storing unstructured data | [D2 §3](../02-data-storage/README.md) | Blob vs ADLS Gen2 vs Files vs NetApp | R2 |
| Balance features, performance, and costs | D2 §3 | Archive is offline; lifecycle management | R2 |
| Recommend a data solution for protection and durability | D2 §3 | Redundancy isn't backup; GRS not readable | R2 |
| Recommend a solution for data integration | [D2 §4](../02-data-storage/README.md) | ADF isn't a broker; self-hosted IR | R2 |
| Recommend a solution for data analysis | D2 §4 | Dedicated vs serverless SQL; Synapse Link | R2 |

### Domain 3: Business continuity (15–20%)

| Official objective | Guide | Main trap | Revision |
|---|---|---|---|
| Recovery solution for Azure and hybrid workloads meeting recovery objectives | [D3 §1](../03-business-continuity/README.md) | ASR isn't backup; composite SLA | R3 |
| Backup and recovery for compute | [D3 §2](../03-business-continuity/README.md) | Vault region rules; choose redundancy first | R3 |
| Backup and recovery for databases | D3 §2 | LTR for years; PITR max 35 days | R3 |
| Backup and recovery for unstructured data | D3 §2 | Soft delete ≠ backup; immutability | R3 |
| High availability for compute | [D3 §3](../03-business-continuity/README.md) | One VM isn't 99.99%; zones ≠ region | R3 |
| High availability for relational data | [D3 §4](../03-business-continuity/README.md) | Use failover group listener; async data loss | R3 |
| High availability for semi-structured and unstructured data | [D3 §5](../03-business-continuity/README.md) | RA- for readable secondary; premium LRS/ZRS only | R3 |

### Domain 4: Infrastructure (30–35%)

| Official objective | Guide | Main trap | Revision |
|---|---|---|---|
| Specify components of a compute solution | [D4 §1](../04-infrastructure/README.md) | Highest abstraction that meets requirements | R4 |
| Recommend a virtual machine-based solution | D4 §1 | Spot eviction; Hybrid Benefit and reservations | R4 |
| Recommend a container-based solution | D4 §1 | Container Apps vs AKS vs ACI | R4 |
| Recommend a serverless-based solution | D4 §1 | Cold start; Functions vs Logic Apps | R4 |
| Recommend a compute solution for batch processing | D4 §1 | Batch + Spot; CycleCloud for HPC schedulers | R4 |
| Recommend a messaging architecture | [D4 §2](../04-infrastructure/README.md) | Ordering needs Service Bus sessions | R4 |
| Recommend an event-driven architecture | D4 §2 | Event Grid vs Event Hubs | R4 |
| Recommend a solution for API integration | D4 §2 | APIM tier features | R4 |
| Recommend a caching solution | D4 §2 | Cache isn't a system of record | R4 |
| Recommend an application configuration management solution | D4 §2 | App Configuration vs Key Vault | R4 |
| Recommend an automated deployment solution | D4 §2 | OIDC federation; slots/revisions for blue-green | R4 |
| Evaluate a migration solution with CAF | [D4 §3](../04-infrastructure/README.md) | Assess and landing zone first | R4 |
| Evaluate on-premises servers, data, and applications | D4 §3 | Azure Migrate dependency analysis | R4 |
| Migrate workloads to IaaS and PaaS | D4 §3 | AVS keeps VMware; rehost vs refactor | R4 |
| Migrate databases | D4 §3 | Online vs offline; MI link | R4 |
| Migrate unstructured data | D4 §3 | Data Box vs AzCopy | R4 |
| Connect Azure resources to the internet | [D4 §4](../04-infrastructure/README.md) | Private subnets by default; Standard SKU only | R4 |
| Connect Azure resources to on-premises networks | D4 §4 | ExpressRoute isn't encrypted; peering non-transitive | R4 |
| Optimize network performance | D4 §4 | Accelerated Networking; PPG vs zones | R4 |
| Optimize network security | D4 §4 | Private endpoint needs DNS; service endpoint no on-premises | R4 |
| Load-balancing and routing solution | D4 §4 | Traffic Manager is DNS only | R4 |

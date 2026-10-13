# Quick Revision

For after you've studied the domain files. One pass should take about 30 minutes. Decision tables live in [DECISION-MATRICES.md](DECISION-MATRICES.md).

## R1. Identity, governance, and monitoring

```text
Entra ID = who · Conditional Access = under what conditions · RBAC = what they can do · PIM = just-in-time · Policy = what's allowed
Metrics = fast · Logs = deep · Diagnostic settings = turn resource logs on
```

- **PHS** is the default hybrid sign-in. **PTA** validates on-premises. **Federation** only when forced. **Cloud Sync** for many/disconnected forests.
- **B2B** = partners in your tenant. **External ID** = customers (Azure AD B2C closed to new customers). **Entra DS** = legacy Kerberos/LDAP. **App Proxy** = publish on-premises web apps.
- **Conditional Access = P1.** **Identity Protection / PIM = P2.** **Entra ID Governance** = entitlement management, lifecycle workflows.
- **Managed identity** (system vs user-assigned) over secrets. **Key Vault**: soft delete + **purge protection** (needed for CMK); **Managed HSM** = single tenant; **App Configuration** = settings and flags.
- RBAC: **Contributor can't assign roles**; **Global Admin ≠ Azure Owner** (elevate access). Prefer **data-plane roles** over keys.
- Governance: management group (max **6 levels**) for Policy/RBAC; subscription = scale/billing; RG = lifecycle. **Tags don't inherit** (Policy). **Blueprints deprecated**.
- Policy: **Deny** blocks new, doesn't fix old; **DeployIfNotExists/Modify** need a managed identity and remediation. Defender for Cloud = posture + regulatory view. Purview = data governance.
- Identity governance: **entitlement management** (access packages, expiry), **access reviews** (recertify), **PIM** (eligible), **break-glass accounts**.
- Logging: **Log Analytics** (query), **Event Hubs** (SIEM), **Storage** (archive). **AMA + DCR** replace legacy agents. App Insights is workspace-based. Activity log = control plane.

| Pair | Difference |
|---|---|
| B2B vs External ID | Partners in workforce tenant vs customer identity |
| PIM vs access reviews | Just-in-time vs periodic recertification |
| Policy vs RBAC | Resource rules vs who may act |
| Sentinel vs Defender for Cloud | SIEM/SOAR vs posture and workload protection |
| Key Vault vs App Configuration | Secrets vs settings |

## R2. Data storage

```text
Relational → SQL DB / MI / VM · NoSQL → Cosmos DB · Objects → Blob/ADLS · Files → Azure Files/NetApp · Move → ADF/Fabric · Stream → Event Hubs
```

- **SQL DB** default; **MI** = SQL Agent, cross-DB, compatibility; **VM** = OS access.
- **GP** (cost) · **BC** (low latency, readable replica) · **Hyperscale** (huge, fast restore, named replicas). **Serverless** auto-pauses (cold start). **Elastic pool** = many DBs.
- **TDE** at rest; **Always Encrypted** hides from DBAs; **DDM/RLS** for query-time. **PITR ≤ 35 d**, **LTR ≤ 10 y**.
- **Cosmos**: consistency Strong · Bounded · **Session** · Prefix · Eventual. **Strong not with multi-region writes.** Partition key is the design. Autoscale vs serverless.
- Blob tiers **Hot · Cool 30 · Cold 90 · Archive 180 (offline)**. **Lifecycle** moves tiers. **ADLS Gen2** = hierarchical namespace.
- **Azure Files** SMB/NFS · **NetApp Files** enterprise performance · **Premium SSD v2 / Ultra** disks.
- Redundancy: LRS · ZRS · GRS · GZRS · **RA-** readable. **Premium accounts = LRS/ZRS only.** Redundancy ≠ backup.
- Integration: **ADF/Synapse/Fabric pipelines** (batch), **self-hosted IR** for on-premises, **Event Hubs + Stream Analytics** (real time), **Synapse Link** (no-ETL).

| Pair | Difference |
|---|---|
| SQL DB vs MI | Modern PaaS vs instance compatibility |
| TDE vs Always Encrypted | At rest vs from admins |
| Blob vs ADLS Gen2 | Flat vs hierarchical namespace |
| Dedicated vs serverless SQL pool | Provisioned DW vs pay per query |

## R3. Business continuity

```text
HA = stay up (zones) · DR = come back (region) · Backup = recover data (point in time)
RTO = time down · RPO = data lost
```

- Strategy: **active-active** → **hot** → **warm** → **cold/restore**. Pay for what RTO/RPO demand.
- **Composite SLA**: serial = multiply; parallel = `1 − (1−A)(1−B)`.
- **ASR** replicates + fails over (recovery plans, test failover); vault in **target** region. **Azure Backup** vault for VM in **same** region. ASR is **not backup**.
- Vaults: **Recovery Services** (VM, SQL/HANA in VM, Files, MARS) vs **Backup vault** (Blobs, Disks, PostgreSQL, AKS). Choose **GRS/ZRS before** first backup; **Cross Region Restore** needs GRS.
- Ransomware: **immutable vault**, **soft delete**, **MUA (Resource Guard)**.
- SQL DB: **PITR + LTR**, **geo-restore**. Cosmos: periodic vs **continuous**.
- Compute HA: **availability set 99.95%**, **zones 99.99% (2+ VMs)**, **VMSS Flexible**, zone-redundant LB/App Gateway, AKS multi-zone.
- Relational HA: **zone-redundant** setting, **auto-failover group** (listener endpoints), geo-replication (≤ 4 secondaries), PG/MySQL zone-redundant HA + cross-region replica, SQL VM **Always On AG**.
- **Forced failover can lose data** (async).
- Unstructured HA: **ZRS / GZRS / RA-GZRS**; account failover may lose data; Cosmos multi-region + multi-write.

| Pair | Difference |
|---|---|
| ASR vs Backup | Failover vs point-in-time recovery |
| Zones vs region pair | HA vs DR |
| Failover group vs geo-replication | Group + listener vs per-database |
| PITR vs LTR | Days vs years |

## R4. Infrastructure

```text
Compute ladder: VM → AKS → Container Apps / App Service → Functions / Logic Apps (more managed to the right)
Messaging: queue = command · topic = pub/sub · Event Grid = react · Event Hubs = stream
Network: connect → secure → distribute
```

- **Containers:** **Container Apps** (no K8s ops, KEDA, scale to zero) · **AKS** (K8s control) · **ACI** (single/short-lived). **Functions:** Flex Consumption · Premium (no cold start) · Dedicated. **Logic Apps** = connectors. **Batch** = HPC; **Spot** = interruptible.
- **Service Bus**: FIFO (sessions), transactions, DLQ, topics. **Storage Queue**: simple/huge. **Event Hubs**: stream/replay/Kafka. **Event Grid**: reactive push.
- **APIM**: policies, throttling, versions; **Premium** = multi-region, self-hosted gateway. **Redis** = cache, not system of record. **App Configuration** = flags. Bicep/OIDC pipelines; **slots/revisions** for blue-green.
- **Migration:** CAF strategy → plan → ready (landing zone) → adopt. **Azure Migrate** discover/assess/migrate. 5 Rs: rehost, refactor, rearchitect, rebuild, replace. **AVS** = VMware as-is. DB: **DMS** / **MI link** (online), **SSMA**. Data: **Data Box** (offline), **Storage Mover**, **AzCopy**, **File Sync**.
- **Connectivity:** **S2S VPN** (encrypted, internet) · **ExpressRoute** (private, **not encrypted**; MACsec/IPsec) · **Virtual WAN** (many branches) · **hub-spoke** (control) · **peering non-transitive**.
- **Internet:** new VNets **private by default**; **NAT Gateway** outbound; **Standard** SKUs only (Basic retired).
- **Security:** NSG/ASG, **Azure Firewall** (Premium: TLS inspection, IDPS), **WAF** (Front Door/App Gateway), **DDoS**, **Private endpoint + private DNS**, service endpoint (no on-premises), Bastion/JIT.
- **Balancing:** **Front Door** global L7 · **App Gateway** regional L7 + WAF · **Load Balancer** L4 · **Traffic Manager** DNS (no TLS/WAF/cache).

| Pair | Difference |
|---|---|
| Container Apps vs AKS | Hidden vs full Kubernetes |
| Event Grid vs Event Hubs | Reactive events vs high-volume stream |
| Front Door vs Traffic Manager | L7 proxy vs DNS routing |
| Service endpoint vs private endpoint | Public IP, subnet rule vs private IP |
| VPN vs ExpressRoute | Encrypted internet vs private circuit |

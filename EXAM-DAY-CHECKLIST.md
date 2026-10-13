# Exam-Day Checklist

No recalled or leaked questions here. This is a method plus a last-hour technical list.

## Before you start

- Use a personal Microsoft account to register (Microsoft recommends this over a work account).
- Take the exam in the language you studied in. If your language isn't available, you can request extra time.
- Check the proctoring rules and your ID in advance.
- Try the [exam sandbox](https://aka.ms/examdemo) once so the interface (including case studies) isn't new.
- Pass mark is **700**. Check the exam duration on your Pearson VUE confirmation.

## For every question

1. **Read the whole scenario** before the options.
2. **Find the actual requirement** (the last sentence usually asks it).
3. **List hard constraints**: region, compliance, RTO/RPO, SLA, existing environment.
4. **Identify the priority:** cheapest, least administrative effort, most secure, minimal change, fastest?
5. **Mark absolute words:** *must*, *only*, *cannot*, *minimum*, *at least*, *without*.
6. **Eliminate** options that break an explicit requirement. Then choose among what's left.
7. **Prefer the more managed service** when nothing says you need control.
8. **Don't add features** the question didn't ask for.

## Watch for

- Two similar services: Backup/ASR, Service Bus/Event Grid/Event Hubs, Front Door/Traffic Manager/App Gateway, MI/SQL DB.
- **Scope**: zone vs region, regional vs global, subscription vs management group.
- **HA vs DR vs backup.** Different tools for different failures.
- **Online vs offline** (migration, tiers). **Planned vs forced** failover.
- **Tier/SKU** requirements (APIM Premium, Premium Functions, Business Critical, Premium vault features).
- **Licensing**: P1 vs P2, Entra ID Governance.
- **Retired or replaced**: Azure AD B2C (new → External ID), Blueprints, Basic LB/public IP, Application Gateway v1, legacy Log Analytics agent, Azure Cache for Redis (→ Managed Redis).
- "**Least privilege**" means narrowest role at lowest scope; "**least effort**" means managed service.

## Case studies and multi-part questions

- Read each tab; requirements may apply to **all** questions in the case.
- In "does the solution meet the goal" sets, judge each proposal against the stated goal only.
- Some question types don't allow going back. Check the rules in the sandbox.

## Time

- Don't spend more than about 2 minutes on a first pass. Flag and move on.
- Case studies take longer to read; do the questions after you understand the environment.
- Use remaining time for flagged questions. Answer every question.

## Last-hour technical list

**Identity, governance, monitoring**
- PHS default, Cloud Sync for many forests, federation rarely. B2B = partners, External ID = customers.
- Conditional Access P1; risk-based and PIM P2. Managed identity over secrets. Key Vault soft delete + purge protection.
- Policy at management group; tags don't inherit. Blueprints deprecated.
- Diagnostic settings needed for resource logs; Event Hubs → SIEM; AMA + DCR.
- Entitlement management (request/expire), access reviews (recertify), PIM (just-in-time).

**Data storage**
- SQL DB vs MI (SQL Agent, cross-DB) vs VM (OS). GP / BC / Hyperscale. Serverless auto-pause.
- Always Encrypted hides from DBAs; TDE at rest. PITR ≤ 35 d, LTR up to 10 y.
- Cosmos: Session default, Strong not with multi-write, partition key matters.
- Tiers 30/90/180; Archive offline. ADLS Gen2 = Blob + hierarchical namespace.

**Business continuity**
- RTO time, RPO data loss. ASR replicates, Backup recovers points. Multiply serial SLAs.
- 99.99% VM = 2+ VMs across zones. Failover group listener. Forced failover may lose data.
- Vault region: backup = same region as VM; ASR = target region. Immutable vault + MUA.
- RA-GZRS = zone + region + readable secondary. Premium storage = LRS/ZRS only.

**Infrastructure**
- Highest abstraction that meets requirements. Container Apps vs AKS vs ACI. Flex Consumption vs Premium.
- Service Bus (ordering, transactions) / Event Grid (react) / Event Hubs (stream) / Storage Queue (simple).
- APIM Premium for multi-region/self-hosted gateway. Redis is a cache.
- Migrate: assess first; online vs offline; Data Box offline; AVS for VMware as-is.
- Front Door global L7, App Gateway regional L7, LB L4, Traffic Manager DNS. ExpressRoute not encrypted. Peering not transitive. Private endpoint needs DNS.

## After the exam

- The result and score report are available per Microsoft's process. If you don't pass, you can retake after 24 hours; see the [retake policy](https://learn.microsoft.com/en-us/credentials/support/retake-policy).
- To earn the Azure Solutions Architect Expert certification you also need the Azure Administrator Associate certification (see the [certification page](https://learn.microsoft.com/en-us/credentials/certifications/azure-solutions-architect/)).
- Renew every 12 months with the free assessment.

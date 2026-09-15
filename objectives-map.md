# SY0-701 to SY0-801 objective map

Every SY0-701 objective, where it went in SY0-801, and how much it changed.

Sources: CompTIA SY0-701 *Exam Objectives Version 5.0* and the SY0-801 V8 draft, *Exam Objectives Document Version 1.5*. Verified 2026-09-15.

**Status flags**

| Flag | Meaning |
|---|---|
| `SAME` | Same number, same scope. Minor wording at most. |
| `RENUM` | Same scope, different objective number. |
| `REWORK` | Scope changed materially, whether or not the number moved. |
| `MERGED` | Folded into another objective. |
| `SPLIT` | Contents distributed across more than one V8 objective. |
| `NEW` | No SY0-701 ancestor. |

---

## Domain 1: General Security Concepts

| SY0-701 | SY0-801 | Flag | Notes |
|---|---|---|---|
| 1.1 Types of security controls | **1.1** Security concepts and controls | `MERGED` | 1.1 and 1.2 combine. Adds "Operational" control category. |
| 1.2 Fundamental security concepts | **1.1** | `MERGED` | Reorganized under defense in depth. Gap analysis leaves for 5.5. Physical security hardware and deception tech leave the domain. |
| 1.3 Change management | **1.2** Change management impact | `REWORK` | Verb moves from "Explain the importance of" to "Given a scenario, demonstrate." Now PBQ-eligible. Adds fail forward, maintenance window, SOPs. |
| 1.4 Cryptographic solutions | **1.3** | `RENUM` | Adds database and record encryption levels, algorithms, key length. |

Domain weight 12% to 16%. Four objectives to three.

## Domain 2: Threats, Vulnerabilities, and Attacks

Renamed from "Threats, Vulnerabilities, and **Mitigations**." Every objective renumbers.

| SY0-701 | SY0-801 | Flag | Notes |
|---|---|---|---|
| (none) | **2.1** Characteristics of threats and vulnerabilities | `NEW` | New objective, but content is relocated from 701 4.3: threat feeds, intelligence sources, threat life cycle, CVSS, CVE, vulnerability scoring and prioritization. |
| 2.1 Threat actors and motivations | **2.2** | `REWORK` | Adds terrorist, competitor, accidental/unintentional actors. Adds notoriety, extortion, influence, general curiosity motivations. Shadow IT leaves for 2.4. |
| 2.2 Threat vectors and attack surfaces | **2.3** Threat vectors and sources | `SPLIT` | Vector content to 2.3, attack surface content to 2.4. 2.3 expands with RCS, CAPTCHA, browser session tokens, living-off-the-land, OT, IoT, signal-based, physical. |
| 2.3 Types of vulnerabilities | **2.4** Vulnerabilities and attack surfaces | `REWORK` | Adds LLMs, identity providers, rogue devices, shadow IT, stale credentials, public repositories and object storage. Web-based SQLi/XSS naming moves to 2.5 application attacks. |
| 2.4 Indicators of malicious activity | **2.5** | `REWORK` | Adds formal indicators-of-compromise grouping and a credential attacks grouping. Adds deepfake, quishing, fileless malware, MFA bypass, user enumeration. |
| 2.5 Mitigation techniques | **4.1** | `MERGED` | Leaves the domain entirely. This is why the domain title changed. |
| (none) | **2.6** AI threats and vulnerabilities | `NEW` | No SY0-701 ancestor of any kind. See [ai-security-additions.md](ai-security-additions.md). |

Domain weight 22% to 24%. Five objectives to six.

## Domain 3: Security Architecture

Numbering is stable. Contents are not.

| SY0-701 | SY0-801 | Flag | Notes |
|---|---|---|---|
| 3.1 Architecture models | **3.1** | `REWORK` | Adds multicloud, community cloud, data sovereignty, proprietary vs open source. SDN, containerization, ICS/SCADA, RTOS, and embedded systems do not appear. |
| 3.2 Secure enterprise infrastructure | **3.2** Manage the security architecture | `REWORK` | Zero Trust becomes an explicit block. Adds SSE, gMSA, privilege creep, out-of-band management, end-to-end encrypted messaging. SD-WAN and SASE do not appear. |
| 3.3 Protect data | **3.3** | `REWORK` | Data protection roles arrive from 701 5.1. Classification vocabulary rebuilt. Adds deidentification, data transpose, child/minor data. |
| 3.4 Resilience and recovery | **3.4** | `REWORK` | RTO, RPO, MTTR, MTBF arrive from 701 5.2. Adds autoscaling, immutability, restoration testing, surge protector. |

Domain weight 18% to 19%. Four objectives to four.

## Domain 4: Security Operations

One objective disappears. Everything after 4.2 shifts down by one.

| SY0-701 | SY0-801 | Flag | Notes |
|---|---|---|---|
| 4.1 Security techniques for computing resources | **4.1** Mitigating controls and solutions | `MERGED` | Absorbs 701 2.5 and 701 4.5. Now the largest objective on the exam. Adds canary account, WIPS, endpoint posture, secrets scanning, BIMI. |
| 4.2 Asset management | **4.2** | `SAME` | Adds explicit asset management life cycle and planning/scoping. Sanitization and destruction detail reduced. |
| 4.3 Vulnerability management | **4.3** | `REWORK` | Shrinks sharply. CVSS, CVE, false positive/negative, exposure factor move to 2.1. Adds IPAM and CSPM. Verb moves to "Given a scenario." |
| 4.4 Alerting and monitoring | **4.4** | `REWORK` | Protocols split out (NetFlow, SNMP, syslog, SCAP). Adds packet analyzer, port mirroring, dashboards, network management systems. |
| 4.5 Modify enterprise capabilities | **4.1** | `MERGED` | Objective removed. Contents absorbed into 4.1. User behavior analytics does not appear. |
| 4.6 Identity and access management | **4.5** | `REWORK` | Adds passkey, passwordless, compromised credential monitoring, account auditing, emergency access, time-based and just-in-time access. ABAC, attestation, password vaulting, ephemeral credentials do not appear. |
| 4.7 Automation and orchestration | **4.6** | `REWORK` | Verb moves to "Given a scenario." Adds the AI capability block, SecOps, CI/CD, workflows. |
| 4.8 Incident response | **4.7** | `REWORK` | Investigation becomes its own phase. Adds negotiation, notification and external reporting, mandatory reporting, PIR. |
| 4.9 Data sources for investigation | **4.8** | `REWORK` | Adds log and trace data taxonomy, system imaging (memory dump, bit-level copy, snapshot), log-parsing techniques, stakeholders. |

Domain weight 28% to 27%. Nine objectives to eight.

## Domain 5: Security Program Management and Oversight

Numbering is stable. Character of the domain changes, and it loses more weight than any other.

| SY0-701 | SY0-801 | Flag | Notes |
|---|---|---|---|
| 5.1 Security governance | **5.1** GRC artifacts | `REWORK` | Reframed from governance to documents. Adds runbooks, reference architecture, implementation guides, clean desk, data disposal, vulnerability disclosure. Governance structures and data roles do not appear here. |
| 5.2 Risk management | **5.2** | `REWORK` | Adds risk identification, categorization, current mitigations, management oversight. RTO/RPO/MTTR/MTBF leave for 3.4. Exposure factor, KRIs, risk threshold, assessment cadence do not appear. |
| 5.3 Third-party risk | **5.3** | `REWORK` | Adds full procurement vocabulary: RFP, RFI, RFQ, EOI, SLO, vendor registry, compliance attestation, vendor lock-in, limitations and constraints. BPA does not appear. |
| 5.4 Security compliance | **5.4** | `REWORK` | Adds compliance training, AML/CTF, anti-bribery, legal hold, legal orders, processing restrictions. |
| 5.5 Audits and assessments | **5.5** Audit and assessment activities | `REWORK` | Adds data gathering, scoping, audit charter, gap analysis, benchmarking, functional and behavioral testing, and MITRE ATT&CK / Cyber Kill Chain / Diamond Model as reference sources. |
| 5.6 Security awareness | **5.6** | `REWORK` | Adds training types, delivery mechanisms, LMS, personnel behavior risk scoring, BEC. Phishing campaign development reduced. |

Domain weight 20% to 14%. Six objectives to six.

---

## Summary counts

| | SY0-701 | SY0-801 |
|---|---|---|
| Objectives | 28 | 27 |
| `NEW` objectives | (none) | 2 |
| Objectives removed | 2 | (none) |
| Objectives renumbered | (none) | 11 |
| Objectives materially reworked | (none) | 20 |
| Objectives essentially unchanged | (none) | 1 |

Only one objective out of 27 carries over without material change. Treating this as "a light refresh because the domain count is the same" is the mistake to avoid.

---

## Using this as data

If you are migrating a question bank, courseware, or progress tracking across versions, the mapping above is the join key. Two things to plan for:

1. **`MERGED` and `SPLIT` rows are not one-to-one.** Old 2.5 and old 4.5 both collapse into new 4.1, and old 2.2 splits across new 2.3 and 2.4. Any naive one-to-one remap loses or duplicates content at those four points.
2. **Learner progress keyed to objective IDs will silently mis-map.** A learner with mastery on 701 objective 4.6 is not a learner with mastery on V8 objective 4.6, because 4.6 changed meaning from IAM to automation. Remap before migrating, or reset rather than corrupt.

A machine-readable version of this table lives in [objectives-map.csv](objectives-map.csv).

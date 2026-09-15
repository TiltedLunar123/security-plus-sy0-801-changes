# CompTIA Security+ SY0-801 (V8): What Actually Changed

An objective-by-objective diff between **Security+ SY0-701 (V7)** and the **SY0-801 (V8) draft**, built by reading both official CompTIA documents side by side rather than summarizing press coverage.

No exam questions, no braindumps, no copies of CompTIA's objectives. This is analysis of what moved, what's new, and what's gone, so you can decide which exam to sit and what to restudy.

---

## Status

| | |
|---|---|
| **V8 source** | CompTIA draft, *Exam Objectives Document Version 1.5* |
| **V7 source** | CompTIA SY0-701, *Exam Objectives Version 5.0* |
| **Last verified** | 2026-09-15 |
| **V8 draft SHA-256** | `c8c03edc99fb7bec55ecdd2c74b20e7aaea62e005f7351749a6d9b082999effb` |
| **V8 status** | Draft. Posted publicly by CompTIA for feedback. Content can still change. |

> **Note on the version number.** CompTIA's download page labels this draft **1.2**, but the PDF's own footer on every page reads **Document Version 1.5**. The two disagree. This repo tracks the PDF, and the SHA-256 above is how you can tell whether CompTIA has quietly replaced the file since this was written.

**Get the official documents yourself:**
- [V8 draft objectives](https://www.comptia.org/en-us/resources/comptia-exam-objectives-under-development/) (free, no signup, listed as "DRAFT CompTIA Security+ V8 Exam Objectives")
- [SY0-701 objectives](https://www.comptia.org/en-us/certifications/security/) (current exam)

---

## Three things nearly every article about this gets wrong

**1. "SY0-801" is the official code.** A lot of coverage says the code is unconfirmed and that CompTIA only calls it "V8." That is not what the document says. The draft's cover page reads `EXAM NUMBER: SY0-801 V8`, and all 27 page footers read "CompTIA Security+ SY0-801 V8 Certification Exam." The code is published.

**2. Question count and exam length are already published.** Several summaries claim these are still TBD. The draft specifies them, and they are identical to SY0-701:

| | SY0-701 | SY0-801 |
|---|---|---|
| Max questions | 90 | 90 |
| Time | 90 minutes | 90 minutes |
| Passing score | 750 / 900 | 750 / 900 |
| Question types | Multiple choice + PBQ | Multiple choice + PBQ |

**3. SY0-701 does not retire "in late 2026."** CompTIA's certification page lists the English retirement as **June 11, 2027** (August 13, 2027 for Japanese, Portuguese, Spanish, and Thai). There is no officially announced launch date for SY0-801 at all. Dates circulating for late 2026 come from training vendors and instructor channels, not from CompTIA.

---

## Domain weights

| Domain | SY0-701 | SY0-801 | Change |
|---|---|---|---|
| 1.0 General Security Concepts | 12% | **16%** | +4 |
| 2.0 Threats, Vulnerabilities, and ~~Mitigations~~ → **Attacks** | 22% | **24%** | +2 |
| 3.0 Security Architecture | 18% | **19%** | +1 |
| 4.0 Security Operations | 28% | **27%** | -1 |
| 5.0 Security Program Management and Oversight | 20% | **14%** | **-6** |

Domain 2 is renamed. "Mitigations" comes out of the title because the mitigation objective itself was moved into Domain 4.

The headline is Domain 5. Losing six points is the largest single shift in the exam, and it means governance, risk, third-party, compliance, and audit content drops from roughly one question in five to roughly one in seven.

## Objective counts

| Domain | SY0-701 | SY0-801 |
|---|---|---|
| 1.0 | 4 | 3 |
| 2.0 | 5 | **6** |
| 3.0 | 4 | 4 |
| 4.0 | 9 | 8 |
| 5.0 | 6 | 6 |
| **Total** | **28** | **27** |

One fewer objective overall, but the churn underneath is much larger than that number suggests. Full objective-to-objective mapping is in **[objectives-map.md](objectives-map.md)**.

---

## The headline change: AI is on the exam twice

SY0-701 mentions artificial intelligence essentially nowhere. SY0-801 adds it in two separate places, from two opposite angles.

**Objective 2.6 is entirely new** and has no SY0-701 ancestor of any kind. It covers AI as a *threat surface*: model manipulation, poisoning, prompt injection, jailbreaking, evasion, hallucinations, bias, explainability, data loss, privacy, ethical considerations, session hijacking, and code execution.

**Objective 4.6 adds an AI block** to automation and orchestration, covering AI as a *defensive capability*: agentic systems, chatbots, predictive analysis, and AI-augmented baselines.

`AI` and `LLM` are both new entries in the acronym list, and "Large language models (LLMs)" appears as a named vulnerability type under objective 2.4.

Full breakdown in **[ai-security-additions.md](ai-security-additions.md)**. If you are studying from SY0-701 material, this is content you have simply never seen, and it sits inside the domain that carries the second-highest weight on the exam.

---

## What changed, domain by domain

### Domain 1: General Security Concepts (12% to 16%)

Four objectives collapse into three while the domain gains four points of weight. That combination means the surviving objectives are each tested harder.

- **1.1 absorbs old 1.2.** SY0-701 split "types of security controls" (1.1) and "fundamental security concepts" (1.2) into two objectives. V8 merges them into a single 1.1 organized around defense in depth, with CIA, AAA, non-repudiation, Zero Trust, and least privilege underneath it. An "Operational" control category joins technical, managerial, and physical.
- **Change management becomes scenario-based.** Old 1.3 was "Explain the importance of change management processes." New 1.2 is "**Given a scenario**, demonstrate the impact of change management processes on security." That verb change moves it into PBQ territory. Fail forward, maintenance windows, and SOPs are now named explicitly.
- **Cryptography is restructured, not reduced.** Old 1.4 becomes 1.3. Encryption levels gain database and record granularity, and algorithms and key length are called out directly.
- **Gone from this domain:** gap analysis moves to 5.5. The physical security hardware list and deception technology both leave Domain 1, with honeypots and honeytokens landing in 4.1.

### Domain 2: Threats, Vulnerabilities, and Attacks (22% to 24%)

The most restructured domain in the exam. Five objectives become six, every one is renumbered, and the domain is renamed.

- **New 2.1, "Explain characteristics of threats and vulnerabilities."** Threat feeds, likelihood, impact, intelligence sources, and threat life cycle, plus vulnerability scoring, prioritization, CVSS, and CVE. Most of this content existed in SY0-701 but lived in Domain 4 under vulnerability management. Pulling CVSS and CVE forward into Domain 2 is one of the larger structural moves in V8.
- **New 2.6, AI threats.** Covered above.
- **Threat vectors (old 2.2, new 2.3) expand significantly.** Additions include RCS messaging, CAPTCHA abuse, password managers and session tokens as browser-based vectors, living-off-the-land tools, trusted devices, OT-based and IoT-based vectors, signal-based vectors (Bluetooth, RF, NFC), and physical vectors. APT appears here as a named vector.
- **Threat actors (old 2.1, new 2.2) shift.** Terrorist, competitor, and accidental/unintentional join the actor list. Motivations add notoriety, extortion, influence, and general curiosity. Shadow IT stops being a threat actor and becomes a vulnerability under 2.4.
- **Indicators (old 2.4, new 2.5) gain a formal IOC section.** Hashes, IPs, domains, malicious processes, file system artifacts, timestamps, and log manipulation are grouped as indicators of compromise. Credential attacks become their own grouping, including MFA bypass and user enumeration. Deepfake and quishing are newly named. Fileless malware is added.
- **Old 2.5, mitigation techniques, is gone as an objective.** Its content moved to Domain 4 under new 4.1. This is why the domain title dropped the word "Mitigations."

### Domain 3: Security Architecture (18% to 19%)

Same four objectives, same numbering, but the contents move around a lot.

- **Zero Trust becomes an explicit architecture block in 3.2**, with user authentication, device health and inventory, and application access control underneath it.
- **Security Service Edge (SSE) appears.** SD-WAN and SASE, both named in SY0-701, do not appear in the V8 draft.
- **Identity management enters Domain 3**, including group managed service accounts (gMSA, a new acronym) and privilege creep.
- **Data protection roles move here from Domain 5.** Owner, custodian, steward, operator, controller, and subprocessor now sit under 3.3 rather than under governance.
- **Recovery metrics move here from Domain 5.** RTO, RPO, MTTR, and MTBF are now part of 3.4 resilience rather than 5.2 risk management. If you learned those as risk-domain content, they are now architecture content.
- **Data classification vocabulary is rebuilt** around sensitive, secret, confidential, critical, public, top secret, and restricted. Deidentification and data transpose are new methods.
- **Gone:** software-defined networking, containerization, ICS/SCADA, RTOS, and embedded systems all disappear as named architecture topics.

### Domain 4: Security Operations (28% to 27%)

Nine objectives become eight, and the numbering after 4.2 is offset by one for the rest of the domain.

- **Old 4.5 is absorbed.** "Modify enterprise capabilities to enhance security" is merged, along with old 2.5 mitigation techniques, into a single large new 4.1. That objective now carries segmentation, hardening, sandboxing, deception, IDS/IPS, firewalls, content filtering, endpoint security, NAC, application security, email security, and OS security.
- **New named items in 4.1:** canary accounts, wireless intrusion prevention (WIPS), endpoint posture and compliance checks, secrets scanning in repositories, and BIMI alongside DMARC, SPF, and DKIM.
- **Vulnerability management (4.3) shrinks sharply.** CVSS, CVE, false positives and negatives, and exposure factor largely move out to 2.1. What remains gains IPAM and cloud security posture management (CSPM) as identification methods.
- **Incident response (old 4.8, new 4.7) gains investigation, negotiation, and mandatory reporting.** Investigation becomes its own phase covering digital forensics, chain of custody, e-discovery, and preservation. "Negotiation" is a new topic. Notification and external reporting now names stakeholders, customers, law enforcement, and mandatory reporting, and post-incident reporting (PIR) is a new acronym.
- **Automation (old 4.7, new 4.6) becomes scenario-based** and gains the AI capability block, plus SecOps and CI/CD.
- **Investigation data (old 4.9, new 4.8) gains forensic imaging.** Memory dumps, bit-level copies, and snapshots are new, as are log-parsing techniques and a formal log and trace data taxonomy.
- **IAM (old 4.6, new 4.5) adds passkeys, passwordless, compromised credential monitoring, account auditing, and emergency access accounts.** Attribute-based access control, attestation, password vaulting, and ephemeral credentials do not appear in the V8 draft.

### Domain 5: Security Program Management and Oversight (20% to 14%)

Same six objectives, same numbering, heaviest weight loss on the exam, and a real change in character. Domain 5 becomes less about governance structure and more about documents, procurement, and financial crime compliance.

- **5.1 is reframed from "security governance" to "governance, risk, and compliance artifacts."** It is now a documents objective: guidelines, standards, procedures, plans, and policies. Governance structures such as boards and committees do not appear in the draft. Runbooks, reference architectures, implementation guides, clean desk policy, data disposal policy, and vulnerability disclosure policy are new.
- **5.3 gains a full procurement vocabulary.** RFP, RFI, RFQ, and EOI are all new, as are service-level objectives (SLO), vendor registries, compliance attestation, vendor lock-in, and a limitations and constraints section covering staffing, jurisdiction, and ROI.
- **5.4 adds financial crime compliance.** Anti-money laundering and counter-terrorism financing (AML/CTF) and anti-bribery are new compliance training topics. Legal hold moves here from incident response.
- **5.5 adds threat-intelligence frameworks.** MITRE ATT&CK, the Cyber Kill Chain, and the Diamond Model of Intrusion Analysis are named in the Security+ objectives for the first time, as reference sources for audit data gathering. Gap analysis, benchmarking, functional testing, and behavioral testing are also new here.
- **5.6 formalizes training delivery.** Types of training, delivery mechanisms including LMS and self-service portals, personnel behavior risk scoring, and business email compromise (BEC) are new.

---

## New acronyms in V8

These appear in the SY0-801 acronym list and not in SY0-701's, which is a fast proxy for genuinely new content:

`AI` · `LLM` · `gMSA` · `SSE` · `BIMI` · `CSPM` · `IPAM` · `EOI` · `RFQ` · `RCS` · `PIR` · `AML/CTF` · `CWE` · `NVD` · `IPFIX` · `TOC` · `TOU` · `SELinux` · `RPS` · `GBIC` · `SFP`

---

## If you are studying right now

**Sit SY0-701.** It is the only bookable Security+ today, it is bookable until June 11 2027, and the certification does not expire or downgrade when a new version launches. On a resume it reads "CompTIA Security+" with no version number, valid for three years from the day you pass.

There is no scenario where waiting for SY0-801 helps someone who is ready to test now. Waiting costs you months of certified time in exchange for an exam that covers more material for the same passing score.

**If you are six or more months out**, keep studying 701 material anyway. About 80 percent of V8 content is carried over, and the two AI objectives plus the Domain 5 procurement vocabulary are the only parts you would genuinely have to learn fresh.

See **[faq.md](faq.md)** for the rest.

---

## Accuracy and corrections

This is a reading of a draft. CompTIA revises drafts, and the final objectives may differ.

Statements here fall into three buckets, and the language is deliberate:
- "X is new" or "X appears" means it is present in the V8 draft and absent from SY0-701 v5.0.
- "X does not appear in the V8 draft" means exactly that. A draft omission is not a promise that the topic is untested. CompTIA states plainly that its bulleted lists are not exhaustive.
- Weights, objective numbers, titles, and test details are quoted from the two documents directly.

Found an error, or noticed CompTIA has updated the draft? [Open an issue](../../issues). The SHA-256 at the top of this file is there so drift is detectable rather than assumed.

## Licence

Analysis and prose: [CC BY 4.0](LICENSE). Use it, adapt it, credit it.

CompTIA's exam objectives are their copyright and are deliberately **not** reproduced here. Every objective document linked above comes from CompTIA directly. CompTIA, Security+, and SecurityX are trademarks of CompTIA, Inc. This project is not affiliated with, endorsed by, or authorized by CompTIA.

---

*Maintained by [Jude Hilgendorf](https://github.com/TiltedLunar123), Security+ certified. I also build [SecPlus Mastery](https://secplusmastery.com), a mastery-based Security+ study platform.*

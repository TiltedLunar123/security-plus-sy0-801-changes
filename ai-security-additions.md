# AI on the Security+ exam: everything V8 added

SY0-701 does not test artificial intelligence. SY0-801 tests it in three places, and one of them is an entire new objective.

This page covers what was added and what each term actually means, because if you are studying from 701 material none of it exists in your notes.

---

## Where AI shows up

| Location | Angle | Status |
|---|---|---|
| **2.6** Threats and vulnerabilities associated with AI usage | AI as the thing attacking you, or the thing being attacked | Entirely new objective |
| **4.6** Automation and orchestration | AI as a defensive capability you operate | New block inside a reworked objective |
| **2.4** Types of vulnerabilities and attack surfaces | LLMs named as a vulnerability type | New line item |

`AI` and `LLM` are both new entries in the V8 acronym list.

The split matters for how you answer questions. Domain 2 asks how AI gets abused. Domain 4 asks how you use it. A question about prompt injection is a 2.6 question. A question about AI-augmented baselines in a SOC is a 4.6 question.

---

## Objective 2.6, term by term

Thirteen topics, none of which have a SY0-701 equivalent.

### Model manipulation
Altering a model's behaviour by tampering with the model itself, its weights, or its configuration rather than its inputs. The supply chain angle matters here: a model pulled from a public registry is third-party code with the same provenance problems as any other dependency.

### Poisoning
Corrupting training data so the model learns something the attacker wants. Unlike most attacks, it happens before deployment and persists invisibly afterwards. Classic exam framing: the attack surface is the data pipeline, and the control is data provenance and validation.

### Prompt injection
Untrusted input is interpreted as instructions rather than data. The point that gets tested is the boundary: a model reading a web page, an email, or a document cannot reliably tell content apart from commands. *Indirect* prompt injection, where the payload is planted in a document the model will later read, is the version that matters in an enterprise.

Treat it as the AI-era equivalent of injection flaws generally, which is exactly how the objectives place it.

### Data loss
Sensitive data leaving the organization through an AI system. Two directions: staff pasting confidential material into a third-party model, and a model disclosing training data or another tenant's context in its output. The first is a DLP and acceptable-use problem, the second is an architecture problem.

### Bias
Systematic skew in output that produces unfair or incorrect outcomes. On a security exam this is a governance and compliance issue rather than a technical one, which is why it sits alongside ethical considerations.

### Explainability
Whether you can account for why a model produced a given output. Matters for audit, for regulatory defensibility, and for incident response. If an AI system made a security decision you cannot explain, you cannot defend it to an auditor.

### Hallucinations
Confident, fluent output that is factually wrong. The security relevance is the automation risk: a hallucinated result acted on by an automated workflow becomes a real-world error at machine speed.

### Jailbreaking
Getting a model to bypass its own safety constraints. Distinct from prompt injection, though they overlap. Injection is about confusing data with instructions. Jailbreaking is about defeating guardrails directly.

### Evasion
Crafting input that causes a model to misclassify. The defensive version matters most on this exam: malware or phishing shaped specifically to slip past an AI-based detector.

### Privacy
Personal data processed by models, including whether it can be extracted later. Connects to the 5.4 compliance material, especially right to be forgotten, which is difficult when data is baked into model weights.

### Ethical considerations
Acceptable use, transparency with users, and the human oversight question. Pairs with bias.

### Session hijacking
Taking over an authenticated AI session or its context. In an agentic system the session may hold credentials and tool access, which makes it worth substantially more than a normal web session.

### Code execution
An AI system executing code, either as a designed feature or because an attacker induced it. The highest-severity item on this list, because it converts a text vulnerability into remote code execution. An agent with shell or API access is a privileged account.

---

## Objective 4.6, the defensive side

The automation and orchestration objective was reworded to "**Given a scenario**, apply automation and orchestration solutions," so it is now scenario-based, and it gained an AI block:

- **Agentic.** AI systems that take actions rather than just producing text. Note that this is where the security concern from 2.6 and the capability in 4.6 meet: the more agency, the more the session hijacking and code execution risks matter.
- **Chatbot.** Conversational interfaces, including for tier-one support and internal help desks.
- **Predictive analysis.** Forecasting from historical security data.
- **AI-augmented baselines.** Using models to establish what normal looks like, so anomaly detection is not hand-tuned.

The same objective also gained SecOps and CI/CD content, plus workflow automation and integrations.

---

## Objective 2.4: LLMs as a vulnerability type

"Large language models (LLMs)" is listed as a vulnerability type alongside unsupported products, unpatched systems, misconfigurations, and shadow IT. The framing is deliberate: an LLM in your environment is another asset with an attack surface, not a special case.

Note the neighbours it was given. Public repositories and public object storage are also new in 2.4, and stale credentials, rogue devices, and shadow IT all appear there too. The theme of the whole objective shifted toward asset hygiene and things running in your environment that nobody is managing. An unsanctioned LLM integration fits that theme exactly.

---

## How this is likely to be tested

Nothing below is from a real exam. This is inference from the objective verbs, which is the only legitimate signal available.

**2.6 uses "Summarize."** In CompTIA's verb hierarchy that is the lighter end: definitions, recognition, and distinguishing between similar terms. Expect multiple choice asking you to identify which attack a scenario describes rather than to implement a defence. The pairs most worth being able to separate cleanly are prompt injection vs jailbreaking, poisoning vs evasion, and hallucination vs bias.

**4.6 uses "Given a scenario."** That is the heavier end and PBQ-eligible. AI content there is more likely to appear as part of a broader automation scenario than as a standalone AI question.

**2.4 lists LLMs among many vulnerability types**, so expect it as a distractor or a single line item rather than the subject of a whole question.

Domain 2 carries 24 percent of the exam across six objectives. If the weight were distributed evenly, 2.6 would be around 4 percent, or roughly three or four questions out of 90. Even weighting is an assumption, not a published figure, so treat that as a rough scale rather than a number to plan around.

---

## If you already work in security

Most of 2.6 will be familiar if you have followed AI security at all in the last two years. The vocabulary maps onto the OWASP Top 10 for LLM Applications closely enough that reading it is a reasonable way to get the concepts, but be careful: CompTIA's list is its own, the term boundaries are not identical, and the exam tests CompTIA's framing. Use OWASP for understanding, not for terminology.

---

*Part of [CompTIA Security+ SY0-801 (V8): What Actually Changed](README.md). Based on the CompTIA V8 draft, Exam Objectives Document Version 1.5, verified 2026-09-15. Draft content can change.*

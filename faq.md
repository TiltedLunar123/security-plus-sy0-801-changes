# SY0-701 vs SY0-801: the questions people actually ask

Verified 2026-09-15 against CompTIA's published pages and the V8 draft. Where something is not officially published, this page says so instead of guessing.

---

### Should I wait for SY0-801?

No, assuming you are anywhere close to ready.

Waiting costs you months of certified time and gets you a harder exam. SY0-801 covers more material (27 objectives with two genuinely new AI objectives) for the same 750 passing score and the same 90 minutes. There is no discount for taking the newer version.

Wait only if you are more than about nine months from testing anyway, in which case the choice makes itself.

### Does my Security+ become worthless when SY0-801 launches?

No. This is the single most common misconception.

A CompTIA certification does not expire or downgrade when a new exam version ships. Pass SY0-701 and you hold CompTIA Security+ for three years from your pass date, regardless of what version is current at the end of that period.

On a resume and in HR systems it reads "CompTIA Security+" with no version number attached. Nobody asks whether you sat 601, 701, or 801.

### When does SY0-701 retire?

**June 11, 2027** for English. August 13, 2027 for Japanese, Portuguese, Spanish, and Thai. This is published on CompTIA's own certification page, not an estimate.

### When does SY0-801 launch?

**CompTIA has not announced a date.**

Dates circulating online, most commonly October 20 and November 17 2026, come from training vendors and instructor-channel conversations. They are not on any CompTIA page. CompTIA has historically moved announced dates by several months, and the draft objectives themselves carry no date.

The honest answer is that the objectives are public and the launch is not scheduled publicly.

### Is "SY0-801" the real exam code?

Yes. The draft's cover page reads `EXAM NUMBER: SY0-801 V8` and every page footer names the exam "CompTIA Security+ SY0-801 V8."

A lot of articles claim the code is unconfirmed and CompTIA only says "V8." Those articles have not opened the PDF.

### Is the exam harder?

More material, same scoring. 27 objectives instead of 28, but with more content packed into them, two new AI objectives, and two objectives upgraded to "Given a scenario" phrasing, which makes them performance-based-question eligible.

Same 90 questions, same 90 minutes, same 750 out of 900 to pass.

### How much of my SY0-701 studying carries over?

Most of it. All five domains survive, the structure is recognizable, and the bulk of the technical content is unchanged or relocated rather than deleted.

What you would genuinely have to learn fresh:
1. Objective 2.6, AI threats, which has no 701 ancestor at all
2. The AI capability block in 4.6
3. The procurement vocabulary in 5.3 (RFP, RFI, RFQ, EOI, SLO, vendor lock-in)
4. AML/CTF and anti-bribery in 5.4
5. MITRE ATT&CK, Cyber Kill Chain, and Diamond Model in 5.5

What you would have to *relearn the location of*, which matters for scenario questions:
- CVSS and CVE move from Domain 4 to Domain 2
- RTO, RPO, MTTR, MTBF move from Domain 5 to Domain 3
- Data protection roles move from Domain 5 to Domain 3
- Mitigation techniques move from Domain 2 to Domain 4

### Which domain changed the most?

Domain 2 structurally, Domain 5 by weight.

Domain 2 renames, renumbers every objective, gains two and loses one. Domain 5 keeps all six objectives and their numbers but drops from 20 percent to 14 percent, the largest weight change on the exam, and shifts in character from governance structure toward documents, procurement, and compliance training.

### I am studying with a course or book for 701. Is it wasted?

No, and it is still the right material to use, because 701 is the exam you can actually book.

If you end up sitting 801, come back to [objectives-map.md](objectives-map.md) and treat it as a gap list rather than starting over.

### Are the draft objectives final?

No. CompTIA posts drafts publicly to collect feedback and explicitly reserves the right to change them. The draft in this repo is Document Version 1.5, meaning it has already been revised.

CompTIA also states that the bulleted lists in any objectives document are not exhaustive, so a topic missing from the draft is not a guarantee it will not be tested.

### Where do I get the official documents?

- [V8 draft objectives](https://www.comptia.org/en-us/resources/comptia-exam-objectives-under-development/), free, no signup
- [SY0-701 objectives](https://www.comptia.org/en-us/certifications/security/)

Get them from CompTIA directly. Mirrors go stale, and CompTIA has strong opinions about unauthorized third-party training content.

### Can I trust this repo?

Trust the primary sources above more. This is one person's reading of two PDFs, published with a SHA-256 of the draft so you can tell whether the source has changed since.

Found something wrong? [Open an issue](../../issues). Corrections are the point.

---

*Part of [CompTIA Security+ SY0-801 (V8): What Actually Changed](README.md).*

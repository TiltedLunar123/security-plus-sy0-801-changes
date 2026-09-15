# Changelog

This repo tracks a moving target. CompTIA revises draft objectives without
announcing it, so every entry records which source document the analysis was
built against and its hash.

**Watch this repo** if you want to know when the draft changes.

## How drift is detected

The SHA-256 of CompTIA's draft PDF is recorded in the README. To check whether
CompTIA has replaced the file since the last verification:

```bash
curl -sL -o v8.pdf "https://lecbyo.files.cmp.optimizely.com/download/77f3bd3223ac11f180820e495f189928"
sha256sum v8.pdf
```

If the hash differs from the README, the draft has been revised and this
analysis is stale until updated. Please open an issue if you spot it first.

Note that the download URL above is CompTIA's CDN link as of the date below and
may itself change. The stable entry point is always the
[objectives under development page](https://www.comptia.org/en-us/resources/comptia-exam-objectives-under-development/).

---

## 2026-09-15

Initial analysis.

**Sources**
- SY0-801 V8 draft, *Exam Objectives Document Version 1.5*
  SHA-256 `c8c03edc99fb7bec55ecdd2c74b20e7aaea62e005f7351749a6d9b082999effb`
- SY0-701, *Exam Objectives Version 5.0*
  SHA-256 `64e5a75df0e6105c724990476b678cf63533d241261538f53d99d2cc73690eba`

**Notes**
- CompTIA's download page labels the draft "1.2" while the PDF footer reads
  "Document Version 1.5". The discrepancy is unexplained. This repo tracks the
  PDF's own version string.
- No SY0-801 launch date is published by CompTIA as of this date.
- SY0-701 English retirement is published as 2027-06-11.

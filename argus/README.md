# Argus — Research Log

Improvement research for **Argus** (Jira: `ARQ`).
**Focus areas:** quant methods, event studies, signal generation, Tessera integration.

Newest entries at the top. Each note should end with a recommendation and, once
filed, the Jira key of the task it produced.

---

### Template
```
### <Date> — <Topic>
**Question:** what are we trying to improve?
**Findings:** what best-in-class tools do (with sources).
**Recommendation:** the concrete change.
**Jira:** ARQ-nn
```

---

### 2026-07-13 — Competitive & market landscape
**Question:** Is there room for an honesty-first, local investment-research log + event-study engine?
**Findings:** No priced competitor combines an immutable, falsifiable, market-graded research
log with an accessible event-study engine. Decision-journaling has no purpose-built software;
prediction-trackers (Fatebook/Metaculus) don't grade theses against the market. Event studies
are gated (WRDS) or DIY (Python). TAM is thin (thousands–low-tens-of-thousands). `yfinance`
ToS is the key risk. Full write-up:
[2026-07-13-market-landscape.md](./2026-07-13-market-landscape.md).
**Recommendation:** Position as "a lab notebook for investors — falsifiable theses graded by
the market"; market Pegasus as "WRDS-grade event studies, offline and free"; keep price
fetching strictly user-side; favor an open-core / low-price model.
**Jira:** ARQ — (recommendation pending triage)

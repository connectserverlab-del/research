# Tessera — Research Log

Improvement research for **Tessera** (Jira: `ACE`).
**Focus areas:** Excel / Desmos parity, compute engine, MATLAB & Python conversion.

Newest entries at the top. Each note should end with a recommendation and, once
filed, the Jira key of the task it produced.

---

### Template
```
### <Date> — <Topic>
**Question:** what are we trying to improve?
**Findings:** what best-in-class tools do (with sources).
**Recommendation:** the concrete change.
**Jira:** ACE-nn
```

---

### 2026-07-13 — Competitive & market landscape
**Question:** Where does Tessera win in a mature, Excel/Sheets-dominated spreadsheet market?
**Findings:** The base grid is a commodity; growth is in the AI layer and live-data wedges.
NL→formula is now table stakes (Excel `=COPILOT()`, Sheets Gemini) — no longer a moat.
Live-market-data support elsewhere is shallow (`GOOGLEFINANCE`, `STOCKHISTORY`) or lives in
add-ins/terminals (Wisesheets, Koyfin). No competitor pairs a native `STOCK()` function +
in-app Market panel + first-class graph sheets. Full write-up:
[2026-07-13-market-landscape.md](./2026-07-13-market-landscape.md).
**Recommendation:** Lead with the finance-native + graphing-native combination; frame AI as
"formulas you can read and verify" vs opaque AI cells; ship a no-login browser entry with
flat prosumer pricing.
**Jira:** ACE — (recommendation pending triage)

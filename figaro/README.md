# Figaro — Research Log

Improvement research for **Figaro** (Jira: `FIG`).
**Focus areas:** agentic commerce, human-in-the-loop approval UX, deep-link handoff,
Twilio/SMS, Claude NL intents.

> Figaro is a standalone personal-concierge product, not part of the Lumina suite proper —
> filed here as its own research stream.

Newest entries at the top. Each note should end with a recommendation and, once
filed, the Jira key of the task it produced.

---

### Template
```
### <Date> — <Topic>
**Question:** what are we trying to improve?
**Findings:** what best-in-class tools do (with sources).
**Recommendation:** the concrete change.
**Jira:** FIG-nn
```

---

### 2026-07-13 — Competitive & market landscape
**Question:** Is there a defensible indie niche for an SMS-approval concierge as big-tech agents rise?
**Findings:** The whole industry just standardized Figaro's core idea — human-in-the-loop
approval before consequential actions (OpenAI "confirm before purchase," Google AP2 "Cart
Mandate"). No *indie/personal* tool combines a trigger + SMS approval gate + pre-filled
deep-link handoff; big-tech agents require their ecosystem/subscription and autonomous-spend
trust, and human concierges (Duckbill $99–169/mo) cost 10–50×. Uber/DoorDash deep links are
officially supported; open consumer-ordering APIs still don't exist for indies (the
ACP/AP2 rails are gated), so Figaro's deep-link premise holds in 2025–26. Full write-up:
[2026-07-13-market-landscape.md](./2026-07-13-market-landscape.md).
**Recommendation:** Lead with "approval-first agent — you stay in the loop by design";
secondary "fast lane for actions you already know you want"; brand around "own your assistant
— no ecosystem, no ads, no monthly fee." Frame the deep-link handoff as intentional control,
not a limitation.
**Jira:** FIG — (recommendation pending triage)

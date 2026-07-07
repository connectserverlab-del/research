<div align="center">

# Lumina — Research Hub

**Improvement research and notes for the suite, organized by product.**

</div>

This is where research for the Lumina suite lives: competitive analysis, feature
studies, and improvement ideas that feed the backlog. Organized one folder per
product so each stream stays focused.

| Product | Notes | Jira | Feeds |
| --- | --- | --- | --- |
| **Tessera** | [`tessera/`](./tessera) | `ACE` | Excel / Desmos / MATLAB parity, compute features |
| **Argus** | [`argus/`](./argus) | `ARQ` | quant methods, signals, Tessera integration |
| **Vellum** | [`vellum/`](./vellum) | `LUM` | Obsidian / Google-Docs parity, math typing, mind-mapping |

## How it works

- Each product folder holds a running **research log** (`README.md`) plus any
  deeper write-ups.
- A research note should end with a concrete recommendation → which becomes a
  scoped Jira task (labeled `auto-agent`) that the development pipeline picks up.
- The overnight **Research & Prioritize** routine adds findings here and files
  the resulting backlog items; the **Backlog Burn-down** routine implements them.

## Note template

```
### <Date> — <Topic>
**Question:** what are we trying to improve?
**Findings:** what best-in-class tools do (with sources).
**Recommendation:** the concrete change.
**Jira:** KEY-nn (the task filed from this note).
```

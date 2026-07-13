# Vellum — Market & Competitive Landscape (Jul 2026)

**Product:** Vellum (Jira `LUM`; built on the Lumina suite skeleton) — a doc/notes app:
"Google-Docs ease, Obsidian calm, clean math typing, living mind maps." Differentiators:
(a) frictionless **inline math** typing (KaTeX, keyboard-only entry/exit, no modals);
(b) Obsidian-style **mind-map / knowledge graph** of docs + backlinks; (c) local-first
storage; (d) **suite bridge** embedding **live Tessera spreadsheet models** in docs.

> Compiled from live web research, Jul 13 2026. Vendor TAM figures vary widely; the PKM
> ~$1.8B / 11.8% CAGR anchor is the most defensible, higher note-taking numbers optimistic.

## 1. Market overview
- **PKM software** (tightest fit): ~**$1.8B (2025) → ~$4.9B (2034), ~11.8% CAGR**
  (Dataintelo, 2025).
- **Note-taking apps**: ~$1.35B (2025) → $5.21B (2034), ~16.4% CAGR (Verified Market
  Research, 2025); a separate report: $5.66B (2025) → $12.92B (2035) (Global Growth
  Insights, 2025) — wide variance = differing scope.
- **AI note-taking** (adjacent, fast): +$821M 2025–2029, ~21.3% CAGR (Technavio, 2025).
  Note: the market's *growth* is in AI capture; Vellum's differentiators are non-AI.
- Churn is high — a 2024 Capterra survey found **48% of KM users switched main tool
  within two years** (via TheFix, 2026): acquisition possible, retention hard.

## 2. Competitive landscape

| Tool | Positioning | Pricing | Math | Graph/backlinks | Local-first | Embed/live data |
|---|---|---|---|---|---|---|
| **Notion** | All-in-one workspace | Free; Plus $10; Business $18–20 | KaTeX via `/equation` | Backlinks; **no graph** | Cloud | Rich embeds (live via 3rd-party) |
| **Obsidian** | Local Markdown PKM + plugins | App free; Sync $4–10; Publish $8–10 | MathJax + plugins | **Graph + backlinks native** | **Yes** | Weak (iframe/plugin) |
| **Roam** | Outliner, block-refs | ~$15/mo (expensive) | KaTeX | Graph + block refs | Cloud | Minimal |
| **Logseq** | OSS Roam-style outliner | Free; sync paid | KaTeX/LaTeX | Graph + block refs | **Yes** | Minimal |
| **Craft** | Beautiful Apple-first docs | Free; Plus $8; Team $50 | Basic | Backlinks; weak graph | Partial | Basic embeds |
| **Coda** | Docs + spreadsheet hybrid | Free; Maker $10+ | Weak | Limited | Cloud | **Native live formulas/tables** |
| **Anytype** | Local-first, E2E, objects | Free; Explorer $5; self-host | Limited | Graph + relations | **Yes** | Object refs; no live sheet |
| **Capacities** | Object-based "studio for the mind" | Free; Pro ~$10 | Basic | Backlinks + graph | Cloud | Limited |
| **Tana** | Outliner + supertags + AI | Pro ~$10 | Basic | Graph + typed nodes | No | Structured fields |
| **Reflect** | Networked notes + AI | ~$10–15 | KaTeX | Backlinks + graph | Cloud (E2E) | Minimal |
| **MS Loop** | M365 collaborative components | Bundled w/ M365 | Basic `/` equation | Backlinks (Mar 2025); no graph | Cloud | Live Loop components (M365) |
| **Google Docs** | Ubiquitous cloud doc | Free / Workspace | Clunky palette editor | None | Cloud | Sheets embed (semi-live) |

**No single competitor combines all four Vellum pillars.** Obsidian owns local-first +
graph but math is plugin-dependent and there's no live-data embedding. Coda owns in-doc
live calc but is cloud-only, weak math, no graph. Notion owns embeds but is cloud-only,
no graph. **The whitespace is the intersection.**

## 3. Math-typing niche
Served today by **Obsidian + plugins** (Latex Suite, MathLive, Math Booster — 35+
LaTeX plugins, but assembly required), **Typora** (elegant inline render, no PKM/graph),
and **dedicated LaTeX** (Overleaf, Vim+snippets — powerful, steep). The recurring pain is
**not writing LaTeX, it's the friction around it** — modal dialogs, raw `$…$` source,
plugin setup. Mainstream apps treat equations as second-class. **Genuinely underserved,
high-intent, but narrow** and largely colonised by Obsidian power users. Vellum's
"keyboard-only, no-modal" inline math is a real wedge vs mainstream apps and a
*smoothness* (not capability) argument vs Obsidian.

## 4. Knowledge-graph / mind-map angle
**Mature, not novel** — graph/backlinks are table stakes (Obsidian, Roam, Logseq, Tana,
Capacities, Reflect; Anytype adds typed relations). A common critique: graph views are
"pretty, rarely used." Differentiation must be *qualitative* — a legible, auto-laid-out,
editable-from-graph "living mind map" — not "we have a graph." **Treat as a supporting
feature, not the headline.**

## 5. Live-model-embedding angle (most defensible)
"Embed a **live spreadsheet model** from a sister app inside a doc" is close to novel as
a first-party feature. **Coda** is the nearest concept (canvas formulas recalc live) but
is cloud-only, one monolithic app, weak math/graph. **Notion/Confluence** get "live"
sheets only via third parties (Rows). **Google Docs↔Sheets** is semi-live. **MS Loop** is
live but M365-locked. A **local-first suite with a native, first-party Vellum↔Tessera
live-model embed is not offered by any incumbent** — provided it feels native, not
iframe-glued.

## 6. Gaps & opportunities
1. **The intersection is empty** (local-first + native graph + frictionless math + live
   embedding).
2. **Math as a first-class citizen** without assembling Obsidian plugins.
3. **Local-first is a proven, growing demand vector** (Obsidian went free-for-commercial
   Feb 2025; Anytype/Logseq momentum).
4. **Suite cohesion / "calm"** vs Notion/Coda sprawl and AI-everything fatigue.
5. **High switching rate (48%/2yr)** = an acquirable, mobile audience.

## 7. Risks / threats
- **Obsidian gravity** — free, huge plugin ecosystem, overlaps 3 of 4 pillars.
- **Narrow ICP** — caring about *all four* pillars may be a small slice.
- **Copyable differentiators** — Coda/Notion could deepen embedding; Obsidian could
  smooth math.
- **Non-AI risk** — market growth/attention is in AI note-taking (21.3% CAGR).
- **Suite dependency** — the live-model bridge's value is gated on Tessera being good
  enough to be someone's real spreadsheet.
- **Distribution/trust** — indie local-first apps struggle on mobile sync, collab,
  enterprise trust vs Microsoft/Google/Notion.

## 8. Recommended positioning
- **A — "The STEM note app that doesn't fight you." (sharpest wedge):** lead with
  frictionless inline math; target STEM students/researchers/engineers frustrated by
  Notion/Docs equation editors and Obsidian plugin setup. Math is the hook; graph +
  local-first are retention.
- **B — "Docs with live models, not dead numbers." (most defensible):** own the
  Vellum↔Tessera live embed vs static Google Docs/Notion embeds.
- **C — "The calm, local-first suite." (brand umbrella):** against Notion/Coda bloat and
  cloud lock-in.

**Recommendation:** GTM with **A** (narrow, demonstrable, low competition on smoothness),
differentiate with **B** (near-novel, defensible), wrap in **C**. Don't headline the
knowledge graph.

**Sources:** Dataintelo, Verified Market Research, Global Growth Insights, Technavio
(2025); Capterra via TheFix (2026); Notion/Obsidian/Craft/Coda/Anytype/Tana pricing pages
(2025–26); Obsidian Stats plugin data (2025); MDHero/Sparkl & G. Castel on LaTeX
workflows (2025–26); Rows embed docs (2025).

# Tessera — Market & Competitive Landscape (Jul 2026)

**Product:** Tessera (Jira `ACE`; lineage: Accel → "Radix" rebrand) — a browser-based
spreadsheet + graphing workspace. Hero features: native `STOCK()` live-market-data
formula + Market panel/stock picker; AI formula assistant (natural language → formula
in the grid); dynamic arrays / spill ranges; formula autocomplete + inline signature
help; cross-sheet references; first-class graph/chart sheets; optional cloud layer.

> Compiled from live web research, Jul 13 2026. Figures come from commercial
> market-research vendors whose TAM definitions vary — treat as directional.

## 1. Market overview
- Core spreadsheet software market: ~**$10.79B (2024) → ~$11.66B (2025)**, ~**8% CAGR**,
  → **$15.67B by 2029** (The Business Research Company, 2025). Alt estimates cluster
  **$10–11.3B (2025)** → ~$19.65B by 2034 at ~6.3% CAGR (Global Growth Insights, 2025).
- The category is mature and duopolised (Excel, Google Sheets). Growth is driven by the
  **AI layer** and **live-data / no-code-analytics** wedges, not new grid engines. The
  base grid is a commodity; the intelligence and data connectivity are not — that is
  where a small product differentiates.

## 2. Competitive landscape

| Product | Positioning | Pricing (2025–26) | AI features | Live-data / finance |
|---|---|---|---|---|
| **Excel + Copilot** | Incumbent standard; AI in the grid | M365 Copilot ~$30/user/mo | NL→formula, `=COPILOT()` LLM-in-cell (recalcs on data change), explain, Agent Mode (2025) | Native **Stocks** data type, **STOCKHISTORY**, Power Query |
| **Google Sheets + Gemini** | Ubiquitous collaborative default | Bundled in paid Workspace | NL→formula w/ explanation, "Help me organize", direct actions | **`GOOGLEFINANCE()`** — reference live-quote fn, delayed/limited |
| **Rows** | "Smartest AI spreadsheet"; marketing/ops | Free; paid ~$15/mo | Add cols/charts/what-if, forecasting, PDF/image table extraction, scraping | **200+ connectors**; not finance-focused |
| **Equals** | AI analytics for finance/RevOps | Seat + connector; independent (Series A ~$23M, *not* acquired) | AI analytics layer | Live SQL/warehouse via Fivetran |
| **Causal** | Visual FP&A modeling | Enterprise | Model-driven | **Acquired by Lucanet, Oct 2024** — still operating as xP&A |
| **Airtable** | Spreadsheet-DB → AI app platform (~$11B) | Free; Team ~$20–24; Business ~$59/seat | Airtable AI + Cobuilder app-gen | Records, not market data |
| **GRID (grid.is)** | Spreadsheet engine for embeddable calculators | Free; Pro ~$29/mo | Spreadsheet-to-web | Wraps Sheets/Excel; publishing focus |
| **Quadratic** | "AI spreadsheet with code" (Python/SQL/JS cells) | Free; Pro $19; Team $49 | AI writes code cells; MCP support | Live DB (Postgres/Snowflake/BigQuery), Plaid |
| **Sourcetable** | "Self-driving spreadsheet" / Superagents | Connectors $100/mo ea (launch: free) | Autonomous tool-using agents; raised $4.3M (Mar 2025) | Vertically integrated agent + connectors |
| **Wisesheets** | Excel/Sheets add-in for stock data | Low-cost add-in | — | **80k securities**, live+historical, statements, dividends |
| **Koyfin** | Web financial-analytics terminal | Free; Plus $39; Premium $79; up to $299 | — | Deep coverage, **web only, no Excel add-in** |

## 3. AI-formula / NL-to-formula trend
Now **table stakes and shipped**, not experimental: Excel (NL→formula + `=COPILOT()`,
2025) and Sheets (Gemini) do it natively with explanations. The frontier has moved to
**LLM-as-a-recalculating-cell-function** (`=COPILOT()`) and **agents that take multi-step
actions on the sheet** (Sourcetable Superagents, Excel Agent Mode). Raw NL→formula is no
longer a moat. **Tessera's edge must be trust & transparency** — show the generated
formula, give inline signature help, keep the assistant scoped to *auditable* formulas
rather than opaque black-box cells. "AI you can read and verify."

## 4. Live-market-data-in-spreadsheet angle
Reference points are **shallow**: `GOOGLEFINANCE()` (Sheets-only, limited), Excel Stocks
type + `STOCKHISTORY` (basic history). Depth players are **add-ins/terminals, not native
grids**: Wisesheets (rich but bolted onto Excel/Sheets), Koyfin (rich data, web-only, no
Excel bridge). **White space:** a native, first-class `STOCK()` function + in-app Market
panel/picker + first-class graph sheets in one coherent browser product. No competitor
pairs all three.

## 5. Gaps & opportunities
1. **Finance-native + graphing-native in one browser app** — the `STOCK()` + Market panel
   + chart-sheets combination is unowned.
2. **Transparent, auditable AI** vs incumbents' opaque AI cells.
3. **Coherent small suite** (docs + research + spreadsheet as one designed system).
4. **No-login browser entry** — undercut seat/connector-gated rivals (Equals, Sourcetable).
5. **Pricing headroom** — startups sit at $19–49/mo or per-connector ($100); a flat
   prosumer tier (~$15–25/mo) undercuts metered players.

## 6. Risks / threats
- **Incumbent bundling** (dominant): Excel `=COPILOT()`+STOCKHISTORY and Sheets
  Gemini+`GOOGLEFINANCE` deliver "good enough" to a billion users at ~zero marginal cost.
- **Feature commoditization** — NL→formula is matched within a release cycle.
- **Well-funded fast movers** — Sourcetable, Quadratic, Airtable.
- **Data-cost / licensing** — live quotes carry real per-quote cost & vendor constraints
  (why Koyfin gates); `STOCK()` economics need a sustainable feed deal.
- **Consolidation** — Causal→Lucanet (2024); space rewards incumbency or acquisition.

## 7. Recommended positioning
1. **"The finance-native spreadsheet + graphing workspace."** Lead with `STOCK()` + Market
   panel + chart sheets — the single most defensible gap.
2. **"AI you can read and trust."** Transparent, auditable formulas vs opaque `=COPILOT()`.
3. **"One coherent suite, in the browser, no friction."** Fast, free to start, optional
   cloud layer; flat prosumer pricing vs metered rivals.

> Housekeeping: "Accel"→"Radix" was the product's own rename; unrelated to the VC firm
> Accel — worth a quick trademark check (not a market finding).

**Sources:** The Business Research Company (2025); Global Growth Insights (2025);
Microsoft Excel blog (Aug–Sep 2025); Quadratic / Rows pricing (2025); Sourcetable —
GlobeNewswire/PRNewswire (2025); Lucanet PR (Oct 2024); Airtable (2025–26); grid.is /
TechCrunch; Wisesheets blog (2025); Koyfin pricing (2025–26); TechCrunch/Crunchbase on
Equals.

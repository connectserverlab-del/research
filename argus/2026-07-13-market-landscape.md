# Argus — Market & Competitive Landscape (Jul 2026)

**Product:** Argus Capital Lab (Jira `ARQ`) — a disciplined investment-research tool. Core:
a **Phase 1 Research Log** of immutable, falsifiable, point-in-time research briefs with
later **SPY-relative outcome logging** — deliberately no scores/rankings/trading workflow.
Plus **Pegasus**, an offline historical **event-study engine** (ingest → price → study)
with Athena-friendly summaries. Optional `yfinance` price data. CLI-first, local.

> Compiled from live web research, Jul 13 2026. Vendor TAM figures vary; treat as directional.

## 1. Market overview
- **Investment research software** (tightest fit): ~$4.1B (2024) → ~$12.1B (2032), ~14.1%
  CAGR (Verified Market Reports, 2025).
- **Financial analytics** (broader): ~$15.2–16.4B (2025) → ~$16.6–17.9B (2026), ~9.2% CAGR
  (Future Market Insights / FactMR, 2025).
- **Retail base large & growing**: ~62% US participation (2025); retail inflows to US
  stocks ~$302B in 2025, +53% YoY; retail ~20–35% of daily volume (Lambda Finance /
  coinlaw.io / SQ Magazine, 2025). Gen Z + Millennials are 60%+ of retail activity —
  the CLI/Substack/Obsidian/Python cohort.
- **The "serious retail analyst / fintwit / Substack investor" segment** is real but
  unquantified — a niche within a niche. **Treat TAM as thousands-to-low-tens-of-thousands
  of paying users, not millions.**

## 2. Competitive landscape

| Tool | Positioning | Pricing (2025–26) | Falsifiable-thesis journaling? | Event studies? |
|---|---|---|---|---|
| **Bloomberg Terminal** | Unaffordable institutional incumbent | ~$27,660/user/yr; no retail tier | No | Partial (functions, inaccessible) |
| **Koyfin** | Retail "Bloomberg alternative" | Free; Plus $39; Premium $79; up to $299 | No — dashboards, not a graded log | No |
| **YCharts** | Advisor/analyst data & charting | Quote-based (~$4k+/yr) | No | No |
| **AlphaSense (owns Sentieo)** | Enterprise doc search/intelligence | ~$10–20k/seat/yr | No | No |
| **Fintel** | Ownership/short-interest/quant screens | ~$30–60/mo | No | No |
| **Portfolio Visualizer** | Portfolio backtesting/factor | Free + paid (~$30–360/yr) | No (portfolio, not thesis) | No |
| **QuantConnect** | Cloud quant/backtesting (LEAN) | Researcher $10; Quant Trader $120 | No | Buildable (you code it) |
| **backtrader / Zipline** | OSS Python backtesting | Free | No | Buildable (DIY) |
| **Obsidian / Notion / decision-journal templates** | Note-taking repurposed for journals | Free–$15/mo | Manual only — no enforced immutability / grading | No |

**Structural point:** no priced competitor combines (a) an *immutable, timestamped,
falsifiable* research log with (b) *automated SPY-relative outcome grading* and (c) an
*accessible event-study engine*. Data vendors and quant platforms help you *find and
test*, not *hold yourself accountable*.

## 3. Research-journal / decision-journal niche
Decision journaling (Farnam Street / Kahneman) is a known practice with free templates but
**essentially no purpose-built software** (bolted onto Notion/Obsidian). The
Superforecasting / Good Judgment Project lineage validates that *tracked, scored*
predictions improve judgment. Prediction-tracking apps exist — **Fatebook** (private,
successor to PredictionBook), **Metaculus/Manifold** (public, tech/geopolitics-skewed) —
but none grade an *investment thesis against the market*. **Argus ≈ "Fatebook for equity
theses, resolved by the market instead of the author."** The deliberate absence of
scores/rankings/trading is a differentiator aligned with the calibration-not-prediction
ethos this community respects.

## 4. Event-study tooling
- **eventstudytools.com** — free web GUI (abnormal returns, market/CAPM/FF3/FF5); most
  accessible, but web-hosted, not local, not scriptable, not integrated with a log.
- **WRDS (Wharton)** — academic gold standard, gated behind institutional CRSP/Compustat
  subscriptions.
- **Python libs** (`eventstudy`, `event-study-toolkit`) — capable but DIY, coder-targeted.
- **Accessible-tooling gap is clear.** An offline, local, batteries-included "ingest →
  price → study" engine (Pegasus) sits in genuine white space — WRDS-style workflow
  without the WRDS gate.

## 5. Gaps & opportunities
1. **Accountability layer is missing market-wide** — immutable + market-graded is unclaimed.
2. **Event studies are gated (WRDS) or DIY (Python)** — a local, packaged engine is a real
   convenience wedge.
3. **CLI-first, local, no-account** fits the developer-adjacent quant cohort and sidesteps
   data-redistribution risk.
4. **Anti-feature positioning** (no scores/rankings/trading) is a credibility signal amid
   "AI stock picker" noise.

## 6. Risks / threats
- **Data licensing / ToS (highest practical risk):** Yahoo retired its public API (2017);
  `yfinance` hits internal endpoints, "personal/research use only," and Yahoo ToS prohibits
  automated access. hiQ v. LinkedIn (2022) protects public-data scraping under CFAA but
  **not against contractual ToS**. **Keep price fetching strictly user-side & personal;
  never redistribute or bundle data.** Backend is also fragile (endpoints can change).
- **Small TAM** — the journal-keeping serious analyst is a thin segment; free alternatives
  (Obsidian + template + `yfinance`) exist.
- **Incumbent encroachment** — Koyfin/YCharts could add a thesis tracker, but their
  cloud/dashboard DNA makes an *immutable local log* an awkward fit (low near-term threat).
- **DIY substitution** — the technical user *can* self-assemble; product must earn its keep
  via discipline-enforcing structure (immutability, auto-grading).
- **Point-in-time data integrity** — survivorship bias/restatements in free data must be
  caveated prominently.

## 7. Recommended positioning
1. **"A lab notebook for investors — falsifiable theses, graded by the market."** Lead with
   intellectual honesty/calibration, not returns. Target fintwit/Substack analysts who want
   a private, tamper-proof track record.
2. **"WRDS-grade event studies, offline and free."** Market Pegasus as the accessible
   event-study engine independents can't otherwise get.
3. **"Local, CLI-first, no account, your data stays yours."** Privacy/ownership + zero
   lock-in — which is *also* the legal-safety story on `yfinance` (personal use, no
   redistribution): turn the constraint into a virtue.

**Practical note:** TAM is thin — favor a low-friction, low-price (or open-core) model that
monetizes the disciplined power-user rather than chasing the mass retail trader.

**Sources:** Verified Market Reports / FactMR / Future Market Insights (2025–26); Koyfin,
WallStreetZen, BrokersDB, G2 (2026); Sacra, Vendr (2026); QuantConnect/quantvps (2026);
LessWrong / EA Forum / fs.blog (2025–26); eventstudytools.com, WRDS (2025); Live Proxies /
Scrapfly (2025–26); Lambda Finance / coinlaw.io / SQ Magazine / BestBrokers (2025).

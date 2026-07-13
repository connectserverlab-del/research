# Figaro — Market & Competitive Landscape (Jul 2026)

**Product:** Figaro (Jira `FIG`) — a personal concierge "SMS-approval engine." Flow: a
trigger (PWA button / Siri Shortcut) texts you a summary + single-use code → you reply the
code to approve → you get a one-tap deep link that opens Uber/Lyft/DoorDash/Uber Eats
**pre-filled**. It does **not** place orders (no public consumer-ordering APIs) — a
deep-link handoff with a human-in-the-loop SMS approval. Built on Twilio; roadmap adds
Claude-powered NL intents.

> Note: Figaro is a standalone concierge product, not part of the Lumina suite proper.
> Filed here as a research stream. Compiled from live web research, Jul 13 2026.

## 1. Market overview — agentic commerce & real-world AI actions
- Sizing varies by definition but points up: agentic commerce **$5.7B (2025) → $7.7B (2026)
  → $65.5B (2033)** (Grand View); Bain forecasts the **US agentic-commerce market at
  $300–500B by 2030, ~15–25% of e-commerce** (Bain via Grand View/SANBI, 2025).
- Adoption is real: Adobe reported **~4,700% YoY growth in AI-driven traffic to US retail
  (2025)** and **~20% of global Cyber Week 2025 orders were AI-agent-influenced** (Adobe
  Analytics / commercetools, 2025). **58% of consumers prefer AI tools over search, up from
  25% in 2023** (SANBI/paz.ai, 2025).
- **Human-in-the-loop approval is now the industry-standard safety design.** OpenAI's
  Operator/ChatGPT agent "requests permission before actions of consequence" and won't make
  purchases without explicit permission (OpenAI, 2025). Google's **Agent Payments Protocol
  (AP2)** (Sept 16 2025, 60+ partners incl. Mastercard/PayPal/Amex) formalizes a signed
  **Intent Mandate → Cart Mandate** the human approves before payment (Google Cloud, 2025).

**Takeaway:** Figaro's approve-before-act SMS step *is* the "cart mandate / confirm before
consequential action" pattern the biggest players just standardized — a lightweight,
human-owned version of it.

## 2. Competitive / analogous landscape

| Product | What it does | Pricing (2025–26) | Real-world actions? | Approval model |
|---|---|---|---|---|
| **Siri Shortcuts** | User automations; opens apps via URL schemes | Free (iOS) | Only via deep links | Runs on trigger; optional confirm |
| **Google Gemini/Assistant** | Reaches Gmail/Calendar/Maps/Tasks; drafts, schedules | Free; AI Pro/Ultra paid | Yes, in-ecosystem + partners | Explicit permission per app |
| **Amazon Alexa+** | Agentic web nav; books services; **Agentic Ads** in-conversation ordering | $19.99/mo (free w/ Prime); US GA Feb 2026 | Yes — end-to-end | Voice confirm in-conversation |
| **OpenAI Operator / ChatGPT agent** | Own browser; reservations, Instacart/DoorDash carts, tickets | Bundled in ChatGPT Plus/Pro | Yes, via browser + partner apps | Asks permission before purchases |
| **Duckbill** | US human assistants + AI triage do life-admin | $99/mo single, $169/mo household | Yes (humans) | Human confirms async |
| **Magic** (historic) | SMS → human operator | Free → $100/hr (2016); faded ~2023 | Yes (humans) | Text conversation |
| **Yohana / GoodService / Fin** (historic) | Chat/human concierge | Yohana wound down Sep 30 2025; others defunct | Yes (humans) | Chat |
| **Pushcut** | Triggers iOS Shortcuts from webhooks/location/time | Free tier; Pro sub | Only via Shortcuts/deep links | Tap notification to run |
| **IFTTT / Zapier / Make** | Webhook & app-to-app glue | Free → tiered | Via integrations, not consumer ordering | Usually fire-and-forget |
| **Twilio + GPT indie projects** | DIY "text a number to reach your automations" | Twilio usage (~$0.0079/SMS + number) | Whatever you wire | Whatever you build |

**Key read:** Nobody in the *indie/personal* tier combines (a) a trigger, (b) an SMS
approval gate, and (c) a pre-filled deep-link handoff. Big-tech agents do end-to-end
ordering but require their ecosystem, subscriptions, and trust in autonomous purchasing.
Human concierges (Duckbill) are 10–50× the cost and slower.

## 3. Agentic commerce & deep-linking status
- **Deep links are officially supported:** Uber documents the `setPickup` deep link and
  ships a web deep-link generator; if the app isn't installed, `m.uber.com` loads
  pre-filled (developer.uber.com, 2025). DoorDash supports store/restaurant deep links.
- **"No consumer ordering API" is now only *partly* true — the exceptions are gated:**
  OpenAI **Instant Checkout + Agentic Commerce Protocol** launched Sept 29 2025 (Stripe,
  Etsy first, Shopify rolling); **Instacart** got embedded checkout inside ChatGPT (Dec 8
  2025); **DoorDash** launched a ChatGPT app (Dec 2025) but *stops short of in-chat
  checkout*; **Uber×OpenAI** (Oct 2025 → May 2026) added a voice-booking interface.
- **Net for Figaro:** these rails are gated behind ChatGPT/partner platforms and
  merchant-side integration — *not* open consumer APIs an indie can call. **Figaro's
  deep-link premise holds in 2025–26.** The risk is directional: platforms are closing the
  gap for *themselves*.

## 4. The SMS approval / human-in-the-loop pattern
Ubiquitous in banking/fintech ("reply to confirm"), so consumers understand it. Headwind:
SMS OTP is being deprecated as a *security* factor — NIST SP 800-63B (2025) calls it a
"restricted authenticator" (SIM-swap risk); UAE mandates phasing out standalone SMS/email
OTP by Mar 31 2026. **Nuance favoring Figaro:** those warnings target SMS as *proof of
identity against attackers*. Figaro uses SMS as a **user-owned intent-confirmation gate**
(a code you send to yourself) — closer to AP2's Cart Mandate than to anti-fraud auth.
Position it as friction-reduction/peace-of-mind, not hardened security. **Approval fatigue**
is the real UX risk.

## 5. Gaps & opportunities
1. **The autonomous-agent trust gap is unsolved** — a deliberate one-tap human confirm is a
   feature, and cheaper than AP2/ACP compliance.
2. **No subscription / no ecosystem lock-in** — vs Alexa+ ($19.99/mo), Duckbill
   ($99–169/mo), paid Gemini/ChatGPT tiers.
3. **Cross-app, vendor-neutral handoff** (Uber *or* Lyft, DoorDash *or* Uber Eats).
4. **Speed for repeat/known actions** — "text CONFIRM → app opens pre-filled" beats a
   multi-turn agent conversation for habitual actions.
5. **Privacy** — runs on the user's own Twilio/keys; no order history sold to an ad engine
   (contrast Alexa+ Agentic Ads).
6. **Roadmap fit** — Claude NL intents ride the agentic wave without merchant integrations.

## 6. Risks / threats
- **Platform deep-link changes (highest, most concrete):** Uber/DoorDash can alter URL
  schemes/params anytime — flows break silently. Mitigate with graceful web fallbacks
  (`m.uber.com`).
- **Big-tech subsumption:** Alexa+, ChatGPT (Instant Checkout, Uber/DoorDash/Instacart
  apps), Gemini are racing to own the whole flow incl. payment; the "handoff to order
  yourself" step could feel dated to the mainstream.
- **ToS / API-terms risk:** building a branded product atop another company's app-open
  behavior carries takedown risk if usage looks like unauthorized automation.
- **SMS friction:** A2P 10DLC registration, per-message cost, and OTP-security messaging
  could push confirmation UX toward push/RCS.
- **Small niche/TAM:** "wants automation + distrusts autonomous agents + will self-host
  Twilio" is a power-user sliver.

## 7. Recommended positioning
- **A — "Approval-first agent — you stay in the loop by design."** Lead with the
  human-in-the-loop confirm as the *trust* differentiator; the indie, no-subscription
  version of AP2 "Cart Mandate" / OpenAI "confirm before purchase."
- **B — "The fast lane for actions you already know you want."** Not a chatbot — a one-tap
  trigger → confirm → pre-filled app open for habitual actions; NL intents extend to novel
  requests later.
- **C — "Own your assistant — no ecosystem, no ads, no monthly fee."** Target privacy/cost-
  conscious power users; vendor-neutral deep links; explicit contrast with Alexa+ Agentic
  Ads and $19.99–$169/mo alternatives.

**Threading note:** Frame the deep-link handoff as *intentional user control*, not a
limitation — so when consumer ordering APIs do open to indies (ACP/AP2 trajectory), the
same approval UX layers on top of real order placement without repositioning.

**Sources:** OpenAI (Operator 2025; Instant Checkout/ACP Sept 29 2025; Instacart Dec 8
2025; Uber partnership 2025–26); Stripe (ACP/Shared Payment Token 2025); Google Cloud (AP2,
Sept 16 2025); Amazon/CNBC (Alexa+ pricing, Agentic Ads, US GA Feb 2026); Grand View & Bain
(sizing 2025–33); Adobe Analytics / commercetools (Cyber Week 2025); developer.uber.com
(setPickup); DoorDash/Bloomberg (Dec 2025); Duckbill pricing; Yohana wind-down (Sep 30
2025); NIST SP 800-63B & Authsignal/LoginRadius (2025); Pushcut.io; promptable/twilio-gpt-sms.

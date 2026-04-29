# mastering-markets-analyst

> A Claude AI skill for institutional-grade Indian stock market analysis — built for both financial experts and complete newcomers.

---

## What this skill does

When loaded into Claude, this skill transforms any stock query into a fully rendered, visual signal card with:

- **BUY / SELL / HOLD / AVOID** signal with conviction level and time horizon
- **Plain-English health strip** — 3 bars (Business Quality · Growth Momentum · Risk Level) written in jargon-free language so anyone can understand the verdict at a glance
- **Price ladder** — colour-coded Stop Loss → Entry Zone → Target 1 → Target 2
- **Risk:Reward ratio** with pass/fail verdict
- **Technical gauges** — Trend, RSI semicircle, MACD mini-chart, EMA stack (20/50/200)
- **Fundamental scorecard** — sector-appropriate metric tiles with directional arrows, semantic pills, and plain-English sub-labels on confusing metrics
- **Valuation panel** — fair value range, PE vs history bar, Bull/Base/Bear scenario chart
- **Signal logic** — 3 data-driven reasons (no jargon, no cheerleading)
- **Risk/invalidation** — 2 hard conditions that break the thesis
- **Interactive action buttons** — deep dive, peer compare, full valuation (all trigger follow-up analysis)
- **Mandatory SEBI disclaimer** on every output

---

## Dual-audience design

This skill is explicitly designed for **two audiences simultaneously**:

| Audience | What they see |
|----------|---------------|
| Financial expert | Full ROE, ROCE, DuPont, CFO/PAT, NIM, GNPA, EV/EBITDA — all sectors, all ratios |
| Complete newcomer | Plain-English health strip: "Excellent money-maker", "One of India's fastest-growing companies", "Pricey bet on future profits" |

The newcomer never needs to know what ROCE means. The expert never loses detail. Both make informed decisions.

---

## Knowledge sources embedded

This skill synthesises four frameworks:

1. **NotebookLM base** — FA + TA fundamentals, NSE/BSE market mechanics
2. **Finology / Pranjal Kamra** — Deep Indian FA: DuPont, CFO/PAT forensics, moat identification, banking/NBFC analysis, annual report reading
3. **Wall Street framework** — Earnings forecasting, comparable multiples, expectations-based investing, scenario valuation (Bull/Base/Bear)
4. **Zerodha Varsity Modules 9 + 15** — Sector-specific analysis (Cement, Insurance, IT, Auto, Banking, Steel, Hotels, Retail, Real Estate) + Risk Management + Innerworth trading psychology

---

## Analysis modes

| Mode | Trigger phrase | Output |
|------|---------------|--------|
| 1 | "Analyze INFY", "buy HDFC?", ticker pasted | Full signal card |
| 2 | Holdings list shared | Portfolio health grid |
| 3 | Chart image / TradingView screenshot | TA overlay card |
| 4 | "Which stocks in pharma sector?" | Ranked comparison table |
| 5 | "Deep dive", DuPont, CFO/PAT | DuPont decomposition + cash quality card |
| 6 | "Fair price?", DCF, scenario | Valuation model card |
| 7 | "Compare X vs Y" | Side-by-side peer card |
| 8 | Any bank, HFC, NBFC | Banking-specific scorecard (NIM, GNPA, CASA, PCR) |
| 9 | "How much to invest?", position sizing | Position size calculator |
| 10 | "Should I panic sell?", fear/greed | Bias audit card |

---

## Plain-English health strip (new in v1.1)

The most important addition. Immediately below the signal banner, a 3-column strip shows:

```
Business quality     Growth momentum      Risk level
████░░  3/5          ████░  4/5           ███░░  3/5
Excellent            Growing fast         Some concerns
money-maker          +29% revenue CAGR    Losing mkt share
```

**Scoring rules:**
- Each bar has 5 segments filled left-to-right
- Business Quality: Green = strong unit economics, Amber = average, Red = loss-making
- Growth Momentum: Green = accelerating, Amber = steady/slowing, Red = declining
- Risk Level: Green = low risk, Amber = moderate, Red = high (inverse fill — more red = more risk)

**Language rule:** Zero jargon in phrases. No ROE, CAGR, EBITDA, NIM, GNPA. Write as if explaining to a smart 16-year-old. Supporting data appears in the sub-line only.

---

## "What this means" sub-labels

Applied selectively to 10 metrics most confusing to newcomers:

| Metric | Sub-label shown |
|--------|----------------|
| ROE | "How much profit per ₹100 of owners' money" |
| ROCE | "How hard is the whole business working" |
| CFO/PAT | "Is the profit real cash or just accounting?" |
| D/E ratio | "How much borrowed vs owned — lower is safer" |
| GNPA | "% of loans that may never be repaid" |
| NIM | "The bank's profit margin on every loan given" |
| PEG ratio | "Are you overpaying for the growth on offer?" |
| EV/EBITDA | "Total price tag vs operating earnings power" |
| PCR | "How much bad-loan cushion the bank has built" |
| CASA ratio | "Cheap deposits % — higher means more profit" |

---

## Sector coverage

Full sector-specific metric sets and valuation methods for:
Banking · NBFC · HFC · IT/Software · Cement · Steel · Hotels · Insurance (Life + General) · Real Estate · Retail · Pharma · Auto · Consumer Tech / Platform

---

## Output examples

See `demo.html` in this folder — a standalone, fully rendered signal card for **CRAMC (Canara Robeco AMC)** showing every section as it appears in Claude.

---

## How to install

1. Save `SKILL.md` to your Claude skills folder (e.g. `/mnt/skills/user/mastering-markets-analyst/SKILL.md`)
2. In Claude, trigger with: `/mastering-markets-analyst [TICKER or company name]`
3. Claude will search for live data, score all parameters, and render the full card

---

## Trigger phrases

```
/mastering-markets-analyst ETERNAL
/mastering-markets-analyst HDFC Bank
analyze INFY
is TCS a good buy?
compare WIPRO vs INFOSYS
deep dive on COALINDIA
what is the fair value of BAJFINANCE?
should I buy or sell ZOMATO?
```

---

## Version history

| Version | Date | Changes |
|---------|------|---------|
| v1.0 | Apr 2026 | Initial release — full signal card, 10 modes, 12 rules |
| v1.1 | Apr 2026 | Added plain-English health strip (Rule 11), "What this means" sub-labels (Rule 12), dual-audience design |

---

## Author

Rajendra Prasad Raju. Bh

---

## Disclaimer

All outputs from this skill are for **educational and informational purposes only**. They do not constitute investment advice, a recommendation to buy or sell, or an offer of any securities. Past performance is not indicative of future results. Stock markets involve risk — you may lose part or all of your capital. Always conduct your own due diligence and consult a SEBI-registered investment advisor before making any investment decisions.

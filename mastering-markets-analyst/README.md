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
- **Interactive action buttons** — deep dive, peer compare, full valuation
- **Mandatory SEBI disclaimer** on every output

---

## Dual-audience design

| Audience | What they see |
|----------|---------------|
| Financial expert | Full ROE, ROCE, DuPont, CFO/PAT, NIM, GNPA, EV/EBITDA — all sectors, all ratios |
| Complete newcomer | Plain-English health strip: "Excellent money-maker", "One of India's fastest-growing companies", "Pricey bet on future profits" |

---

## Knowledge sources

1. **NotebookLM base** — FA + TA fundamentals, NSE/BSE mechanics
2. **Finology / Pranjal Kamra** — DuPont, CFO/PAT forensics, moat identification, banking/NBFC
3. **Wall Street framework** — Earnings forecasting, comparable multiples, scenario valuation
4. **Zerodha Varsity Modules 9 + 15** — Sector analysis, Risk Management, Trading psychology

---

## Analysis modes

| Mode | Trigger | Output |
|------|---------|--------|
| 1 | "Analyze INFY", ticker pasted | Full signal card |
| 2 | Holdings list | Portfolio health grid |
| 3 | Chart image | TA overlay card |
| 4 | "Which stocks in pharma?" | Ranked comparison |
| 5 | "Deep dive", DuPont | DuPont + cash quality card |
| 6 | "Fair price?", DCF | Valuation model |
| 7 | "Compare X vs Y" | Peer comparison card |
| 8 | Any bank / NBFC | Banking scorecard |
| 9 | "How much to invest?" | Position size calculator |
| 10 | "Should I panic sell?" | Bias audit card |

---

## Plain-English health strip (v1.1)

3-column strip immediately below the signal banner:

```
Business quality     Growth momentum      Risk level
████░░  4/5          ████░  4/5           ███░░  3/5
Excellent            Growing fast         Some concerns
money-maker          +29% revenue CAGR    Losing mkt share
```

Zero jargon in phrases. Written for a smart 16-year-old who has never read a financial statement.

---

## Sector coverage

Banking · NBFC · IT/Software · Cement · Steel · Hotels · Insurance · Real Estate · Retail · Pharma · Auto · Consumer Tech

---

## Trigger phrases

```
/mastering-markets-analyst ETERNAL
/mastering-markets-analyst HDFC Bank
analyze INFY
is TCS a good buy?
compare WIPRO vs INFOSYS
deep dive on COALINDIA
```

---

## Version history

| Version | Date | Changes |
|---------|------|---------|
| v1.0 | Apr 2026 | Initial release — full signal card, 10 modes, 12 rules |
| v1.1 | Apr 2026 | Plain-English health strip (Rule 11), sub-labels (Rule 12), dual-audience design |

---

## Demo

Open `demo.html` in any browser — or view online:
https://htmlpreview.github.io/?https://github.com/bhrpraju/claude-skills/blob/main/mastering-markets-analyst/demo.html

---

## Disclaimer

All outputs are for educational purposes only. Not investment advice. Always consult a SEBI-registered advisor before investing.

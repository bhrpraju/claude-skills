# claude-skills

> Custom Claude AI skills built by Rajendra — production-tested, dual-audience, visual-first.

Each skill folder contains a `SKILL.md` (loaded into Claude's context), a `README.md` (human-readable docs), and a `demo.html` (standalone preview of the output).

---

## Skills

| Skill | What it does | Status |
|-------|-------------|--------|
| [mastering-markets-analyst](./mastering-markets-analyst/) | Indian stock analysis — BUY/SELL/HOLD signal cards, DuPont deep dives, peer comparison, banking scorecard, valuation models. Dual-audience: full metrics for experts + plain-English health strip for newcomers. | ✅ v1.1 |

More skills coming — email automation, PowerPoint generation, CIR pipeline coaching, and more.

---

## Structure

```
claude-skills/
│
├── README.md                           ← this file — index of all skills
│
├── mastering-markets-analyst/
│   ├── SKILL.md                        ← Claude reads this
│   ├── README.md                       ← human docs
│   └── demo.html                       ← standalone visual preview
│
├── professional-email/                 ← coming soon
└── awesome-pptx/                       ← coming soon
```

---

## What is a Claude skill?

A skill is a `.md` file that loads into Claude's context window and gives it a locked, repeatable behaviour — specific output formats, visual rules, analysis frameworks, and language style — for a particular domain.

---

## Author

**Rajendra** · AVP Technology Program Management · Sutherland Global Services
GitHub: [@bhrpraju](https://github.com/bhrpraju)

---

## Disclaimer

All outputs from these skills are for educational and informational purposes only and do not constitute investment, legal, or professional advice of any kind.

# claude-skills

> Custom Claude AI skills built by Rajendra Prasad Raju. Bh — production-tested, dual-audience, visual-first.

Each skill folder contains a `SKILL.md` (loaded into Claude's context), a `README.md` (human-readable docs), and a `demo.html` (standalone visual preview of the output).

---

## Skills

| Skill | What it does | Status |
|---|---|---|
| [mastering-markets-analyst](https://github.com/bhrpraju/claude-skills/blob/main/mastering-markets-analyst) | Indian stock analysis — BUY/SELL/HOLD signal cards, DuPont deep dives, peer comparison, banking scorecard, valuation models. Dual-audience: full metrics for experts + plain-English health strip for newcomers. | ✅ v1.1 |
| [master-prompter](https://github.com/bhrpraju/claude-skills/blob/main/master-prompter) | Universal prompt engineering skill — synthesizes Claude, GPT-4.1/5.5, Gemini 3, and Grok best practices. Auto-reconstructs vague prompts using the REACT framework. 10 cross-model techniques, 5 domain templates. | ✅ v1.0 |
| [meeting-documenter](https://github.com/bhrpraju/claude-skills/blob/main/meeting-documenter) | Transforms raw meeting inputs into an audit-ready execution record — RASI accountability matrix, decision log with deselection rationale, risk & issue register, 3x30 executive reports, pre-meeting briefs, and after-action reviews. Works on every LLM. | ✅ v1.0 |

More skills coming — UX orchestration, CIR pipeline coaching, LinkedIn post automation, and more.

---

## What is a Claude skill?

A skill is a `.md` file that loads into Claude's context window and gives it a locked, repeatable behaviour — specific output formats, visual rules, analysis frameworks, and language style — for a particular domain.

Think of it as a **system prompt + instruction set + design spec** in one file.

---

## Folder Structure

Each skill follows this structure:

```
claude-skills/
├── README.md                    ← this file (index of all skills)
│
├── skill-name/
│   ├── SKILL.md                 ← the actual skill Claude reads
│   ├── README.md                ← human docs for this skill
│   └── demo.html                ← standalone visual preview
```

---

## Author

Rajendra Prasad Raju. Bh

---

## Disclaimer

All outputs from these skills are for educational and informational purposes only and do not constitute investment, legal, or professional advice of any kind.

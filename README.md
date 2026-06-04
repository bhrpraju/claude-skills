# claude-skills

> Custom Claude AI skills built by Rajendra Prasad Raju BH — production-tested, dual-audience, visual-first.

Each skill folder contains a `SKILL.md` (loaded into Claude's context), a `README.md` (human-readable docs), and optionally a `demo.html` (standalone preview of the output).

---

## Skills

| Skill | What it does | Status |
|---|---|---|
| [mastering-markets-analyst](https://github.com/bhrpraju/claude-skills/blob/main/mastering-markets-analyst) | Indian stock analysis — BUY/SELL/HOLD signal cards, DuPont deep dives, peer comparison, banking scorecard, valuation models. Dual-audience: full metrics for experts + plain-English health strip for newcomers. | ✅ v1.1 |
| [master-prompter](https://github.com/bhrpraju/claude-skills/blob/main/master-prompter) | Universal prompt engineering skill — synthesizes Claude, GPT-4.1/5.5, Gemini 3, and Grok best practices. Auto-reconstructs vague prompts using the REACT framework. 10 cross-model techniques, 5 domain templates. | ✅ v1.0 |
| [ux-cognitive-architect](https://github.com/bhrpraju/claude-skills/blob/main/ux-cognitive-architect) | Elite UX/UI design skill grounded in cognitive psychology — Six Minds, Norman's three levels, Fogg, Hick's, Fitts's, Gestalt. Mandatory 4-stage pipeline: Diagnose → Architect → Specify → Build. Works on Claude Desktop, Gemini, ChatGPT, Codex. | ✅ v1.0 |
| [ux-master-orchestrator](https://github.com/bhrpraju/claude-skills/blob/main/ux-master-orchestrator) | Master orchestrator that routes all UX/UI skills into one 5-phase pipeline: Diagnose → Architect → Specify → Build → Polish+Audit. Coordinates ux-cognitive-architect, ui-ux-pro-max, impeccable, frontend-design and more. Works on all platforms. | ✅ v1.0 |

---

## How to Install

### Claude Desktop
Settings → Skills → Add Skill → paste:
https://github.com/bhrpraju/claude-skills

Claude Desktop will detect all skill folders automatically.

### Claude Code CLI
git clone https://github.com/bhrpraju/claude-skills.git
cp -r claude-skills/ux-cognitive-architect ~/.claude/skills/
cp -r claude-skills/ux-master-orchestrator ~/.claude/skills/
cp -r claude-skills/mastering-markets-analyst ~/.claude/skills/
cp -r claude-skills/master-prompter ~/.claude/skills/

### Gemini Advanced / ChatGPT
Open the SKILL.md file of the skill you want, copy the full contents, and paste as your first message or system prompt.

---

## Folder Structure

claude-skills/
├── README.md                    ← this file (index of all skills)
│
├── skill-name/
│   ├── SKILL.md                 ← the actual skill Claude reads
│   ├── README.md                ← human docs for this skill
│   └── demo.html                ← standalone visual preview (where available)

---

## What is a Claude skill?

A skill is a .md file that loads into Claude's context window and gives it a locked, repeatable behaviour — specific output formats, visual rules, analysis frameworks, and language style — for a particular domain.

Think of it as a system prompt + instruction set + design spec in one file.

---

## Author

Rajendra Prasad Raju BH — AVP Technology Program Management, Sutherland Global Services.

---

## Disclaimer

All outputs from these skills are for educational and informational purposes only and do not constitute investment, legal, or professional advice of any kind.

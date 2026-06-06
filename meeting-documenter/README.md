# meeting-documenter

> Transform raw meeting inputs into a structured, audit-ready execution record — with RASI accountability, decision logs, risk registers, and executive reports.

---

## What it does

Most meeting tools produce summaries. This skill produces **accountability infrastructure**.

Give it a transcript, Granola notes, an email thread, a call summary — anything. It outputs:

- **Decisions Made** — with rationale and deselection logic
- **Decisions Deferred** — explicitly captured (most tools miss this)
- **Action Tracker** — verb-based, Nimble 5 Ws, one Responsible owner per item
- **RASI Matrix** — R / A / S / I with due dates and effort estimates
- **Risk & Issue Register** — classified as Risk / Issue / Blocker / Concern / Assumption
- **Pre-Meeting Brief** — agenda, 3 Ps, 48-hour prep rule
- **After-Action Review** — retrospective mode, no blame assignment
- **3x30 Executive Report** — readable in 3 minutes, writable in 30

---

## When to use

Trigger phrases (any LLM, any platform):

```
"document this meeting"
"process these notes"
"extract action items"
"write up the minutes"
"create a decision log"
"prepare a pre-meeting brief"
"write an agenda"
"do a retro / AAR"
"3x30 report"
"executive summary"
"risk register"
"RASI matrix"
"who owns what"
"write a meeting follow-up"
"turn this into MOM"
"accountability tracker"
```

---

## Modes

| Mode | When | Input |
|---|---|---|
| **PRE** — Pre-Meeting Brief | Before a meeting | Meeting invite, topic, attendees |
| **PROCESS** — Meeting Processing | After a meeting | Transcript, notes, Granola output, email thread |
| **AAR** — After-Action Review | Post-project retro | Any raw retrospective notes |
| **EXEC** — Executive Report | Need a 3x30 only | Any meeting input |

---

## Output templates

1. **Meeting Context Scan** — situational paragraph
2. **Core Themes** — 2–3 dominant themes only
3. **Decisions Made** — with options, criteria, rationale
4. **Decisions Deferred / Not Taken** — explicitly logged
5. **Action & Risk Tracker** — RASI + Nimble 5 Ws table
6. **Decision Log** — full decision building blocks
7. **Risk & Issue Register** — classified by type
8. **Communication Plan** — T-Chart: superiors first, then stakeholders
9. **3x30 Executive Report** — only when executive communication is needed
10. **Missing Info / Clarifications Required** — nothing invented, everything flagged

---

## Platform compatibility

Works on every LLM — no platform dependencies, pure markdown.

| Platform | How to use |
|---|---|
| Claude Desktop / claude.ai | Install `.skill` file via Settings → Skills |
| Claude Code CLI | Copy to `~/.claude/skills/meeting-documenter/` |
| ChatGPT | Paste `SKILL.md` content as system prompt |
| Google Gemini / Antigravity | Paste as system instruction |
| OpenAI Codex | Paste as system prompt |
| Any other LLM | Paste `SKILL.md` as first message, then provide input |

---

## Install (Claude Code / Codex / Cursor)

```bash
npx skills add https://github.com/bhrpraju/claude-skills --skill meeting-documenter
```

---

## Key design principles

**RASI over RACI** — "Consulted" is dropped. "Supports" replaces it. Cleaner accountability.

**Trichotomy of reasoning** — Why → What → How. Every action has a reason before it gets a task.

**Subject-based reporting** — Never "Raj said X." Always "The team confirmed that..."

**Missing information protocol** — Nothing invented. `Owner unclear`, `Not stated`, `Decision pending` — every gap is visible, not papered over.

**Negative decision capture** — Decisions NOT to act are logged. Most meeting tools miss this entirely.

---

## Author

Rajendra Prasad Raju. Bh — AVP, Technology Program Management, Sutherland Global Services

31+ years across IT, program management, and healthcare BPO. PMP | CISA | ITIL | ISO 27001 LA | MBA | MS

---

## Disclaimer

Outputs from this skill are for documentation and organizational purposes only and do not constitute legal, compliance, or professional advisory advice of any kind.

---
name: meeting-documenter
description: >
  Expert Meeting Documentation, Accountability, and Audit Trail System.
  ALWAYS trigger this skill when the user provides meeting notes, transcripts, call summaries,
  chat discussions, Granola notes, email threads, or any raw meeting input and asks to
  document, summarize, process, or turn it into minutes, action items, or a structured record.
  Also trigger when the user says: "document this meeting", "process these notes",
  "extract action items", "write up the minutes", "create a decision log", "prepare a
  pre-meeting brief", "write an agenda", "do a retro", "AAR", "after-action review",
  "3x30 report", "executive summary", "risk register", "RASI matrix", "what did we decide",
  "who owns what", "write a meeting follow-up", "turn this into MOM", or "accountability tracker".
  Works across Claude Desktop, Claude Code CLI, OpenAI ChatGPT, Google Gemini, Antigravity,
  Codex, and any LLM without modification.
---

# Meeting Documenter — Cross-Platform Skill

This skill transforms raw meeting inputs into a structured, audit-ready execution record.
It runs on **any LLM** — Claude (Desktop, Code, claude.ai), ChatGPT, Gemini, Antigravity,
Codex, or any other assistant — without platform-specific dependencies.

---

## STEP 0 — Identify Mode

Determine which mode applies before producing any output.

| Mode | When to Use |
|---|---|
| **PRE** — Pre-Meeting Brief | User wants an agenda, pre-read, or preparation guide |
| **PROCESS** — Meeting Processing | User provides transcript, notes, Granola output, email thread, or call summary |
| **AAR** — After-Action Review | User wants a retrospective or post-project review |
| **EXEC** — Executive Report Only | User wants only a 3x30 executive summary |

If mode is unclear, default to **PROCESS**.

---

## STEP 1 — Core Operating Principles (Universal)

Apply these on every platform, in every mode, without exception.

### 1.1 Subject-Based Reporting
Never write minutes as a transcript.
Do NOT write: "Raj said X. John replied Y."
DO write: "The team confirmed that the migration timeline remains at risk due to pending client approval."
Use names ONLY for: action ownership, decision accountability, escalation, approval.

### 1.2 Trichotomy of Reasoning
For every major item, reason in this order before writing output:
1. **Why** — What objective or intent drives this?
2. **What** — What decision, issue, risk, or action emerged?
3. **How** — How will it be executed, tracked, or communicated?

### 1.3 Neutral Documentation
Stay objective. Do not judge, praise, criticize, or emotionally interpret.
Document facts, agreements, trade-offs, and unresolved items only.

### 1.4 Missing Information Protocol
Never invent owners, dates, costs, decisions, or rationale.
When information is absent, use these exact markers:
- `Not stated`
- `Owner unclear — requires assignment`
- `Due date not stated`
- `Decision pending`
- `Requires confirmation`
- `Objective linkage unclear`
- `Consensus not confirmed`

### 1.5 Holarchy Check
Every major action or decision must connect upward:
Meeting topic → Project objective → Business objective → Organizational outcome.
If connection is unclear: mark as `Objective linkage unclear — requires clarification.`

---

## STEP 2 — PRE-MEETING BRIEF MODE

Use when: user asks to prepare a meeting, create an agenda, or send a pre-read.

### 2.1 Define the 3 Ps

**Purpose**
- State exactly why the meeting is happening.
- Define what "done" looks like.
- If no clear purpose: recommend cancelling or converting to async.

**People**
Assign every participant one of these roles:
Leader / Facilitator / Decision Maker / Information Giver / Information Getter /
Note Taker / Approver / Support Owner / Observer

If role is unclear for any invitee: `Role unclear — confirm whether this person is required.`

**Process**
Define: Timebox | Agenda sequence | Decision points | Required inputs | Expected outputs | Follow-up owner

### 2.2 Agenda Rule
Maximum 3 major discussion items. Each must be framed as a question or decision.
Example:
1. What decision must be made today?
2. What risks are blocking execution?
3. What action ownership must be confirmed?

### 2.3 48-Hour Preparation Rule
Recommend: Agenda + pre-read sent 48 hrs before. Reminder sent 24 hrs before.
If not done: flag as `Preparation gap.`

---

## STEP 3 — MEETING PROCESSING WORKFLOW

Use when: user provides any raw meeting input.

### 3.1 Scan
Extract the situation context. Identify:
Background | Current state | Prior decisions | Open dependencies | Known blockers |
Desired future state | Meeting objective

Output as a short contextual paragraph — not bullets.

### 3.2 Focus
Identify the 2–3 core themes driving the meeting.
Examples: Timeline risk | Client approval dependency | Budget/resource constraint |
Scope change | Operational readiness | Quality issue | Governance decision | Stakeholder concern

Do not list every minor topic.

### 3.3 Act
Isolate execution outputs:
Decisions made | Decisions deferred | Action items | Owners | Deadlines |
Risks | Escalations | Communication requirements

---

## STEP 4 — ACTION ITEM EXTRACTION

Every valid action item must answer the **Nimble 5 Ws**:

| Element | Requirement |
|---|---|
| Who | Named owner or accountable role |
| What | Verb-based task |
| When | Due date or required timing |
| Where | Project, platform, client, workstream, or meeting context |
| Why | Purpose or intended benefit |

### Action Wording Rule
Start every action with a verb.
✅ "Validate migration readiness with the client to confirm go-live feasibility."
✅ "Share revised project timeline with stakeholders to align expectations."
❌ "Discussion on timeline" | "Need to check" | "Follow-up required"

### 2-by-4 Capture Rule
Frame open issues as:
> To [what needs to be done], by [who] by [when], for [purpose].

### Assignment Rules
- Do not assign to absent people unless the meeting explicitly named them.
- For immediate work: use named owners.
- For long-term/departmental work: assign to roles so accountability survives personnel changes.

---

## STEP 5 — RESPONSIBILITY MATRIX (RASI)

Use RASI — NOT RACI. Do not use "Consulted." Use "Supports" instead.

| Role | Meaning |
|---|---|
| R — Responsible | One and only one accountable owner for delivery |
| A — Authorizes | Person or group approving, funding, or authorizing |
| S — Supports | People or teams actively helping the R owner |
| I — Informed | People or groups kept updated |

Every assignment must have **exactly one** Responsible owner.
If multiple possible owners exist: `Responsibility conflict — one Responsible owner must be confirmed.`

**Enrich each cell where possible:**
> R: [Name / Role] | Due: [Date] | Cost: [₹ or Not stated] | FTP: [Hours or Not stated]

---

## STEP 6 — DECISION LOGGING

Capture a decision when the group: chooses, rejects, defers, decides not to act,
changes direction, confirms status quo, or escalates.

**Negative decisions must be captured.**
Example: "The team decided not to proceed with the revised timeline until client approval is received."

Every decision log captures:
1. Purpose — Why was this decision needed?
2. Options considered — What alternatives were discussed?
3. Criteria used — What factors mattered?
4. Final decision — What was chosen?
5. Deselection rationale — Why were other options rejected?
6. Impact — Cost, time, risk, effort, or FTP.

**Consensus Definition:** The group will professionally support the decision, even if not everyone's preference.
If unclear: `Consensus not confirmed.`

---

## STEP 7 — RISK & ISSUE CLASSIFICATION

Every risk or issue must include:
Description | Proposed resolution | Target date | Owner (if stated) | Escalation need

Classifications:
- **Risk** — Something that may happen.
- **Issue** — Something already happening.
- **Blocker** — Something preventing progress now.
- **Concern** — Stakeholder worry needing monitoring.
- **Assumption** — Something treated as true but not yet validated.

---

## STEP 8 — AFTER-ACTION REVIEW MODE

Use for post-project or retrospective meetings.

Capture facts only. Include:
- What worked
- What hampered progress
- What assumptions proved true or false
- What changed during execution
- What should be repeated
- What should be improved
- What should be stopped

Do not assign blame to individuals.

---

## STEP 9 — COMMUNICATION PLAN (T-Chart)

At the end of every output, define the communication plan.

Answer:
1. What do we tell superiors we got done today?
2. What do we tell stakeholders if they ask?

Sequence:
1. Inform executive sponsor first.
2. Inform project leadership.
3. Inform impacted stakeholders.
4. Update action tracker or project system.

---

## STEP 10 — 3x30 EXECUTIVE REPORT

When executive communication is needed, produce this report.
Must be: writable in 30 min | readable in 3 min | focused on bottom line, ask, decisions, next steps.

---

## OUTPUT QUALITY GATE

Before finalizing any output, verify all of the following:
- [ ] All explicit decisions captured?
- [ ] Deferred or negative decisions captured?
- [ ] Every action starts with a verb?
- [ ] Every action has exactly one Responsible owner?
- [ ] Missing owners or dates clearly flagged?
- [ ] Risks/issues separated from actions?
- [ ] Output understandable to someone not in the meeting?
- [ ] Irrelevant tangents removed?
- [ ] Tone neutral?
- [ ] Assumptions marked as assumptions?
- [ ] All unresolved items clearly visible?

---

## OUTPUT TEMPLATES

Produce output in this sequence unless the user requests otherwise:
1. Meeting Context Scan
2. Core Themes (2–3 only)
3. Decisions Made
4. Decisions Deferred or Not Taken
5. Ultimate Action & Risk Tracker (Template A)
6. Decision Log (Template B)
7. Risk & Issue Register (Template C)
8. Communication Plan
9. 3x30 Executive Report (only if executive communication is needed)
10. Missing Information / Clarifications Required

Always separate:
- What was explicitly stated
- What was inferred
- What is missing
- What needs confirmation

---

### Template A — Ultimate Action & Risk Tracker

| ID / Date | Action — What & Why | RASI Assignment | Deadline | Est. Impact / FTP | Status | Risk / Issue & Resolution |
|---|---|---|---|---|---|---|
| #001 / [Date] | [Verb-based task] to [purpose] | R: [One Owner]<br>A: [Approver]<br>S: [Supporters]<br>I: [Informed] | [Date or Not stated] | Cost: [₹ or Not stated]<br>FTP: [Hours or Not stated] | [🟢 Green / 🟡 Amber / 🔴 Red] / [%] | Issue: [Obstacle]<br>Resolution: [Plan by Date] |

---

### Template B — Decision Log

| Date | Topic & Purpose | Options Considered | Key Criteria | Final Decision | Rationale & Deselection | Impact / FTP |
|---|---|---|---|---|---|---|
| [Date] | [Why this decision was needed] | 1. [Option A]<br>2. [Option B]<br>3. [Option C] | [Criterion 1]<br>[Criterion 2] | [Final decision] | Selected: [reason]. Rejected: [deselection rationale]. | Cost: [₹ or Not stated]<br>FTP: [Labor or Not stated] |

---

### Template C — Risk & Issue Register

| ID / Date | Type | Description | Impact | Owner | Mitigation / Resolution | Target Date | Escalation? |
|---|---|---|---|---|---|---|---|
| R-001 / [Date] | [Risk / Issue / Blocker / Concern / Assumption] | [Description] | [Business/project impact] | [Owner or Not stated] | [Mitigation or resolution] | [Date or Not stated] | [Yes / No / Unclear] |

---

### Template D — 3x30 Executive Report

```
Subject: ACTION REQUIRED: [Project Name] — 3x30 Executive Report

📌 SCAN AND RESPOND: Review the Bottom Line and the Ask below, then reply with approval, guidance, or a decision.

BOTTOM LINE
[1–2 sentences: what the team accomplished, what changed, or what requires attention.]

THE ASK / ESCALATION
[Blocker, decision, approval, budget request, or guidance needed. Phrased for a quick executive reply.]

KEY DECISIONS MADE
1. [Decision]
   Rationale: [Objective criteria. Why alternatives were deselected.]

2. [Decision]
   Rationale: [Objective criteria. Why alternatives were deselected.]

IMMEDIATE NEXT STEPS
Who: [Owner] | What: [Verb-based task] | When: [Deadline] | Where: [Project/workstream] | Why: [Purpose]
Who: [Owner] | What: [Verb-based task] | When: [Deadline] | Where: [Project/workstream] | Why: [Purpose]

RISKS / ISSUES REQUIRING ATTENTION
• [Risk or issue] — [Mitigation or escalation required]

COMMUNICATION PLAN
Audience           | Message                              | Timing   | Owner
Superiors/Sponsors | [What they need to know first]       | [Timing] | [Owner]
Stakeholders       | [What they should be told if asked]  | [Timing] | [Owner]
```

---

## PLATFORM NOTES

This skill works on all platforms without modification. No platform-specific dependencies.

| Platform | Notes |
|---|---|
| Claude Desktop / claude.ai | Full output with tables. Artifacts available if enabled. |
| Claude Code CLI | Plain text and markdown tables render cleanly in terminal. |
| ChatGPT (GPT-4o / o1 / o3) | Paste SKILL.md into system prompt or first user message. Tables render in canvas. |
| Google Gemini Advanced | Paste SKILL.md as system instruction. Markdown tables supported. |
| Antigravity | Same as Gemini Advanced. |
| OpenAI Codex | Text and markdown. Pipe meeting notes as stdin if needed. |
| Any other LLM | Paste SKILL.md as system prompt. All output is plain markdown — no special tools required. |

**To use on any LLM without a skill system:**
Paste the full contents of this SKILL.md as the system prompt (or first message), then provide your meeting notes.

---
name: master-prompter
description: >
  Universal prompt engineering skill that synthesizes best practices from Claude (Anthropic), GPT-4.1/GPT-5.5 (OpenAI), Gemini 3 (Google), and Grok (xAI). ALWAYS trigger this skill when:
  (1) A user prompt is vague, ambiguous, or lacks enough context to produce a high-quality response — reconstruct and rewrite the prompt internally before answering;
  (2) The user explicitly asks to "improve", "rewrite", "fix", or "engineer" a prompt;
  (3) The user asks how to prompt Claude, ChatGPT, Gemini, or any AI model;
  (4) The user says something like "help me write a prompt", "make this better", "I'm not getting good results", "what's the best way to ask this";
  (5) Output quality seems at risk due to missing role, goal, format, or audience specification;
  (6) The user asks for a LinkedIn post, email draft, or any copy-paste content — ALWAYS apply the relevant domain template and wrap the final output in a code block.
  This skill makes Claude auto-reconstruct vague inputs into high-quality structured prompts AND teaches the user how to craft better prompts themselves. Never skip this skill when prompts are ambiguous or incomplete.
---

# Master Prompter — Universal Prompt Engineering Skill

This skill synthesizes best practices from **Claude (Anthropic)**, **GPT-4.1 / GPT-5.5 (OpenAI)**, **Gemini 3 (Google)**, and **Grok (xAI)** into a single unified framework.

---

## CRITICAL OUTPUT RULES (apply to every response)

1. **LinkedIn posts** — ALWAYS wrap the final post in a code block so it can be copied in one click. No exceptions.
2. **Emails** — ALWAYS wrap the final email body in a code block.
3. **Prompts** — ALWAYS wrap engineered prompts in a code block.
4. **Any copy-paste content** — if the user will paste it somewhere else, it goes in a code block.
5. **LinkedIn requests** — ALWAYS apply the Content/LinkedIn template from Part 4, even if the prompt seems clear. Never write a LinkedIn post without running it through the template first.

---

## PART 1: WHEN TO USE THIS SKILL

### Auto-Trigger: Vague Prompt Detection
If a user's message is missing **2 or more** of the 5 REACT components (Role, Expected Output, Audience, Context, Task), **internally reconstruct the prompt** using the framework below BEFORE answering. Show the reconstructed prompt to the user so they learn.

**Vague signals to detect:**
- Single sentence with no goal specification ("write something about X")
- Missing audience or format ("create content for my team")
- No success criteria ("make this better")
- Domain ambiguity ("help me with my project")
- No output length or structure specified

**Domain auto-triggers (always apply the matching template, even for clear prompts):**
- "write a LinkedIn post / tweet / social post" → apply Content/LinkedIn template
- "write an email" → apply Business/Email template
- "write a drill / session plan" → apply Cricket Coaching template
- "analyze this stock / company" → apply Analysis/Research template
- "write code / fix this script" → apply Technical/Coding template

**When vague:** Do not ask a list of clarifying questions. Instead, state your reconstructed prompt and proceed. Flag any assumptions you made.

---

## PART 2: THE UNIFIED PROMPT FRAMEWORK

### The REACT Structure (Universal)
Every high-quality prompt contains these 5 components:

| Component | What It Covers | Example |
|-----------|----------------|---------|
| **R**ole | Who the AI is / persona | "You are a senior cricket coach with 20+ years experience" |
| **E**xpected Output | Format, length, structure | "Give me a 5-point bullet list, under 200 words" |
| **A**udience | Who will read/use this | "For a 10-year-old beginner, not a professional" |
| **C**ontext | Background, constraints, data | "I have a 2-hour session, 15 kids, one pitch" |
| **T**ask | The actual ask | "Create a fielding drill progression" |

---

## PART 3: TECHNIQUE LIBRARY (Cross-Model)

### 3.1 Zero-Shot Prompting
Use when the task is clear and no examples are needed.
```
[Role] + [Task] + [Expected Output Format]

Example:
"You are a program manager. Summarize this email thread in 3 bullet points, each under 15 words."
```

### 3.2 Few-Shot Prompting (OpenAI + Google best practice)
Provide 2–3 examples of input → output to anchor the pattern.
```
Here are examples of what I want:

Input: "delayed project"
Output: "Project is running 2 weeks behind due to resource conflict. Mitigation: reallocate Team B."

Input: "budget overrun"
Output: "Budget exceeded by 12% due to unplanned vendor invoice. Mitigation: raise CR with client."

Now apply this to: [new input]
```

### 3.3 Chain-of-Thought (CoT) — All Models
Force step-by-step reasoning before the final answer.
```
Before answering, think through this step by step:
1. What is the user's actual goal?
2. What information is missing or assumed?
3. What's the best structure for the output?
Then provide your final answer.
```

### 3.4 Role + Persona Anchoring (Claude + Gemini)
Assign a strong persona at the start. This shapes tone, depth, and reasoning style.
```
You are [specific role] with [X years] experience in [domain].
You are known for [key trait — e.g., being blunt, detail-oriented, simplifying complex ideas].
You never [anti-pattern — e.g., use jargon without explaining, give generic advice].
```

### 3.5 Constraint-First Prompting (Gemini 3)
Place behavioral rules and constraints BEFORE the task content.
```
CONSTRAINTS (apply throughout your response):
- Maximum 150 words
- No bullet points — use prose only
- Avoid technical jargon
- Write in second person ("you")

TASK: [Insert task here]

CONTEXT: [Insert context here]
```

### 3.6 XML Structural Tagging (Gemini 3 + Claude)
Use XML tags to separate instructions from data — prevents model confusion.
```xml
<role>You are a senior program manager at a BPO company.</role>

<constraints>
- Formal tone
- No abbreviations
- Max 3 paragraphs
</constraints>

<context>
[Paste email / data / document here]
</context>

<task>
Write a client-facing status update based on the context above.
</task>
```

### 3.7 Self-Critique Loop (Gemini 3)
Ask the model to evaluate its own output before delivering it.
```
After generating your response, check:
1. Did I answer the user's intent, not just their literal words?
2. Is the tone right for the audience?
3. Did I flag any assumptions I made?
4. Is any part of this vague or could be misunderstood?
If any check fails, revise before responding.
```

### 3.8 Explicit Planning Directive (Gemini 3 + OpenAI)
For complex tasks, force decomposition first.
```
Before providing the final answer:
1. Parse the goal into distinct sub-tasks
2. Identify what information is missing — if critical, stop and ask; otherwise, state your assumption
3. Check if there's a smarter/faster approach than the obvious one
4. Create a step-by-step plan
5. Execute the plan
6. Validate the output against the original goal
```

### 3.9 Persona Persistence + Context Anchoring (GPT-4.1)
For multi-turn or long-context tasks, re-anchor the model periodically.
```
[After large context block]
"Based on the information above, and keeping in mind that you are [role] tasked with [goal]..."
```

### 3.10 Output Scaffolding (All Models)
Pre-define the response structure so the model fills it in — reduces hallucination and drift.
```
Respond using EXACTLY this structure:

**Summary** (1 sentence):
**Key Finding** (2–3 bullet points):
**Recommended Action** (numbered steps):
**Risk / Caveat** (if any):
```

---

## PART 4: DOMAIN-SPECIFIC PROMPT TEMPLATES

### Business / Program Management
```
You are a senior AVP-level Program Manager with 30+ years of IT and BPO experience.

Context: [Paste situation here]

Task: [What you need — status update / escalation / risk memo / intake summary]

Output format: [Email / bullet points / table / executive summary]

Constraints:
- Formal, senior tone
- No filler phrases ("As per our discussion", "Please find attached")
- Max [X] words
- Audience: [Client / internal team / leadership]
```

### Technical / Automation / Coding
```
You are a [Python/bash/n8n/React] expert.

Task: [Specific coding task]

Constraints:
- Production-ready code only
- Include error handling
- Add inline comments for every non-obvious step
- No partial snippets — complete, copy-paste ready code only
- Target environment: [Mac/Ubuntu/Docker]

Context:
[Paste relevant code, error message, or system config here]
```

### Content / LinkedIn / Communication

**MANDATORY for every LinkedIn post request — apply all rules below without exception:**

```
Role: You are a professional content strategist writing for a senior IT leader's
personal brand on LinkedIn.

Audience: IT professionals, AVPs, CXOs, program managers on LinkedIn.

Voice rules:
- Short punchy sentences. No sentence over 20 words.
- Data and specifics over adjectives ("196% revenue growth" not "impressive results")
- Escalation phrasing — build tension before the payoff
- Contrast pivots — "X used to require Y. Now it takes one prompt."
- First-person, experience-backed — write as if the author lived this
- 70% insight / 30% story ratio

Format:
- Hook: 1 punchy line (stops the scroll)
- Body: 3–5 short paragraphs, each 2–4 sentences max
- CTA: 1 line — question or invitation, not a command
- Hashtags: max 5, relevant only — no hashtag spam

Length: Max 280 words / 3,000 characters

Hard bans — NEVER use:
- "In today's fast-paced world"
- "leverage", "synergy", "game-changer", "rockstar", "guru"
- Generic motivational conclusions ("Keep pushing!", "The future is bright")
- Passive voice openings
- More than 5 hashtags
- Tagging companies or clients by name

OUTPUT RULE: Wrap the final LinkedIn post in a code block for easy copying.
```

### Analysis / Research / Stock
```
You are a [domain] analyst.

Data/Context: [Paste source data, URLs, or context]

Task: [What analysis is needed]

Output format:
1. Summary (3 sentences)
2. Key Findings (bullet points, each with data citation)
3. Recommendation (with reasoning)
4. Risks / Assumptions

Citation rule: Every specific claim must reference its source. If no source is available, label it as "estimate."
```

### Cricket Coaching / Fitness
```
You are a Level 3 cricket coach with 30+ years of coaching and playing experience.
You run an academy with youth players aged 8–18.

Context: [Age group / skill level / available time / equipment / facility]

Task: [Drill / session plan / technique correction / training program]

Output format:
- Drill name
- Objective
- Setup (equipment + player positions)
- Instructions (numbered steps)
- Coaching cues (what to say to kids)
- Common errors + corrections
- Progression (easier → harder variants)
```

---

## PART 5: VAGUE PROMPT RECONSTRUCTION PROTOCOL

When Claude detects a vague prompt, follow this process:

### Step 1: Diagnose what's missing
Check for each REACT component. Note which are absent.

### Step 2: Apply intelligent defaults
Use context from the conversation history and any available user profile to fill gaps. Apply sensible defaults based on the domain of the request — professional/formal for business tasks, technical for coding tasks, casual for creative tasks.

### Step 3: Reconstruct and announce
Say: *"Your prompt was broad, so I've reconstructed it with these additions: [list assumptions]. Here's what I'm working with:"*

Then show the enriched prompt in a formatted block.

### Step 4: Execute and flag
Deliver the output. At the end, note: *"Assumptions made: [X, Y, Z]. Reply to adjust any of these."*

---

## PART 6: PROMPT QUALITY CHECKLIST

Before finalizing any prompted output, verify:

- [ ] Role is specific and domain-appropriate
- [ ] Task is unambiguous — a new reader would understand it
- [ ] Output format is pre-defined (length, structure, tone)
- [ ] Audience is named
- [ ] Context / data is provided or assumptions are stated
- [ ] Constraints are front-loaded, not buried
- [ ] No open-ended instructions ("make it good", "be creative")
- [ ] Success criteria are clear — what does "done" look like?
- [ ] Copy-paste outputs (LinkedIn, email, prompts) are wrapped in a code block

---

## PART 7: CROSS-MODEL REFERENCE (Quick Guide)

| Model | Key Strength | Best Technique |
|-------|-------------|----------------|
| **Claude** | Nuanced reasoning, long context | XML tags, self-critique, persona anchoring |
| **GPT-4.1 / 5.5** | Instruction following, structured output | Few-shot, output scaffolding, system message separation |
| **Gemini 3** | Planning, decomposition, multimodal | Explicit planning, constraint-first, XML tagging |
| **Grok** | Real-time data, casual reasoning | Direct questions, context compression, minimal verbosity |

---

## PART 8: ANTI-PATTERNS TO AVOID

Never do these — they consistently degrade output quality:

1. **Vague quality words** — "make it professional / good / better" → specify what "good" means
2. **Instruction at the end** — for long context, put your question AFTER the data, but role + constraints BEFORE
3. **Over-asking** — one prompt, one primary goal. Split complex tasks.
4. **No format spec** — always state expected output structure
5. **Assuming context** — if the model doesn't know your role or situation, state it
6. **"Be creative"** without guardrails — creativity without direction = inconsistent output
7. **Conversational drift** — in long chats, re-anchor role and goal every 5–6 turns
8. **Raw copy-paste output** — LinkedIn posts, emails, and prompts must always be in a code block

---

## PART 9: QUICK-FIRE PROMPT IMPROVER

When a user says "improve this prompt", apply this transform:

**Input (vague):** "Write me a LinkedIn post about AI"

**Output (engineered):**
```
Role: Senior IT leader, 30+ years experience, personal brand on LinkedIn.
Audience: IT professionals, CXOs, program managers.
Tone: Direct, no hype, experience-backed. Short sentences.
Format: Hook → 3-4 paragraphs → CTA. Max 250 words.
Topic: How AI automation is changing program management workflows —
with a specific real-world example, not generic observations.
Do NOT use: "In today's fast-paced world", "leverage", "game-changer",
hashtag spam, or generic motivational conclusions.
OUTPUT: Wrap final post in a code block.
```

---

*Skill v1.1 — synthesized from: Google Gemini API Prompting Strategies, Gemini for Workspace October 2024 Guide, Phil Schmid's Gemini 3 Best Practices, Anthropic Claude Prompt Engineering Overview, OpenAI GPT-4.1 Prompting Guide, OpenAI GPT-5.5 Prompt Guidance, and cross-model community research.*

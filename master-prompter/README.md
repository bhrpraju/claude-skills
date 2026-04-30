# master-prompter

> Universal prompt engineering skill for Claude — synthesizes best practices from Claude, GPT-4.1/5.5, Gemini 3, and Grok into one framework.

---

## What it does

This skill has two jobs:

1. **Auto-reconstructs vague prompts** — when your input is missing key components, the skill internally builds a better prompt, states its assumptions, and delivers the output. You get results AND you learn.
2. **Teaches structured prompting** — the REACT framework, 10 cross-model techniques, 5 domain templates, and an anti-pattern checklist.

---

## The REACT Framework

Every high-quality prompt needs all 5 of these:

| Component | What It Covers |
|-----------|----------------|
| **R**ole | Who the AI is / persona |
| **E**xpected Output | Format, length, structure |
| **A**udience | Who will read/use the output |
| **C**ontext | Background, constraints, data |
| **T**ask | The actual ask |

---

## Techniques Covered

| # | Technique | Best For |
|---|-----------|----------|
| 3.1 | Zero-Shot | Clear, simple tasks |
| 3.2 | Few-Shot | Pattern matching, formatting |
| 3.3 | Chain-of-Thought | Reasoning, analysis |
| 3.4 | Role + Persona Anchoring | Tone and depth control |
| 3.5 | Constraint-First | Output discipline |
| 3.6 | XML Structural Tagging | Long or complex prompts |
| 3.7 | Self-Critique Loop | Quality assurance |
| 3.8 | Explicit Planning | Multi-step tasks |
| 3.9 | Context Anchoring | Long conversations |
| 3.10 | Output Scaffolding | Consistent structure |

---

## Domain Templates Included

- Business / Program Management
- Technical / Automation / Coding
- Content / LinkedIn / Communication
- Analysis / Research / Stock
- Cricket Coaching / Fitness

---

## Trigger Phrases

This skill fires automatically when you say:
- "help me write a prompt"
- "improve this prompt"
- "I'm not getting good results"
- "make this better"
- "how do I ask Claude / ChatGPT / Gemini to..."
- Any vague request missing Role, Goal, Audience, Context, or Format

---

## Version History

| Version | Date | Changes |
|---------|------|---------|
| v1.0 | Apr 2026 | Initial release — REACT framework, 10 techniques, 5 domain templates |

---

## Sources

Synthesized from official documentation of:
- [Google Gemini API Prompting Strategies](https://ai.google.dev/gemini-api/docs/prompting-strategies)
- [Phil Schmid's Gemini 3 Best Practices](https://www.philschmid.de/gemini-3-prompt-practices)
- [Anthropic Claude Prompt Engineering Overview](https://platform.claude.com/docs/en/build-with-claude/prompt-engineering/overview)
- [OpenAI GPT-4.1 Prompting Guide](https://developers.openai.com/cookbook/examples/gpt4-1_prompting_guide)
- OpenAI GPT-5.5 Prompt Guidance

---

**Author:** Rajendra Prasad Raju. Bh

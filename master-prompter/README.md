# master-prompter

> Universal prompt engineering skill for Claude — synthesizes best practices from Claude, GPT-4.1/5.5, Gemini 3, and Grok into one framework.

**v1.1** — Added LinkedIn auto-template enforcement and code block output rule for all copy-paste content.

---

## What it does

This skill has two jobs:

1. **Auto-reconstructs vague prompts** — when your input is missing key components, the skill internally builds a better prompt, states its assumptions, and delivers the output. You get results AND you learn.
2. **Teaches structured prompting** — the REACT framework, 10 cross-model techniques, 5 domain templates, and an anti-pattern checklist.

---

## Critical Output Rules (v1.1)

- LinkedIn posts → always in a code block
- Emails → always in a code block
- Engineered prompts → always in a code block
- LinkedIn requests → always run through the Content/LinkedIn template first, even if the prompt seems clear

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

## Domain Auto-Triggers

| Request type | Template applied automatically |
|---|---|
| "write a LinkedIn post" | Content/LinkedIn template |
| "write an email" | Business/Program Management template |
| "analyze this stock" | Analysis/Research template |
| "write code / fix script" | Technical/Coding template |
| "write a drill / session plan" | Cricket Coaching template |

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

## Version History

| Version | Date | Changes |
|---------|------|---------|
| v1.1 | Apr 2026 | LinkedIn auto-template enforcement; code block rule for all copy-paste output; domain auto-triggers added |
| v1.0 | Apr 2026 | Initial release — REACT framework, 10 techniques, 5 domain templates |

---

## Sources

- [Google Gemini API Prompting Strategies](https://ai.google.dev/gemini-api/docs/prompting-strategies)
- [Phil Schmid's Gemini 3 Best Practices](https://www.philschmid.de/gemini-3-prompt-practices)
- [Anthropic Claude Prompt Engineering Overview](https://platform.claude.com/docs/en/build-with-claude/prompt-engineering/overview)
- [OpenAI GPT-4.1 Prompting Guide](https://developers.openai.com/cookbook/examples/gpt4-1_prompting_guide)
- OpenAI GPT-5.5 Prompt Guidance

---

**Author:** Rajendra Prasad Raju. Bh

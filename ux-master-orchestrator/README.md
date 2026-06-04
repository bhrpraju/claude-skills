# UX Master Orchestrator

> A single entry point that coordinates all installed UX/UI skills into one disciplined, end-to-end design pipeline.

Stop invoking design skills individually. This orchestrator routes every design request through the right specialist skill at the right stage — automatically.

---

## What This Skill Does

Most design workflows are fragmented — you jump between tools, forget steps, skip the diagnosis, go straight to code. This skill enforces a complete 5-phase pipeline every single time:

1. **Diagnose** — cognitive psychology, behavioral economics, Six Minds
2. **Architect** — layout strategy, UX laws, design system selection
3. **Specify** — exact visual parameters, palette, typography, spacing
4. **Build** — production-ready code for your platform
5. **Polish + Audit** — anti-pattern detection, critique, final pass

---

## The Skill Stack It Coordinates

| Skill | Role |
|---|---|
| ux-cognitive-architect | Phase 1 — cognitive diagnosis |
| ux-designer-skill | Phase 2 — WCAG, IA, interaction patterns |
| ui-ux-pro-max | Phase 2+3 — design system generation |
| frontend-design-multiplatform | Phase 3 — anti-generic aesthetics |
| mobile-app-ui-design | Phase 3 (mobile) — touch, gestures, emotion |
| interface-design | Phase 3 (dashboards) — domain exploration |
| web-design-guidelines | Phase 3 (web) — Vercel standards |
| impeccable | Phase 5 — polish, audit, anti-pattern detection |

Missing skills are flagged at the end of every response — never silently skipped.

---

## When to Use This Skill

Use this as your default for ALL design work. It replaces invoking individual design skills manually.

**Trigger phrases:**
- "Design a screen for..."
- "Build me a UI for..."
- "Create a dashboard for..."
- "What should this look like?"
- "Is this good UX?"
- "Improve this design"
- "Audit this interface"
- "Polish this before shipping"
- "Design an onboarding flow for..."
- "Build a mobile app UI for..."
- "Create a landing page for..."
- "Review this wireframe"
- "Help me choose a design system for..."

---

## The 5-Phase Pipeline

Every request runs all five phases. No exceptions. No skipping.

Phase 1 — DIAGNOSE (ux-cognitive-architect)
  Persona + End Goal + Experience Goal
  Six Minds — Vision, Wayfinding, Memory, Language, Decision Making, Emotion
  Norman's Visceral, Behavioral, Reflective levels
  Hook Loop if retention is required
  Output: written diagnostic — no code yet

Phase 2 — ARCHITECT (ux-designer-skill + ui-ux-pro-max)
  Information architecture + navigation pattern
  WCAG 2.2 AA accessibility requirements
  Hick's, Fitts's, Jakob's, Tesler's, Gestalt applied explicitly
  Design system selection — style, color family, font pairing, stack
  Output: architecture spec — layout in words or ASCII wireframe

Phase 3 — SPECIFY (frontend-design-multiplatform + platform variants)
  Named aesthetic direction — deliberate, not generic
  No Inter-everywhere, no purple-blue gradients, no nested cards
  8px grid spacing values
  HSL color palette
  Typography scale with exact px values
  Shadow elevation levels
  Output: complete visual spec

Phase 4 — BUILD (platform-appropriate code)
  Claude Desktop: React .jsx artifact + Tailwind
  Claude Code CLI: .jsx + .css component files
  Gemini Advanced / ChatGPT: single copy-paste HTML file
  OpenAI Codex: separate .jsx + .css files
  Pre-build checklist enforced before writing a single line

Phase 5 — POLISH + AUDIT (impeccable)
  27 deterministic anti-pattern rules
  UX critique — hierarchy, IA, emotional resonance
  Technical audit — contrast, focus states, touch targets
  P0 to P3 severity ratings on all findings
  Output: audit report with specific fixes

---

## Skill Gap Reporting

At the end of every response:

SKILLS USED: list of skills applied
SKILLS MISSING: skills that would have added value but are not installed
MANUAL FALLBACKS: where built-in knowledge substituted for a missing skill

---

## Platform Support

| Platform | Full Pipeline | Code Delivery | CLI Tools |
|---|---|---|---|
| Claude Desktop | Yes | React artifact | No |
| Claude Code CLI | Yes | Component files | Yes — ui-ux-pro-max search, impeccable commands |
| Gemini Advanced | Phases 1-3 full, 4-5 manual | Copy-paste HTML | No |
| ChatGPT | Phases 1-3 full, 4-5 manual | Copy-paste HTML | No |
| OpenAI Codex | Yes | .jsx + .css files | Partial |

---

## Example Prompts

Design a fintech dashboard for retail investors in India. Mobile-first. Dark mode.

I am building a WhatsApp-based book learning platform for non-technical users aged 35-55. Design the onboarding flow.

Here is my current SaaS admin panel [paste code]. Run a full audit and tell me what to fix.

Design a women's health symptom tracking app. Users are anxious and time-poor. Medicine 3.0 approach.

Build a cricket live score card component for WhatsApp-style delivery. Compact, scannable, high information density.

---

## Quick Decision Tree

Is this a polish or audit request only?
  Yes — skip to Phase 5 (impeccable)
  No — continue

Does the user already have specs and just need code?
  Yes — start at Phase 4, use their specs
  No — run full pipeline Phase 1 through 5

---

## Install

Claude Desktop: Settings, Skills, Add Skill, paste https://github.com/bhrpraju/claude-skills

Claude Code CLI:
git clone https://github.com/bhrpraju/claude-skills.git
cp -r claude-skills/ux-master-orchestrator ~/.claude/skills/

Gemini Advanced / ChatGPT: Open SKILL.md, copy the full contents, paste as your first message or system prompt.

---

## Part of the UX Stack

ux-cognitive-architect  — diagnose (standalone or via orchestrator)
ux-master-orchestrator  — THIS SKILL — full pipeline coordinator
ui-ux-pro-max           — design system database (install separately)
impeccable              — polish + audit (install separately)

Install all four for maximum coverage. This orchestrator detects which are present and routes accordingly.

---

## Author

Rajendra Prasad Raju BH
github.com/bhrpraju
linkedin.com/in/rajendrabhupathi

---

Version: 1.0 | License: MIT

---
name: ux-master-orchestrator
description: >
  Master UX/UI design orchestrator. ALWAYS trigger for ANY design request: build a screen,
  design a component, evaluate a UI, audit a layout, choose colors or typography, review a
  wireframe, write design specs, dashboard, onboarding, mobile UI, landing page, SaaS,
  admin panel. Trigger on: "design", "UI", "UX", "interface", "layout", "component",
  "look and feel", "improve this", "audit this", "polish this", "is this good UX",
  "build me a page", "style this", "make it beautiful", "responsive", "dark mode",
  "color palette", "typography", "spacing", "accessibility", "design system".
  Runs a mandatory 5-phase pipeline: Diagnose → Architect → Specify → Build → Polish+Audit.
  Routes each phase to the correct specialist skill. Works on Claude Desktop, Claude Code
  CLI, Gemini Advanced, OpenAI Codex, and ChatGPT. Never skip phases. Never go straight
  to code.
---

# UX Master Orchestrator

A single entry point that coordinates all installed UX/UI skills into one disciplined,
end-to-end design pipeline. You do not use these skills independently anymore —
everything routes through here.

---

## The Skill Stack This Orchestrator Manages

| Skill | Role in Pipeline | Platform |
|---|---|---|
| `ux-cognitive-architect` | Phase 1 — Diagnose: psychology, behavior, cognitive laws | All |
| `ux-designer-skill` (szilu) | Phase 2 — Architect: WCAG, IA, interaction patterns, forms, mobile, ethical design | All |
| `ui-ux-pro-max` | Phase 2+3 — Design system generation: 161 palettes, 57 font pairings, 10 stacks | Claude Code / Desktop |
| `frontend-design` / `frontend-design-multiplatform` | Phase 3 — Anti-generic aesthetics, intentional visual direction | All |
| `mobile-app-ui-design` (ceorkm) | Phase 3 (mobile) — Mobile-specific patterns: touch, gestures, emotion | Mobile targets |
| `interface-design` (dammyjay93) | Phase 3 (tools/dashboards) — Domain exploration, layered hierarchy | Dashboards/admin |
| `web-design-guidelines` (vercel-labs) | Phase 3 (web) — Spacing, typography, interaction, accessibility compliance | Web/Vercel stack |
| `impeccable` (pbakaus) | Phase 5 — Polish, audit, critique, anti-pattern detection | Claude Code / Desktop |

**If a skill listed above is not installed**, skip it and note the gap at the end of
your response. Never fabricate its output.

---

## Platform Detection — Step 0 (Always First)

Before running any phase, identify the platform:

| Signal | Platform | Code Delivery Format |
|---|---|---|
| claude.ai web/desktop app | **Claude Desktop** | React `.jsx` artifact or HTML artifact |
| `claude` CLI, `.claude/skills/` present | **Claude Code CLI** | Component files + CSS, skill CLI tools available |
| Google Gemini interface | **Gemini Advanced** | Single copy-paste HTML block |
| ChatGPT / OpenAI interface | **ChatGPT** | Single copy-paste HTML block |
| `codex` CLI, OpenAI Codex env | **OpenAI Codex** | Separate `.jsx` + `.css` files |

Record the platform. It affects Phase 4 delivery only. All other phases are platform-agnostic.

---

## The 5-Phase Pipeline

Every design request — no exceptions — runs all five phases in order.
Never skip. Never reorder. Never merge phases to save space.

---

### PHASE 1 — DIAGNOSE
*Skill: `ux-cognitive-architect`*

Run the full cognitive diagnostic before any layout or code:

**1A. Persona & Goals**
- Who is the user? (novice/expert, device, emotional state, context)
- End Goal — what outcome are they completing?
- Experience Goal — how do they want to feel?

**1B. Six Minds Assessment** (mark which are critical for this problem)
- Vision/Attention — what draws the eye first? Is hierarchy clear?
- Wayfinding — can the user orient themselves?
- Memory — does this match existing mental models?
- Language — does terminology match user vocabulary?
- Decision Making — how many micro-decisions? Are advanced options hidden?
- Emotion — Appeal → Enhance → Awaken

**1C. Norman's Three Levels**
- Visceral (aesthetic first impression)
- Behavioral (usability, feedback, expectations)
- Reflective (long-term self-image, does the product make them feel capable?)

**1D. Hook Loop** (only if the product requires repeated engagement)
- Trigger → Action → Variable Reward → Investment

**Output of Phase 1:** A written diagnostic. No code yet.

---

### PHASE 2 — ARCHITECT
*Skills: `ux-designer-skill` + `ui-ux-pro-max`*

Translate the diagnostic into structural decisions.

**2A. Layout Strategy** (from `ux-designer-skill`)
- Information Architecture: what hierarchy does the content need?
- Navigation pattern: tab bar / sidebar / hamburger / breadcrumb?
- Interaction design: modals, tooltips, drag-drop — which patterns apply?
- Accessibility: WCAG 2.2 AA requirements for this interface
- If mobile target: apply mobile-first touch patterns, safe areas, gesture conflicts
- If form-heavy: field grouping, inline validation, error recovery strategy
- If ethical concern exists (dark patterns, GDPR): flag it explicitly

**2B. Design System Selection** (from `ui-ux-pro-max`, if installed)
- Run mental equivalent of `--design-system` for the product type
- State: product type, recommended style, color family, font pairing, stack
- If `ui-ux-pro-max` not installed: derive from `ux-cognitive-architect` HSL logic

**2C. Apply UX Laws**
- Hick's Law: max 5–7 nav items, progressive disclosure for advanced options
- Fitts's Law: primary CTA large + thumb-reachable, destructive actions separated
- Jakob's Law: use established conventions, flag any intentional deviation
- Tesler's Law: list every complexity point absorbed by the design
- Gestalt: specify proximity groupings, similarity rules, closure technique

**Output of Phase 2:** Architecture spec. Layout described in words and/or ASCII wireframe. Still no code.

---

### PHASE 3 — SPECIFY
*Skills: `frontend-design-multiplatform` + platform-specific skills*

Define the exact visual parameters.

**3A. Aesthetic Direction** (from `frontend-design` / `frontend-design-multiplatform`)
- Choose a deliberate aesthetic — name it (e.g., "editorial minimalism", "warm utility", "technical precision")
- Explicitly reject generic AI defaults: no Inter-everywhere, no purple-blue gradients, no nested card soup
- Font choice must be intentional — state why this typeface for this product
- Color must have a rationale — state the emotional/brand logic

**3B. Platform-Specific Patterns**
- Mobile target → apply `mobile-app-ui-design`: Peak-End Rule, haptic moments, gesture affordances
- Dashboard/admin → apply `interface-design`: domain exploration, whisper-quiet elevation, token architecture
- Web/Vercel stack → apply `web-design-guidelines`: spacing, interaction, accessibility compliance

**3C. Granular Specs** (from `ux-cognitive-architect`)

*Spacing — 8px grid only:*
Values: 4, 8, 12, 16, 24, 32, 48, 64, 96px. No arbitrary numbers.
Space around a group ≥ 1.5× space within it.

*Typography scale:*
| Role | Size | Weight |
|---|---|---|
| Display/H1 | 32–48px | 700–800 |
| H2 | 24–28px | 600–700 |
| H3 | 18–20px | 600 |
| Body | 16px | 400 |
| Caption | 14px | 400 |
| Label | 12px | 500 |

*Color — HSL only:*
```
Primary:    hsl(H, 70%, 50%)
Hover:      hsl(H, 75%, 44%)
Pressed:    hsl(H, 80%, 38%)
Disabled:   hsl(H, 30%, 70%)
Background: hsl(H, 10%, 97%)
Text:       hsl(H, 15%, 15%)
Muted:      hsl(H, 10%, 55%)
Error:      hsl(0, 70%, 50%)
Success:    hsl(142, 65%, 42%)
```

*Shadows — 4 elevation levels:*
```css
/* L1 Button */   box-shadow: 0 1px 3px hsla(0,0%,0%,0.10), 0 1px 2px hsla(0,0%,0%,0.06);
/* L2 Dropdown */ box-shadow: 0 4px 6px hsla(0,0%,0%,0.07), 0 2px 4px hsla(0,0%,0%,0.06);
/* L3 Card */     box-shadow: 0 10px 15px hsla(0,0%,0%,0.08), 0 4px 6px hsla(0,0%,0%,0.05);
/* L4 Modal */    box-shadow: 0 25px 50px hsla(0,0%,0%,0.18), 0 12px 20px hsla(0,0%,0%,0.10);
```

**Output of Phase 3:** Complete visual spec. Typography, palette, spacing values, shadow levels. Named aesthetic direction.

---

### PHASE 4 — BUILD
*Skills: `frontend-design-multiplatform` + `ui-ux-pro-max` stack guidance*

Deliver production-ready code using every spec from Phases 1–3.

**Pre-build checklist — verify before writing a single line:**
- [ ] All spacing on 8px grid
- [ ] Typography matches the scale
- [ ] Colors in HSL
- [ ] Touch targets ≥ 44px (mobile) / 48dp (Android)
- [ ] Primary CTA is visually dominant
- [ ] Nav ≤ 7 items
- [ ] Hover + focus states defined
- [ ] Destructive actions separated from primary
- [ ] No generic AI aesthetics (Inter/purple-blue/nested cards)

**Delivery format by platform:**

*Claude Desktop*
→ React `.jsx` artifact with Tailwind. Inline styles for HSL values only.
→ No `localStorage`/`sessionStorage`. State via `useState`/`useReducer`.

*Claude Code CLI*
→ Component files: `ComponentName.jsx` + `ComponentName.css`
→ Run `ui-ux-pro-max` search script if design system lookup needed
→ Export as default, props with sensible defaults

*Gemini Advanced / ChatGPT*
→ Single self-contained HTML file, CSS + JS embedded
→ CDN from cdnjs.cloudflare.com only
→ Inline comments on key design decisions

*OpenAI Codex*
→ Separate `.jsx` + `.css` files
→ Props with defaults, export default

---

### PHASE 5 — POLISH + AUDIT
*Skill: `impeccable` (pbakaus)*

Run after build. If `impeccable` is not installed, run the manual checklist below.

**If `impeccable` is installed (Claude Code / Desktop):**
- Run `/impeccable audit` — technical quality: accessibility, contrast, focus states, anti-patterns
- Run `/impeccable critique` — UX review: visual hierarchy, information architecture, emotional resonance
- Run `/impeccable polish` — final pass: tighten spacing, sharpen type, clean edges

**If `impeccable` is NOT installed — manual audit:**

Anti-pattern checklist (flag any present):
- [ ] Inter as the only font — replace with intentional choice
- [ ] Purple-to-blue gradient as hero — replace with brand-specific palette
- [ ] Cards nested inside cards — flatten hierarchy
- [ ] Gray text on colored background — check contrast ratio (≥ 4.5:1 WCAG AA)
- [ ] No visible focus state — add `:focus-visible` ring
- [ ] Touch targets < 44px — enlarge
- [ ] Emoji used as navigation icons — replace with SVG
- [ ] Destructive action adjacent to primary CTA — separate with distance or visual weight

**Output of Phase 5:** Audit report with specific line-level fixes. P0 (must fix) → P3 (nice to have) severity ratings.

---

## Skill Gap Reporting

At the end of every response, output a brief gap report:

```
SKILLS USED:         [list which skills were applied]
SKILLS MISSING:      [list any skill from the stack not installed that would have added value]
MANUAL FALLBACKS:    [note where you substituted built-in knowledge for a missing skill]
```

This keeps the user informed about what to install next.

---

## Quick Decision Tree

```
User request arrives
       │
       ▼
Is this a POLISH / AUDIT request only?
  YES → Skip to Phase 5 (impeccable)
  NO  ↓

Is this a BUILD-ONLY request (user already has specs)?
  YES → Start at Phase 4, reference their specs
  NO  ↓

Run full pipeline: Phase 1 → 2 → 3 → 4 → 5
```

---

## Law Reference Card

| Law | Rule |
|---|---|
| Hick's | Fewer choices = faster decisions |
| Fitts's | Bigger + closer = easier to hit |
| Jakob's | Match what users already know |
| Tesler's | Absorb complexity, never pass to user |
| Krug | Users scan. Design for first good-enough target |
| Gestalt | Proximity, similarity, closure |
| Norman | Visceral → Behavioral → Reflective |
| Fogg | Behavior = Motivation + Ability + Prompt |
| Peak-End | Users remember the peak moment and the ending |
| Clarity > Consistency | Always choose the clearer option |

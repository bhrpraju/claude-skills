---
name: ux-cognitive-architect
description: >
  Elite UX/UI design AI that applies cognitive psychology, behavioral economics, and
  production-grade visual design laws to every interface decision. ALWAYS trigger this
  skill when the user asks to: design a screen, evaluate a UI, build a layout, review
  a wireframe, write design specs, suggest improvements to an interface, create a
  component, design an onboarding flow, build a dashboard, or asks "how should this
  look", "is this UX good", "improve this design", "what's wrong with this UI", or
  describes a product and asks how users will experience it. Also trigger for any
  mention of: user experience, UX audit, conversion optimization, design system,
  color palette, typography, spacing, Figma prompt, Canva layout, Tailwind component,
  React UI, or cognitive load. Produces output in a structured 4-stage sequence:
  Cognitive Diagnostic → Structural Architecture → Granular UI Specs → Builder Blueprint.
  Works across Claude Desktop, Gemini Advanced, OpenAI Codex, and ChatGPT.
---

# UX Cognitive Architect

A world-class UX/UI design skill grounded in human cognitive psychology, behavioral economics, and production-ready visual design laws. Every design decision traces back to how the human brain actually works.

---

## Step 0 — Platform Detection

Identify your platform before generating any output:

| Platform | Signal | Output Format |
|---|---|---|
| **Claude Desktop** | claude.ai web/desktop | Artifacts (React/HTML), inline specs |
| **Gemini Advanced** | Google Gemini interface | Markdown specs + copy-paste code blocks |
| **OpenAI Codex / ChatGPT** | ChatGPT or Codex CLI | Markdown specs + copy-paste code blocks |

Platform affects **how** you deliver code. The design frameworks below apply **universally on every platform**.

---

## Step 1 — Cognitive Diagnostic

Before touching layout or code, diagnose the human problem.

### 1A. Define the Persona & Goals

Answer these three questions explicitly:

1. **Who is the user?** (novice vs. expert, emotional state, device, context of use)
2. **End Goal** — What outcome are they trying to achieve? (e.g., "book a flight")
3. **Experience Goal** — How do they want to *feel* while doing it? (e.g., "confident, not confused")

### 1B. Apply the Six Minds Checklist

Evaluate the design against all six simultaneously:

| Mind | Question to Answer |
|---|---|
| **Vision / Attention** | What is the first thing the eye lands on? Does visual hierarchy guide the user to the most important element, or is the screen too dense? |
| **Wayfinding** | Can the user tell where they are, where they came from, and where to go next? |
| **Memory** | Does this match mental models from other apps the user already knows (Jakob's Law)? Are you forcing them to learn a new pattern? |
| **Language** | Is the terminology matched to the user's vocabulary level? No system jargon for novices. |
| **Decision Making** | How many micro-decisions are required? Are advanced choices hidden until needed? |
| **Emotion** | Appeal (immediate visual pull) → Enhance (daily value) → Awaken (deeper life goal or fear relief) |

### 1C. Norman's Three Levels

| Level | Design Obligation |
|---|---|
| **Visceral** | Immediate aesthetic reaction. Design for calm, not anxiety. Use proper visual hierarchy and spacing. |
| **Behavioral** | Usability and expectations. Every action must provide immediate feedback. Never break learned patterns. |
| **Reflective** | Long-term self-image. Does the product make the user feel smart, capable, or part of something? |

### 1D. Hook Loop (only for retention-required products)

If the product needs repeated return visits, define:

- **Trigger** → External (notification/badge) attached to Internal (boredom, FOMO, anxiety)
- **Action** → Apply Fogg: Behavior = Motivation + Ability + Prompt. Make the action effortless.
- **Variable Reward** → Tribe (social), Hunt (search/discovery), or Self (mastery/completion)
- **Investment** → What data/preference does the user input that improves their next session?

---

## Step 2 — Structural Architecture

Translate the cognitive diagnosis into layout decisions.

### Apply These Laws Explicitly

**Hick's Law** — Time to decide grows with number of choices.
- Maximum 5–7 items in any navigation or menu.
- Progressive disclosure: hide advanced options behind "More" or secondary screens.
- Group complex choices into smaller, sequential categories.

**Fitts's Law** — Time to hit a target grows with distance and shrinks with size.
- Primary CTA: large, thumb-reachable (bottom 40% of mobile screen).
- Destructive actions (delete, cancel): never adjacent to primary actions.
- Touch targets minimum 44×44px (Apple HIG) / 48×48dp (Material).

**Jakob's Law** — Users expect your site to work like every other site.
- Use established conventions: hamburger for mobile nav, cart icon top-right, search top-center.
- Do not reinvent unless there is a genuine cognitive gain.

**Tesler's Law** — Complexity is conserved. Designer absorbs it so users don't have to.
- Every form field that can be pre-filled, should be.
- Every decision that can be defaulted intelligently, should be.

**Gestalt Principles**
- **Proximity**: Group related elements. Space between groups must be visibly larger than space within groups.
- **Similarity**: Related actions must look identical (same button style, same icon family).
- **Closure**: Use alignment and implied borders, not heavy boxes, to create sections.

**Satisficing (Krug)** — Users pick the first "good enough" option, not the optimal one.
- Design for scanning: bold headings, short bullets, obvious tap targets.
- Never bury the primary action in a wall of text.

---

## Step 3 — Granular UI Specs

### Spacing: The 8px Grid
Use only these values for all padding, margin, gap: **4, 8, 12, 16, 24, 32, 48, 64, 96px**
- Never use arbitrary values like 11px, 17px, 23px.
- Start with too much whitespace. Tighten only if the layout feels wasteful.
- The space *around* a group must be at least 1.5× the space *within* it.

### Typography Scale
Use a modular scale (ratio ≈ 1.25 or 1.333):

| Role | Size | Weight | Color Lightness |
|---|---|---|---|
| Display / H1 | 32–48px | 700–800 | 90–95% (near black on light) |
| H2 | 24–28px | 600–700 | 85–90% |
| H3 | 18–20px | 600 | 80–85% |
| Body | 16px | 400 | 70–80% |
| Secondary / Caption | 14px | 400 | 50–60% (softer) |
| Label / Micro | 12px | 500 | 50–60% |

- Use **px or rem only**. Never `em` for padding (causes cascading fractional pixels).
- Hierarchy via **weight and color contrast first**, size second.

### Color: HSL Logic
```
Primary:    hsl(H, 70%, 50%)
Hover:      hsl(H, 75%, 44%)   ← lower lightness, slightly higher saturation
Pressed:    hsl(H, 80%, 38%)
Disabled:   hsl(H, 30%, 70%)   ← low saturation signals inactive
Background: hsl(H, 10%, 97%)   ← near white, slight hue tint
Surface:    hsl(H, 8%, 100%)
Text/Dark:  hsl(H, 15%, 15%)
Muted text: hsl(H, 10%, 55%)
Error:      hsl(0, 70%, 50%)
Success:    hsl(142, 65%, 42%)
```
Rule: When darkening a color, **lower lightness AND increase saturation**. Colors lose intensity near black.

### Elevation / Shadow System
Consistent light source: top-left, 15° angle.

```css
/* Level 1 — Button, chip */
box-shadow: 0 1px 3px hsla(0,0%,0%,0.10), 0 1px 2px hsla(0,0%,0%,0.06);

/* Level 2 — Dropdown, tooltip */
box-shadow: 0 4px 6px hsla(0,0%,0%,0.07), 0 2px 4px hsla(0,0%,0%,0.06);

/* Level 3 — Card */
box-shadow: 0 10px 15px hsla(0,0%,0%,0.08), 0 4px 6px hsla(0,0%,0%,0.05);

/* Level 4 — Modal / Drawer */
box-shadow: 0 25px 50px hsla(0,0%,0%,0.18), 0 12px 20px hsla(0,0%,0%,0.10);
```

### Clarity Trumps Consistency
If making one element slightly inconsistent makes it dramatically clearer, choose clarity. Consistency is a means, not the goal.

---

## Step 4 — Builder Blueprint

Output production-ready code using the specs from Steps 1–3.

### Platform-Specific Delivery

**Claude Desktop**
- Deliver as a React `.jsx` artifact or HTML artifact.
- Use Tailwind utility classes where possible.
- Inline styles only for HSL values not expressible in standard Tailwind.
- Do not use `localStorage` or `sessionStorage` in artifacts (not supported in claude.ai).
- Use `useState`/`useReducer` for all state.

**Gemini Advanced / ChatGPT**
- Deliver as a standalone HTML file with embedded CSS and JS.
- No external dependencies unless from a CDN (cdnjs.cloudflare.com preferred).
- Wrap all code in a single copy-paste block.
- Include brief inline comments on key design decisions.

**OpenAI Codex**
- Deliver as React component files.
- Separate concerns: `ComponentName.jsx` + `ComponentName.css`.
- Export as default.
- Props with sensible defaults.

### Code Quality Checklist (before outputting)
- [ ] All spacing values on the 8px grid
- [ ] Typography follows the scale above
- [ ] Colors expressed in HSL
- [ ] Touch targets ≥ 44px
- [ ] Primary CTA is the visually dominant element
- [ ] No more than 7 items in any nav/menu
- [ ] Hover and focus states defined
- [ ] Destructive actions separated from primary actions

---

## Output Sequence (mandatory)

Every response must follow this order:

```
1. COGNITIVE DIAGNOSTIC
   → Persona | End Goal | Experience Goal
   → Six Minds assessment (which are critical for this problem)
   → Hook Loop (if retention is required)

2. STRUCTURAL ARCHITECTURE
   → Layout strategy
   → Hick's / Fitts's / Jakob's application
   → Gestalt groupings

3. GRANULAR UI SPECS
   → Typography scale for this design
   → Spacing values used
   → HSL color palette
   → Shadow levels used

4. BUILDER BLUEPRINT
   → Production-ready code (platform-appropriate format)
```

---

## Quick Reference — Laws at a Glance

| Law | Core Rule |
|---|---|
| Hick's | Fewer choices = faster decisions. Progressive disclosure. |
| Fitts's | Bigger + closer = easier to hit. |
| Jakob's | Match what users already know. |
| Tesler's | Absorb complexity. Never pass it to the user. |
| Krug | Users scan, not read. Design for the first good-enough target. |
| Gestalt | Group by proximity, similarity, and closure. |
| Norman | Visceral → Behavioral → Reflective. Design for all three. |
| Fogg | Behavior = Motivation + Ability + Prompt. |
| Clarity > Consistency | If in doubt, choose the clearer option. |

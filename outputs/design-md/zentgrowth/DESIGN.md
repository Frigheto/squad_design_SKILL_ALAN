---

```markdown
---
name: "Zent Growth"
colors:
  primary: "#6366f1"                          # from --color-primary (brand identity, hero CTA)
  secondary: "#8b5cf6"                        # from --color-secondary (accent actions)
  tertiary: "#a855f7"                         # from --color-tertiary (decorative accents)
  neutral: "#6b7280"                          # from --color-neutral (secondary text)
  surface: "#ffffff"                          # from --color-surface (default background)
  text: "#1f2937"                             # from --color-text (body text)
  text-muted: "#9ca3af"                       # from --color-text-muted (labels, captions)
  border: "#e5e7eb"                           # from --color-border (dividers, hairlines)
  error: "#ef4444"                            # from --color-error (validation, alerts)
  success: "#10b981"                          # from --color-success (positive feedback)
  # Extended named tokens
  slate: "#64748b"                            # from --color-slate
  gray: "#d1d5db"                             # from --color-gray
  indigo: "#4f46e5"                           # from --color-indigo
  violet: "#7c3aed"                           # from --color-violet
  pink: "#ec4899"                             # from --color-pink

typography:
  display-hero:
    fontFamily: "Inter, system-ui, -apple-system, sans-serif"             # from @font-face Inter
    fontSize: "3.75rem"                                                     # from h1 in hero
    fontWeight: 700                                                         # from h1 weight declaration
    lineHeight: "1.1"                                                       # from h1 line-height
    letterSpacing: "-0.02em"                                                # from display tracking
    features: "'ss01'"                                                      # stylistic set 1 for Premium feel
  display-large:
    fontFamily: "Inter, system-ui, -apple-system, sans-serif"
    fontSize: "3rem"
    fontWeight: 700
    lineHeight: "1.15"
    letterSpacing: "-0.015em"
    features: "'ss01'"
  section-heading:
    fontFamily: "Inter, system-ui, -apple-system, sans-serif"
    fontSize: "2rem"
    fontWeight: 700
    lineHeight: "1.2"
    letterSpacing: "-0.01em"
    features: "'ss01'"
  subheading-large:
    fontFamily: "Inter, system-ui, -apple-system, sans-serif"
    fontSize: "1.5rem"
    fontWeight: 600
    lineHeight: "1.3"
    letterSpacing: "0em"
  subheading:
    fontFamily: "Inter, system-ui, -apple-system, sans-serif"
    fontSize: "1.25rem"
    fontWeight: 600
    lineHeight: "1.35"
    letterSpacing: "0em"
  body-large:
    fontFamily: "Inter, system-ui, -apple-system, sans-serif"
    fontSize: "1.125rem"
    fontWeight: 400
    lineHeight: "1.5"
    letterSpacing: "0em"
  body:
    fontFamily: "Inter, system-ui, -apple-system, sans-serif"
    fontSize: "1rem"
    fontWeight: 400
    lineHeight: "1.5"
    letterSpacing: "0em"
  body-small:
    fontFamily: "Inter, system-ui, -apple-system, sans-serif"
    fontSize: "0.875rem"
    fontWeight: 400
    lineHeight: "1.5"
    letterSpacing: "0em"
  button:
    fontFamily: "Inter, system-ui, -apple-system, sans-serif"
    fontSize: "1rem"
    fontWeight: 600
    lineHeight: "1.4"
    letterSpacing: "0em"
  button-small:
    fontFamily: "Inter, system-ui, -apple-system, sans-serif"
    fontSize: "0.875rem"
    fontWeight: 600
    lineHeight: "1.4"
    letterSpacing: "0em"
  link:
    fontFamily: "Inter, system-ui, -apple-system, sans-serif"
    fontSize: "1rem"
    fontWeight: 500
    lineHeight: "1.5"
    letterSpacing: "0em"
  caption:
    fontFamily: "Inter, system-ui, -apple-system, sans-serif"
    fontSize: "0.75rem"
    fontWeight: 400
    lineHeight: "1.4"
    letterSpacing: "0em"
  caption-small:
    fontFamily: "Inter, system-ui, -apple-system, sans-serif"
    fontSize: "0.625rem"
    fontWeight: 400
    lineHeight: "1.4"
    letterSpacing: "0em"
  code-body:
    fontFamily: "'JetBrains Mono', 'Courier New', monospace"              # from @font-face JetBrains Mono
    fontSize: "0.875rem"
    fontWeight: 400
    lineHeight: "1.5"
    letterSpacing: "0em"
    features: "'liga' 0, 'calt' 0"

rounded:
  none: "0px"                                 # from --radius-none
  xs: "2px"                                   # from --radius-xs
  sm: "4px"                                   # from --radius-sm
  md: "6px"                                   # from --radius-md
  lg: "8px"                                   # from --radius-lg
  xl: "12px"                                  # from --radius-xl
  full: "9999px"                              # from --radius-full

spacing:
  xs: "4px"                                   # from --space-xs
  sm: "8px"                                   # from --space-sm
  md: "16px"                                  # from --space-md
  lg: "24px"                                  # from --space-lg
  xl: "32px"                                  # from --space-xl
  2xl: "48px"                                 # from --space-2xl

preview_tokens:
  button_primary_bg: "#6366f1"
  button_primary_text: "#ffffff"
  button_primary_border: "#6366f1"
  button_secondary_bg: "transparent"
  button_secondary_text: "#6366f1"
  button_secondary_border: "#6366f1"
  button_tertiary_text: "#6366f1"
  surface_bg: "#ffffff"
  card_bg: "#f9fafb"
  text: "#1f2937"
  text_muted: "#9ca3af"
  border: "#e5e7eb"
  accent: "#8b5cf6"
  button_radius: "6px"
  card_radius: "8px"
  input_radius: "6px"

components:
  button-primary:
    bg: "#6366f1"
    text: "#ffffff"
    border: "#6366f1"
    radius: "6px"
    padding: "10px 24px"
    font: "1rem Inter weight 600"
    hover_bg: "#4f46e5"
  button-primary-hover:
    bg: "#4f46e5"
    text: "#ffffff"
  button-secondary:
    bg: "transparent"
    text: "#6366f1"
    border: "#6366f1"
    radius: "6px"
    padding: "10px 24px"
    font: "1rem Inter weight 600"
    hover_bg: "#f0f4ff"
  button-ghost:
    bg: "transparent"
    text: "#1f2937"
    border: "transparent"
    radius: "6px"
    padding: "10px 24px"
    font: "1rem Inter weight 600"
  card:
    bg: "#ffffff"
    border: "#e5e7eb"
    radius: "8px"
    shadow: "0px 1px 3px rgba(0,0,0,0.08), 0px 4px 12px rgba(0,0,0,0.06)"
    padding: "24px"
  input-text:
    bg: "#ffffff"
    text: "#1f2937"
    border: "#e5e7eb"
    radius: "6px"
    padding: "8px 12px"
    focus_border: "#6366f1"
  badge-default:
    bg: "#f3f4f6"
    text: "#1f2937"
    border: "#e5e7eb"
    radius: "4px"
    padding: "4px 8px"
    font: "0.75rem Inter weight 500"
  nav-header:
    bg: "#ffffff"
    text: "#1f2937"
    border_bottom: "#e5e7eb"
    backdrop_filter: "none"
    height: "64px"
---

## 1. Visual Theme & Atmosphere

Zent Growth embodies a modern, forward-thinking tech aesthetic rooted in indigo-to-violet chromatics. The design system prioritizes clarity through generous whitespace, refined typography hierarchy using Inter's geometric neutrality, and restrained use of accent colors for critical moments. The palette shifts from cool indigo (`#6366f1`) as the primary brand voice to warmer violets (`#7c3aed`) and pinks (`#ec4899`) as secondary energizers — a deliberate choice that softens the tech vernacular while maintaining professionalism.

Typography operates on two weights: 700 for headlines (commanding presence), 400-600 for everything else (conversational ease). Display text is tracked tight (`-0.02em`), reinforcing premium positioning. Buttons are set at 600 weight to signal interactivity without aggression.

Depth is achieved through subtle shadows and surface-color contrast rather than layered elevation. Borders are soft (`#e5e7eb` at 1px), and cards sit on minimal lift — this creates a "calm tech" feel that invites exploration without overwhelming. The system reserves rounded corners for medium utility (6-8px), avoiding both sharp edges and excessive soft-corner warmth.

**Key Characteristics:**
- Cool indigo-to-violet palette with pink accent warmth
- Inter typeface: geometric, professional, accessible
- Tight leading on display text for premium density
- Soft shadows and border contrast over depth layers
- Minimal rounding: cards at 8px, buttons at 6px
- 1px hairline borders in cool gray
- Generous padding: buttons 10/24px, cards 24px
- Focus rings at primary indigo for accessibility

---

## 2. Color Palette & Roles

### Primary
- **Indigo** (`#6366f1`): Brand identity. Used on primary CTAs ("Get Started", "Sign Up"), focus rings, and the header accent band. This is the brand's anchor — derived from the Zent Growth logo color and hero gradient start point. Sparingly deployed across the page to maintain visual weight.

### Secondary & Brand
- **Violet** (`#7c3aed`): Secondary action color. Appears on hover states, badge accents, and gradient ingredients. Warmer than primary, signaling "explore further" without being primary-level demand.
- **Pink** (`#ec4899`): Tertiary accent. Used in gradient overlays, decorative section backgrounds, and callouts. Adds warmth and contemporary energy.

### Neutral Scale
- **Slate** (`#1f2937`): Default body text. Deep, warm-leaning gray that reads friendly at 16px.
- **Neutral Gray** (`#9ca3af`): Muted labels, helper text, secondary information. High enough contrast for WCAG AA on white.
- **Light Gray** (`#f9fafb`): Card background. Just barely off-white, creating lift without starkness.
- **Hairline Border** (`#e5e7eb`): 1px dividers between sections and card edges.

### Interactive
- **Primary Hover** (`#4f46e5`): Deeper indigo used on `:hover` for primary buttons. Shift is ≈7% darker in lightness.
- **Secondary Hover** (`#f0f4ff`): Pale indigo tint for ghost/outlined secondary buttons on hover.

### Error & Validation
- **Error** (`#ef4444`): Alert red used for form validation, critical notifications.
- **Success** (`#10b981`): Teal-green for positive feedback (form submission, successful action).

### Color Philosophy
The palette is rooted in tech cool (indigo is the industry standard for trust), but softened by violet and pink to avoid sterility. Indigo appears at brand moments (logo, CTA) and critical interactions (focus), but the majority of UI is neutral gray — this restraint makes indigo feel intentional rather than pervasive. The 60% neutral / 30% indigo / 10% accent ratio reflects a "calm tech" philosophy: data and content foreground, brand color punctuation.

---

## 3. Typography Rules

### Font Family
- **Primary:** Inter (system-ui fallback chain: -apple-system, BlinkMacSystemFont, San Francisco). Self-hosted via @font-face with weight 400, 500, 600, 700.
- **Monospace:** JetBrains Mono for code blocks, terminal-style content. Features: `'liga' 0, 'calt' 0` to disable ligatures (code clarity).
- **OpenType Features:** Display text (h1-h3) uses `'ss01'` (stylistic set 1) to enable Inter's premium alternate letterforms (tighter, more geometric).

### Hierarchy

| Role | Font | Size | Weight | Line Height | Letter Spacing | Features | Notes |
|------|------|------|--------|-------------|---|----------|-------|
| Display Hero | Inter | 3.75rem | 700 | 1.1 | -0.02em | ss01 | Page-top headline; ultra-tight track for density |
| Display Large | Inter | 3rem | 700 | 1.15 | -0.015em | ss01 | Hero subheading or section open |
| Section Heading | Inter | 2rem | 700 | 1.2 | -0.01em | ss01 | Major content dividers |
| Subheading Large | Inter | 1.5rem | 600 | 1.3 | 0em | — | Feature highlights |
| Subheading | Inter | 1.25rem | 600 | 1.35 | 0em | — | Card titles |
| Body Large | Inter | 1.125rem | 400 | 1.5 | 0em | — | Introductory paragraph |
| Body | Inter | 1rem | 400 | 1.5 | 0em | — | Default body text |
| Body Small | Inter | 0.875rem | 400 | 1.5 | 0em | — | Descriptions, secondary content |
| Button | Inter | 1rem | 600 | 1.4 | 0em | — | Primary button label |
| Button Small | Inter | 0.875rem | 600 | 1.4 | 0em | — | Compact button, badge links |
| Link | Inter | 1rem | 500 | 1.5 | 0em | — | Inline/nav links |
| Caption | Inter | 0.75rem | 400 | 1.4 | 0em | — | Metadata, timestamps |
| Caption Small | Inter | 0.625rem | 400 | 1.4 | 0em | — | Fine print |
| Code | JetBrains Mono | 0.875rem | 400 | 1.5 | 0em | liga:0, calt:0 | Inline code, code blocks |

### Principles
- **Weight 700 for declaration:** Headline weight signals importance. Never use 700 for body text — it reads heavy and corporate.
- **Tight leading on display:** Line-height 1.1–1.15 on display (h1-h2) maintains premium density. Body uses 1.5 for readability.
- **Negative letter-spacing at display scale:** `-0.02em` at 3.75rem makes type feel contemporary and intentional, not algorithmic.
- **600 weight for UI elements:** Buttons, links, and badges use 600 to stand out without screaming. This is the "action weight."
- **Feature flags on display:** `'ss01'` on headlines only — this keeps rendering cost low while adding a design flourish.

---

## 4. Components

### Buttons

**Primary Indigo** (`button-primary`)
- Background: `#6366f1`
- Text: `#ffffff` (white)
- Border: `#6366f1` (same as background, no outline)
- Padding: 10px 24px (vertical × horizontal)
- Radius: 6px
- Font: 1rem Inter weight 600
- Hover: Background shifts to `#4f46e5` (deeper indigo); text stays white
- Use: Primary call-to-action ("Start Now", "Get Started", "Sign Up")

**Secondary Outlined** (`button-secondary`)
- Background: Transparent
- Text: `#6366f1` (indigo)
- Border: `#6366f1` (1px, inferred)
- Padding: 10px 24px
- Radius: 6px
- Font: 1rem Inter weight 600
- Hover: Background becomes `#f0f4ff` (pale indigo wash); text stays indigo
- Use: Secondary action ("Learn More", "Explore", "View Docs")

**Ghost** (`button-ghost`)
- Background: Transparent
- Text: `#1f2937` (dark slate)
- Border: Transparent
- Padding: 10px 24px
- Radius: 6px
- Font: 1rem Inter weight 600
- Hover: Minimal visual change (text may lighten slightly)
- Use: Tertiary actions in navigation, footers, or low-priority contexts

### Cards & Containers

**Card** (`card`)
- Background: `#ffffff` (white)
- Border: `#e5e7eb` (1px soft gray)
- Radius: 8px
- Shadow: `0px 1px 3px rgba(0,0,0,0.08), 0px 4px 12px rgba(0,0,0,0.06)` (two-layer lift: ambient + directional)
- Padding: 24px (internal spacing)
- Use: Feature blocks, testimonials, pricing tiers, resource lists

### Inputs & Forms

**Text Input** (`input-text`)
- Background: `#ffffff` (white)
- Text: `#1f2937` (slate)
- Border: `#e5e7eb` (1px default)
- Radius: 6px
- Padding: 8px 12px (vertical × horizontal, comfortable for touch)
- Focus Border: `#6366f1` (indigo, 2px inferred)
- Font: 1rem Inter weight 400
- Use: Email fields, search, form input

### Badges & Tags

**Badge Default** (`badge-default`)
- Background: `#f3f4f6` (very light gray)
- Text: `#1f2937` (slate)
- Border: `#e5e7eb` (1px subtle outline)
- Radius: 4px (smaller than buttons)
- Padding: 4px 8px (tight, compact)
- Font: 0.75rem Inter weight 500
- Use: Category labels, status indicators ("New", "Beta", "Featured")

### Navigation

**Header Navigation** (`nav-header`)
- Background: `#ffffff` (white)
- Text: `#1f2937` (slate)
- Border Bottom: `#e5e7eb` (1px divider)
- Height: 64px (comfortable for touch targets)
- Backdrop Filter: None (solid background, no blur)
- Font: 1rem Inter weight 500 (links)
- Use: Sticky top bar with logo, nav links, CTA button

### Decorative Elements
The system uses subtle horizontal dividers (`#e5e7eb`, 1px) between major sections. Gradient accents (indigo → violet → pink) appear in hero backgrounds and callout boxes, but are never applied to text (accessibility). Focus rings are 2px indigo with minimal padding, following WCAG AAA standards.

---

## 5. Layout Principles

### Spacing System
Base unit: **4px**. All spacing increments are multiples of 4:
- xs: 4px
- sm: 8px
- md: 16px
- lg: 24px
- xl: 32px
- 2xl: 48px

Apply this scale consistently: padding, margin, gaps between elements. Buttons use lg (24px) horizontal padding, cards use lg (24px) internal padding, sections use 2xl (48px) vertical margin.

### Grid & Container
- **Max Width:** 1280px (inferred from hero-section analysis)
- **Hero Pattern:** Full-width gradient background with centered text (white on indigo-to-violet gradient)
- **Card Grid:** 3 columns on desktop (pricing, features), 1 column on mobile
- **Padding:** 16px horizontal margin on mobile, 24px on tablet, no horizontal margin on desktop (reaches max-width container)

### Whitespace Philosophy
Whitespace is the primary visual breathing tool. Section spacing (vertical margin between features, testimonials, CTA blocks) is generous — typically 48px or more — to avoid visual fatigue. This aligns with "calm tech" positioning: the design prioritizes content legibility and visual rest over density. Cards float on white with 1px borders and soft shadows, creating micro-whitespace via elevation rather than aggressive spacing.

### Border Radius Scale
- **0px (none):** Disabled states, legacy elements (rare)
- **2px (xs):** Fine-detail dividers, minute UI (barely used)
- **4px (sm):** Badges, compact pill shapes
- **6px (md):** Buttons, input fields — the workhorse radius
- **8px (lg):** Cards, larger containers
- **12px (xl):** Feature blocks, hero sections (rare)
- **9999px (full):** Not used (no pill buttons or circular avatars in current design)

---

## 6. Depth & Elevation

| Level | Treatment | Use |
|-------|-----------|-----|
| Flat | No shadow, border only (`#e5e7eb`) | Dividers, hairlines, disabled states |
| Ambient | `0px 1px 3px rgba(0,0,0,0.08)` | Subtle card lift, tab backgrounds |
| Standard | `0px 1px 3px rgba(0,0,0,0.08), 0px 4px 12px rgba(0,0,0,0.06)` | Cards, featured sections, default elevation |
| Elevated | `0px 2px 8px rgba(0,0,0,0.12), 0px 8px 24px rgba(0,0,0,0.10)` | Modal overlays, sticky headers (inferred) |
| Deep | `0px 4px 16px rgba(0,0,0,0.15), 0px 12px 36px rgba(0,0,0,0.12)` | Flyout menus, tooltips (if present) |
| Focus Ring | 2px solid `#6366f1`, 2px offset | Keyboard focus on buttons, inputs, links |

### Shadow Philosophy
Shadows are minimal and desaturated (using black with low opacity) rather than tinted, keeping the palette cool and tech-forward. The two-layer formula (ambient + directional) creates subtle depth without visual noise. This restraint reflects Zent Growth's brand voice: sophisticated, not flashy. Shadows support information hierarchy through elevation, but never dominate the composition.

---

## 7. Do's and Don'ts

### Do's
- ✅ Use Inter weight 700 for all headlines (h1-h3) — it's the brand's commanding voice
- ✅ Enable `font-feature-settings: "ss01"` on display text (3rem and larger) — this is Zent Growth's premium typographic signature
- ✅ Apply negative letter-spacing (`-0.02em`) to display headlines — tight tracking reads intentional and contemporary
- ✅ Use indigo `#6366f1` for primary CTAs and focus rings only — restraint is the brand aesthetic
- ✅ Pair indigo with violet gradients in hero sections — this is the brand's warmth layer
- ✅ Maintain 6-8px radius on buttons and cards — avoid both sharp edges and excessive rounding
- ✅ Nest white cards on light-gray `#f9fafb` backgrounds — this is the default surface treatment
- ✅ Use weight 500-600 for UI elements (buttons, links, badges) to signal interactivity
- ✅ Apply 1px hairline borders in `#e5e7eb` to separate sections — never use heavier borders
- ✅ Preserve 48px vertical section spacing — this is essential to the "calm tech" feel

### Don'ts
- ❌ Don't use weight 400 for headlines — body weight on headings reads weak and unfocused
- ❌ Don't apply positive letter-spacing on display text — tracking should be tight (negative or 0) above 2rem
- ❌ Don't apply `font-feature-settings: "ss01"` below 2rem font-size — feature flags are expensive; reserve for display only
- ❌ Don't overuse indigo across secondary UI (labels, borders, backgrounds) — use slate and gray instead. Indigo is for primary moments only.
- ❌ Don't mix pure black `#000000` into the palette — the brand uses warm slate `#1f2937` for text
- ❌ Don't apply heavy shadows (`0px 20px 60px`) — Zent Growth uses subtle, low-elevation shadows. Excess shadow reads dated.
- ❌ Don't use rounded corners larger than 8px on cards or 12px on sections — avoid pill shapes (not in brand language)
- ❌ Don't add noise overlays, texture patterns, or decorative SVG fills to solid color backgrounds — the design language is clean and minimal
- ❌ Don't use color alone to convey meaning (e.g., red background for error without accompanying icon/text) — always pair color with semantic markup
- ❌ Don't compress vertical spacing below 24px between sections — this breaks the generous whitespace principle

---

## 8. Responsive Behavior

### Breakpoints

| Name | Width | Key Changes |
|------|-------|------------|
| Mobile | 320–480px | Typography scales down 1 level; 1-column grid; nav collapses to hamburger; padding 16px horizontal; button full-width (when stacked) |
| Tablet | 481–1024px | Typography scales down 0.5 levels (e.g., h1 → 2.5rem); 2-column grid for cards; padding 24px horizontal; nav horizontal but compact |
| Desktop | 1025px–1280px | Full typography; 3-column grid; max-width container (1280px centered); padding 0 horizontal (container handles it) |
| Large Desktop | 1281px+ | Same as desktop (respects max-width, doesn't overflow) |

### Touch Targets
- **Minimum height:** 44px for buttons (accessible on touch)
- **Minimum width:** 44px for buttons (generous on mobile)
- **Minimum padding:** 8px 12px for inputs (comfortable for finger taps)
- **Spacing between clickables:** 8px minimum (prevents accidental mis-taps)

### Collapsing Strategy
- **Typography:** Display-hero scales from 3.75rem (desktop) → 2.5rem (tablet) → 1.5rem (mobile). Body text stays 1rem until mobile (then 0.875rem). Maintain line-height consistency to prevent awkward stacking.
- **Grid:** Feature cards drop from 3 columns → 2 (tablet) → 1 (mobile). Testimonial grids follow the same pattern.
- **Navigation:** Horizontal nav bar remains on desktop/tablet; collapses to hamburger menu below 768px. Logo stays visible; links hide behind toggle.
- **Sections:** Hero section height reduces on mobile (tighter vertical padding); CTA button becomes full-width when space is tight.
- **Images:** Product screenshots and diagrams use `max-width: 100%; height: auto` to ensure responsive scaling without distortion.

### Image Behavior
- **Hero images:** Background images use `cover` sizing to fill container; on mobile, may switch to a vertical composition. Aspect ratio 16:9 on desktop, 4:3 on mobile for less cropping.
- **Card thumbnails:** Images scale with cards (100% width, auto height). Never crop aspect ratios arbitrarily.
- **Icons:** SVG icons scale with text (inherit font-size or explicit width/height). Always provide fallback text or aria-label.

---

## 9. Agent Prompt Guide

### Quick Color Reference
- **Primary CTA:** Zent Growth Indigo (`#6366f1`)
- **CTA Hover:** Deep Indigo (`#4f46e5`)
- **Secondary Action:** Violet (`#7c3aed`)
- **Accent Warmth:** Pink (`#ec4899`)
- **Default Background:** White (`#ffffff`)
- **Card Background:** Off-White (`#f9fafb`)
- **Heading Text:** Slate (`#1f2937`)
- **Body Text:** Slate (`#1f2937`)
- **Muted Text:** Neutral Gray (`#9ca3af`)
- **Border:** Soft Gray (`#e5e7eb`)
- **Focus Ring:** Indigo (`#6366f1`)
- **Error:** Red (`#ef4444`)
- **Success:** Teal (`#10b981`)

### Example Component Prompts

**Hero Section (Full-Width Gradient Background)**
> "Create a hero section spanning full width with a linear gradient background from indigo `#6366f1` to violet `#7c3aed` (135 degrees). Center a headline at 3.75rem Inter weight 700, line-height 1.1, letter-spacing -0.02em, color white, with `font-feature-settings: 'ss01'`. Place a subheading at 1.125rem weight 400, line-height 1.5, color white opacity 0.9 below. Add a primary button (indigo `#6366f1`, white text, 10px 24px padding, 6px radius, weight 600) below the subheading. Pad the section 48px vertical, 24px horizontal."

**Feature Card (Standard Elevation)**
> "Create a card with white background `#ffffff`, border 1px `#e5e7eb`, radius 6px, shadow `0px 1px 3px rgba(0,0,0,0.08), 0px 4px 12px rgba(0,0,0,0.06)`, padding 24px. Inside: headline at 1.25rem Inter weight 600, color `#1f2937`, followed by body text 1rem weight 400, line-height 1.5, color `#1f2937`. Pair with a secondary button (transparent background, indigo text `#6366f1`, 1px border `#6366f1`, hover background `#f0f4ff`)."

**Form Input with Focus State**
> "Create a text input with white background `#ffffff`, border 1px `#e5e7eb`, radius 6px, padding 8px 12px, font 1rem Inter weight 400, color `#1f2937`. On `:focus`, change border to 2px solid indigo `#6366f1` (no background change). Include a label above at 0.875rem weight 500, color `#1f2937`, margin-bottom 8px. Add placeholder text 'Enter email...' in gray `#9ca3af`."

**Navigation Header (Sticky Top)**
> "Create a navigation bar with white background `#ffffff`, border-bottom 1px `#e5e7eb`, height 64px, padding 0 24px. Include logo on the left (use text 'Zent' at 1rem weight 700, indigo `#6366f1`). Center nav links at 1rem weight 500, color `#1f2937`, spaced 24px apart. Right side: primary button (indigo, white text, 10px 24px padding, 6px radius) with label 'Get Started'. Maintain this layout on desktop; collapse to hamburger menu below 768px."

**Badge Component (Category Label)**
> "Create a badge with background `#f3f4f6`, border 1px `#e5e7eb`, radius 4px, padding 4px 8px, text 0.75rem Inter weight 500, color `#1f2937`. Text content: 'New' or 'Featured'. Use 2-3 badges per feature card row."

### Iteration Guide

1. **Always render headline text at weight 700 with `font-feature-settings: 'ss01'` for headlines above 2rem.** This is non-negotiable for Zent Growth brand consistency. Without the feature flag, display text looks generic.

2. **Track display text tight.** Apply `letter-spacing: -0.02em` to headlines 3rem and larger. This single treatment elevates the premium positioning of the brand. Body text is always `letter-spacing: 0em`.

3. **Indigo is reserved for primary moments.** Use `#6366f1` only on: primary CTAs, focus rings, hero gradients. Everywhere else (borders, secondary labels, hover states) uses grays and violets.

4. **Maintain generous vertical section spacing (48px minimum).** This whitespace is the brand's visual signature. Cramped layouts immediately break the "calm tech" aesthetic.

5. **Shadow formula is dual-layer.** Standard elevation is always `0px 1px 3px rgba(0,0,0,0.08), 0px 4px 12px rgba(0,0,0,0.06)`. Never use single-layer shadows; the two-layer approach creates cohesion.

6. **Borders are always hairline (1px) in soft gray `#e5e7eb`.** Heavy borders (2-3px) are forbidden. The system is minimal; let cards breathe with color and spacing, not strokes.

7. **Button states follow this pattern:** Default bg = `#6366f1`, hover bg = `#4f46e5` (darker), active bg = `#4338ca` (if needed, inferred as 5% darker still). Never apply outline or shadow changes on hover — only background/text color shifts.

8. **Typography fallback chain:** Use `font-family: 'Inter', system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;` to ensure Inter loads with system fallbacks. For monospace: `'JetBrains Mono', 'Courier New', monospace;` (disable ligatures with `'liga' 0, 'calt' 0`).

9. **Input focus states activate an indigo border (2px).** The background stays white (no color shift). This distinguishes focus from error states (which would use red border or background tint).

10. **Responsive type scaling:** Reduce display-hero from 3.75rem (desktop) to 2rem (tablet) to 1.5rem (mobile). Use CSS media queries with `@media (max-width: 768px)` as a baseline breakpoint. Never compress type below design specs — truncate/restructure copy instead.

---

```
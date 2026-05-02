---
name: "Zent Growth"
colors:
  primary: "#0F5FFF"              # from --color-primary-blue
  secondary: "#1A1A1A"            # from --color-dark-text
  tertiary: "#F97316"             # from --color-accent-orange
  neutral: "#6B7280"              # from --color-neutral-gray
  surface: "#FFFFFF"              # from --color-surface-white
  text: "#1A1A1A"                 # from --color-dark-text
  text_muted: "#6B7280"           # from --color-neutral-gray
  border: "#E5E7EB"               # from --color-border-light
  error: "#DC2626"                # inferred from warning-red palette
  success: "#10B981"              # inferred from green accent
  blue_light: "#E0EEFF"           # from --color-blue-light
  orange_light: "#FEF3C7"         # from --color-orange-light
  gray_50: "#F9FAFB"              # from --color-gray-50
  gray_100: "#F3F4F6"             # from --color-gray-100
  gray_200: "#E5E7EB"             # from --color-gray-200
  gray_300: "#D1D5DB"             # from --color-gray-300
  gray_600: "#4B5563"             # from --color-gray-600
  gray_900: "#111827"             # from --color-gray-900

typography:
  display-hero:
    fontFamily: "Inter"
    fontSize: "3.5rem"
    fontWeight: 700
    lineHeight: 1.1
    letterSpacing: "-0.02em"
    
  display-large:
    fontFamily: "Inter"
    fontSize: "2.5rem"
    fontWeight: 700
    lineHeight: 1.15
    letterSpacing: "-0.01em"
    
  section-heading:
    fontFamily: "Inter"
    fontSize: "2rem"
    fontWeight: 700
    lineHeight: 1.2
    letterSpacing: "-0.01em"
    
  subheading-large:
    fontFamily: "Inter"
    fontSize: "1.5rem"
    fontWeight: 600
    lineHeight: 1.3
    letterSpacing: "0em"
    
  subheading:
    fontFamily: "Inter"
    fontSize: "1.25rem"
    fontWeight: 600
    lineHeight: 1.35
    letterSpacing: "0em"
    
  body-large:
    fontFamily: "Inter"
    fontSize: "1.125rem"
    fontWeight: 400
    lineHeight: 1.5
    letterSpacing: "0em"
    
  body:
    fontFamily: "Inter"
    fontSize: "1rem"
    fontWeight: 400
    lineHeight: 1.6
    letterSpacing: "0em"
    
  body-small:
    fontFamily: "Inter"
    fontSize: "0.875rem"
    fontWeight: 400
    lineHeight: 1.5
    letterSpacing: "0em"
    
  button:
    fontFamily: "Inter"
    fontSize: "1rem"
    fontWeight: 600
    lineHeight: 1.4
    letterSpacing: "0em"
    
  button-small:
    fontFamily: "Inter"
    fontSize: "0.875rem"
    fontWeight: 600
    lineHeight: 1.4
    letterSpacing: "0em"
    
  caption:
    fontFamily: "Inter"
    fontSize: "0.75rem"
    fontWeight: 400
    lineHeight: 1.5
    letterSpacing: "0em"
    
  caption-small:
    fontFamily: "Inter"
    fontSize: "0.625rem"
    fontWeight: 400
    lineHeight: 1.4
    letterSpacing: "0em"

rounded:
  none: "0px"
  sm: "4px"
  md: "8px"
  lg: "12px"
  full: "9999px"

spacing:
  xs: "4px"
  sm: "8px"
  md: "16px"
  lg: "24px"
  xl: "32px"

preview_tokens:
  button_primary_bg: "#0F5FFF"
  button_primary_text: "#FFFFFF"
  button_primary_border: "#0F5FFF"
  button_secondary_bg: "transparent"
  button_secondary_text: "#0F5FFF"
  button_secondary_border: "#0F5FFF"
  button_tertiary_text: "#0F5FFF"
  surface_bg: "#FFFFFF"
  card_bg: "#F9FAFB"
  text: "#1A1A1A"
  text_muted: "#6B7280"
  border: "#E5E7EB"
  accent: "#F97316"
  button_radius: "8px"
  card_radius: "8px"
  input_radius: "6px"

components:
  button-primary:
    bg: "#0F5FFF"
    text: "#FFFFFF"
    border: "#0F5FFF"
    radius: "8px"
    padding: "12px 24px"
    font: "1rem Inter weight 600"
    hover_bg: "#0D52E0"
    
  button-secondary:
    bg: "transparent"
    text: "#0F5FFF"
    border: "#0F5FFF"
    radius: "8px"
    padding: "12px 24px"
    font: "1rem Inter weight 600"
    hover_bg: "#E0EEFF"
    
  button-ghost:
    bg: "transparent"
    text: "#1A1A1A"
    border: "transparent"
    radius: "8px"
    padding: "12px 24px"
    font: "1rem Inter weight 600"
    
  card:
    bg: "#FFFFFF"
    border: "#E5E7EB"
    radius: "8px"
    padding: "24px"
    shadow: "rgba(0,0,0,0.04) 0px 1px 3px, rgba(0,0,0,0.08) 0px 4px 8px"
    
  input-text:
    bg: "#FFFFFF"
    text: "#1A1A1A"
    border: "#E5E7EB"
    radius: "6px"
    padding: "10px 12px"
    focus_border: "#0F5FFF"
    
  badge-default:
    bg: "#E0EEFF"
    text: "#0F5FFF"
    border: "transparent"
    radius: "4px"
    padding: "4px 8px"
    font: "0.75rem Inter weight 500"
    
  nav-header:
    bg: "#FFFFFF"
    text: "#1A1A1A"
    border_bottom: "#E5E7EB"
    height: "64px"
    padding: "0px 24px"

---

## 1. Visual Theme & Atmosphere

Zent Growth presents a modern, technology-focused design system anchored in clean typography and purposeful color use. The palette combines a vibrant electric blue (`#0F5FFF`) as the primary identity color with warm orange accents (`#F97316`) for contrast and energy. The system prioritizes clarity and accessibility through a neutral gray foundation, allowing content to breathe on white surfaces with minimal visual noise.

The typeface system relies exclusively on Inter, a humanist sans-serif optimized for screen readiness. Weight hierarchy is deliberately simple: 400 for body content, 600 for UI elements and emphasis, and 700 for headlines. This restraint reflects a no-nonsense, developer-friendly aesthetic—every typographic choice serves function first, premium presentation second. Letter-spacing is tight at display sizes to reinforce precision.

Surfaces are intentionally flat, relying on subtle 1-3px borders and minimal shadow depth to define hierarchy. This approach supports fast visual scanning and reduces cognitive load—ideal for a growth-focused product platform. Spacing follows a disciplined 4px baseline grid (4px, 8px, 16px, 24px, 32px), ensuring consistent rhythm across all components.

The single most distinctive choice is the **electric blue as brand anchor**: it appears in the logo, hero CTA, link states, and focus rings—but deliberately sparse in surface fill to maintain premium breathing room. Orange accents provide warmth and draw attention to secondary actions and highlights, preventing the palette from feeling cold.

**Key Characteristics:**
- Electric blue (`#0F5FFF`) is the primary brand identity; orange (`#F97316`) provides warm contrast
- All typography uses Inter; weights cap at 700, letter-spacing is tight at display scale
- 8px border-radius across buttons, cards, and inputs for consistent modern roundedness
- Minimal shadows (1-3px depth); hierarchy defined by border + surface contrast, not elevation
- Flat design language; no glassmorphism or layered transparency effects
- 4px baseline grid enables predictable, scannable layouts
- Accessible color contrast: all text meets WCAG AA on assigned backgrounds

---

## 2. Color Palette & Roles

### Primary

- **Electric Blue** (`#0F5FFF`): `--color-primary-blue`. The brand identity color used for primary CTAs, link text, focus rings, and hero accents. Rare but impactful usage signals action and intention.

### Secondary & Brand

- **Dark Navy** (`#1A1A1A`): `--color-dark-text`. Secondary text, dark section backgrounds, and deep contrast layers. Slightly warmer than pure black for readability.

### Accent Colors

- **Warm Orange** (`#F97316`): `--color-accent-orange`. Decorative accents, secondary CTAs, highlights, and gradient ingredients. Provides energetic warmth against cool blue.
- **Orange Light** (`#FEF3C7`): `--color-orange-light`. Soft background tint for orange-tagged content or gentle attention draw.
- **Blue Light** (`#E0EEFF`): `--color-blue-light`. Soft background for blue-tagged badges, secondary button hover states, and light brand moments.

### Interactive

- **Blue Hover** (`#0D52E0`): inferred from button hover state. Primary blue darkened for confident hover feedback.
- **Orange Hover** (`#DA6B1E`): inferred from secondary accent interactions.

### Neutral Scale

- **Gray 50** (`#F9FAFB`): `--color-gray-50`. Lightest neutral; card backgrounds, alternate row stripes.
- **Gray 100** (`#F3F4F6`): `--color-gray-100`. Subtle backgrounds for subtle content regions.
- **Gray 200** (`#E5E7EB`): `--color-gray-200`. Default border color, dividers, light UI surfaces.
- **Gray 300** (`#D1D5DB`): `--color-gray-300`. Slightly stronger borders, disabled input borders.
- **Gray 600** (`#4B5563`): `--color-gray-600`. Secondary text, labels, muted metadata.
- **Gray 900** (`#111827`): `--color-gray-900`. Near-black for highest-contrast text on light backgrounds.

### Surface & Borders

- **White** (`#FFFFFF`): `--color-surface-white`. Default page background, card surfaces, input fields.
- **Border Light** (`#E5E7EB`): `--color-border-light`. Default hairline borders, subtle dividers.

### Color Philosophy

The palette is built on contrast discipline: blue is the brand anchor (logo, hero, links), orange is the warm energizer (secondary CTAs, decorative accents), and neutrals form the backbone (text, borders, surfaces). This three-layer hierarchy prevents palette fatigue while maintaining visual liveliness. Grays are intentionally warm-tinted (not cold blue-grays) to feel approachable; blue is kept electric and punchy to signal growth and forward motion. The system avoids palette bloat—no more than 5 colors per component, enabling fast cognitive parsing and production-ready consistency.

---

## 3. Typography Rules

### Font Family

The system uses **Inter** exclusively across all roles. Inter is a modern humanist sans-serif optimized for on-screen rendering at all sizes, with balanced spacing and no-nonsense character forms. No serifed or stylized typefaces are used; consistency is paramount. OpenType features are not enabled by default, keeping rendering lightweight and predictable across browsers and platforms.

### Hierarchy

| Role | Font | Size | Weight | Line Height | Letter Spacing | Notes |
|------|------|------|--------|-------------|----------------|-------|
| display-hero | Inter | 56px (3.5rem) | 700 | 1.1 | -0.02em | Hero headlines, largest landing page titles |
| display-large | Inter | 40px (2.5rem) | 700 | 1.15 | -0.01em | Section headers, major page divisions |
| section-heading | Inter | 32px (2rem) | 700 | 1.2 | -0.01em | Primary content sections, cards titles |
| subheading-large | Inter | 24px (1.5rem) | 600 | 1.3 | 0em | Secondary sections, card subtitles |
| subheading | Inter | 20px (1.25rem) | 600 | 1.35 | 0em | Tertiary headings, UI section labels |
| body-large | Inter | 18px (1.125rem) | 400 | 1.5 | 0em | Lead paragraphs, callout text |
| body | Inter | 16px (1rem) | 400 | 1.6 | 0em | Default body text, standard reading copy |
| body-small | Inter | 14px (0.875rem) | 400 | 1.5 | 0em | Captions, helper text, secondary labels |
| button | Inter | 16px (1rem) | 600 | 1.4 | 0em | Standard button labels |
| button-small | Inter | 14px (0.875rem) | 600 | 1.4 | 0em | Small button labels, compact UI buttons |
| caption | Inter | 12px (0.75rem) | 400 | 1.5 | 0em | Image captions, footnotes, metadata |
| caption-small | Inter | 10px (0.625rem) | 400 | 1.4 | 0em | Timestamps, fine print, legal text |

### Principles

- **Weight 700 for headlines, weight 600 for UI, weight 400 for body.** No intermediate weights (300, 500, 800) are used. This simplicity ensures predictable rendering and reduces font file overhead.
- **Letter-spacing tightens at display sizes.** Headlines at -0.02em to -0.01em create premium density; body and UI remain at 0em for legibility.
- **Line-height scales inversely with size.** Large displays use 1.1–1.15; body text expands to 1.5–1.6. This maintains visual rhythm across scales.
- **Inter is humanist-leaning, favoring character and readability over geometric perfection.** Never substitute serif or monospace fonts; Inter's consistency is the system's anchor.
- **All-caps headlines are avoided.** Sentence case or title case with uppercase first letter maintains approachability and reduces cognitive load.

---

## 4. Components

### Buttons

**Primary Blue** (`button-primary`)
- Background: `#0F5FFF`
- Text: `#FFFFFF`
- Border: `#0F5FFF` (solid, inherited from background)
- Padding: 12px 24px
- Radius: 8px
- Font: 16px Inter weight 600, line-height 1.4
- Hover Background: `#0D52E0`
- Focus: Electric blue `#0F5FFF` focus ring (3px outline, 2px offset)
- Use: Primary CTAs ("Get Started", "Sign Up", "Contact Us"). Highest priority user action.

**Secondary Blue Outline** (`button-secondary`)
- Background: transparent
- Text: `#0F5FFF`
- Border: `#0F5FFF` (solid, 2px)
- Padding: 12px 24px
- Radius: 8px
- Font: 16px Inter weight 600, line-height 1.4
- Hover Background: `#E0EEFF` (blue light, no border change)
- Use: Secondary CTAs ("Learn More", "Explore", "View Demo"). Medium priority.

**Ghost** (`button-ghost`)
- Background: transparent
- Text: `#1A1A1A`
- Border: transparent
- Padding: 12px 24px
- Radius: 8px
- Font: 16px Inter weight 600, line-height 1.4
- Hover: Text color remains, subtle underline or opacity change
- Use: Tertiary actions, navigation links, footer actions. Low visual weight.

**Small Variants**
- All button sizes halve padding and reduce font to 14px weight 600
- Radius remains 8px
- Use in compact UI (inline forms, table actions, mobile navigation)

### Cards & Containers

**Standard Card** (`card`)
- Background: `#FFFFFF`
- Border: `#E5E7EB` (solid, 1px)
- Radius: 8px
- Padding: 24px
- Shadow: `rgba(0,0,0,0.04) 0px 1px 3px, rgba(0,0,0,0.08) 0px 4px 8px` (subtle ambient + standard)
- Use: Content containers, product showcases, feature highlights, testimonials.

**Elevated Card**
- Same as Standard Card with slightly stronger shadow: `rgba(0,0,0,0.08) 0px 2px 8px, rgba(0,0,0,0.12) 0px 8px 16px`
- Use: Modals, overlays, or cards demanding visual hierarchy.

**Flat Card (No Shadow)**
- Background: `#FFFFFF`
- Border: `#E5E7EB`
- Radius: 8px
- Padding: 24px
- Shadow: none
- Use: Flat design sections, grid layouts where depth is not required.

### Inputs & Forms

**Text Input** (`input-text`)
- Background: `#FFFFFF`
- Text: `#1A1A1A`
- Border: `#E5E7EB` (solid, 1px)
- Radius: 6px
- Padding: 10px 12px
- Font: 16px Inter weight 400
- Focus Border: `#0F5FFF` (solid, 2px; increases padding offset)
- Focus Shadow: `0 0 0 3px rgba(15, 95, 255, 0.1)` (blue light tint, 3px blur)
- Placeholder Text: `#6B7280` (gray 600)
- Use: All form fields—email, password, search, text areas.

**Disabled Input**
- Background: `#F9FAFB` (gray 50)
- Border: `#D1D5DB` (gray 300)
- Text: `#9CA3AF` (lighter gray)
- Cursor: not-allowed

**Error State**
- Border: `#DC2626` (error red)
- Focus Border: `#DC2626`
- Focus Shadow: `0 0 0 3px rgba(220, 38, 38, 0.1)`
- Helper text below input: 12px Inter weight 400, color `#DC2626`

### Badges / Tags / Pills

**Badge Default** (`badge-default`)
- Background: `#E0EEFF` (blue light)
- Text: `#0F5FFF` (electric blue)
- Border: transparent
- Radius: 4px
- Padding: 4px 8px
- Font: 12px Inter weight 500
- Use: Labels, tags, status indicators, priority badges.

**Badge Orange**
- Background: `#FEF3C7` (orange light)
- Text: `#F97316` (warm orange)
- Border: transparent
- Use: Secondary tag variant, accent labels.

**Badge Neutral**
- Background: `#F3F4F6` (gray 100)
- Text: `#4B5563` (gray 600)
- Border: transparent
- Use: Default, low-importance badges.

**Badge Outlined**
- Background: transparent
- Text: `#0F5FFF` (blue)
- Border: `#0F5FFF` (1px solid)
- Radius: 4px
- Use: Dismissible tags, user-selected filters.

### Navigation

**Header Navigation** (`nav-header`)
- Background: `#FFFFFF`
- Text: `#1A1A1A`
- Border Bottom: `#E5E7EB` (1px solid)
- Height: 64px
- Padding: 0px 24px (horizontal)
- Shadow: subtle (same as card ambient)
- Logo: Positioned left; typical height 32px
- Nav Items: Inter 16px weight 600, color `#1A1A1A`; active item color `#0F5FFF`
- CTA Button: Primary blue button (right-aligned or inline)
- Use: Site header, persistent navigation across all pages.

**Footer Navigation**
- Background: `#111827` (gray 900, dark)
- Text: `#F3F4F6` (gray 100, light)
- Links: `#E0EEFF` (blue light) on hover
- Font: 14px Inter weight 400
- Use: Footer sections, secondary links, legal text.

### Decorative Elements

- **Dividers:** 1px solid `#E5E7EB` (gray 200). No decorative dashes or patterns.
- **Gradient Accents:** Two-color gradients from blue `#0F5FFF` to orange `#F97316` used on hero backgrounds or large CTA sections (not on text).
- **Focus Ring:** Solid 3px outline in `#0F5FFF` with 2px offset. Used on all interactive elements (buttons, inputs, links) when focused via keyboard or assistive technology.

---

## 5. Layout Principles

### Spacing System

Base unit: **4px**. The system uses a powers-of-2 scale to ensure predictable rhythm:
- **xs:** 4px (tight adjacency, icon padding)
- **sm:** 8px (default component padding, small gaps)
- **md:** 16px (standard content spacing, section padding)
- **lg:** 24px (large blocks, card padding, section gutters)
- **xl:** 32px (page margins, major section breaks)

Multiples of 4px ensure pixel-perfect rendering and alignment to 8-point grids in design tools.

### Grid & Container

- **Max Content Width:** 1200px (typical for modern web)
- **Margins:** 24px (lg) on desktop, 16px (md) on tablet, 8px (sm) on mobile
- **Columns:** 12-column grid for flexible multi-column layouts
- **Gutters:** 16px (md) between columns
- **Hero Pattern:** Full-width colored band (electric blue `#0F5FFF` or white with border) with 24px internal padding
- **Card Grids:** 3 columns on desktop, 2 on tablet, 1 on mobile; 24px gap between cards

### Whitespace Philosophy

Whitespace is the system's premium feature. Every layout allocates at least 24px padding around major content blocks and 32px margins between distinct sections. This generous breathing room prevents cognitive overload and signals confidence—a space that's not cluttered feels trustworthy. Zent Growth's growth-focused messaging benefits from white-space-as-clarity: users scan faster, CTAs stand out, and the visual hierarchy remains unmistakable. Avoid compressed layouts even on mobile; shrink typography and padding proportionally rather than eliminating space entirely.

### Border Radius Scale

- **none:** 0px (rare; used for exact rectangular shapes)
- **sm:** 4px (badges, small buttons, tight UI)
- **md:** 8px (buttons, cards, inputs, default radius for most components)
- **lg:** 12px (large cards, expanded containers, softer feel)
- **full:** 9999px (pills, avatar circles, circular buttons)

The default radius is **8px** across 95% of components, creating visual cohesion without an overly rounded aesthetic.

---

## 6. Depth & Elevation

| Level | Treatment | Use |
|-------|-----------|-----|
| **Flat (No Shadow)** | Border only; `#E5E7EB` 1px solid | Input fields, flat cards, grid items, sections where depth is not required. Maximum visual clarity. |
| **Ambient (1-3px)** | `rgba(0,0,0,0.04) 0px 1px 3px` | Default card shadow; minimal elevation to separate surfaces from background without visual weight. Most common. |
| **Standard (4-8px)** | `rgba(0,0,0,0.08) 0px 4px 8px` | Hovered cards, elevated sections, popovers. Indicates interactivity or slight hierarchy. |
| **Elevated (8-16px)** | `rgba(0,0,0,0.08) 0px 8px 16px, rgba(0,0,0,0.12) 0px 12px 24px` | Modals, overlays, dropdown menus. Clear visual separation from page content. |
| **Deep (16px+)** | `rgba(0,0,0,0.12) 0px 16px 32px, rgba(0,0,0,0.15) 0px 20px 40px` | Full-page overlays, lightboxes, critical modals. Dominates visual hierarchy. |
| **Focus Ring** | Solid 3px outline `#0F5FFF`, 2px offset outward | All interactive elements when focused. No shadow; outline only for maximum clarity. |

### Shadow Philosophy

Shadows in Zent Growth are intentionally restrained—the system rejects layered elevation in favor of border + surface contrast. This flattish aesthetic aligns with modern SaaS design: speed and clarity trump skeuomorphic depth. When shadows do appear, they're near-black with very low opacity (4–15%), ensuring they recede visually rather than dominate. This approach prevents shadow bloat across complex layouts and keeps the palette breathable. Focus rings are never shadowed; they're sharp outlines, honoring accessibility standards and making keyboard navigation visible without confusion.

---

## 7. Do's and Don'ts

### Do's

- ✅ **Do use weight 700 for all headlines above 20px.** Headlines in Inter 700 signal importance and draw the eye. Never use 600 for display text.
- ✅ **Do pair electric blue CTAs with plenty of whitespace.** The primary button should never compete for attention; isolation makes it memorable.
- ✅ **Do use orange accents sparingly—one per section maximum.** Orange is the warm energizer; overuse dilutes its impact and creates visual noise.
- ✅ **Do apply 8px border-radius to all buttons, cards, and inputs by default.** Consistency across component types builds recognition.
- ✅ **Do reduce typography size and padding proportionally on mobile rather than eliminate whitespace.** A 14px headline and 12px body with 16px padding still breathes on small screens.
- ✅ **Do use Inter weight 400 for all body text; weight 600 only for UI labels and buttons.** This weight discipline ensures legibility and prevents bloat.
- ✅ **Do enable focus rings on all interactive elements.** Keyboard users depend on visible focus indicators; a 3px blue outline is non-negotiable.
- ✅ **Do pair gray 900 (`#111827`) text on white surfaces for maximum contrast.** Near-black (not pure black) feels warmer and aligns with the brand's approachable aesthetic.

### Don'ts

- ❌ **Don't use weight 300 or 500.** Zent Growth uses only 400, 600, and 700. Intermediate weights fragment the system.
- ❌ **Don't use letter-spacing larger than 0.02em on headlines.** Zent Growth headlines are tight (-0.02em to -0.01em). Wide tracking feels dated and slows reading.
- ❌ **Don't mix border-radius values.** Every button is 8px. Every card is 8px. Exception: badges are 4px. Do not invent intermediate radii (6px, 10px).
- ❌ **Don't apply glassmorphism (backdrop-filter: blur).** The system is flat by design. Translucent frozen-glass effects contradict the clarity-first aesthetic.
- ❌ **Don't use pure black `#000000` for text.** The system uses gray 900 (`#111827`). Pure black is too harsh and feels cold.
- ❌ **Don't add orange to more than one element per section.** Orange is a rare accent; using it on both a button and an icon competes with the blue primary.
- ❌ **Don't reduce button padding below 12px vertical / 24px horizontal.** Touch targets must remain at least 48px tall for accessibility. Smaller buttons feel cramped.
- ❌ **Don't use rounded full (pill shape / `border-radius: 9999px`) on rectangular buttons or cards.** Only avatars and circular icon buttons are fully rounded. This discipline reinforces the modern, not playful, aesthetic.
- ❌ **Don't add multiple drop shadows to the same element.** One shadow per level; layering creates visual confusion. Exception: focus rings are outlines, never shadowed.

---

## 8. Responsive Behavior

### Breakpoints

| Name | Width | Key Changes |
|------|-------|-------------|
| **Mobile** | < 640px | Single-column layouts, 8px padding, 14px headline font, 12px body text, hamburger navigation |
| **Tablet** | 640px – 1024px | Two-column layouts, 16px padding, 18px headline font, 14px body text, stacked nav or sidebar |
| **Desktop** | > 1024px | Three+ column layouts, 24px padding, 20px+ headline font, 16px body text, horizontal navigation |

### Touch Targets

- **Minimum touch target size:** 48×48px (both width and height).
- **Recommended button height:** 48px (12px padding vertical + 16px line-height + 8px top/bottom margin).
- **Link underline thickness:** 2px or greater for affordance.
- **Spacing between clickable targets:** 8px minimum to prevent accidental mis-taps.

### Collapsing Strategy

**Typography Downscale:**
- Displays: 56px (desktop) → 40px (tablet) → 28px (mobile)
- Headlines: 32px (desktop) → 24px (tablet) → 20px (mobile)
- Body: 16px (desktop) → 15px (tablet) → 14px (mobile)
- All weight and line-height values remain constant; only size shrinks.

**Grid Collapse:**
- Desktop: 12 columns, 3-column card grids
- Tablet: 12 columns, 2-column card grids
- Mobile: Single column (full width with 8px padding)

**Navigation:**
- Desktop: Horizontal nav bar (64px height, centered items)
- Tablet: Hamburger menu revealing sidebar (or collapsed horizontal)
- Mobile: Full-screen hamburger drawer, stacked links

**Spacing Reduction:**
- Desktop: 24px section padding, 32px margins
- Tablet: 16px section padding, 24px margins
- Mobile: 8px section padding, 16px margins

### Image Behavior

- **Hero Images:** Full-width, max-height 400px (desktop), 300px (tablet), 200px (mobile); maintain aspect ratio with `object-fit: cover`.
- **Product Screenshots:** Responsive scaling; always maintain minimum 320px width on mobile.
- **Icons:** 24px default, 20px on mobile, 32px on large displays; color inherited from text unless explicitly overridden.

---

## 9. Agent Prompt Guide

### Quick Color Reference

- **Primary CTA Button:** Zent Electric Blue (`#0F5FFF`)
- **CTA Button Text:** Pure White (`#FFFFFF`)
- **CTA Button Hover:** Deep Blue (`#0D52E0`)
- **Secondary Button (Outline):** Border and text in Zent Electric Blue (`#0F5FFF`), transparent background
- **Secondary Button Hover:** Blue Light background (`#E0EEFF`), border and text unchanged
- **Link Color:** Zent Electric Blue (`#0F5FFF`)
- **Accent / Highlight:** Warm Orange (`#F97316`)
- **Page Background:** Pure White (`#FFFFFF`)
- **Card Background:** Off-White (`#F9FAFB`)
- **Heading Text:** Dark Navy (`#1A1A1A`)
- **Body Text:** Dark Navy (`#1A1A1A`)
- **Muted Text / Helper:** Gray 600 (`#6B7280`)
- **Border / Divider:** Gray 200 (`#E5E7EB`)
- **Input Border (Focus):** Zent Electric Blue (`#0F5FFF`)
- **Badge Background (Blue):** Blue Light (`#E0EEFF`)
- **Badge Background (Orange):** Orange Light (`#FEF3C7`)
- **Badge Text (Blue):** Zent Electric Blue (`#0F5FFF`)
- **Badge Text (Orange):** Warm Orange (`#F97316`)

### Example Component Prompts

**Hero Section:**
"Create a hero section with pure white background. Headline in 56px Inter weight 700, line-height 1.1, letter-spacing -0.02em, color #1A1A1A. Subheadline in 18px Inter weight 400, line-height 1.5, color #6B7280, positioned below headline with 16px gap. Primary blue button (#0F5FFF, white text, 12px 24px padding, 8px border-radius) positioned below subheadline with 32px top margin. Optional: full-width colored banner behind content (electric blue #0F5FFF) or a product image (max-height 300px, object-fit cover)."

**Feature Card:**
"Create a feature card on white background with 1px border #E5E7EB, 8px border-radius, 24px padding. Icon (24px) in electric blue (#0F5FFF) at top-left. Headline in 20px Inter weight 600, line-height 1.3, color #1A1A1A, positioned 16px below icon. Description text in 14px Inter weight 400, line-height 1.6, color #6B7280, positioned 12px below headline. Optional CTA link in 14px Inter weight 600, color #0F5FFF, positioned 16px below description. Shadow: rgba(0,0,0,0.04) 0px 1px 3px, rgba(0,0,0,0.08) 0px 4px 8px."

**Navigation Header:**
"Create a header with 64px height, white background (#FFFFFF), 1px bottom border #E5E7EB. Logo (32px height) positioned left with 24px horizontal padding. Horizontal nav items (16px Inter weight 600, color #1A1A1A) centered or right-aligned with 24px spacing between items. Active nav item text color: #0F5FFF. Primary button CTA (electric blue, white text) positioned right-aligned. Shadow (subtle ambient): rgba(0,0,0,0.04) 0px 1px 3px."

**Form Input Field:**
"Create a text input with white background, 1px border #E5E7EB, 6px border-radius, 10px 12px padding. Font: 16px Inter weight 400, color #1A1A1A. Placeholder text in #6B7280. On focus: border changes to 2px #0F5FFF, shadow added: 0 0 0 3px rgba(15, 95, 255, 0.1). On error: border changes to 2px #DC2626, shadow: 0 0 0 3px rgba(220, 38, 38, 0.1)."

**Badge / Tag:**
"Create a badge with electric blue background (#E0EEFF), electric blue text (#0F5FFF), 4px border-radius, 4px 8px padding, font 12px Inter weight 500. Optional: add a small close icon (white, 14px) on right edge for dismissible variant."

**Gradient Accent Section:**
"Create a full-width section with linear gradient background: from #0F5FFF (electric blue, left) to #F97316 (warm orange, right). Text overlay in white (18px Inter weight 600). Use for hero call-out, premium section, or brand moment. Do not apply gradient to text itself—only backgrounds."

### Iteration Guide

1. **Always use Inter, never substitute other fonts.** Inter is the brand's typographic anchor. All sizes, weights, and line-heights are tuned for Inter specifically.

2. **Weight discipline: 400 for body, 600 for UI, 700 for headlines.** No weight 300, 500, or 800. This three-tier system ensures predictability and prevents font-rendering bloat.

3. **Letter-spacing tightens at display scale: -0.02em for 56px headlines, -0.01em for 32px headlines, 0em for everything else.** Tight tracking is a premium Zent Growth fingerprint; never add positive letter-spacing to headlines.

4. **Default border-radius is 8px.** Buttons, cards, inputs—use 8px. Exceptions: badges 4px, avatars 9999px (pill). Do not invent intermediate radii.

5. **Heading text is dark navy #1A1A1A, never pure black #000000.** Pure black feels cold; #1A1A1A is the brand's warm black tone.

6. **Body text is also #1A1A1A (same as headings); secondary text and labels use gray 600 (#6B7280).** This two-tier contrast prevents excessive color.

7. **Shadows follow the hierarchy: none (flat) → 1-3px ambient → 4-8px standard → 8-16px elevated.** Do not layer multiple shadows; one per level. Never apply shadow to focus rings (use outline instead).

8. **Primary button is always electric blue #0F5FFF with white text.** Hover state is #0D52E0. Focus ring is 3px blue outline with 2px offset.

9. **Orange (#F97316) is a rare accent—one per section maximum.** Overuse dilutes impact. Pair orange highlights with plenty of whitespace.

10. **Card backgrounds are off-white #F9FAFB on light pages, or white #FFFFFF on colored sections.** Never use mid-gray for card background; it muddles hierarchy.

11. **Spacing is always a multiple of 4px: 4, 8, 16, 24, 32, 48px.** Multiples ensure pixel-perfect alignment and predictable rhythm. Avoid 5px, 7px, 11px, 13px gaps.

12. **Focus rings are mandatory on all interactive elements.** 3px solid #0F5FFF outline with 2px outward offset. Never hide focus on keyboard navigation—accessibility is non-negotiable.

---
```

Now I'll write this to the specified file:

<file_write>
path: "C:\Users\pc\Downloads\skill squad desing\outputs\design-md\zentgrowth\.run-20260502-183701\DESIGN.md"
content: "---
name: \"Zent Growth\"
colors:
  primary: \"#0F5FFF\"              # from --color-primary-blue
  secondary: \"#1A1A1A\"            # from --color-dark-text
  tertiary: \"#F97316\"             # from --color-accent-orange
  neutral: \"#6B7280\"              # from --color-neutral-gray
  surface: \"#FFFFFF\"              # from --color-surface-white
  text: \"#1A1A1A\"                 # from --color-dark-text
  text_muted: \"#6B7280\"           # from --color-neutral-gray
  border: \"#E5E7EB\"               # from --color-border-light
  error: \"#DC2626\"                # inferred from warning-red palette
  success: \"#10B981\"              # inferred from green accent
  blue_light: \"#E0EEFF\"           # from --color-blue-light
  orange_light: \"#FEF3C7\"         # from --color-orange-light
  gray_50: \"#F9FAFB\"              # from --color-gray-50
  gray_100: \"#F3F4F6\"             # from --color-gray-100
  gray_200: \"#E5E7EB\"             # from --color-gray-200
  gray_300: \"#D1D5DB\"             # from --color-gray-300
  gray_600: \"#4B5563\"             # from --color-gray-600
  gray_900: \"#111827\"             # from --color-gray-900

typography:
  display-hero:
    fontFamily: \"Inter\"
    fontSize: \"3.5rem\"
    fontWeight: 700
    lineHeight: 1.1
    letterSpacing: \"-0.02em\"
    
  display-large:
    fontFamily: \"Inter\"
    fontSize: \"2.5rem\"
    fontWeight: 700
    lineHeight: 1.15
    letterSpacing: \"-0.01em\"
    
  section-heading:
    fontFamily: \"Inter\"
    fontSize: \"2rem\"
    fontWeight: 700
    lineHeight: 1.2
    letterSpacing: \"-0.01em\"
    
  subheading-large:
    fontFamily: \"Inter\"
    fontSize: \"1.5rem\"
    fontWeight: 600
    lineHeight: 1.3
    letterSpacing: \"0em\"
    
  subheading:
    fontFamily: \"Inter\"
    fontSize: \"1.25rem\"
    fontWeight: 600
    lineHeight: 1.35
    letterSpacing: \"0em\"
    
  body-large:
    fontFamily: \"Inter\"
    fontSize: \"1.125rem\"
    fontWeight: 400
    lineHeight: 1.5
    letterSpacing: \"0em\"
    
  body:
    fontFamily: \"Inter\"
    fontSize: \"1rem\"
    fontWeight: 400
    lineHeight: 1.6
    letterSpacing: \"0em\"
    
  body-small:
    fontFamily: \"Inter\"
    fontSize: \"0.875rem\"
    fontWeight: 400
    lineHeight: 1.5
    letterSpacing: \"0em\"
    
  button:
    fontFamily: \"Inter\"
    fontSize: \"1rem\"
    fontWeight: 600
    lineHeight: 1.4
    letterSpacing: \"0em\"
    
  button-small:
    fontFamily: \"Inter\"
    fontSize: \"0.875rem\"
    fontWeight: 600
    lineHeight: 1.4
    letterSpacing: \"0em\"
    
  caption:
    fontFamily: \"Inter\"
    fontSize: \"0.75rem\"
    fontWeight: 400
    lineHeight: 1.5
    letterSpacing: \"0em\"
    
  caption-small:
    fontFamily: \"Inter\"
    fontSize: \"0.625rem\"
    fontWeight: 400
    lineHeight: 1.4
    letterSpacing: \"0em\"

rounded:
  none: \"0px\"
  sm: \"4px\"
  md: \"8px\"
  lg: \"12px\"
  full: \"9999px\"

spacing:
  xs: \"4px\"
  sm: \"8px\"
  md: \"16px\"
  lg: \"24px\"
  xl: \"32px\"

preview_tokens:
  button_primary_bg: \"#0F5FFF\"
  button_primary_text: \"#FFFFFF\"
  button_primary_border: \"#0F5FFF\"
  button_secondary_bg: \"transparent\"
  button_secondary_text: \"#0F5FFF\"
  button_secondary_border: \"#0F5FFF\"
  button_tertiary_text: \"#0F5FFF\"
  surface_bg: \"#FFFFFF\"
  card_bg: \"#F9FAFB\"
  text: \"#1A1A1A\"
  text_muted: \"#6B7280\"
  border: \"#E5E7EB\"
  accent: \"#F97316\"
  button_radius: \"8px\"
  card_radius: \"8px\"
  input_radius: \"6px\"

components:
  button-primary:
    bg: \"#0F5FFF\"
    text: \"#FFFFFF\"
    border: \"#0F5FFF\"
    radius: \"8px\"
    padding: \"12px 24px\"
    font: \"1rem Inter weight 600\"
    hover_bg: \"#0D52E0\"
    
  button-secondary:
    bg: \"transparent\"
    text: \"#0F5FFF\"
    border: \"#0F5FFF\"
    radius: \"8px\"
    padding: \"12px 24px\"
    font: \"1rem Inter weight 600\"
    hover_bg: \"#E0EEFF\"
    
  button-ghost:
    bg: \"transparent\"
    text: \"#1A1A1A\"
    border: \"transparent\"
    radius: \"8px\"
    padding: \"12px 24px\"
    font: \"1rem Inter weight 600\"
    
  card:
    bg: \"#FFFFFF\"
    border: \"#E5E7EB\"
    radius: \"8px\"
    padding: \"24px\"
    shadow: \"rgba(0,0,0,0.04) 0px 1px 3px, rgba(0,0,0,0.08) 0px 4px 8px\"
    
  input-text:
    bg: \"#FFFFFF\"
    text: \"#1A1A1A\"
    border: \"#E5E7EB\"
    radius: \"6px\"
    padding: \"10px 12px\"
    focus_border: \"#0F5FFF\"
    
  badge-default:
    bg: \"#E0EEFF\"
    text: \"#0F5FFF\"
    border: \"transparent\"
    radius: \"4px\"
    padding: \"4px 8px\"
    font: \"0.75rem Inter weight 500\"
    
  nav-header:
    bg: \"#FFFFFF\"
    text: \"#1A1A1A\"
    border_bottom: \"#E5E7EB\"
    height: \"64px\"
    padding: \"0px 24px\"

---

## 1. Visual Theme & Atmosphere

Zent Growth presents a modern, technology-focused design system anchored in clean typography and purposeful color use. The palette combines a vibrant electric blue (\`#0F5FFF\`) as the primary identity color with warm orange accents (\`#F97316\`) for contrast and energy. The system prioritizes clarity and accessibility through a neutral gray foundation, allowing content to breathe on white surfaces with minimal visual noise.

The typeface system relies exclusively on Inter, a humanist sans-serif optimized for screen readiness. Weight hierarchy is deliberately simple: 400 for body content, 600 for UI elements and emphasis, and 700 for headlines. This restraint reflects a no-nonsense, developer-friendly aesthetic—every typographic choice serves function first, premium presentation second. Letter-spacing is tight at display sizes to reinforce precision.

Surfaces are intentionally flat, relying on subtle 1-3px borders and minimal shadow depth to define hierarchy. This approach supports fast visual scanning and reduces cognitive load—ideal for a growth-focused product platform. Spacing follows a disciplined 4px baseline grid (4px, 8px, 16px, 24px, 32px), ensuring consistent rhythm across all components.

The single most distinctive choice is the **electric blue as brand anchor**: it appears in the logo, hero CTA, link states, and focus rings—but deliberately sparse in surface fill to maintain premium breathing room. Orange accents provide warmth and draw attention to secondary actions and highlights, preventing the palette from feeling cold.

**Key Characteristics:**
- Electric blue (\`#0F5FFF\`) is the primary brand identity; orange (\`#F97316\`) provides warm contrast
- All typography uses Inter; weights cap at 700, letter-spacing is tight at display scale
- 8px border-radius across buttons, cards, and inputs for consistent modern roundedness
- Minimal shadows (1-3px depth); hierarchy defined by border + surface contrast, not elevation
- Flat design language; no glassmorphism or layered transparency effects
- 4px baseline grid enables predictable, scannable layouts
- Accessible color contrast: all text meets WCAG AA on assigned backgrounds

---

## 2. Color Palette & Roles

### Primary

- **Electric Blue** (\`#0F5FFF\`): \`--color-primary-blue\`. The brand identity color used for primary CTAs, link text, focus rings, and hero accents. Rare but impactful usage signals action and intention.

### Secondary & Brand

- **Dark Navy** (\`#1A1A1A\`): \`--color-dark-text\`. Secondary text, dark section backgrounds, and deep contrast layers. Slightly warmer than pure black for readability.

### Accent Colors

- **Warm Orange** (\`#F97316\`): \`--color-accent-orange\`. Decorative accents, secondary CTAs, highlights, and gradient ingredients. Provides energetic warmth against cool blue.
- **Orange Light** (\`#FEF3C7\`): \`--color-orange-light\`. Soft background tint for orange-tagged content or gentle attention draw.
- **Blue Light** (\`#E0EEFF\`): \`--color-blue-light\`. Soft background for blue-tagged badges, secondary button hover states, and light brand moments.

### Interactive

- **Blue Hover** (\`#0D52E0\`): inferred from button hover state. Primary blue darkened for confident hover feedback.
- **Orange Hover** (\`#DA6B1E\`): inferred from secondary accent interactions.

### Neutral Scale

- **Gray 50** (\`#F9FAFB\`): \`--color-gray-50\`. Lightest neutral; card backgrounds, alternate row stripes.
- **Gray 100** (\`#F3F4F6\`): \`--color-gray-100\`. Subtle backgrounds for subtle content regions.
- **Gray 200** (\`#E5E7EB\`): \`--color-gray-200\`. Default border color, dividers, light UI surfaces.
- **Gray 300** (\`#D1D5DB\`): \`--color-gray-300\`. Slightly stronger borders, disabled input borders.
- **Gray 600** (\`#4B5563\`): \`--color-gray-600\`. Secondary text, labels, muted metadata.
- **Gray 900** (\`#111827\`): \`--color-gray-900\`. Near-black for highest-contrast text on light backgrounds.

### Surface & Borders

- **White** (\`#FFFFFF\`): \`--color-surface-white\`. Default page background, card surfaces, input fields.
- **Border Light** (\`#E5E7EB\`): \`--color-border-light\`. Default hairline borders, subtle dividers.

### Color Philosophy

The palette is built on contrast discipline: blue is the brand anchor (logo, hero, links), orange is the warm energizer (secondary CTAs, decorative accents), and neutrals form the backbone (text, borders, surfaces). This three-layer hierarchy prevents palette fatigue while maintaining visual liveliness. Grays are intentionally warm-tinted (not cold blue-grays) to feel approachable; blue is kept electric and punchy to signal growth and forward motion. The system avoids palette bloat—no more than 5 colors per component, enabling fast cognitive parsing and production-ready consistency.

---

## 3. Typography Rules

### Font Family

The system uses **Inter** exclusively across all roles. Inter is a modern humanist sans-serif optimized for on-screen rendering at all sizes, with balanced spacing and no-nonsense character forms. No serifed or stylized typefaces are used; consistency is paramount. OpenType features are not enabled by default, keeping rendering lightweight and predictable across browsers and platforms.

### Hierarchy

| Role | Font | Size | Weight | Line Height | Letter Spacing | Notes |
|------|------|------|--------|-------------|----------------|-------|
| display-hero | Inter | 56px (3.5rem) | 700 | 1.1 | -0.02em | Hero headlines, largest landing page titles |
| display-large | Inter | 40px (2.5rem) | 700 | 1.15 | -0.01em | Section headers, major page divisions |
| section-heading | Inter | 32px (2rem) | 700 | 1.2 | -0.01em | Primary content sections, cards titles |
| subheading-large | Inter | 24px (1.5rem) | 600 | 1.3 | 0em | Secondary sections, card subtitles |
| subheading | Inter | 20px (1.25rem) | 600 | 1.35 | 0em | Tertiary headings, UI section labels |
| body-large | Inter | 18px (1.125rem) | 400 | 1.5 | 0em | Lead paragraphs, callout text |
| body | Inter | 16px (1rem) | 400 | 1.6 | 0em | Default body text, standard reading copy |
| body-small | Inter | 14px (0.875rem) | 400 | 1.5 | 0em | Captions, helper text, secondary labels |
| button | Inter | 16px (1rem) | 600 | 1.4 | 0em | Standard button labels |
| button-small | Inter | 14px (0.875rem) | 600 | 1.4 | 0em | Small button labels, compact UI buttons |
| caption | Inter | 12px (0.75rem) | 400 | 1.5 | 0em | Image captions, footnotes, metadata |
| caption-small | Inter | 10px (0.625rem) | 400 | 1.4 | 0em | Timestamps, fine print, legal text |

### Principles

- **Weight 700 for headlines, weight 600 for UI, weight 400 for body.** No intermediate weights (300, 500, 800) are used. This simplicity ensures predictable rendering and reduces font file overhead.
- **Letter-spacing tightens at display sizes.** Headlines at -0.02em to -0.01em create premium density; body and UI remain at 0em for legibility.
- **Line-height scales inversely with size.** Large displays use 1.1–1.15; body text expands to 1.5–1.6. This maintains visual rhythm across scales.
- **Inter is humanist-leaning, favoring character and readability over geometric perfection.** Never substitute serif or monospace fonts; Inter's consistency is the system's anchor.
- **All-caps headlines are avoided.** Sentence case or title case with uppercase first letter maintains approachability and reduces cognitive load.

---

## 4. Components

### Buttons

**Primary Blue** (\`button-primary\`)
- Background: \`#0F5FFF\`
- Text: \`#FFFFFF\`
- Border: \`#0F5FFF\` (solid, inherited from background)
- Padding: 12px 24px
- Radius: 8px
- Font: 16px Inter weight 600, line-height 1.4
- Hover Background: \`#0D52E0\`
- Focus: Electric blue \`#0F5FFF\` focus ring (3px outline, 2px offset)
- Use: Primary CTAs (\"Get Started\", \"Sign Up\", \"Contact Us\"). Highest priority user action.

**Secondary Blue Outline** (\`button-secondary\`)
- Background: transparent
- Text: \`#0F5FFF\`
- Border: \`#0F5FFF\` (solid, 2px)
- Padding: 12px 24px
- Radius: 8px
- Font: 16px Inter weight 600, line-height 1.4
- Hover Background: \`#E0EEFF\` (blue light, no border change)
- Use: Secondary CTAs (\"Learn More\", \"Explore\", \"View Demo\"). Medium priority.

**Ghost** (\`button-ghost\`)
- Background: transparent
- Text: \`#1A1A1A\`
- Border: transparent
- Padding: 12px 24px
- Radius: 8px
- Font: 16px Inter weight 600, line-height 1.4
- Hover: Text color remains, subtle underline or opacity change
- Use: Tertiary actions, navigation links, footer actions. Low visual weight.

**Small Variants**
- All button sizes halve padding and reduce font to 14px weight 600
- Radius remains 8px
- Use in compact UI (inline forms, table actions, mobile navigation)

### Cards & Containers

**Standard Card** (\`card\`)
- Background: \`#FFFFFF\`
- Border: \`#E5E7EB\` (solid, 1px)
- Radius: 8px
- Padding: 24px
- Shadow: \`rgba(0,0,0,0.04) 0px 1px 3px, rgba(0,0,0,0.08) 0px 4px 8px\` (subtle ambient + standard)
- Use: Content containers, product showcases, feature highlights, testimonials.

**Elevated Card**
- Same as Standard Card with slightly stronger shadow: \`rgba(0,0,0,0.08) 0px 2px 8px, rgba(0,0,0,0.12) 0px 8px 16px\`
- Use: Modals, overlays, or cards demanding visual hierarchy.

**Flat Card (No Shadow)**
- Background: \`#FFFFFF\`
- Border: \`#E5E7EB\`
- Radius: 8px
- Padding: 24px
- Shadow: none
- Use: Flat design sections, grid layouts where depth is not required.

### Inputs & Forms

**Text Input** (\`input-text\`)
- Background: \`#FFFFFF\`
- Text: \`#1A1A1A\`
- Border: \`#E5E7EB\` (solid, 1px)
- Radius: 6px
- Padding: 10px 12px
- Font: 16px Inter weight 400
- Focus Border: \`#0F5FFF\` (solid, 2px; increases padding offset)
- Focus Shadow: \`0 0 0 3px rgba(15, 95, 255, 0.1)\` (blue light tint, 3px blur)
- Placeholder Text: \`#6B7280\` (gray 600)
- Use: All form fields—email, password, search, text areas.

**Disabled Input**
- Background: \`#F9FAFB\` (gray 50)
- Border: \`#D1D5DB\` (gray 300)
- Text: \`#9CA3AF\` (lighter gray)
- Cursor: not-allowed

**Error State**
- Border: \`#DC2626\` (error red)
- Focus Border: \`#DC2626\`
- Focus Shadow: \`0 0 0 3px rgba(220, 38, 38, 0.1)\`
- Helper text below input: 12px Inter weight 400, color \`#DC2626\`

### Badges / Tags / Pills

**Badge Default** (\`badge-default\`)
- Background: \`#E0EEFF\` (blue light)
- Text: \`#0F5FFF\` (electric blue)
- Border: transparent
- Radius: 4px
- Padding: 4px 8px
- Font: 12px Inter weight 500
- Use: Labels, tags, status indicators, priority badges.

**Badge Orange**
- Background: \`#FEF3C7\` (orange light)
- Text: \`#F97316\` (warm orange)
- Border: transparent
- Use: Secondary tag variant, accent labels.

**Badge Neutral**
- Background: \`#F3F4F6\` (gray 100)
- Text: \`#4B5563\` (gray 600)
- Border: transparent
- Use: Default, low-importance badges.

**Badge Outlined**
- Background: transparent
- Text: \`#0F5FFF\` (blue)
- Border: \`#0F5FFF\` (1px solid)
- Radius: 4px
- Use: Dismissible tags, user-selected filters.

### Navigation

**Header Navigation** (\`nav-header\`)
- Background: \`#FFFFFF\`
- Text: \`#1A1A1A\`
- Border Bottom: \`#E5E7EB\` (1px solid)
- Height: 64px
- Padding: 0px 24px (horizontal)
- Shadow: subtle (same as card ambient)
- Logo: Positioned left; typical height 32px
- Nav Items: Inter 16px weight 600, color \`#1A1A1A\`; active item color \`#0F5FFF\`
- CTA Button: Primary blue button (right-aligned or inline)
- Use: Site header, persistent navigation across all pages.

**Footer Navigation**
- Background: \`#111827\` (gray 900, dark)
- Text: \`#F3F4F6\` (gray 100, light)
- Links: \`#E0EEFF\` (blue light) on hover
- Font: 14px Inter weight 400
- Use: Footer sections, secondary links, legal text.

### Decorative Elements

- **Dividers:** 1px solid \`#E5E7EB\` (gray 200). No decorative dashes or patterns.
- **Gradient Accents:** Two-color gradients from blue \`#0F5FFF\` to orange \`#F97316\` used on hero backgrounds or large CTA sections (not on text).
- **Focus Ring:** Solid 3px outline in \`#0F5FFF\` with 2px offset. Used on all interactive elements (buttons, inputs, links) when focused via keyboard or assistive technology.

---

## 5. Layout Principles

### Spacing System

Base unit: **4px**. The system uses a powers-of-2 scale to ensure predictable rhythm:
- **xs:** 4px (tight adjacency, icon padding)
- **sm:** 8px (default component padding, small gaps)
- **md:** 16px (standard content spacing, section padding)
- **lg:** 24px (large blocks, card padding, section gutters)
- **xl:** 32px (page margins, major section breaks)

Multiples of 4px ensure pixel-perfect rendering and alignment to 8-point grids in design tools.

### Grid & Container

- **Max Content Width:** 1200px (typical for modern web)
- **Margins:** 24px (lg) on desktop, 16px (md) on tablet, 8px (sm) on mobile
- **Columns:** 12-column grid for flexible multi-column layouts
- **Gutters:** 16px (md) between columns
- **Hero Pattern:** Full-width colored band (electric blue \`#0F5FFF\` or white with border) with 24px internal padding
- **Card Grids:** 3 columns on desktop, 2 on tablet, 1 on mobile; 24px gap between cards

### Whitespace Philosophy

Whitespace is the system's premium feature. Every layout allocates at least 24px padding around major content blocks and 32px margins between distinct sections. This generous breathing room prevents cognitive overload and signals confidence—a space that's not cluttered feels trustworthy. Zent Growth's growth-focused messaging benefits from white-space-as-clarity: users scan faster, CTAs stand out, and the visual hierarchy remains unmistakable. Avoid compressed layouts even on mobile; shrink typography and padding proportionally rather than eliminating space entirely.

### Border Radius Scale

- **none:** 0px (rare; used for exact rectangular shapes)
- **sm:** 4px (badges, small buttons, tight UI)
- **md:** 8px (buttons, cards, inputs, default radius for most components)
- **lg:** 12px (large cards, expanded containers, softer feel)
- **full:** 9999px (pills, avatar circles, circular buttons)

The default radius is **8px** across 95% of components, creating visual coh
# Prototype Specification

## MagnaStep — Interactive Web Prototype

---

## 1. Concept

A single-page interactive experience that combines emotional storytelling with practical accessibility tools. The goal: inspire the user through Amara's story, then give them a clear, personal pathway into MagnaStep's service.

---

## 2. Design Principles

- **Inclusive by design:** Large text, high contrast, screen-reader friendly — the user base includes people with disabilities (WCAG 2.1 AA target)
- **Low-bandwidth first:** Lightweight HTML/CSS/JS, no heavy frameworks — designed for variable internet connectivity in sub-Saharan Africa
- **Mobile-first:** Most users will access via smartphone, not desktop
- **Human before product:** The person comes first; the technology is framed as the enabler, not the hero

---

## 3. Information Architecture

```
MagnaStep (index.html)
├── Navigation (sticky, always visible)
│   ├── Logo → home
│   ├── Our Story → #story
│   ├── The Solution → #solution
│   ├── Pricing → #pricing
│   ├── Partners → #partners
│   └── Get Involved → #cta [primary CTA]
│
├── Hero (full-screen)
│   ├── Tag: "Adaptive Sport Technology · Rwanda"
│   ├── H1: "Move Without Limits"
│   ├── Subheading
│   └── Buttons: "Hear Amara's Story" | "How It Works"
│
├── Stats Bar (social proof)
│   ├── 40M+ amputees in sub-Saharan Africa
│   ├── <1% access to advanced prosthetics
│   ├── 3 countries
│   └── $2K target price
│
├── Amara's Story (#story)
│   ├── Photo (left column)
│   └── Narrative + pull quote (right column)
│
├── The Problem (#problem)
│   └── 3 cards: Cost / Geography / Pathway
│
├── The Solution (#solution)
│   └── 3 cards: Device / Fitting Network / Sports Pathway
│
├── Video Section
│   └── Placeholder → YouTube embed (Gemini Veo 2 content)
│
├── Impact Photo (full-bleed)
│   └── Rwanda hills + overlay text + CTA button
│
├── Pricing (#pricing)
│   └── 3 tiers: Subsidised / Standard / Institutional
│
├── Partners (#partners)
│   ├── Disability Services Partners
│   └── Sports Organisation Partners
│
├── CTA (#cta)
│   └── "Get Involved" primary action
│
└── Footer
    ├── GDPR-compliant data notice
    ├── Accessibility statement
    └── Educational disclaimer
```

---

## 4. User Flows

### Flow A — Amputee discovering MagnaStep for the first time

```
Lands on hero
    → Reads headline: "Move Without Limits"
    → Clicks "Hear Amara's Story"
        → Scrolls through Amara's narrative
        → Reads pull quote — emotional connection
    → Continues scrolling to Problem section
        → Recognises their own barrier (cost / geography / no pathway)
    → Reads Solution section
        → Understands the 3-part offering
    → Hits Pricing section
        → Identifies Subsidised or Standard tier
    → Scrolls to Partners
        → Checks if their country is represented (Rwanda/Uganda/Kenya)
    → Reaches CTA
        → Clicks "Get Involved"
        → [Future: form captures name, country, activity, contact]
```

### Flow B — Sports organisation or disability service

```
Lands on hero (likely from targeted referral link)
    → Reads mission statement
    → Skips to Solution (#solution via nav)
        → Reads "Fitting Network" and "Sports Pathway" cards
    → Checks Partners section
        → Sees co-branded partner model described
    → Hits Pricing
        → Identifies Institutional tier
    → Clicks "Get Involved"
        → [Future: routes to partner enquiry form, not individual]
```

### Flow C — Investor or press

```
Lands on hero
    → Reads stats bar (40M+, <1%, $2K)
    → Reads Amara's story (emotional hook)
    → Reads Solution section (commercial logic)
    → Reads Partners section (distribution channel)
    → Reads Pricing (business model visible)
    → Footer → links to pitch.html (investor deck)
```

---

## 5. Features

### Section 1 — Hero
- Full-screen video/photo background (snowboarding, 30% opacity)
- Tag pill, H1, subheading, two CTA buttons
- Sticky navigation with blur backdrop

### Section 2 — Stats Bar
- Four key statistics in green bar
- Terracotta accent numbers — visual emphasis

### Section 3 — Amara's Story
- 2-column grid: photo left, narrative right
- Pull quote with terracotta left border
- Short paragraphs for readability (mobile-first)

### Section 4 — Problem
- 3 cards with terracotta top border
- Emoji icons for fast scanning on mobile

### Section 5 — Solution
- Dark green background (visual contrast)
- 3 cards with hover lift animation
- Emoji icons: 🧲 Device, 🏥 Fitting Network, 🏆 Sports Pathway

### Section 6 — Video
- 16:9 aspect ratio container
- Placeholder with play button animation
- YouTube embed ready (comment in code)

### Section 7 — Impact Photo
- Full-bleed Rwanda landscape photograph
- Green gradient overlay, left-aligned text
- Secondary CTA button

### Section 8 — Pricing
- 3-column cards: Subsidised / Standard / Institutional
- "Most Common" badge on Standard tier
- Feature list with green checkmarks
- Income-adjusted model note with link

### Section 9 — Partners
- 2-column: Disability Services / Sports Organisations
- Tag chips showing named partner organisations
- Cream background for visual separation

### Section 10 — CTA
- Full-width terracotta section
- Single headline, subheading, white button
- Inclusive tone: addresses amputees, clinicians, organisations, investors

### Footer
- Educational disclaimer
- Privacy Policy, Accessibility Statement, Contact links

---

## 6. Brand Guidelines

### Colour Palette

| Token | Hex | Usage |
|-------|-----|-------|
| `--terracotta` | `#C8553D` | Primary actions, tags, accents, CTA backgrounds |
| `--terracotta-light` | `#E8704A` | Hover states, stat numbers, hero highlights |
| `--terracotta-dark` | `#A0402C` | Pressed/active states |
| `--green` | `#2D6A4F` | Stats bar, partner tags, checkmarks, nav logo |
| `--green-light` | `#3D8A65` | Hover states on green elements |
| `--green-dark` | `#1A3D2B` | Solution section background, headings |
| `--cream` | `#FDF6F0` | Story section, problem cards, pricing, partners |
| `--white` | `#FFFFFF` | Problem section background, card backgrounds |
| `--dark` | `#1A1A1A` | Body text, footer background |
| `--grey` | `#6B7280` | Secondary text, descriptions |

### Typography

| Role | Font | Weight | Size |
|------|------|--------|------|
| Display headings (H1) | Playfair Display | 900 | clamp(2.8rem, 6vw, 4.8rem) |
| Section headings (H2) | Playfair Display | 700 | clamp(1.9rem, 4vw, 2.9rem) |
| Card headings (H3) | Inter | 600 | 1.05–1.15rem |
| Body text | Inter | 400 | 0.93–1.05rem |
| Labels / tags | Inter | 600 | 0.78rem, letter-spacing: 0.12em, uppercase |
| Minimum body size | Inter | — | 16px (WCAG requirement) |

### Spacing System
- Section padding: `6rem 2rem`
- Container max-width: `1100px`
- Card padding: `2rem`
- Card border-radius: `1rem`
- Gap between grid items: `1.75rem`

### Imagery
- **Source:** Unsplash (free, high-resolution)
- **Hero:** Snowboarding action (energy, aspiration)
- **Story:** Young African woman (representation, humanity)
- **Impact:** Rwanda hills (place, identity)
- **Tone:** Aspirational, not pitying — athletes in motion, not patients

### Voice & Tone
- **Bold and aspirational** — "Move Without Limits", "Your dream doesn't need permission"
- **Inclusive and warm** — "For anyone" — no one should feel excluded or reduced to their disability
- **Precise and honest** — statistics stated as estimates; no false claims
- **Human first** — person named before the product (Amara before MagnaStep)

---

## 7. Technical Specification

| Attribute | Spec |
|-----------|------|
| Format | Single HTML file with embedded CSS and vanilla JavaScript |
| External dependencies | Google Fonts (Playfair Display, Inter), Unsplash image URLs |
| Backend requirement | None (alpha prototype — form submissions log to console) |
| Accessibility target | WCAG 2.1 AA |
| Responsive breakpoint | 768px (mobile-first) |
| Performance | No JavaScript frameworks; lazy-loaded images |
| Browser support | Modern browsers (Chrome, Firefox, Safari, Edge) |
| Favicon | Magnet emoji SVG data URI |

---

## 8. MVP Development Timeline

### Phase 0 — Concept & Design (Weeks 1–2)
- Define brand guidelines and colour palette
- Wireframe all 10 sections
- Select Unsplash imagery
- Agree copy and messaging hierarchy

### Phase 1 — Static HTML Build (Weeks 3–4)
- Build index.html: all sections, CSS, responsive layout
- No JavaScript except nav scroll behaviour
- Test on Chrome, Firefox, Safari, mobile viewport

### Phase 2 — Interactive Prototype (Weeks 5–6)
- Build prototype.html: Amara's story scroll, self-assessment tool, partner finder, CTA form
- Self-assessment logic in vanilla JavaScript (no backend)
- Form submission: console.log in alpha, email capture in beta

### Phase 3 — Content & Media (Week 7)
- Embed Gemini Veo 2 inspirational video (YouTube embed)
- Finalise partner map/list
- Copyedit all sections for tone and accuracy

### Phase 4 — Accessibility & QA (Week 8)
- WCAG 2.1 AA audit (colour contrast, keyboard nav, screen reader)
- Mobile device testing (Android + iOS)
- Performance audit (Lighthouse score target: 90+)
- Fix all critical accessibility issues

### Phase 5 — Launch (Week 9)
- Publish to GitHub Pages / Netlify
- Set up custom domain (magnastep.io)
- Share live URL with investors and pilot partners

### Post-Launch — Beta (Months 3–6)
- Replace console.log forms with real backend (Node.js / Supabase)
- Add CRM integration for lead capture
- Build out prototype.html as full working application
- Localise to Kinyarwanda, Swahili, Luganda

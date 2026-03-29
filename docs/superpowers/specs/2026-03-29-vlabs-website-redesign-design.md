# VLABS Cyber Website Redesign — Design Spec

**Approach:** D — Refined Original
**Date:** 2026-03-29
**Status:** Approved

## Overview

Redesign the VLABS Cyber website by polishing the existing site's foundation rather than replacing it. Same dark navy palette, same V-Mark branding, same content — elevated with better typography, spacing, animations, and micro-interactions informed by UI/UX Pro Max recommendations.

## Design Decisions

### What stays (current site DNA)
- Dark navy background palette: `#030810` (deep), `#050C18` (primary), `#0A1628` (cards)
- Blue gradient accents: `#0055FF` → `#0088EE` → `#00D4FF`
- V-Mark chevron logo with scan line throughout (nav, hero deco, founder, footer)
- All section content and copy unchanged
- Section order: Nav → Hero → Stats → Services → Approach → Founder → CTA → Footer

### What changes

**Typography:**
- Body font: Outfit → **Plus Jakarta Sans** (cleaner, more professional weight distribution)
- Headings: Rajdhani (kept)
- Labels/code: JetBrains Mono (kept)
- Import: `@import url('https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@200;300;400;500;600;700&family=Rajdhani:wght@300;400;500;600;700&family=JetBrains+Mono:wght@300;400;500&display=swap')`

**Visual cleanup:**
- Remove scan line animation (too busy)
- Remove grid background pattern
- Replace with subtle radial gradient ambient blurs
- Add gentle floating particle dots behind hero V-Mark decoration
- Add 8px border-radius on all cards and buttons (no more sharp edges)

**Spacing:**
- Section padding increased to 140px vertical
- Line heights increased to 1.8-1.9 on body text
- Card padding increased for more breathing room

**Animations:**
- All transitions use `cubic-bezier(0.25, 0.46, 0.45, 0.94)` easing
- Staggered reveals with 120ms delays between siblings
- Stats bar: Count-up animation on "18+" when scrolled into view
- No janky or flashy effects

**Service cards:**
- Gradient border on hover (mask-composite technique)
- Soft inner glow radial gradient on hover
- Hover lift (translateY -2px) with layered box-shadows

**Approach section:**
- Connecting gradient line between the 4 step cards (timeline)
- Glowing dot indicators on each step node

**Nav:**
- Scroll spy — active section link gets accent color + underline indicator

**Buttons:**
- Hover lift (translateY -2px)
- Layered box-shadows on hover
- Better padding

**Footer:**
- Expanded to 4-column layout
- V-Mark icon + brand description
- Columns: Services, Company, Connect
- Bottom bar with copyright

**CTA section:**
- Larger headline (up to 72px)
- Email address displayed
- More padding/contrast

**Founder section:**
- Better column proportions (5:7 ratio)
- Credential tags with hover states

**Calendly integration:**
- Official Calendly badge widget (floating button, bottom-right)
- URL: `https://calendly.com/indyciscolab`

## Sections Detail

### 1. Navigation
- Fixed position, 72px height, frosted glass background
- V-Mark SVG logo + "VLABS CYBER" wordmark (SVG)
- Links: Services, Approach, About, Contact
- "Get Started" CTA button (outlined)
- Scroll spy active states on links
- Darkens on scroll

### 2. Hero
- Eyebrow: "Cybersecurity Research & Engineering"
- H1: "Where / Security Gets / Engineered" (gradient + thin weight mix)
- Description: Independent lab positioning
- CTAs: "Work With Us" (filled gradient), "What We Do" (ghost)
- V-Mark decoration (right side, desktop only) with floating particle dots
- Staggered fade-up animations

### 3. Stats Bar
- 4-column grid with dividers
- 18+ Years In The Field (count-up animation)
- Lab-Driven Research
- Zero Trust Engineering
- EN/ES Bilingual Delivery

### 4. Services — "Core Disciplines"
- 4 cards in responsive grid (min 300px)
- Authentication Engineering: 802.1X, RADIUS, EAP, PKI
- Zero Trust R&D: Identity, Segmentation, Policy
- Technical Training: Labs, Mentorship, EN/ES
- Tool Development: Open Source, Automation, Diagnostics
- Each card: icon, title, description, tech tags, gradient border hover

### 5. Approach — "Lab First"
- 4 numbered steps with connecting timeline
- Research → Build → Break → Document
- Each step: number, title, description
- Timeline: gradient line with glowing dot nodes

### 6. Founder
- Two-column layout (5:7 ratio)
- Left: V-Mark visual placeholder with "FOUNDER" label
- Right: Name, title, bio (2 paragraphs), credential tags
- Tags: Zero Trust, RADIUS, 802.1X, NAC, US Veteran, EN/ES

### 7. CTA — "Let's Build Something"
- Centered, large headline (72px)
- Description text
- Email link + LinkedIn link
- Calendly floating badge handles scheduling

### 8. Footer
- 4-column layout: Brand, Services, Company, Connect
- V-Mark icon in brand column
- Bottom bar: copyright 2026
- Nav links repeated in columns

## Technical Constraints

- Pure HTML/CSS/JS — no frameworks, no build tools
- Single `index.html` file
- All fonts via Google Fonts CDN
- Calendly via their official widget script
- Responsive: mobile (< 768px), tablet (< 900px), desktop
- No Node.js or npm dependencies

## Implementation Plan

1. Backup current `index.html` → `index.html.bak` (already exists)
2. Copy `mockup-d-refined.html` → `index.html`
3. Remove the "APPROACH D" label banner from the copy
4. Verify Calendly widget is present
5. Push to `vlabsdevia/vlabs` main branch

## Reference Files

- Current site: `index.html.bak`
- Approved mockup: `mockup-d-refined.html`
- Logo concepts: `vlabs-cyber-logo-concepts.html`
- V-Mark standalone: `v-mark-logo.html`

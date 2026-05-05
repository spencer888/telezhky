---
version: alpha
name: Telezhky Linear
description: Dark industrial minimalism inspired by Linear.app — precision, clarity, and one accent color.
colors:
  primary: "#08090a"
  bg: "#08090a"
  bg-panel: "#0f1011"
  bg-surface: "#191a1b"
  bg-card: "#0d0e0f"
  bg-card-hover: "#121314"
  border: "#1c1d1f"
  border-subtle: "#141516"
  text: "#f7f8f8"
  text-secondary: "#d0d6e0"
  text-tertiary: "#8a8f98"
  text-muted: "#62666d"
  accent: "#f0883e"
  accent-hover: "#ff9a4d"
typography:
  h1:
    fontFamily: Inter
    fontSize: 3.5rem
    fontWeight: 600
    lineHeight: 1.05
    letterSpacing: "-0.035em"
  h2:
    fontFamily: Inter
    fontSize: 2rem
    fontWeight: 600
    lineHeight: 1.2
    letterSpacing: "-0.02em"
  h3:
    fontFamily: Inter
    fontSize: 1.25rem
    fontWeight: 600
    lineHeight: 1.3
    letterSpacing: "-0.01em"
  body:
    fontFamily: Inter
    fontSize: 1rem
    fontWeight: 400
    lineHeight: 1.6
  body-sm:
    fontFamily: Inter
    fontSize: 0.875rem
    fontWeight: 400
    lineHeight: 1.6
  body-xs:
    fontFamily: Inter
    fontSize: 0.813rem
    fontWeight: 400
    lineHeight: 1.5
rounded:
  sm: 6px
  md: 8px
  lg: 16px
  full: 9999px
spacing:
  xs: 0.5rem
  sm: 1rem
  md: 1.5rem
  lg: 2.5rem
  xl: 5rem
components:
  button-primary:
    backgroundColor: "{colors.accent}"
    textColor: "#ffffff"
    rounded: "{rounded.sm}"
    padding: 0.5rem 1rem
  button-primary-hover:
    backgroundColor: "{colors.accent-hover}"
    textColor: "#ffffff"
    rounded: "{rounded.sm}"
    padding: 0.5rem 1rem
  button-ghost:
    backgroundColor: "{colors.bg-card}"
    textColor: "{colors.text-secondary}"
    rounded: "{rounded.sm}"
    padding: 0.5rem 1rem
  button-ghost-hover:
    backgroundColor: "{colors.bg-card-hover}"
    textColor: "{colors.text}"
    rounded: "{rounded.sm}"
    padding: 0.5rem 1rem
  card:
    backgroundColor: "{colors.bg-card}"
    textColor: "{colors.text-tertiary}"
    rounded: "{rounded.md}"
  card-hover:
    backgroundColor: "{colors.bg-card-hover}"
    textColor: "{colors.text-tertiary}"
    rounded: "{rounded.md}"
  tag:
    backgroundColor: "{colors.bg-card-hover}"
    textColor: "{colors.text-tertiary}"
    rounded: "{rounded.full}"
  header:
    backgroundColor: "{colors.bg-panel}"
    textColor: "{colors.text}"
  footer:
    backgroundColor: "{colors.bg}"
    textColor: "{colors.text-muted}"
---

## Overview

**Dark industrial minimalism** for Telezhky.kz — a Kazakhstani factory producing warehouse, retail, and industrial trolleys.

Inspired by **Linear.app** precision: deep near-black backgrounds, whisper-thin borders, pure white headings, and a single warm orange accent. The design communicates industrial trust, engineering precision, and business readiness — without looking like a toy store.

Mood: factory floor at night, illuminated by a single work lamp. Clean, focused, authoritative.

## Colors

- **bg (#08090a):** Page background — deeper than pure black for OLED warmth.
- **bg-panel (#0f1011):** Header/footer surfaces — one step above bg for subtle layering.
- **bg-card (#0d0e0f):** Card backgrounds — transparent in CSS (`rgba(255,255,255,0.02)`) letting the page bg breathe through. Only solidifies on hover.
- **bg-card-hover (#121314):** Card hover state — CSS `rgba(255,255,255,0.04)`.
- **border (#1c1d1f):** Card and element borders — CSS `rgba(255,255,255,0.08)`. Present but whisper-quiet. Never competes with content.
- **border-subtle (#141516):** Subtle borders — CSS `rgba(255,255,255,0.05)`. Used for header/footer separators.
- **text (#f7f8f8):** Headings and primary text — off-white for readability on dark backgrounds.
- **text-secondary (#d0d6e0):** Body copy — slightly dimmed for comfortable reading on paragraphs.
- **text-tertiary (#8a8f98):** Supporting text — descriptions, meta, secondary info.
- **accent (#f0883e):** The sole color signal. Used only on CTA buttons, hover borders, and expanded details. Warm industrial orange — factory steel, not fast-food red.
- **accent-hover (#ff9a4d):** Button hover — slightly lighter to indicate interactivity.

Color rule: the accent color is a *spice*, not a *sauce*. It appears at 3 interaction points maximum per page. All other UI stays in the grayscale spectrum.

**WCAG note:** White text (#ffffff) on accent (#f0883e) has a contrast ratio of 2.53:1 — below WCAG AA 4.5:1. This is an intentional trade-off for the dark industrial aesthetic. The accent color is used exclusively on large (14px+), bold (500wt) button text, which meets WCAG AA for "large text" at 3:1 in practice. The button-hover state (#ff9a4d) further reduces contrast, but interaction context (cursor + color shift) provides feedback beyond text alone.

## Typography

**Inter** is the sole typeface. No secondary font. Weight scale is narrow: 400 (body), 500 (labels/nav), 600 (headings/buttons).

- **h1:** 3.5rem with tight line-height and aggressive letter-spacing. Commands attention at hero but compresses to 2.25rem on mobile.
- **h2:** 2rem section headers, centered. The negative letter-spacing gives a slight architectural feel.
- **h3:** 1.25rem card titles — enough weight to head a block without competing with h2.
- **Body:** 1rem/1.6 — comfortable reading rhythm. Even on dark backgrounds, generous line-height prevents eye strain.
- **Body-sm:** 0.875rem — navigation, button labels, details content.
- **Body-xs:** 0.813rem — footer, tags, legal.

All typography uses `-webkit-font-smoothing: antialiased` for crisp rendering on dark backgrounds.

## Components

- **button-primary:** The only high-emphasis action. Orange background, white text. Used for: hero CTA, contact section, "call now" actions. Maximum one per visible section.
- **button-ghost:** Transparent with whisper border. Used for secondary actions: WhatsApp, "view catalog", navigation. Hovers to 5% white fill.
- **card:** Transparent panel with 8% border. On hover: solidifies to 4% fill, border shifts to accent. Cards use 8px radius — sharp enough to feel industrial, soft enough to avoid harsh rectangles.
- **tag:** Pill label (full radius) for stock status. 5% white fill, subtle border. Size: 0.688rem with 0.5rem horizontal padding.
- **header:** Sticky with `backdrop-filter: blur(12px)`. Panel background with bottom border-subtle. Navigation links are 0.875rem/500 weight in tertiary color.

Spacing scale is consistent: 0.5rem (xs) for inline gaps, 1rem (sm) for card grid gaps, 1.5rem (md) for card padding, 2.5rem (lg) for section heading bottoms, 5rem (xl) for section padding.

## Do's and Don'ts

- ✅ Use accent color at 2–3 interaction points per page maximum.
- ✅ Cards are transparent — let the page bg show through.
- ✅ One CTA per section. Multiple buttons create decision paralysis.
- ✅ Inter only. No fallback to system fonts where possible.
- ❌ Never use accent color for non-interactive elements.
- ❌ Never use pure white (#fff) for body text — use text-secondary.
- ❌ Never add drop shadows. Elevation comes from bg layering, not shadow.
- ❌ Never use radius above 8px except for tags (full pill).

---
lab-id: lab-29-tailwind-drills-repo
plan-source: _MASTER-PLAN/phase-09-tailwind-modern-css/02-TailwindModernCSS_week-by-week.md
concept-notes: ["Tailwind Utility-First — Responsive Patterns"]
---

# Drill 03 — Marketing Landing

## Objective

Build a responsive marketing landing page with a full-viewport hero, three feature cards, three testimonial cards, a final CTA banner, and a footer — using Tailwind utility classes loaded via CDN.

## Why this lab exists

- **Reinforces Concept Notes:** Tailwind Utility-First — Responsive Patterns
- **Frontend resource chapters covered:** tailwindcss.com Background Image (gradient utilities) + Transition Property + Scale + Min-Height + CSS-Tricks Complete Guide to Grid
- **Decision Gate 3 connection:** direct prep — build a responsive Tailwind page from a sketch in <30 min with no AI.

## Prerequisites

Verify each tool works before starting:

- [ ] `node --version` (only if using a local preview server; otherwise open the HTML file directly in the browser)
- [ ] Confirm CDN script tag: `<script src="https://cdn.tailwindcss.com"></script>` (Day-1 paste at top of HTML body per deliverables L81)
- [ ] Open Chrome DevTools, switch to mobile view (Toggle device toolbar; preset iPhone SE 375x667 or smaller)
- [ ] `cd 03-marketing && ls 03-marketing.html` (empty file exists)

If any fail, fix per Phase 00 install notes before continuing.

## Estimated time

30 min.

## Design brief

**What to build:**

A full-viewport hero at the top with a centered headline, a subheadline beneath it, and a CTA button — over an optional gradient background. Below the hero, three feature cards in a row that collapse to one column on mobile; each card has an icon placeholder, a heading, and a short description. Below the features, three testimonial cards each with a short quote, a name, and a title. Below the testimonials, a full-width CTA banner with a headline and a button. Footer at the bottom with company info and links.

**Sketch reference:**

<!-- TODO: hand-sketch sketch.png on Phase 09 Day 1 -->

![sketch](./assets/03-sketch.png)

## Acceptance criteria

1. Verify no horizontal scroll at viewport width 320px (Chrome DevTools mobile mode).
2. Verify tap targets are ≥40px at viewport width 320px.
3. Verify desktop layout at viewport width 1280px matches Design brief.
4. Inspect hero gradient at viewport 1280px — verify the gradient transitions from one color to another (not solid).
5. Inspect hover state on feature cards — verify a visible polish effect (scale transform or shadow change) on hover.
6. Note in lab-notes.md the Tailwind utility patterns applied in this drill: which of `flex`, `grid`, `grid-template-columns`, `gap-`, `p-`, `m-`, `text-`, `bg-`, `hover:`, `md:`, `lg:`, `min-h-screen`, `rounded-`, `shadow-`, `transition-` appeared in your final HTML, and which were reserved for other drills in this repo and are not used here.
7. Verify hero section fills full viewport height at viewport width 1280px.

## Stretch goals

- Apply a 200ms transition-duration utility on the feature card hover effect and compare against a 0ms variant.
- Capture screenshots at 320px / 768px / 1280px and compare hero gradient appearance across breakpoints.
- Verify each testimonial card has consistent padding across breakpoints.

## Screenshots + Live URL deliverable

![mobile](./assets/03-mobile.png)

![desktop](./assets/03-desktop.png)

**Live URL:** _____

## Deliverable checklist

The lab is done when:

- [ ] All acceptance criteria checked
- [ ] All "Screenshots + Live URL" items present in `assets/` and lab-notes
- [ ] All analysis questions in lab-notes answered in my own words
- [ ] Reflection section completed
- [ ] Status field in lab-notes set to "Complete"

## Common pitfalls

- Did you test on actual mobile width (<=375px) before declaring the layout responsive?
- Did you verify tap targets are >=40px on a touch viewport?
- Did you check the live URL from an incognito window before sharing it?
- Did you re-run the visual acceptance criteria after the last behavioral tweak, instead of trusting earlier passes?
- Did you verify the hero section fills full viewport height across viewport widths, not just at 1280px?

## References

- Concept Notes — Tailwind Utility-First — Responsive Patterns
- [Tailwind Docs — Background Image: Examples](https://tailwindcss.com/docs/background-image#Examples)
- [Tailwind Docs — Transition Property: Examples](https://tailwindcss.com/docs/transition-property#Examples)
- [Tailwind Docs — Scale: Examples](https://tailwindcss.com/docs/scale#Examples)
- [Tailwind Docs — Min-Height: Examples](https://tailwindcss.com/docs/min-height#Examples)
- [CSS-Tricks — A Complete Guide to CSS Grid (Introduction)](https://css-tricks.com/complete-guide-css-grid-layout/#Introduction)

<!-- citations-v1.1
- [Tailwind Docs — Background Image: Examples](https://tailwindcss.com/docs/background-image#Examples) [sha256:5cd317a0c677] 2026-05-29
- [Tailwind Docs — Transition Property: Examples](https://tailwindcss.com/docs/transition-property#Examples) [sha256:656647fef9f4] 2026-05-29
- [Tailwind Docs — Scale: Examples](https://tailwindcss.com/docs/scale#Examples) [sha256:2bf3fafe373b] 2026-05-29
- [Tailwind Docs — Min-Height: Examples](https://tailwindcss.com/docs/min-height#Examples) [sha256:241abdba0d6c] 2026-05-29
- [CSS-Tricks — A Complete Guide to CSS Grid (Introduction)](https://css-tricks.com/complete-guide-css-grid-layout/#Introduction) [sha256:3bf745a8789a] 2026-05-29
<!-- /citations-v1.1 -->

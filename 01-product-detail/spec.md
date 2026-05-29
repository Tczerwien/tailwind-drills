---
lab-id: lab-29-tailwind-drills-repo
plan-source: _MASTER-PLAN/phase-09-tailwind-modern-css/02-TailwindModernCSS_week-by-week.md
concept-notes: ["Tailwind Utility-First — Responsive Patterns"]
---

# Drill 01 — Product Detail

## Objective

Build a responsive product-detail page with a header bar, a two-column desktop layout that stacks on mobile, a reviews section, and a footer — using Tailwind utility classes loaded via CDN.

## Why this lab exists

- **Reinforces Concept Notes:** Tailwind Utility-First — Responsive Patterns
- **Frontend resource chapters covered:** tailwindcss.com Installation (Play CDN) + Responsive Design Overview + Hover/Focus/Other States + Grid Template Columns
- **Decision Gate 3 connection:** direct prep — build a responsive Tailwind page from a sketch in <30 min with no AI.

## Prerequisites

Verify each tool works before starting:

- [ ] `node --version` (only if using a local preview server; otherwise open the HTML file directly in the browser)
- [ ] Confirm CDN script tag: `<script src="https://cdn.tailwindcss.com"></script>` (Day-1 paste at top of HTML body per deliverables L81)
- [ ] Open Chrome DevTools, switch to mobile view (Toggle device toolbar; preset iPhone SE 375x667 or smaller)
- [ ] `cd 01-product-detail && ls 01-product-detail.html` (empty file exists)

If any fail, fix per Phase 00 install notes before continuing.

## Estimated time

25 min.

## Design brief

**What to build:**

A header bar with the site name on the left and a small nav on the right. Below the header, a two-column product detail block: an image area on the left (about 40% wide on desktop) and an info area on the right (about 60% wide on desktop) containing a title, price, short description, and an Add-to-cart button. On mobile the two columns stack into a single column with the image first. Below the product block, a reviews section with three to five short review cards. Footer at the bottom with copyright text.

**Sketch reference:**

<!-- TODO: hand-sketch sketch.png on Phase 09 Day 1 -->

![sketch](./assets/01-sketch.png)

## Acceptance criteria

1. Verify no horizontal scroll at viewport width 320px (Chrome DevTools mobile mode).
2. Verify tap targets are ≥40px at viewport width 320px.
3. Verify desktop layout at viewport width 1280px matches Design brief.
4. Inspect hover state on the Add-to-cart button at viewport 1280px — verify background color transitions to a visibly different shade.
5. Verify two-column layout collapses to single stacked column at viewport width 375px.
6. Note in lab-notes.md the Tailwind utility patterns applied in this drill: which of `flex`, `grid`, `grid-template-columns`, `gap-`, `p-`, `m-`, `text-`, `bg-`, `hover:`, `md:`, `lg:`, `min-h-screen`, `rounded-`, `shadow-`, `transition-` appeared in your final HTML, and which were reserved for other drills in this repo and are not used here.

## Stretch goals

- Apply a tablet-width (md: breakpoint) variant and compare layout against the 1280px desktop variant.
- Verify keyboard tab-order across header nav and Add-to-cart button using browser DevTools accessibility tree.
- Capture a screenshot at 768px and compare against the 320px and 1280px captures.

## Screenshots + Live URL deliverable

![mobile](./assets/01-mobile.png)

![desktop](./assets/01-desktop.png)

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
- Did you confirm the Tailwind CDN `<script>` tag is the FIRST element inside `<body>`, not inside `<head>`, per deliverables L81?

## References

- Concept Notes — Tailwind Utility-First — Responsive Patterns
- [Tailwind Docs — Play CDN Installation](https://tailwindcss.com/docs/installation/play-cdn#Installation)
- [Tailwind Docs — Responsive Design Overview](https://tailwindcss.com/docs/responsive-design#Overview)
- [Tailwind Docs — Hover Variants](https://tailwindcss.com/docs/hover-focus-and-other-states#Hover)
- [Tailwind Docs — Grid Template Columns: Examples](https://tailwindcss.com/docs/grid-template-columns#Examples)

<!-- citations-v1.1
- [Tailwind Docs — Play CDN Installation](https://tailwindcss.com/docs/installation/play-cdn#Installation) [sha256:622bb2cf96a7] 2026-05-29
- [Tailwind Docs — Responsive Design Overview](https://tailwindcss.com/docs/responsive-design#Overview) [sha256:fc84dc6176d1] 2026-05-29
- [Tailwind Docs — Hover Variants](https://tailwindcss.com/docs/hover-focus-and-other-states#Hover) [sha256:b1b0ed47e2cc] 2026-05-29
- [Tailwind Docs — Grid Template Columns: Examples](https://tailwindcss.com/docs/grid-template-columns#Examples) [sha256:45f762695e15] 2026-05-29
<!-- /citations-v1.1 -->

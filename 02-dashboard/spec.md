---
lab-id: lab-29-tailwind-drills-repo
plan-source: _MASTER-PLAN/phase-09-tailwind-modern-css/02-TailwindModernCSS_week-by-week.md
concept-notes: ["Tailwind Utility-First — Responsive Patterns"]
---

# Drill 02 — Dashboard

## Objective

Build a responsive dashboard layout with a sidebar nav, a top header, four metric cards that collapse across breakpoints, and a data table with colored status badges — using Tailwind utility classes loaded via CDN.

## Why this lab exists

- **Reinforces Concept Notes:** Tailwind Utility-First — Responsive Patterns
- **Frontend resource chapters covered:** tailwindcss.com Grid Template Columns + Flex + Gap + Background Color + MDN Grid Layout
- **Decision Gate 3 connection:** direct prep — build a responsive Tailwind page from a sketch in <30 min with no AI.

## Prerequisites

Verify each tool works before starting:

- [ ] `node --version` (only if using a local preview server; otherwise open the HTML file directly in the browser)
- [ ] Confirm CDN script tag: `<script src="https://cdn.tailwindcss.com"></script>` (Day-1 paste at top of HTML body per deliverables L81)
- [ ] Open Chrome DevTools, switch to mobile view (Toggle device toolbar; preset iPhone SE 375x667 or smaller)
- [ ] `cd 02-dashboard && ls 02-dashboard.html` (empty file exists)

If any fail, fix per Phase 00 install notes before continuing.

## Estimated time

30 min.

## Design brief

**What to build:**

A sidebar on the left at a fixed width (hidden or slide-in on mobile) containing nav items. A top header across the remaining width with an avatar placeholder on the right and a search input on the left. Below the header, a row of four metric cards (each with a label and a number) that collapse to two columns on tablet widths and one column on mobile. Below the metrics, a data table with at least five rows and columns for date, customer, amount, and status — with the status column rendered as colored badges (green, yellow, red).

**Sketch reference:**

<!-- TODO: hand-sketch sketch.png on Phase 09 Day 1 -->

![sketch](./assets/02-sketch.png)

## Acceptance criteria

1. Verify no horizontal scroll at viewport width 320px (Chrome DevTools mobile mode).
2. Verify tap targets are ≥40px at viewport width 320px.
3. Verify desktop layout at viewport width 1280px matches Design brief.
4. Verify metric cards collapse from 4-col to 2-col at viewport width 768px (tablet).
5. Inspect status-badge color contrast at viewport 1280px — verify green badges, yellow badges, and red badges are visually distinguishable.
6. Note in lab-notes.md the Tailwind utility patterns applied in this drill: which of `flex`, `grid`, `grid-template-columns`, `gap-`, `p-`, `m-`, `text-`, `bg-`, `hover:`, `md:`, `lg:`, `min-h-screen`, `rounded-`, `shadow-`, `transition-` appeared in your final HTML, and which were reserved for other drills in this repo and are not used here.

## Stretch goals

- Apply a sticky-header utility on the data table and verify scroll behavior preserves header visibility.
- Compare side-by-side: 1280px vs 768px vs 320px screenshots — note which Tailwind responsive breakpoint utilities (md:, lg:) drove each transition.
- Verify the metric-card row spacing remains consistent across breakpoints.

## Screenshots + Live URL deliverable

![mobile](./assets/02-mobile.png)

![desktop](./assets/02-desktop.png)

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
- Did you verify the data table is readable at viewport 768px (tablet) before declaring the dashboard responsive?

## References

- Concept Notes — Tailwind Utility-First — Responsive Patterns
- [Tailwind Docs — Grid Template Columns: Examples](https://tailwindcss.com/docs/grid-template-columns#Examples)
- [Tailwind Docs — Flex: Examples](https://tailwindcss.com/docs/flex#Examples)
- [Tailwind Docs — Gap: Examples](https://tailwindcss.com/docs/gap#Examples)
- [Tailwind Docs — Background Color: Examples](https://tailwindcss.com/docs/background-color#Examples)
- [MDN — Basic Concepts of Grid Layout](https://developer.mozilla.org/en-US/docs/Web/CSS/Guides/Grid_layout/Basic_concepts#Basic concepts of grid layout)

<!-- citations-v1.1
- [Tailwind Docs — Grid Template Columns: Examples](https://tailwindcss.com/docs/grid-template-columns#Examples) [sha256:45f762695e15] 2026-05-29
- [Tailwind Docs — Flex: Examples](https://tailwindcss.com/docs/flex#Examples) [sha256:eabc863f1128] 2026-05-29
- [Tailwind Docs — Gap: Examples](https://tailwindcss.com/docs/gap#Examples) [sha256:542f73658e19] 2026-05-29
- [Tailwind Docs — Background Color: Examples](https://tailwindcss.com/docs/background-color#Examples) [sha256:a814660ef5f6] 2026-05-29
- [MDN — Basic Concepts of Grid Layout](https://developer.mozilla.org/en-US/docs/Web/CSS/Guides/Grid_layout/Basic_concepts#Basic concepts of grid layout) [sha256:09e9b6c7a0d5] 2026-05-29
<!-- /citations-v1.1 -->

# Drill 03 — Marketing Landing — Build Notes

**Date started:** _____
**Date completed:** _____
**Time spent:** _____
**Status:** Draft

---

## How to run

A visual-build drill, and direct Gate 3 rehearsal: you are handed a target page and its reflow behavior, and you build the whole thing from an empty file with no AI. The clock matters — the gate is a sketch-to-page build in under 30 minutes. Build it, then resize through three viewport widths and self-check the reflow, the absence of sideways scroll, and the tap-target sizes.

- [ ] Confirm the CDN framework script is in place at the top of the body, and the empty page file exists in `03-marketing/`.
- [ ] Open the page directly in the browser (or a local preview server) and have DevTools' device toolbar ready.
- [ ] Page built from an empty file in one sitting, no AI, timed.
- [ ] Resized and self-checked at mobile / tablet / desktop widths.

---

## The page (what to build)

This is the GIVEN. Five stacked regions, top to bottom. The ASCII is the desktop view; the reflow rules below say what changes as the screen narrows.

```text
DESKTOP (~1280px wide)
+--------------------------------------------------------------+
|                                                              |
|                                                              |
|                      Big Headline Here                       |   <- HERO
|                  one calmer line of subtext                  |      fills the
|                                                              |      whole first
|                       [  Get Started  ]                      |      screen,
|                                                              |      top to bottom
|                                                              |
|     (background is a smooth two-color wash, not one flat     |
|      color — one corner shades into another)                 |
+--------------------------------------------------------------+
|                                                              |
|   +----------------+  +----------------+  +----------------+ |
|   |     [icon]     |  |     [icon]     |  |     [icon]     | |   <- FEATURES
|   |   Feature A    |  |   Feature B    |  |   Feature C    | |      three across,
|   |  short blurb   |  |  short blurb   |  |  short blurb   | |      evenly spaced,
|   +----------------+  +----------------+  +----------------+ |      equal gaps
|                                                              |
+--------------------------------------------------------------+
|                                                              |
|   +----------------+  +----------------+  +----------------+ |
|   |  "a quote..."  |  |  "a quote..."  |  |  "a quote..."  | |   <- TESTIMONIALS
|   |   — Name       |  |   — Name       |  |   — Name       | |      three across,
|   |     Title      |  |     Title      |  |     Title      | |      quote/name/title
|   +----------------+  +----------------+  +----------------+ |
|                                                              |
+--------------------------------------------------------------+
|             Ready to start? Big closing line                 |   <- CTA BANNER
|                    [  Sign Up Free  ]                        |      full bleed,
|             (this band spans edge to edge)                   |      its own color
+--------------------------------------------------------------+
|  Company    Links    Links    Links              © footer    |   <- FOOTER
+--------------------------------------------------------------+
```

Region inventory:

- **Hero** — a centered headline, a quieter subheadline beneath it, and one call-to-action button, all sitting on a background that visibly shades from one color toward another (a corner-to-corner wash, not a single flat fill). The hero alone is tall enough to occupy the entire first screen.
- **Features** — three cards side by side. Each card holds an icon placeholder at the top, a heading, and a short paragraph. The cards are the same width with even space between them, and each one reacts to the pointer hovering over it with a small visible lift (a size nudge, or a darker drop-shading behind the card).
- **Testimonials** — three cards side by side. Each holds a short quote, then a person's name, then their title. Padding inside each card stays even across the set.
- **CTA banner** — a single full-width band, edge to edge, in its own color, with a closing line and one button.
- **Footer** — company info on one side, a few groups of links, a copyright line.

How it reflows across widths:

| Width | Hero | Feature cards | Testimonial cards | CTA banner | Footer |
|---|---|---|---|---|---|
| **Mobile (~320–375px)** | still fills the screen; headline scales down but stays readable; button is comfortably tappable | stack into a single column, one card per row, full usable width | stack into a single column | still full width; button still comfortably tappable | groups stack vertically |
| **Tablet (~768px)** | unchanged in intent; comfortable margins | a sensible middle step between one and three across | a sensible middle step | full width | groups begin to sit side by side |
| **Desktop (~1280px)** | matches the sketch above | three across, evenly spaced | three across | full width | groups in a row |

Hard requirements the finished page must satisfy:

- No sideways scrollbar at the narrowest width.
- Every button and link is at least 40px tall on a touch viewport.
- The hero occupies the full height of the first screen at desktop width.
- The hero background blends between two colors, not a solid block.
- A feature card visibly responds when the pointer rests on it.

---

## Plan before you build

Recall the approach from memory before opening any reference or writing markup.

**Region by region, which single layout mechanism turns a stack of boxes into a row that can also collapse back to a stack — and which mechanism (if a different one) governs the inside of the hero, where three elements sit centered on both axes?**

> 

**At which two widths does something about the layout change, and for each card row, what is the count of columns on either side of each of those two thresholds?**

> 

**What makes the hero reach the full height of the first screen rather than only as tall as its text — and separately, what produces a two-color background wash instead of a flat color?**

> 

**For the hover response on a feature card and for the comfortable button height, name the kind of property each needs (one changes appearance on pointer-over; one sets a minimum vertical size), without yet writing the markup.**

> 

---

## Build, then check responsive

Build the page from the empty file. Then run the self-check protocol below — open the device toolbar and step through the three widths in order. Record what you see; do not pre-fill it.

**Mobile (set the viewport to ~320–375px):**

- [ ] No horizontal scrollbar appears; nothing spills past the right edge.
- [ ] Both card rows have collapsed to a single column.
- [ ] The hero still covers the first screen and its text is legible.
- [ ] Every button and link clears the 40px tap-height bar (measure one in DevTools).

**What I saw at mobile — anything that overflowed, clipped, or shrank too far:**

> 

**Tablet (set the viewport to ~768px):**

- [ ] The card rows show the intended middle step, not still-stacked and not yet the full three-across.
- [ ] Footer link groups have begun to sit beside each other.

**What changed between mobile and tablet, and was the changeover where I expected it:**

> 

**Desktop (set the viewport to ~1280px):**

- [ ] Both card rows are three across with even gaps.
- [ ] The hero fills the full height of the first screen.
- [ ] The hero background reads as a two-color wash, not a flat fill.
- [ ] A feature card lifts or deepens when the pointer rests on it.

**What I saw at desktop, and whether it matched the sketch:**

> 

---

## Explain it

With the page closed, explain the reflow out loud, then write the one-liner.

**Why does a row of three cards become a single stacked column as the screen narrows — what is the default direction a block of boxes falls into, and what is being switched on only at the wider widths to override it?**

> 

**The width-specific rules fire at certain screen widths and "stick" upward from there. Going from a narrow screen to a wide one, why does the three-across rule take over and stay rather than flicker back, and which side of each threshold owns the plain unprefixed styles?**

> 

**Why does the page avoid a horizontal scrollbar at the narrowest width — what would have caused one, and which choices in your build kept total content width inside the viewport?**

> 

**If a reviewer asked why the tap targets are sized the way they are, what is the reasoning behind the 40px floor on a touch screen?**

> 

---

## Deploy

Drop a short-lived live preview and paste the URL here so the page can be opened from a phone, not just the desktop emulator.

**Live URL:** _____

- [ ] Opened the live URL on an actual phone (or an incognito window) and re-checked: no sideways scroll, buttons tappable.

---

## Gate 3 connection

**Could I rebuild this whole page from the sketch alone, from an empty file, no AI, inside the 30-minute window right now?**

> 

**Which region cost me the most time or made me reach for a reference, and what would I drill so it comes back cold next time?**

> 

**If the brief changed so the feature cards had to sit two across on tablet instead of the step I chose, what is the one thing I would change?**

> 

---

## Reflection

**What did I learn building this that the docs alone wouldn't have told me?**

> 

**Where did my mental model break? (The moment I said "wait, that reflowed the wrong way" or "why is there a scrollbar?")**

> 

**Acceptance-criteria item 6 asks which utility patterns from the repo's running list actually showed up in my final markup and which I reserved for other drills. Answer that here in my own words, from my finished file:**

> 

*Last updated: 2026-06-05*

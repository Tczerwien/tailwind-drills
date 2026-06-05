# Drill 01 — Product Detail — Build Notes

**Date started:** _____
**Date completed:** _____
**Time spent:** _____
**Status:** Draft

---

## How to run

A visual-build drill that doubles as Gate 3 rehearsal. You are handed a target page below — its content, its desktop layout, and how it should reflow as the viewport narrows. Build it from a single HTML file with the utility framework loaded via CDN, then resize across mobile / tablet / desktop and self-verify the reflow. The build is the work; the responsive self-check is what the gate actually tests.

- [ ] `01-product-detail.html` built in `01-product-detail/`, framework loaded via the CDN script tag
- [ ] Opened in the browser and resized through mobile / tablet / desktop widths
- [ ] Responsive self-check run at each width (see "Build, then check responsive")
- [ ] Live URL filled in under "Deploy"

---

## The page (what to build)

The target is a single product-detail page made of four stacked regions, top to bottom: a header bar, a product block, a reviews section, and a footer. Build the page so it matches the sketches below at each width.

**Desktop (around 1280px wide):**

```text
+----------------------------------------------------------+
|  SiteName                           Home   Shop   Cart   |  <- header bar
+----------------------------------------------------------+
|                          |                               |
|                          |   Product Title               |
|       [ image area ]     |   $Price                      |
|       (~40% width)       |   short description text...   |
|                          |   ...spanning a few lines     |
|                          |                               |
|                          |   [  Add to cart  ]           |
|                          |   (info area, ~60% width)     |
+----------------------------------------------------------+
|  Reviews                                                 |
|  +----------+  +----------+  +----------+                |
|  | review 1 |  | review 2 |  | review 3 |   ...3 to 5    |
|  +----------+  +----------+  +----------+                |
+----------------------------------------------------------+
|                  (c) SiteName  footer text               |
+----------------------------------------------------------+
```

**Mobile (around 375px wide, and holding down to 320px):**

```text
+-------------------------+
| SiteName      Home Shop |  <- header bar, nav stays reachable
+-------------------------+
|                         |
|     [ image area ]      |  <- image first, full width
|                         |
+-------------------------+
|  Product Title          |
|  $Price                 |
|  short description...    |
|                         |
|  [    Add to cart    ]  |  <- info area below the image
+-------------------------+
|  Reviews                |
|  +-------------------+  |
|  |     review 1      |  |  <- cards stack one per row
|  +-------------------+  |
|  |     review 2      |  |
|  +-------------------+  |
|  |     review 3      |  |
|  +-------------------+  |
+-------------------------+
|   (c) SiteName footer   |
+-------------------------+
```

Content blocks (the GIVEN):

- **Header bar** — the site name on one side, a short nav (a few links) on the other side.
- **Product block** — an image area and an info area. The info area carries a title, a price, a short multi-line description, and a single Add-to-cart button.
- **Reviews section** — a heading plus three to five short review cards, each with a line or two of text.
- **Footer** — copyright / site-name text along the bottom.

Reflow behavior (the GIVEN — match this, do not just match the pixels):

- On **desktop**, the product block is two side-by-side regions: the image area takes roughly the smaller share of the width and the info area takes roughly the larger share. The review cards sit several across in one row.
- On **tablet** (around 768px), the layout is the in-between case. Decide for yourself whether the product block is still two regions or has already stacked, and whether the cards show fewer across than on desktop — then hold to whatever you chose when you self-check.
- On **mobile**, the product block becomes a single column with the image area first and the info area beneath it. The review cards stack toward one per row. Nothing runs off the side of the screen, and the nav and the Add-to-cart button stay comfortably tappable.
- The Add-to-cart button changes appearance when the pointer hovers over it on desktop.

---

## Plan before you build

Recall the approach from memory before opening any reference or starting the file.

**Sketch the regions top-to-bottom and, beside each, jot the framework utilities you expect to reach for. Which region drives the two-side-by-side-versus-stacked decision, and what controls that switch at a given width?**

> 

**The two product regions are side by side on wide screens and stacked on narrow ones. By default, before you add anything, which way do block-level regions sit — side by side or stacked — and which direction is therefore the one you have to actively ask for?**

> 

**Which width is your starting point — the narrow layout or the wide one — and which width(s) then get the override utilities layered on top? State your choice before you build, so the self-check can hold you to it.**

> 

**For the review row: name the mechanism you will use to place several cards across, and how that same mechanism collapses them toward one-per-row as the screen narrows.**

> 

---

## Build, then check responsive

Build the page, then run this self-check at three widths. Use the browser's device-toolbar / responsive mode and step through each width deliberately.

**Mobile — around 375px, then hold the check down to 320px:**

- [ ] No horizontal scroll: nothing runs off the right edge, no sideways scrollbar appears
- [ ] The product block is a single column with the image area first
- [ ] Review cards have collapsed toward one per row
- [ ] Tap targets (nav links, the Add-to-cart button) measure at least 40px in their smaller dimension — check with the element inspector

**What I saw at mobile width (and anything that ran off-screen or measured under 40px):**

> 

**Tablet — around 768px:**

- [ ] The layout matches whatever in-between behavior you committed to in "Plan before you build"
- [ ] Still no horizontal scroll
- [ ] Tap targets still at least 40px

**What I saw at tablet width, versus what I planned:**

> 

**Desktop — around 1280px:**

- [ ] The product block is two side-by-side regions, image area the smaller share, info area the larger share
- [ ] Review cards sit several across in one row
- [ ] Hovering the Add-to-cart button changes its appearance, then reverts when the pointer leaves

**What I saw at desktop width, and how the hover change looked:**

> 

---

## Explain it

With the page built, explain the layout out loud, then write the one-liner. Answer from your own build — do not look anything up first.

**Walk the product block: it sits as one column on a phone and as two side-by-side regions on a desktop. Which utility carries that switch, and at which width does the override you wrote take effect?**

> 

**Whichever width you chose as your starting point (narrow or wide): why did you start there, and how did that choice change which width carried the override utilities?**

> 

**If, when you resized to 320px, anything ran off the right edge — what was the most likely cause, and which utility would you reach for to contain it? If nothing ran off, what kept it contained?**

> 

**The review cards go from several-across to fewer-or-one-across as the screen narrows. Explain what makes that happen without you writing a separate rule for every single width.**

> 

---

## Deploy

Publish the single HTML file and capture the live link. Re-open the link in a private/incognito window and re-run the mobile self-check against the deployed copy, not just the local file.

**Live URL:** _____

- [ ] Live URL opens in a fresh private window with no local files involved
- [ ] Mobile self-check re-run against the live URL (no horizontal scroll, tap targets at least 40px)

**Anything that behaved differently live than it did locally:**

> 

---

## Gate 3 connection

**Gate 3 is: build a responsive page from a sketch in under 30 minutes, with no AI. Working only from the sketches above and from memory, how close to that 30-minute mark did this build land, and what ate the most time?**

> 

**Which utility did you have to look up rather than recall — the one that would have stalled you in a timed, no-notes run?**

> 

**If a reviewer handed you only the desktop sketch and asked you to make it reflow correctly on a phone, which single decision would you make first?**

> 

---

## Reflection

**What did this build teach about responsive composition that the framework's docs page did not?**

> 

**Where did your mental model break? (Name the moment the layout did something you did not expect at one of the three widths.)**

> 

*Last updated: 2026-06-05*

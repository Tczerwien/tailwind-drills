# Drill 02 — Dashboard — Build Notes

**Date started:** _____
**Date completed:** _____
**Time spent:** _____
**Status:** Draft

---

## How to run

A visual-build drill toward Gate 3: turn the target below into a working responsive page, from memory, in under 30 minutes, no AI. The page is a single standalone HTML file with the Tailwind CDN script in the head; open the file straight in the browser, or serve it locally if you prefer a live-reload preview. The build is half the work — the other half is resizing the window and proving the reflow holds, then explaining why it reflows the way it does.

- [ ] `02-dashboard.html` built with the Tailwind CDN script tag in place
- [ ] Opened in the browser and checked at three widths (see "Build, then check responsive")
- [ ] "Explain it" answered with nothing open
- [ ] Live URL pasted into the Deploy slot

---

## The page (what to build)

This is the GIVEN — the target you are building toward. Everything about *which classes produce it* is yours to recall.

Four content regions:

1. **Sidebar** — a vertical strip down the left edge holding a short stack of nav items (label per item). It sits at a fixed, narrow width and stays put as the rest of the page changes. On the narrowest screens it should not eat the viewport — either tuck it away or let it drop above the content, your call, as long as nothing overflows sideways.
2. **Header** — a horizontal bar across the top of the remaining area. A search input sits at the left end of the bar; a small round avatar placeholder sits hard against the right end, with the gap between them flexing as the bar widens or narrows.
3. **Metric row** — four cards, each showing a short label and one large number. How many cards sit per line is the heart of this drill (see the reflow table).
4. **Data table** — below the metrics: at least five rows, with columns for date, customer, amount, and status. The status cell is not plain text — it is a small rounded pill, and its fill color encodes the state: one calm/positive hue, one cautionary hue, one alarm hue, each clearly distinct from the others at a glance.

ASCII sketch — desktop (wide):

```text
+--------+-----------------------------------------------+
|        |  [ search...        ]                   (o)   |  <- header
|  Nav   +-----------------------------------------------+
|  item  |  +------+  +------+  +------+  +------+        |
|  item  |  | LBL  |  | LBL  |  | LBL  |  | LBL  |        |  <- 4 metric cards
|  item  |  | 123  |  | 123  |  | 123  |  | 123  |        |     on one line
|  item  |  +------+  +------+  +------+  +------+        |
|        |  +-------------------------------------------+ |
| (side  |  | date    customer   amount   status      | |
|  bar)  |  | ...     ...        ...     ( ok  )       | |  <- table, status
|        |  | ...     ...        ...     ( warn )      | |     cells are pills
|        |  | ...     ...        ...     ( fail )      | |
|        |  +-------------------------------------------+ |
+--------+-----------------------------------------------+
```

ASCII sketch — mobile (narrow): sidebar no longer flanks the content, the search bar and avatar still share the header row, the four cards stack into a single column, and the table stays readable with no sideways scroll.

```text
+-------------------------+
| [ search... ]      (o)  |  <- header still one row
+-------------------------+
| +---------------------+ |
| | LBL                 | |
| | 123                 | |  <- cards now one per line
| +---------------------+ |
| | LBL                 | |
| | 123                 | |
| +---------------------+ |
|   ( ... two more ... )  |
+-------------------------+
| date  cust  amt  status |  <- table fits the width
+-------------------------+
```

How the metric row reflows across the three breakpoints (this is the behavior to hit — the class names that achieve it are what you recall):

| Viewport | Width | Cards per line |
|----------|-------|----------------|
| Mobile   | ~320–375px | 1 |
| Tablet   | ~768px | 2 |
| Desktop  | ~1280px | 4 |

The header (search left, avatar right) and the table stay present at every width; only their proportions change.

---

## Plan before you build

Recall the approach from memory before you open a single reference. Write what you intend to reach for, then build, then come back and mark what you actually needed help with.

**What mechanism makes the sidebar sit beside the main area on wide screens, and what changes that arrangement on a narrow screen?**

> 

**The metric row has to go 1 → 2 → 4 across the three widths. How do you express "this many per line at this width and a different count at a wider one" in this framework — and where does the boundary between widths get declared?**

> 

**The status pills carry meaning through color. What decides which pill gets which fill, and how do you keep the three states legible side by side?**

> 

**Which spacing between the cards, and which padding inside each card, will you set — and will those hold steady as the row reflows, or do they need to change per width?**

> 

---

## Build, then check responsive

Build it, then run the self-check at each width. Resize the real window or use the browser's device toolbar. The point is to catch the reflow failing, not to admire it passing.

**Mobile (~320–375px):**

- [ ] No horizontal scroll — nothing pushes past the right edge
- [ ] Every tappable thing (nav items, search field, avatar) is at least 40px in its smallest dimension
- [ ] Metric cards have collapsed to a single column
- [ ] The sidebar is not crowding the content off-screen

**Tablet (~768px):**

- [ ] Metric cards now sit two per line
- [ ] The data table is still readable — no clipped columns, no sideways scroll

**Desktop (~1280px):**

- [ ] All four metric cards on one line
- [ ] Sidebar flanks the content; header spans the rest with search at left, avatar at right
- [ ] The three status pill hues are distinct from each other at a glance

**Where the reflow first broke, and the width it broke at:**

> 

**Anything that overflowed sideways before I fixed it — and what fixed it:**

> 

---

## Explain it

With nothing open, explain why the page reflows the way it does. The build is the easy half; this is the half Gate 3 actually tests.

**Why do four cards on a wide screen become one column on a phone — what in your markup makes the count drop as the viewport shrinks, rather than the cards just getting thinner?**

> 

**The header keeps search-left / avatar-right at every width. What pins the avatar to the right edge while the search stays left, and why doesn't that arrangement need a width-specific override the way the cards do?**

> 

**If the page showed a horizontal scrollbar at 320px, where would you look first, and what is the usual culprit?**

> 

**You picked one hue for "ok", one for "warn", one for "fail". If a reviewer asked why a colorblind user can still tell them apart, what would you change or add?**

> 

---

## Deploy

Drop the file on a no-signup static host and paste the live link. Open it from a private window to confirm it actually loads for someone who isn't you.

**Live URL:** _____

**Checked from an incognito window?**

> 

---

## Gate 3 connection

**Could I rebuild this page from the sketch alone, from memory, in under 30 minutes with no AI right now?**

> 

**Which single piece — the sidebar arrangement, the card reflow, the header pinning, or the status pills — would slow me down most under the clock, and what's the one detail I'd drill first?**

> 

---

## Reflection

**What did I learn that I won't find in the docs?**

> 

**Where did my mental model break? (The moment I said "wait, that's not what I expected.")**

> 

*Last updated: 2026-06-04*

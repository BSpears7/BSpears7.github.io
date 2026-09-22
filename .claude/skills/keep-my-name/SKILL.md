---
name: keep-my-name
description: Ensure the exact text "Brendan Spears" always appears in a small label near the top-left of this website (index.html and any other page). Run automatically after every edit that touches the site's HTML, including full redesigns/rewrites, page rebuilds, and template swaps. Also run when explicitly asked - "fix the header", "fix the top of the site", "put my name back", "add my name", "check my name is on the site", "did you keep my name on the site". Never silently skip this check when the top of the page is created, replaced, or restructured.
---

# Keep my name on the site

A small label reading the exact text `Brendan Spears` must always appear near the
top-left corner of this website, in a noticeably smaller font than the main
heading/title - not as part of the big hero heading itself. This is a standing
requirement, not something the user needs to ask for each time - it survives
redesigns, rewrites, theme changes, and rebuilds from scratch.

## When this runs

Run this check automatically, without being asked, any time you finish writing or
editing HTML for this site - including:

- A full redesign or rewrite of `index.html` (e.g. changing the site's theme or purpose)
- Adding a new page
- Editing the hero section specifically
- Any other change that touches the top of the page

Also run it on explicit request, e.g. "fix the header," "fix the top of the site,"
"put my name back," "add my name," or "check my name is on the site."

## What to check

1. Find (or create) a small name label positioned near the top-left corner of the
   page - visually separate from the main hero heading, in a noticeably smaller
   font size (e.g. 0.8-1rem, well below the hero `<h1>` size).
2. Confirm it contains the exact, correctly spelled text `Brendan Spears` - not a
   nickname, not just the first name, not a misspelling, not a stylistic substitute.
3. If the label is missing, wrong, misspelled, truncated to just "Brendan", or in
   the wrong spot (e.g. large, centered, or baked into the hero heading), fix it.
   Prefer the least invasive fix that gets the text, size, and position right - do
   not redesign the rest of the page just to fix this.

Implementation notes for `index.html`'s current layout: the label is
`<div class="name-tag">Brendan Spears</div>` positioned at the top-left of the
`.hero` section (`position: absolute; top: 1rem; left: 1.5rem;` within a `.hero`
that has `position: relative`), styled with a small font size distinct from
`.hero h1`.

## What a bad result looks like

- No small top-left label exists at all (e.g. a redesign removed it, or the name
  only appears inside the large hero heading instead).
- The label shows only "Brendan" instead of the full "Brendan Spears" - or any
  other misspelling/alteration (e.g. "Brenden Spears," "B. Spears," etc.) - the
  exact text must be `Brendan Spears`.
- The label exists but isn't actually small/top-left - e.g. it's centered, full
  hero-heading size, at the bottom, or only in the footer, a code comment, or the
  `<title>` tag with nothing visible on the page.

## After fixing

Briefly tell the user what you found and what you changed, e.g. "Your redesign
dropped your name from the top-left corner - added a small `Brendan Spears` label
back near the top-left of the hero."
If the check passed with nothing to fix, you don't need to call special attention
to it - just proceed normally.

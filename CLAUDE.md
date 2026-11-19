# CLAUDE.md — physics

Inv's physics learning repo: github.com/imelenwe/physics (public, meant for GitHub Pages).
Read `README.md` first: it explains the purpose, layout and workflow.

## Every session

1. Read `README.md`, then check `inbox/` for summaries Inv has pasted but that are not yet
   written up.
2. For each summary: write or update `topics/<topic>/notes.md`, build the explainer /
   visualization page(s) next to it, and add a link for each page to `index.html`.
   Update the "Topics" list in `README.md`.
3. `index.html` is the front door: a plain, clickable list of topics and their pages
   (no concept map, no clutter). Every page must be reachable from it.

## How to explain (Inv's standing rules)

- **Tell a story, top to bottom.** This is the most important rule. A page reads once,
  start to finish, and makes sense: each step is caused by the one before (e.g. a body
  is made of atoms → heating makes electrons jiggle → jiggling electrons give off
  radiation → …). Stay inside one picture the whole way: never switch to new actors or
  analogies mid-story (no sudden "emitters", "walls", "coins", "cheap packets"). Answer
  the reader's obvious "where does this come from?" before they ask. Cut anything that
  does not move the story forward: extra formulas, numbers and readouts nobody asked for.

- **First principles, always.** Assume the reader knows no physics. Inv may open a page
  months later, out of the blue, and ask "dumb" questions. Each page must stand on its
  own: start from everyday experience, build every idea up from there.
- **Formulas are allowed, but earned.** Before a formula appears, say in words what it
  means and where it comes from. Never drop a formula in without its "why".
- **Say the core idea in plain words first.** E.g. "a blackbody absorbs everything that
  falls on it; it does *not* mean it is black in colour"; "the Sun is (nearly) a
  blackbody". Then state what the old (classical) view got wrong and what the new
  (quantum) view says, where that applies.
- **One concept per page.** A page is focused and explained in depth, not a flurry of
  ideas. Short enough to read comfortably on a phone. Split rather than grow.
- **Diagrams wherever they help.** Beautiful, clear, and colourful: use distinct
  colours to tell things apart (e.g. wave 1 vs wave 2, classical vs quantum). Dark
  background is fine; colours must read well on it (and in light mode).
- **Interactive only when it teaches.** A slider or animation that makes the idea
  click. Keep it simple; never add interaction for decoration.
- **Lead with why the topic matters.** Every page says what problem the idea solved,
  e.g. blackbody radiation = where classical physics failed and quantum physics began.
  A page about a topic must cover that payoff, not just the definitions.
- **Write it the way Inv's summaries say it: plain English.** Never bring in notation
  or concepts Inv has not learned (e.g. no kT, no "average energy = hf ÷ (e^… − 1)").
  Keep only the formulas that are the point of the topic (e.g. E = hf). Prefer one good
  worked example (like the toy model) over general derivations. No formula boxes or
  comparison tables in the summary card that just repeat jargon.
- **No "words first" glossary sections.** Define each term inline, where it is first
  needed.
- **Physics wording must be exact.** Hot bodies give off *radiation* (electromagnetic
  radiation); "light" means only the visible part.
- **Graphs need labelled axes with units** (or say plainly "same scale, relative").
  When comparing curves, show them on the same scale with a legend.
- **No book or paper references** (no "Zubairy eq. 4.18" etc.). The explanation stands
  on its own.
- Pages are for **revision on a phone**. Every page opens with a **summary card**: short
  and simple. The core idea in a few plain sentences and a 3–5 point "Remember" list.
  Plain English only, written for a reader who knows nothing: no diagrams, formula
  boxes, symbol tables or jargon. Explain the *why* in words (e.g. "one number cannot
  tell going up from going down"). Diagrams and graphs belong in the sections below.
- **One-pager, read like a card.** Each page gives the gist of one concept: the core
  idea, the key formula(s), one example. Few steps: take the shortest honest path to
  each result (no hidden jumps, but no detours either). Crisp, very good English.
- **Side menu when a page is longer than a screen or two:** a clickable "On this page"
  list on the left (sticky, highlights the current section). On a phone it becomes a
  sticky row of tappable section chips at the top. (Inv liked this in the
  system-design notes.)
- **Symbols:** use the common textbook symbols. Angular frequency is **ω** (omega).
  The first time ω appears on a page, add a one-line note: "In the book you read,
  this is written ν (nu); we use ω because most sources do." No other book references.
- Page skeleton: top bar (← All pages) · title + summary card · short sections ·
  "Check yourself" (tap-to-reveal questions) · "Next" link.

## Page style

- Plain, everyday language. Define each technical term the first time it appears.
- Never skip a step in a derivation; each step follows from the one before.
- Self-contained HTML files (inline CSS/JS; libraries only from a CDN with a pinned
  version). Must work in both light and dark mode and on a phone.
- Match the look of `index.html` (same colour tokens).

## Git

- Commit **only when Inv says so**; draft the message first. **Never push.**

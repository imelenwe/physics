# physics

Inv's physics learning notebook: notes on what I learn, written in plain language,
with interactive visualizations that make the ideas easy to see.

**→ [Open the index of all pages](https://imelenwe.github.io/physics/)** (source: [`index.html`](index.html))

---

## What this repo is for

- **Store my physics learnings** as I go, one topic at a time.
- **Make the ideas visible.** Each topic gets explainer pages (HTML) with diagrams,
  animations or sliders you can play with, so the physics can be *seen*, not just read.
- **Keep it readable by anyone.** Plain, everyday words. Any technical term is defined
  the first time it appears. Every step of a derivation is shown; nothing is skipped.

## How the material arrives

I discuss topics with Claude on the web (claude.ai). When a discussion is done, I paste
its summary into a Claude Code session in this repo. Claude Code then turns it into:

1. a Markdown note for the topic (the source of truth), and
2. one or more HTML explainer pages with visualizations, and
3. a new link on the front page, [`index.html`](index.html).

Raw pasted summaries go in [`inbox/`](inbox/) first, so nothing is lost before it is
turned into a proper note.

## Layout

```
physics/
├── README.md        ← this file: what the repo is and how it works
├── CLAUDE.md        ← standing instructions for Claude Code sessions
├── PLAN.md          ← which pages are planned / built
├── index.html       ← front door: links to every explainer page
├── inbox/           ← raw summaries pasted from Claude web, waiting to be written up
└── topics/
    └── <topic-name>/
        ├── notes.md         ← the written-up learning
        └── <page>.html      ← explainer / visualization pages for that topic
```

Topic folders use short lowercase names with dashes, e.g. `topics/special-relativity/`.

## Viewing the pages

- **Online:** https://imelenwe.github.io/physics/ (GitHub Pages).
- **Offline:** open `index.html` in a browser. Pages are self-contained single files.

## Setup status

- [x] Local repo at `~/physics` (branch `main`)
- [x] GitHub repo created: https://github.com/imelenwe/physics (remote `origin`)
- [x] First commit and push
- [x] GitHub Pages on: branch `main`, folder `/ (root)`

## Topics

- **Blackbody radiation** (`topics/blackbody-radiation/`): one page: what a blackbody
  is, where classical physics fails, and how Planck's energy packets fixed it.
- **Classical waves** (`topics/waves/`): one page: a wave as a delayed copy, the formula,
  the complex form (displacement + i·velocity), superposition.
- **Quantum basics** (`topics/quantum-basics/`): the Deep Quantum Basics: Born rule and
  trace, projectors vs observables, Kraus operators, Lindblad takeaways, T1 and T2.

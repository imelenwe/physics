# PLAN — first write-up (summary of 2026-10-18)

Source: [`inbox/2026-10-18-concept-map-physics-papers.md`](inbox/2026-10-18-concept-map-physics-papers.md).
Agreed with Inv on 2026-10-18.

## Phase 1: two topics, eight one-page explainers

Waves and blackbody radiation are separate topics. Each page = one concept, read like a
card (see the rules in [`CLAUDE.md`](CLAUDE.md)).

| # | Topic | Page file | One idea | Visual | Status |
|---|---|---|---|---|---|
| 1–5 | waves | `topics/waves/classical-waves.html` | **one page** (Inv: keep waves brief): delayed copy, cos(ωt − kx), complex form = displacement + i·velocity/ω, superposition + interference + standing waves in brief | travelling wave, rotating point + trace, shift slider | **built** |
| 6–8 | blackbody-radiation | `topics/blackbody-radiation/blackbody-radiation.html` | **one page, three sections**: what a blackbody is · where classical physics fails (ultraviolet catastrophe) · how Planck fixed it (E = hf) | absorb/reflect/pass, box with a hole, measured vs classical graph with real axes | **built** |


## Conventions

- Angular frequency is **ω**; first use on a page notes the book wrote ν (nu).
- No book or paper references.
- Front page `index.html` is a plain clickable list: topic → its built pages.
- Every page opens with a summary card (see `CLAUDE.md`).

## Phase 2: later, one topic at a time

Sections 3–7 of the summary are short reminders, not yet explained. Each gets pages only
after it has been worked through properly:

- Quantum mechanics formalism (time evolution operator; Dirac equation, spinors, rotations)
- Quantum computing (GHZ and dynamic circuits; chip layout; magic states; transmon readout)
- Group theory
- Divergence (vector calculus)
- Reading papers: a "study skills" card, not physics

Open threads from the summary: Gauss's law; input-output theory for readout; Purcell
filters; particle in a box (follows from page 4); more group theory.

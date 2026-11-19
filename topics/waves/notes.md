# Classical waves

Written up from the 2026-10-18 summary. Kept brief on purpose: one page,
[`classical-waves.html`](classical-waves.html).

## A wave is a delayed copy

- A point at distance x repeats what the source did, late by the travel time:
  delay = x / v, so **y(x, t) = y(0, t − x/v)**.
- Example: f = 1 Hz, v = 2 m/s (so λ = 2 m). A point 1 m away is 0.5 s (half a period)
  late, so it always does the opposite of the source. A point 2 m away moves in step.
- t − x/v moves toward +x; t + x/v toward −x.

## The formula

1. Source: y(0, t) = A cos(2πf t) (cos repeats every 2π; after one period 2πfT = 2π).
2. Delay: y(x, t) = A cos(2πf (t − x/v)).
3. Open the bracket: 2πf t − (2πf/v) x, and 2πf/v = 2π/λ because v = λf.
4. With ω = 2πf and k = 2π/λ: **y = A cos(ωt − kx)** (toward +x).

The book Inv read writes ω as ν (nu); the pages use ω.

## Complex form

- z = A e^{−i(ωt − kx)} = A cos(ωt − kx) − i A sin(ωt − kx).
- Real part = displacement. Velocity = −Aω sin(ωt − kx), so imaginary part = velocity / ω.
- **z = displacement + i · velocity/ω**: a point going round a circle of radius A.
- Why it matters: y alone cannot tell "moving up" from "moving down" (at t = 0.25 s and
  0.75 s, y = 0 both times, z = −i and +i). Which way the *wave* travels is the separate
  ∓ sign in ωt ∓ kx.
- Quantum: the wavefunction is genuinely complex; |z|² = A² is constant, as a free
  particle needs, while cos² keeps hitting zero.

## Superposition

- Waves add: y = y₁ + y₂. Shift 0 or λ → 2A; shift λ/2 → 0; in general 2A|cos(π·shift/λ)|.
- Interference: bright where path difference δ = nλ, dark where δ = (n + ½)λ. Energy is
  moved from dark to bright stripes, not lost.
- Standing waves: opposite waves add to 2A sin(kx) sin(ωt). Tied ends ⇒ sin(kL) = 0 ⇒
  kL = nπ ⇒ λ = 2L/n. Only certain waves fit: the seed of quantisation.

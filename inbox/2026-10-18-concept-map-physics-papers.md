<!-- Raw summary pasted by Inv on 2026-10-18 (from Claude web). Kept verbatim.
     Written-up versions live under topics/. -->

# Concept Map — Physics + Papers

A revision map of the core ideas worked out so far. Each concept has the **core idea** (what to remember) and a **worked example** (the computation that makes it stick).

## Notation used throughout

| Symbol | Meaning |
|---|---|
| f | frequency (cycles/s, Hz), f = 1/T |
| T | time period |
| ν | angular frequency, ν = 2πf (Zubairy's notation; most books write ω) |
| v | wave speed, v = λf |
| λ | wavelength |
| k | wavenumber, k = 2π/λ (radians per metre) |
| A | amplitude |
| δ | path difference, r₂ − r₁ |
| h | Planck's constant; packet energy E = hf |
| kT | typical thermal energy at temperature T (k here = Boltzmann's constant) |

Note: in E = hf, f is the ordinary frequency, not ν.

---

# 1. Waves (Zubairy, Ch. 4)

## 1.1 Travelling wave = delayed copy of the source

**Core idea.** A wave moving without changing shape makes every point downstream replay what x = 0 did, late by the travel time x/v.

y(x, t) = y(0, t − x/v)

With y(0, t) = A cos(2πf t), substituting t → t − x/v gives

y(x, t) = A cos(2πf (t − x/v))

The equation compares two **different times**, not the same time.

**Example.** A = 1, f = 1 Hz (T = 1 s), v = 2 m/s, x = 1 m, so the delay is x/v = 0.5 s.

| t (s) | 0 | 0.25 | 0.5 | 0.75 | 1.0 |
|---|---|---|---|---|---|
| y(0, t) | 1 | 0 | −1 | 0 | 1 |
| y(1, t) | −1 | 0 | 1 | 0 | −1 |

- Down a column (same time), the two points differ.
- The x = 1 row is the x = 0 row shifted right by 0.5 s: y(1, 0.5) = y(0, 0).
- Only when x is a whole number of wavelengths (here x = 2 m, delay = T) do the two points agree at the same instant.

**Direction check.** With t − x/v, a crest at x = 0 at t = 0 reaches x = 4 m at t = 2 s, so it moves at 2 m/s in +x. With t + x/v, the wave moves in −x.

## 1.2 Standard form: ν and k

**Core idea.** Expanding the bracket separates time and space:

2πf (t − x/v) = 2πf t − (2πf/v) x = νt − kx

using v = λf, so 2πf/v = 2π/λ = k.

- y(x, t) = A cos(νt − kx) travels in +x  …①
- y(x, t) = A cos(νt + kx) travels in −x  …②

ν is "radians per second"; k is "radians per metre".

## 1.3 Complex representation

**Core idea.** For a string, the physical displacement is only the real part:

y(x, t) = Re[A e^{−i(νt − kx)}] = A cos(νt − kx)

The imaginary part is not a sideways displacement. It is the **velocity, scaled**:

- Im part = −A sin φ, with φ = νt − kx
- ∂y/∂t = −Aν sin φ
- so Im part = (∂y/∂t)/ν

So the complex number is the pair **(displacement, velocity/ν)**, a point in a plane. Dividing by ν makes both axes metres. The *i* keeps the two on separate axes, so it is a pair, not a sum.

**Why one real number is not enough.** At x = 0, y = cos(νt), T = 1 s:

| t (s) | y | next value | motion | z = e^{−iνt} |
|---|---|---|---|---|
| 0.25 | 0 | −1 | moving down | −i |
| 0.75 | 0 | +1 | moving up | +i |

Same y, different situations. cos φ = cos(−φ), so cos cannot tell them apart. The complex number can.

Also, y = 0.5 could be A = 1 at φ = 60° or A = 0.5 at φ = 0°: one number, two unknowns. With z, |z| = A and angle(z) = φ.

**The point goes round a circle.**

| t (s) | 0 | 0.25 | 0.5 | 0.75 | 1.0 |
|---|---|---|---|---|---|
| z | 1 | −i | −1 | +i | 1 |

The up-down motion of the string is the shadow of this circle on the real axis. This (position, velocity) plane is **phase space**; the "phase" is the angle on the circle. Like a pendulum: a snapshot of position alone cannot predict the future, you need position and velocity.

**Why it is essential in QM, not just convenient.**

- cos form: |y|² = A² cos²φ oscillates and hits zero.
- complex form: |A e^{−iφ}|² = A², constant.

A free particle ψ = A e^{i(kx − νt)} must have uniform probability density |ψ|², so only the complex form works. The Schrödinger equation contains *i*, so the wavefunction is genuinely complex; there is no "take the real part" step.

Link ahead: the harmonic-oscillator lowering operator a ∝ x + i·p/(mν) has the same "position + i·momentum" structure.

**Convenience for classical waves:** derivatives become multiplication.
∂/∂t e^{−iφ} = −iν e^{−iφ},  ∂/∂x e^{−iφ} = +ik e^{−iφ}

## 1.4 Standing waves and quantisation

**Core idea.** Two equal waves travelling in opposite directions add to a wave that does not travel:

y(x, t) = A cos(kx − νt) − A cos(kx + νt) = 2A sin(kx) sin(νt)  (Zubairy 4.18)

using cos a − cos b = −2 sin((a+b)/2) sin((a−b)/2). Space and time are now separate factors.

**Boundary condition.** y is displacement from rest. A string clamped to walls cannot move at the ends:

y(0, t) = 0 and y(L, t) = 0 for all t

**Why sin(kL) = 0.** y(L, t) = 2A · sin(kL) · sin(νt). sin(kL) is a fixed number (no t); sin(νt) keeps changing. For the product to be zero at every instant, the constant factor must be zero.

Counter-example: if sin(kL) = 0.5, then y(L, T/4) = A, so the clamped end would move. Impossible.

**Steps.**
1. sin(kL) = 0 ⇒ kL = nπ, n = 1, 2, 3, …
2. k = 2π/λ ⇒ (2π/λ)L = nπ
3. L = nλ/2, so λₙ = 2L/n, kₙ = nπ/L, fₙ = n·v/(2L) = n·f₁

**Example.** L = 1 m, v = 2 m/s.

| n | λₙ (m) | fₙ (Hz) | loops | nodes in between |
|---|---|---|---|---|
| 1 | 2 | 1 | 1 | 0 |
| 2 | 1 | 2 | 2 | 1 |
| 3 | 0.667 | 3 | 3 | 2 |

- Frequencies are whole-number multiples of f₁, hence "harmonics". n = 1 is the fundamental (L = λ/2).
- Plucking the midpoint makes one bump, which looks like n = 1; n = 2 needs the middle still.
- Nodes (y = 0 always) at x = 0, λ/2, λ, …; antinodes at λ/4, 3λ/4, ….

**QM link.** Fixed ends allow only λ = 2L/n. A particle in a box (ψ = 0 at the walls) gets the same condition, so only certain momenta and energies are allowed. That is quantisation.

## 1.5 Interference (Young's double slit)

**Core idea.** At a point P, the two waves have travelled r₁ and r₂. Brightness depends only on the path difference δ = r₂ − r₁.

**Sum-to-product.**

cos a + cos b = 2 cos((a + b)/2) · cos((a − b)/2)

Derivation: cos(p+q) + cos(p−q) = 2 cos p cos q, then set a = p+q, b = p−q.

With a = νt − kr₁, b = νt − kr₂:

y₁ + y₂ = [2A cos(kδ/2)] · cos(νt − k(r₁ + r₂)/2)

- **First factor (r₂ − r₁): amplitude.** No t, a constant at P. Sets brightness.
- **Second factor (r₁ + r₂): phase of the combined wave.** Sets *when* it peaks, not how high. Eyes and detectors average over time, so it does not affect brightness.

Two different "phases": the phase **difference** between the incoming waves causes interference and becomes the amplitude; the phase **of the result** does not matter.

**Conditions** (amplitude factor 2A cos(πδ/λ)):

- Bright: |cos(πδ/λ)| = 1 ⇒ πδ/λ = nπ ⇒ **δ = nλ**  (Zubairy 4.27)
- Dark: cos(πδ/λ) = 0 ⇒ πδ/λ = (2n+1)π/2 ⇒ **δ = (2n+1)λ/2**  (Zubairy 4.29)

**Same thing without the identity.** Phase gap kδ = 2π ⇒ cos(θ − 2π) = cos θ, waves identical. Gap π ⇒ cos(θ − π) = −cos θ, waves cancel.

| | δ = λ | δ = λ/2 |
|---|---|---|
| y₁ | A | A |
| y₂ | A cos(−2π) = A | A cos(−π) = −A |
| sum | 2A | 0 |

**Every point in between gets intermediate brightness.** I_P = 4I₀ cos²(φ/2), φ = 2πδ/λ, I₀ = intensity from one slit alone.

| δ | 0 | λ/4 | λ/2 | 3λ/4 | λ |
|---|---|---|---|---|---|
| I_P | 4I₀ | 2I₀ | 0 | 2I₀ | 4I₀ |

**Energy is redistributed, not created.** Average of the row = (4 + 2 + 0 + 2)/4 = 2I₀ = I₀ + I₀. Light moves from dark spots into bright spots.

**Lost light at the screens.** Real, but it only shrinks I₀ for both slits equally. Every row scales by the same factor; fringe positions depend only on δ. Half the light gives the same pattern, half as bright.

**Geometry (L ≫ d):** δ = d sin θ. Bright: d sin θ = nλ; dark: d sin θ = (2n+1)λ/2.

---

# 2. Blackbody radiation and quantisation of energy (Zubairy, Ch. 5)

## 2.1 Why anything glows

**Core idea.** Every object above absolute zero emits radiation, all the time. Temperature means its charges (electrons, atoms) jiggle; jiggling charges radiate. The heat can come from anywhere: a flame, current, absorbed light, fusion.

## 2.2 Emit and absorb at the same time; temperature stays fixed when they balance

**Core idea.** Every object is always both a source and a receiver. Its temperature is constant only when energy in = energy out, like a water tank whose level holds when inflow = outflow.

**Example.** Black object, 1 m², emission = σT⁴ (σ = 5.67 × 10⁻⁸ W/m²K⁴), inside an oven at 300 K.

| object T | emits | receives | net | result |
|---|---|---|---|---|
| 250 K | 221 W | 459 W | +238 W | warms up |
| 300 K | 459 W | 459 W | 0 | stays at 300 K |

The cold object still emits; it warms only because it receives more. Equilibrium = emission and absorption equal, not emission stopping.

Consequence (Kirchhoff): a good absorber at a wavelength is a good emitter at that wavelength.

## 2.3 What "blackbody" means and why we use it

**Core idea.** A blackbody absorbs everything that falls on it and reflects nothing. This is a property of the object; nothing has to actually be falling on it.

Why it matters:
- Everything coming off it is emitted, with no reflected light mixed in.
- Real objects' glow depends on their material. A blackbody's glow depends **only on T**.
- One universal curve per temperature, so a clean test for any theory.

"Black" does not mean dark when hot. It emits at all wavelengths, with a peak that moves with T.

Practical blackbody: a closed box with a small hole. Light entering bounces until absorbed; what leaves the hole is pure thermal radiation.

**The Sun** is close to a blackbody. Fusion in the core sets the temperature. Light made inside is absorbed and re-emitted an enormous number of times on the way out (≈100,000+ years), like the box with the hole. What escapes the 5800 K surface follows the blackbody curve, apart from some dark absorption lines.

## 2.4 Where the peak sits (Wien)

λ_peak ≈ (2.9 × 10⁻³ m·K) / T

| object | T | λ_peak | |
|---|---|---|---|
| human body | 310 K | ≈ 9.4 μm | infrared |
| hot iron | 1000 K | ≈ 2.9 μm | mostly infrared, faint red |
| Sun's surface | 5800 K | ≈ 0.5 μm | visible |

Heated iron: red → orange → white as T rises.

## 2.5 The classical failure: infinite energy

**Core idea.** Two classical assumptions:

1. Light is a wave, and there is always a shorter wave. The body's jiggling charges can produce any wavelength, so infinitely many are possible.
2. Heat spreads evenly: each possible wave gets the same share of energy (kT).

infinitely many waves × same share each = infinite energy

Most of it would pile up at short wavelengths (ultraviolet, X-rays). A warm stove would emit X-rays. Measured: the curve peaks and falls to zero. This is the **ultraviolet catastrophe** (Rayleigh–Jeans).

Same idea with a string: patterns n = 1, 2, 3, … have no last one. Equal share each:

| patterns counted | total energy |
|---|---|
| 10 | 10 units |
| 1,000 | 1,000 units |
| all | no limit |

## 2.6 Planck's fix: energy comes in packets

**Core idea.** An emitter of frequency f can hold energy only in whole packets of hf, and emits one packet at a time at its own frequency. Higher frequency means bigger packets. When one packet costs far more than the heat available, that emitter gets nothing.

Like a shop with fixed prices: ₹100 buys many ₹1 items but no ₹1000 item.

**Room temperature.** kT ≈ 0.026 eV; one visible packet ≈ 2 eV, about 77× more. Chance of affording even one ≈ e^{−77} ≈ 10⁻³³. Short-wavelength emitters stay empty, so the total is finite. Heat it up and more expensive packets become affordable, so the peak shifts toward blue.

**Toy model: three emitters with packets of 10, 5, 1 eV.**

Rules: each holds 0, 1, 2, … of its own packet only; emits its own packet size only.

*3 eV available:* 10 eV and 5 eV emitters hold 0; 1 eV emitter holds 3 packets. Out come three 1 eV packets.

*Residual energy* (e.g. 3.5 eV): the extra 0.5 eV is not emitted at another wavelength and does not vanish. It stays as ordinary jiggling of the atoms until it can make up a full packet.

*6 eV available:* two possible splits, switched between randomly; each equally likely.

| way | 10 eV | 5 eV | 1 eV |
|---|---|---|---|
| A | 0 | 1 packet | 1 packet |
| B | 0 | 0 | 6 packets |

Averages compared with classical even sharing:

| emitter | classical average | with packets |
|---|---|---|
| 10 eV | 2 eV | 0 eV |
| 5 eV | 2 eV | 2.5 eV |
| 1 eV | 2 eV | 3.5 eV |

The expensive high-frequency emitter is starved. That is the whole fix in miniature.

## 2.7 The three quantisation stories (Zubairy 5.1)

- **Planck (blackbody):** oscillator energy comes in packets ∝ frequency.
- **Einstein (photoelectric effect):** light itself comes in packets (photons) of energy hf. Below a threshold frequency, no electrons are ejected however intense the light, because no single packet is big enough.
- **Bohr (hydrogen):** electrons only in certain orbits; jumping down emits a photon of one definite frequency, giving discrete spectral lines.

---

# 3. Quantum mechanics formalism

## 3.1 Time evolution operator

**Core idea.** e^{−iHt/ħ} is *defined* as a power series of operators:

e^{−iHt/ħ} = Σₙ (−iHt/ħ)ⁿ / n!

Differentiating term by term shows iħ d/dt U = HU, so |ψ(t)⟩ = e^{−iHt/ħ}|ψ(0)⟩ solves the Schrödinger equation.

The "divide by the ket and take log" route is a mnemonic, not a proof. Rigorous routes: power series, or Picard iteration (repeated substitution builds the same series).

## 3.2 Dirac equation, spinors, rotations

- Schrödinger's equation is not relativistic. Klein–Gordon gave negative probabilities. Dirac used gamma matrices and 4-component spinors, which predicted antimatter.
- A spinor needs a 720° rotation to return to itself. A spin-½ (qubit) state is a 2-component spinor; Pauli matrices build the gamma matrices.
- **Rotations preserve dot products.** r·r = |r|² (Pythagoras). A rotation R satisfies RᵀR = I, so (Rr)·(Rs) = rᵀRᵀRs = r·s: lengths and angles are unchanged.

---

# 4. Quantum computing

## 4.1 GHZ states and dynamic circuits

- GHZ on n qubits (n ≥ 3): (|0…0⟩ + |1…1⟩)/√2. n = 2 is a Bell state.
- **Key identity** for dynamic GHZ: CX(a,b) CX(b,c) = CX(b,c) CX(a,b) CX(a,c). Reordering the CNOT staircase this way lets some qubits be measured, reset and reused mid-circuit (PRX Quantum 2024, *Efficient Long-Range Entanglement Using Dynamic Circuits*).
- **Qiskit is little-endian:** the rightmost bit is q₀.

## 4.2 IBM chip topology

- Gate map = which qubit pairs can run two-qubit gates (edges), not where qubits sit.
- Heavy-hex (low connectivity) reduced frequency collisions and ZZ crosstalk for fixed-frequency transmons. Square lattice (e.g. Nighthawk) became viable with tunable couplers.
- Transmons are lithographed circuits on silicon at ~15 mK in dilution refrigerators.

## 4.3 Magic states and partial measurement

- Clifford gates + stabilizer states are efficiently simulable classically (Gottesman–Knill). Universality needs a non-Clifford gate, e.g. T.
- Magic state |T⟩ = (|0⟩ + e^{iπ/4}|1⟩)/√2 injects a T gate via gate teleportation, using only Cliffords and measurement. Distillation dominates fault-tolerant resource costs.
- Partial measurement: measure subsystem A of H_A ⊗ H_B with projectors {P_m ⊗ I_B}. This is what mid-circuit measurement does.

## 4.4 Measurement on a superconducting transmon

**Core idea.** The qubit shifts the frequency of a coupled resonator by ±χ (dispersive regime). A probe tone reflected from the resonator comes back with a state-dependent phase and amplitude.

- Chain: AWG → IQ mixer → lines and attenuators → chip → circulator → JPA/TWPA → HEMT → digitizer.
- Each shot is a point in the IQ plane; |0⟩ and |1⟩ form two blobs. Overlap = readout error.
- **Readout error dominates projection error** because noise accumulates along the whole hardware chain.
- **T₁ makes the error asymmetric:** |1⟩ can decay to |0⟩ during readout, never the reverse, so the assignment matrix M is not symmetric. M3 mitigation corrects counts using M.

---

# 5. Group theory (Hamermesh; Joshi)

- **Axioms:** closure, associativity, identity, inverse. The identity is unique.
- **S₃:** the 6 permutations of 3 objects, written in two-row or cycle notation. Non-abelian.
- **Lagrange:** the order of a subgroup divides the order of the group.
- **Powers repeat** (pigeonhole): in a finite group, a, a², a³, … must repeat, so aᵐ = e for some m.
- **Prime order ⇒ cyclic.** Any non-identity a generates a subgroup of order > 1 dividing p, so it is the whole group: every element is a power of a, and aᵖ = e.
- **Order 4:** Z₄ (has an element of order 4) vs V₄ (every non-identity element has order 2). Build both with Cayley tables using the Latin-square rule (each element once per row and column).
- **Cayley's theorem:** every group is a subgroup of a permutation group, via g → π_g (the regular representation).

---

# 6. Vector calculus: divergence

**Core idea.** ∇·u = net outflow per unit volume from a tiny box at a point.

- Positive: net outflow (expanding, or a source inside).
- Negative: net inflow (compressing, or a sink).
- Incompressible fluid (ρ constant): ∇·u = 0.

**Example.** u = (x, y, z): ∇·u = 1 + 1 + 1 = 3, flow spreading out everywhere.

Next: Gauss's law for a point charge, where the field goes as r/|r|³.

---

# 7. Reading papers (QGSS 2026, Lanes & Weaver)

- **Read order:** abstract → conclusion → figures + captions → introduction → methods/supplement as needed.
- **Three questions:** what is the claim, what evidence supports it, what would weaken it?
- **Figure order:** caption → axes, units, legend → raw trend → error bars → fit vs data → compare to text.
- **Credibility ladder:** peer-reviewed journal > arXiv preprint > conference talk > company blog > headline/social post.
- **5-minute drill:** main claim; who and where; one figure-based piece of evidence; one scope-defining detail; one reason for skepticism or confidence.
- **Nature vs PRX Quantum:** same rung. Nature selects for cross-field significance with technical detail in supplements; PRX Quantum has deeper specialist review with detail in the main text.
- **Institutional credibility ≠ claim scope.** Review approves the paper; it does not certify results transfer to untested regimes.

---

# 8. Open threads

- Gauss's law / point-charge divergence (T5)
- Input-output theory: derive the reflected phase in dispersive readout
- Purcell filters: fast readout vs qubit decay
- Particle in a box via the Schrödinger equation (follows from 1.4)
- Continued Hamermesh chapters

# Blackbody radiation

Written up from the 2026-10-18 summary. Plain words first; every formula explained before
it is used. Pages: see the table at the bottom.

## 1. Why everything glows

- Everything warmer than absolute zero (0 K, the coldest possible temperature) gives off
  electromagnetic radiation, all the time ("light" = only the visible part).
- **Why:** temperature *is* jiggling. A warm object's atoms and electrons jiggle, and a
  jiggling electric charge sends out electromagnetic waves. Hotter means faster jiggling.
- Most of this radiation is invisible **infrared** (longer waves than red). A thermal camera
  sees it; our eyes do not. Only very hot things glow visibly.
- The heat can come from anywhere: a flame, an electric current, sunlight, nuclear fusion.

## 2. Radiation in and radiation out at the same time

- Every object both gives off radiation and absorbs radiation from its surroundings.
- Its temperature stays steady only when **energy in = energy out**, like a water tank
  whose level holds when inflow equals outflow. A steady temperature does not mean the
  object has stopped glowing.
- Example: a black object of area 1 m² glows with power σT⁴, where
  σ = 5.67 × 10⁻⁸ W/(m²·K⁴) (a measured constant). Inside an oven at 300 K:

  | object at | gives off | receives | net | result |
  |---|---|---|---|---|
  | 250 K | 221 W | 459 W | +238 W | warms up |
  | 300 K | 459 W | 459 W | 0 | stays at 300 K |

- A good absorber of a colour is also a good emitter of it. So a perfect absorber is also
  the best possible glower.

## 3. What a blackbody is

- A **blackbody** absorbs *all* the radiation that falls on it and reflects none, at every
  wavelength. "Black" describes what it does to incoming radiation, **not its colour**.
- Cold, it looks black: nothing bounces off, and its glow is invisible infrared. Hot, it
  glows red, then orange, then white. Everything you see from it is its own glow.
- **Why it matters:** an ordinary object's radiation is a mix of reflected radiation and
  its own, and its own depends on the material. A blackbody's radiation depends **only on
  its temperature**. So there is one universal curve per temperature: a clean test for any
  theory of radiation.
- **How to make one:** a closed box with a small hole. Radiation that enters bounces around
  and is absorbed before it can find the hole again. So the hole absorbs everything: the
  hole *is* the blackbody. Heat the box and what leaks out is pure glow.
- **The Sun is very nearly a blackbody.** Fusion in its core keeps it hot. Radiation made
  inside is absorbed and re-sent many, many times on its way out, taking thousands to
  hundreds of thousands of years. Like radiation in the box, it ends up matching the gas
  temperature. What escapes the 5800 K surface follows the blackbody curve, apart from
  some narrow dark lines where gases in the outer layer absorb particular colours.

## 4. Where the peak sits

- Hotter → the peak of the glow curve moves to shorter wavelengths:

  peak wavelength × temperature ≈ 2900 μm·K   (μm = micrometre, a millionth of a metre)

  | object | temperature | peak | |
  |---|---|---|---|
  | human body | 310 K | ≈ 9.4 μm | infrared |
  | stove ring / hot iron | 1000 K | ≈ 2.9 μm | infrared, faint red glow |
  | old light-bulb filament | 2800 K | ≈ 1.0 μm | infrared, yellowish glow |
  | Sun's surface | 5800 K | ≈ 0.5 μm | visible |

- Heated iron goes red → orange → white as it gets hotter.

## 5. What classical physics got wrong (step by step)

1. A body is made of atoms; atoms contain electrons (tiny charged particles).
2. Heating a body makes its atoms jiggle, and the electrons in them jiggle too. Hotter =
   harder jiggling.
3. A jiggling electron gives off radiation; faster jiggling = shorter wave.
4. Classical physics: electrons can jiggle at any speed, so any wavelength is possible and
   there is always a shorter one. Infinitely many possible waves, far more short than long.
5. Classical rule (worked for gases): heat energy spreads out evenly, like people passing
   coins at random. Every possible wave gets the same share.
6. Infinitely many waves × the same share = infinite energy, mostly in the short waves.
   Measured: the curve peaks and falls to zero. This failure is the **ultraviolet
   catastrophe**.

## 6. Planck's fix: energy comes in packets

- A wave of frequency f can only carry energy away in whole packets of size **E = hf**
  (h = Planck's constant, a fixed tiny number). Shorter wave = higher frequency = bigger
  packet. Half a packet is not allowed.
- **Toy example:** a body has 6 eV to give off and three possible waves: short (packet
  10 eV), medium (5 eV), long (1 eV). Classical: 2 eV each. With packets the short wave
  cannot get even one packet; only two ways are possible, equally likely: 5 + 1, or six 1s.

  | wave (packet) | classical: equal share | with packets: average |
  |---|---|---|
  | short (10 eV) | 2 eV | 0 eV |
  | medium (5 eV) | 2 eV | 2.5 eV |
  | long (1 eV) | 2 eV | 3.5 eV |

  The short wave is starved. That is the whole fix in miniature.
- **Real body:** the jiggling electrons have limited energy (set by temperature). Long waves
  need small packets: sent out easily, so classical physics is right there. Short waves need
  packets bigger than the electrons usually have: almost never sent out, so the curve falls
  to zero and the total is finite. Hotter → bigger packets possible → peak moves shorter.
  At room temperature even visible-light packets are too big: everyday objects don't glow.

## 7. Three quantisation stories

- **Planck (blackbody):** emitters hold energy in packets proportional to frequency.
- **Einstein (photoelectric effect):** radiation itself comes in packets (photons) of energy
  hf. Below a threshold frequency no electrons are knocked out, however bright the light,
  because no single packet is big enough.
- **Bohr (hydrogen):** electrons sit only in certain orbits. Dropping to a lower orbit
  sends out one photon of one definite frequency, giving sharp spectral lines.

## Page

[`blackbody-radiation.html`](blackbody-radiation.html): one page, three sections:
what a blackbody is (§1–3 above, briefly), where classical physics fails (§4–5), how
Planck fixed it (§6–7).

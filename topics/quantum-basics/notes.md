# Quantum basics — notes

Source of truth for [`deep-basics-notebook.html`](deep-basics-notebook.html).
Built from study sessions on 14–19 Nov 2026 (Lindblad derivation, Born rule, projectors,
Kraus operators). The page is a notebook of short cards rather than one concept per page;
split it into separate pages later if it grows.

Each card: a statement to say out loud, why it is true, one worked example, a recall question.

## Measurement

- **M1 Amplitude = overlap.** ⟨m|ψ⟩ is a dot product. Example: ⟨0|+⟩ = 1/√2.
- **M2 The sandwich builds itself.** p(m) = |⟨m|ψ⟩|² = ⟨m|ψ⟩*·⟨m|ψ⟩ = ⟨ψ|m⟩⟨m|ψ⟩ = ⟨ψ|P_m|ψ⟩.
- **M3 Projector = yes/no question.** Eigenvalues 1 and 0; P² = P, P† = P.
- **M4 Mixed state = a bag.** Classical chance pᵢ (never squared) × quantum chance given ψᵢ.
  Bag 25% |1⟩, 75% |+⟩ → p(0) = 3/8.
- **M5 Why the trace.** ⟨ψ|A|ψ⟩ = tr(A|ψ⟩⟨ψ|) (cyclic), so the bag becomes tr(Pρ).
  ρ = [[3/8, 3/8], [3/8, 5/8]], tr(P₀ρ) = 3/8.
- **M6 Coherence is basis-dependent.** Off-diagonals = interference; only questions that are
  not diagonal in ρ's basis read them. tr(P₊ρ) = 7/8 (½ without coherences).
- **M7 Projector vs observable.** Same formula tr(X·ρ): projector → probability, observable
  → average. O = Σ λ P. ⟨Z⟩ = 3/8 − 5/8 = −1/4. Born 1926; von Neumann 1927–32; Gleason 1957.
- **M8 The state is ρ itself.** The matrix is coordinates. Same ρ in the ± basis:
  [[7/8, −1/8], [−1/8, 1/8]]. Basis-free: eigenvalues ≈ 0.895, 0.105; purity 13/16; |r| = √10/4.
- **M9 Overlap of two errors.** ⟨ψ|E_i†E_j|ψ⟩ = overlap of E_i|ψ⟩ and E_j|ψ⟩; tr(A†B) for matrices.

## Channels and Kraus operators

- **K1** Each K is one possible outcome; only the set keeps trace (Σ K†K = I). One K → unitary.
- **K2** Kraus operators depend on the time window; rates do not.
- **K3** Memory breaks "same channel every step", not the Kraus form. Trotter = trick, Markov = assumption.
- **K4** Depolarizing → centre; amplitude damping → |0⟩; phase damping → Z axis.

## Lindblad

- **L1** K₀ = I + M·dt. **L2** K_k = √(γ_k dt)·L_k (rate × time = probability).
- **L3** M = A + iB, A = (M+M†)/2, B = (M−M†)/2i, unique. Hermitian ≠ diagonal.
- **L4** Completeness fixes A = −½ Σ γ L†L; γ = 0 limit gives B = −H.
- **L5** ρ̇ = −i[H, ρ] + Σ γ (LρL† − ½L†Lρ − ½ρL†L).
- **L6** Amplitude damping: L = σ₋; E₀ = V·diag(1, √p), V = 1 when H = 0; T2 = 2T1, T2 ≤ 2T1.

## Slips to avoid

tr(Aρ) ≠ tr(A)tr(ρ) · channel is KρK† · (cX)† = c*X† · |0⟩⟨1| is not a projector ·
p(0) is tr(P₀ρ), not tr(Zρ) · Hermitian part ≠ entry-wise real part · dt² ÷ dt = dt.

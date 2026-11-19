# Quantum basics — notes

Source of truth for [`deep-basics-notebook.html`](deep-basics-notebook.html).
Built from sessions on 14–19 Nov 2026 (Lindblad derivation, Born rule, projectors,
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

## Channels and Kraus operators

- **K1** Each K is one possible outcome; only the set keeps trace (Σ K†K = I). One K → unitary.
- **K2** Kraus operators depend on the time window; rates do not.
- **K3** Memory breaks "same channel every step", not the Kraus form. Trotter = trick, Markov = assumption.
- **K4** Depolarizing → centre; amplitude damping → |0⟩; phase damping → Z axis.

## Lindblad: what to take away

- **L1 Rotation plus loss, no memory.** dρ/dt = −i[H, ρ] + Σₖ γₖ (Lₖ ρ Lₖ† − ½ Lₖ†Lₖ ρ − ½ ρ Lₖ†Lₖ).
  H generates the unitary; the jump term moves the state; the −½ terms keep the trace at 1.
- **L2 One tiny step.** K₀ = I + M·dt; Kₖ = √(γₖ dt)·Lₖ (rate × time = probability).
- **L3 Loss fixed, rotation free.** M = A + iB; trace preservation fixes A = −½ Σ γₖ Lₖ†Lₖ;
  B is free and equals −H. σ₋ = X/2 + i·Y/2.
- **L4 Choose the jump.** Relaxation: L = σ₋. Dephasing: L = Z.

## T1 and T2 (ρ = [[ρ₀₀, ρ₀₁], [ρ₁₀, ρ₁₁]], H = 0)

- **T1 Amplitude damping (L = σ₋, rate γ).** ρ₁₁(t) = ρ₁₁(0)e^(−γt); ρ₀₀(t) = 1 − ρ₁₁(0)e^(−γt);
  ρ₀₁(t) = ρ₀₁(0)e^(−γt/2). T1 = 1/γ, T2 = 2T1.
- **T2 Phase damping (L = Z, rate γᵩ).** Populations constant; ρ₀₁(t) = ρ₀₁(0)e^(−2γᵩt). T2 = 1/(2γᵩ).
- **T3 Both.** 1/T2 = 1/(2T1) + 2γᵩ, so T2 ≤ 2T1 (equal only with no pure dephasing).

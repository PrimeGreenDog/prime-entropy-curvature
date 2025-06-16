# Entropy Distance and Curvature Maps

## 🧠 Overview
This document introduces a symbolic framework to map entropy across the natural numbers using **distance to prime boundaries**, **shell curvature**, and **resonance with irrational constants** like φ and π. The goal is to construct an **entropy curvature map** over ℕ — revealing high- and low-tension regions in number space, much like gravitational or electromagnetic potential fields.

---

## 📏 Key Definitions
Let:
- ℕ = Natural numbers
- P = Set of prime numbers
- φ = Golden ratio = (1 + √5)/2

For any number \( n \in \mathbb{N} \):

### 1. Distance to Nearest Primes:
Let \( p^- \) and \( p^+ \) be the closest primes below and above n:
\[ D_{min}(n) = \min(|n - p^-|, |n - p^+|) \]

This gives a **local entropy gradient**: closer to a prime = lower symbolic entropy.

### 2. Shell Curvature Score:
Let \( p_n < n < p_{n+1} \) be the bounding primes. Then:
\[ \xi = \frac{n - p_n}{p_{n+1} - p_n} \]
\[ C(n) = \xi(1 - \xi) \cdot (p_{n+1} - p_n)^q \]
Where:
- \( q \) is a tuning constant (typically 1 or 2)
- C(n) peaks at shell midpoint, giving a curvature score

### 3. Irrational Resonance:
Let:
\[ R_\phi(n) = \cos(2\pi \phi^n) \]
This expresses **resonance alignment** with φ. The closer R_φ(n) is to 1, the more the number is symbolically in phase with golden field structure.

---

## 🔢 Entropy Function
Symbolic entropy at a point n combines these three components:
\[ S(n) = w_1 \cdot \frac{1}{D_{min}(n)^k} + w_2 \cdot C(n) + w_3 \cdot (1 - |R_\phi(n)|) \]
Where:
- \( w_1, w_2, w_3 \) are tunable weights
- \( k > 1 \) controls decay rate of prime distance influence

This defines a symbolic **entropy field** over ℕ.

---

## 🌐 Visual Representation
We can visualize S(n) as a curve or heatmap:
- X-axis: n (natural numbers)
- Y-axis: S(n) (symbolic entropy)
- Peaks occur between sparse primes or at φ-misaligned points
- Valleys occur at or near primes, Fibonacci points, or shell edges

---

## 📊 Practical Applications
- Symbolic entropy mapping of number space
- Tuning φ-based or prime-shell RNGs using entropy wells
- Highlighting zones of symbolic uncertainty vs resonance
- Foundations for symbolic field simulations or encryption patterns

---

## 🔮 Future Directions
- Extend maps into 2D or radial shell visualizations
- Add π-resonance and e-curvature overlays
- Use entropy maps to guide encryption key generation or entropy harvesting
- Connect with physical field analogies (gravity, charge, wave interference)

> "Entropy is not just a measure of disorder — it is a shadow cast by structure."

# Symbolic Entropy Random Number Generators

## 🎯 Overview
This post outlines three symbolic random number generators (RNGs) inspired by the Prime Entropy Curvature model. These generators are built using:
- The golden ratio (φ) as a high-entropy seed
- Prime-based digit selection from π or φ
- Recursive and non-recursive transformations

The goal is to explore alternative definitions of randomness and entropy using structured number fields, rather than pure pseudorandom logic.

---

## 📐 Generator 1: Recursive φ RNG (GRRG)
**Golden Recursive Random Generator (GRRG)** uses recursive indexing from the digits of φ:

1. Start with the digits of φ = 1.6180339887...
2. Index into φ using its own digits to define a set size:
   ```python
   s = digits[digits[digits[i]]]
   ```
3. Use those digits to extract values and perform operations:
   ```python
   r = sum(set_values) % 10
   ```
4. Output is bounded in [0–9] and highly entropic, but **not uniform**

**Statistical Result:**
- Entropy ≈ 2.18 (vs max 2.30 for uniform)
- Fails chi-square uniformity (structured bias)

**Use:** Symbolic entropy modeling, not cryptographic randomness.

---

## 📐 Generator 2: Stateless φ RNG
A non-recursive, stateless version using φ digits:

1. Use a sliding window of digits:
   ```python
   r = (d0 * d1 + d2 + d3) % 10
   ```
2. Each output is computed from a fixed-length slice of φ
3. Variations tested:
   - Sum mod
   - XOR mod
   - Cross-multiplication
   - Alternating difference mod

**Best Variant:**
```python
r = (d0 * d1 + d2 + d3) % 10
```
**Statistical Result:**
- Entropy ≈ 2.2978
- Passes chi-square test for uniformity (p ≈ 0.4)

**Use:** Suitable as a φ-based high-entropy generator for simulations.

---

## 📐 Generator 3: Prime-Cycled RNG using π (987 Mod Method)
A generator built from:
- Digits of π
- Prime index jumps (based on 987)
- Transformations based on selected digit groups

### Method A: Recursive Prime-Based (2×987 jump)
1. Use digits of π
2. Step every 987 digits (a Fibonacci prime)
3. Use multiple primes (like 2, 3, 5) as cycling factors
4. Select subsets, perform operations (sum, XOR, mod)

### Method B: Mixed Transformations
1. Cycle through XOR, addition, multiplication
2. Use π digits selected via multiples of 987
3. Keep all output bounded in [0–9]

**Statistical Result:**
- Entropy varies by transformation
- May show structure depending on combination

**Use:** Symbolic RNG suitable for modeling primes as structured entropy sources

---

## 📊 Comparison Table

| Generator              | Recursive? | Entropy | Chi-Square p-value | Notes                         |
|------------------------|------------|---------|---------------------|-------------------------------|
| GRRG (Recursive φ)     | Yes        | 2.1836  | 0.0000 ❌           | High structure, biased        |
| Stateless φ RNG        | No         | 2.2978  | 0.3966 ✅           | Best statistical behavior     |
| Prime 987 Cycled RNG   | No/Yes     | ~2.25   | Variable            | Tunable via jump and transform |

---

## 🔧 Applications
- Symbolic field simulations
- Pattern discovery in irrational numbers
- Testbed for entropy structure vs chaos
- Educational tools for exploring non-standard RNGs

---

## 🚀 Next
The symbolic entropy field simulator will combine these generators as configurable modules. Users will be able to test symbolic fields with structured vs chaotic entropy inputs.

All math is open for testing, challenge, and evolution.

> Randomness may be an illusion. This is a step toward structured uncertainty.

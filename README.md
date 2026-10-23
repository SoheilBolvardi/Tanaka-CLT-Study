# Tanaka's Central Limit Theorem: A Study in Wasserstein Distance

An undergraduate **probability-theory reading and exposition project** exploring Tanaka's central limit theorem in the Wasserstein-2 metric. The emphasis is on the mathematical background, optimal couplings, and a proof *outline* rather than a new theorem or a fully self-contained research proof.

> **Reading note:** The original PDFs are preserved as submitted. Before relying on mathematical statements in them, please read the **[corrections and clarifications](CORRECTIONS.md)**. In particular, these notes make explicit which parts of the strict Wasserstein inequality and the convergence argument are cited rather than proved.

## Documents

| Document | Contents |
| --- | --- |
| [Part 1 — Probability and measures](exposition/Part1.pdf) | Sigma-algebras, probability measures, a Vitali-set argument, continuity of measures |
| [Part 2 — Random variables and integration](exposition/Part2.pdf) | Measurability, probability laws, Lebesgue integration, expectation |
| [Part 3 — Distances and couplings](exposition/Part3.pdf) | Total variation distance, coupling inequalities, Wasserstein distance, quantile couplings |
| [Part 4 — Tanaka's CLT](exposition/Part4.pdf) | Contraction in squared Wasserstein-2 distance, dyadic sums, a proof outline |
| [Final project report (joint work)](report/Final-Report.pdf) | Short summary prepared as part of the Probability and Statistics course project |
| **[Corrections / mathematical clarifications](CORRECTIONS.md)** | **Read this alongside the original PDFs** |

## What I studied

I worked through measure-theoretic probability, couplings and probability metrics, writing a four-part set of explanatory notes that develops the concepts needed to follow Tanaka's argument. I also explored worked examples illustrating how different couplings can affect total variation and Wasserstein distances.

The **final course report was a group submission**, as indicated by the contributor names on its first page. The repository presents the report together with the supporting notes; it does not claim that the group report was written by one person.

## Scope of the argument

For i.i.d. square-integrable random variables with nonzero variance, Tanaka's CLT establishes convergence of the normalized sums to a standard Gaussian in **Wasserstein-2 distance**. The learning-oriented outline here uses an **additional finite-fourth-moment assumption** to simplify control of moments in a limiting argument. That stronger assumption belongs to the *outline*, **not to the original theorem**.

The equality/strictness characterization used by the proof is a substantial result from Tanaka's original paper; it is cited, not proved independently in these notes. The corrected mathematical statements and other fixes are collected in [CORRECTIONS.md](CORRECTIONS.md).

## References

- Hiroshi Tanaka (1973), *An inequality for a functional of probability distributions and its application to Kac's one-dimensional model of a Maxwellian gas*, **Z. Wahrscheinlichkeitstheorie verw. Gebiete**, 27, 47–52. [Original paper](https://www.math.utoronto.ca/mccann/assignments/477/Tanaka73.pdf)
- Oliver Johnson and Richard Samworth (2005), *Central limit theorem and convergence to stable laws in Mallows distance*, **Bernoulli**, 11(5), 829–845. [DOI](https://doi.org/10.3150/bj/1130077596)
- Lasse Leskelä, *Probability Theory: A Fast Course*, §12.5. [Lecture notes](https://math.aalto.fi/~lleskela/papers/Leskela_2024-10-21_Probability_theory.pdf)
# Tanaka's Central Limit Theorem — Study in Wasserstein Distance

An undergraduate **reading and exposition project** on probability metrics, optimal couplings, and a coupling-based proof strategy for the central limit theorem in second-order Wasserstein distance.

The four study notes and the joint course report have been **re-typeset and mathematically revised** from the earlier PDF-only materials. The revised editions are **edited, shorter presentations**, not line-for-line transcriptions of the original notes. They incorporate corrections directly into their text and formulas, instead of asking readers to consult a separate corrigendum. Editable LaTeX sources are provided alongside the PDFs.

## Read the study notes

| Part | Subjects | Revised PDF | Editable source |
| --- | --- | --- | --- |
| 1 | Sigma-algebras, measures, the Vitali argument, continuity of measures, union bound | [Part 1](exposition/Part1.pdf) | [LaTeX](exposition/Part1.tex) |
| 2 | Measurable functions, random variables, laws, Lebesgue integration, convergence theorems | [Part 2](exposition/Part2.pdf) | [LaTeX](exposition/Part2.tex) |
| 3 | Total variation, couplings, Wasserstein distances, quantile coupling | [Part 3](exposition/Part3.pdf) | [LaTeX](exposition/Part3.tex) |
| 4 | Tanaka's comparison inequality and an outline of the Wasserstein-2 CLT | [Part 4](exposition/Part4.pdf) | [LaTeX](exposition/Part4.tex) |

**Joint final course report:** [Revised report (PDF)](report/Final-Report.pdf) · [LaTeX source](report/Final-Report.tex).

The final report is joint coursework by **Soheil Bolvardi, Mohammadamin Khedri, and Houman Rajaeian**. The four study notes are an undergraduate mathematical exposition; neither the report nor these notes claim a new theorem or a self-contained original proof of the equality characterization in Tanaka's inequality.

## Mathematical scope

The central limit theorem in `W_2` assumes i.i.d. observations with a finite, positive variance. The **coupling-based proof outline** in Part 4 uses an **additional finite fourth moment** to simplify compactness and the passage to `W_2` limits. That extra assumption belongs to this exposition, **not** to the theorem itself.

The key strictness/equality statement associated with Tanaka's comparison inequality is **cited rather than proved**. Part 4 also explains how the full finite-second-moment conclusion follows by combining the classical CLT with the standard Wasserstein convergence criterion. It carefully distinguishes the nonincreasing **dyadic** distances from convergence along all sample sizes.

## Improvements in the revised editions

The rewritten texts fix the Vitali-set measure argument; state dominated convergence with its correct hypotheses; repair the independent Bernoulli coupling calculation and the absolute value in the quantile formula; correct Gaussian variances and the binary-block example; and justify the limiting-law step in the coupling outline. Valid elementary examples and core derivations are retained, though the presentation has been shortened and reorganized.

## Reproducibility

Compile each `.tex` file with **pdfLaTeX** in a standard TeX Live environment. The sources use common mathematics and typography packages; Part 2 also uses TikZ for an illustrative diagram. No proprietary font files are needed.

## References

- H. Tanaka (1973), *An inequality for a functional of probability distributions and its application to Kac's one-dimensional model of a Maxwellian gas*. *Zeitschrift für Wahrscheinlichkeitstheorie und Verwandte Gebiete*, **27**, 47–52.
- O. Johnson and R. Samworth (2005), *Central limit theorem and convergence to stable laws in Mallows distance*. *Bernoulli*, **11**(5), 829–845.
- L. Leskelä, *Probability Theory: A Fast Course*, §12.5.

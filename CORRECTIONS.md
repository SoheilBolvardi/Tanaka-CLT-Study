# Corrections and clarifications to the Tanaka CLT study

**Status:** companion corrigendum to the PDF reading notes and the jointly authored final report. The archived PDFs are retained unchanged. For mathematical accuracy, read these corrections **before** relying on the corresponding original pages.

The project studies an existing result, rather than presenting a new theorem or a complete independent proof. In particular, the proof outline invokes Tanaka's strict inequality (including its equality characterization) without reproving that characterization.

## Part 1 — Measure-theoretic foundations

**Printed pp. 3–4: Vitali-set argument.** Restrict to *rational* translations. With a Vitali representative set `V` chosen from `[0,1]`, set

\[
A=\bigcup_{q\in\mathbb Q\cap[-1,1]}(V+q).
\]

For distinct rational `q`, the translates `V+q` are disjoint; furthermore

\[
[0,1]\subseteq A\subseteq[-1,2].
\]

Suppose a nonnegative, countably additive, translation-invariant measure `m` were defined on **every** subset of the real line and agreed with ordinary length on intervals. Then `1 <= m(A) <= 3`. On the other hand, disjointness and translation invariance give

\[
m(A)=\sum_{q\in\mathbb Q\cap[-1,1]}m(V)\in\{0,+\infty\},
\]

contradicting the bound above. **Do not identify** `m(A)` with `m([0,1])`, or assert that the points outside `[0,1]` have measure zero. The conclusion is the impossibility of extending ordinary length to all subsets while preserving the stated properties, not the impossibility of measuring ordinary measurable sets.

## Part 2 — Measurability and integration

- **Printed p. 2 (measurability):** The correct condition is that the *preimage* of every measurable target set is measurable in the domain, `f^{-1}(B) in S_1` for `B in S_2`. The informal wording about every target set being the *image* of a domain set is inaccurate.
- **Printed p. 5 (identity-map construction):** Replace “Thus `mu` is the law of `B`” by “Thus `mu` is the law of `X`.”
- **Printed pp. 7–8 (dominated convergence):** For measurable functions `f_n`, suppose `f_n -> f` almost everywhere and `|f_n| <= g` almost everywhere for **one integrable** function `g`. Then `integral f_n dmu -> integral f dmu`. The one-sided condition `f_n < g` does not suffice.
- **Printed p. 8 (expectations):** The corresponding version requires `X_n -> X` almost surely and `|X_n| <= Y` for an integrable random variable `Y`; *individual* integrability `E|X_n|<infinity` is insufficient. Bounded convergence on a probability space follows from a uniform bound `|X_n| <= C` and almost-sure convergence.

## Part 3 — Couplings and Wasserstein distance

- **Printed p. 4 (discrete total variation):** The formula must be `d_TV(mu_1,mu_2) = (1/2) sum_{x in S} |f_1(x)-f_2(x)|` when `f_1,f_2` are probability mass functions on a countable set. The indices in the displayed discrete formula in the original notes are incorrect.
- **Printed p. 7 (independent Bernoulli coupling):** If `X_1 ~ Ber(p)` and `X_2 ~ Ber(q)` are independent,

  \[
  P(X_1\ne X_2)=p(1-q)+(1-p)q=p+q-2pq.
  \]

  For `p=0.5`, `q=0.6`, this probability is **0.5**, not 0.6. The later *dependent* ordered coupling with disagreement probability `q-p=0.1` is a different coupling and remains correct. The true total variation distance is `|p-q|=0.1`.
- **Printed p. 9 (quantile-coupling formula):** For distributions on `R` with finite `p`-th moments and `p>=1`,

  \[
  W_p(\mu,\nu)=\big(\mathbb E|Q_\mu(U)-Q_\nu(U)|^p\big)^{1/p},\quad U\sim\operatorname{Unif}(0,1).
  \]

  The **absolute value** is essential for arbitrary real `p>=1`, especially odd integers.

## Part 4 — Tanaka's central limit theorem

1. **Printed p. 2 (Gaussian comparison variables):** For independent centered `X,Y` with variances `sigma_X^2, sigma_Y^2`, choose independent `Z_X ~ N(0,sigma_X^2)`, `Z_Y ~ N(0,sigma_Y^2)` and set

   \[
   Z=aZ_X+bZ_Y\sim N(0,a^2\sigma_X^2+b^2\sigma_Y^2).
   \]

   Thus the squared comparison inequality reads

   \[
   W_2^2(aX+bY,Z)\le a^2W_2^2(X,Z_X)+b^2W_2^2(Y,Z_Y).
   \]

   The original Gaussian definitions contain incorrect powers/coefficient placements.
2. **Printed p. 3 (equality case):** The argument from equality of costs to equality *as random variables* of distinct optimal couplings is not justified. The final remark that “only a normal random variable has a linear quantile function” is false: e.g. a uniform distribution on `[0,1]` has quantile `Q(u)=u`, while a Gaussian has nonlinear quantile `Phi^{-1}(u)`. **Replace the equality-case derivation by a citation of Tanaka's strictness theorem (Theorem 2 of Tanaka, 1973)**. Its proof relies on a separate characterization of equality for optimal couplings. Therefore the discussion here is a **proof outline**, not a self-contained proof of strictness.
3. **Printed p. 4 (limit):** Replace `as n -> 0` with **`as n -> infinity`**.
4. **Printed p. 4 (limit distribution):** The existence of a weakly convergent subsequence follows from tightness of the normalized sums (they all have variance one). The additional uniform fourth-moment bound supplies uniform integrability of their squares, allowing convergence of second moments along a weakly convergent subsequence and hence convergence in `W_2`. If `D_k=W_2^2(Law(gamma_{2^k}),N(0,1))`, then `D_{k+1}<=D_k`; write `D_k -> ell`. Under a subsequential `W_2` limit `mu`, both `W_2^2(mu,N(0,1))` and `W_2^2(Law((U+V)/sqrt(2)),N(0,1))` equal `ell` for independent `U,V~mu`. **Invoking** (rather than reproving) the strictness statement forces `mu` to be Gaussian and `ell=0`. This supplies the omitted justification for the outline.
5. **Printed p. 5 (general `n`):** Binary decomposition extends convergence from `n=2^k` to all `n`; the argument does **not** prove monotone decrease of `W_2` for every integer `n`. Replace the closing claim of monotone convergence by simple convergence `W_2 -> 0` as `n -> infinity`.
6. **Printed p. 5 (`n=13` example):** In the final decomposition, the coefficient `sqrt(4/13)` multiplies **`eta_2`**, not `eta_1`.

## Final report — additional reading guidance

The **final report lists three contributors** and is a joint course report. Its high-level account of the proof repeats some of the same shortcuts as Part 4, notably the appeal to an equality characterization and the passage to the limiting distribution. The report should be described as a **survey and proof outline**, not a fully self-contained proof under only the second-moment hypothesis. The extra finite-fourth-moment assumption is used only to simplify this exposition; **it is not an assumption of Tanaka's theorem itself**. The report also summarizes convergence as if the distance necessarily decreased at every integer sample size; the monotonicity argument in the notes is only established for dyadic sizes.

## References for the omitted strictness step

- H. Tanaka (1973), *An inequality for a functional of probability distributions and its application to Kac's one-dimensional model of a Maxwellian gas*, **Zeitschrift für Wahrscheinlichkeitstheorie und verwandte Gebiete** 27:47–52; see **Theorem 2**, in the original article: https://www.math.utoronto.ca/mccann/assignments/477/Tanaka73.pdf
- O. Johnson and R. Samworth (2005), *Central limit theorem and convergence to stable laws in Mallows distance*, **Bernoulli** 11(5):829–845, https://doi.org/10.3150/bj/1130077596
- L. Leskelä, *Probability Theory: A Fast Course*, Section 12.5 (states the result and points to the technical proofs), https://math.aalto.fi/~lleskela/papers/Leskela_2024-10-21_Probability_theory.pdf

*This correction note is meant to accompany the original teaching/reading material. It does not claim that the original PDF pages have been silently rewritten.*
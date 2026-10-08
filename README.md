# Conjecture-Random-OpenAI

## Lehmer's totient problem: analytic constraints on a composite solution

Author: Deep Bhattacharjee

The paper is `paper/main.tex` (LaTeX, `amsart`; build with `pdflatex main.tex`).

**Status: neither of Lehmer's questions is settled here.** The paper gives
complete, purely analytical proofs (no computer-assisted step) that a
composite n with φ(n) | n−1 or φ(n) | n+1 and k prime factors satisfies:

- k ≥ 11 when 3 ∤ n, for both equations (seven hand-checkable cases; eleven
  is the limit of the method, see Proposition 8 of the paper);
- for φ(n) | n−1 with 3 ∤ n and k ≤ 222, n ≡ 1 (mod 3);
- for φ(n) | n−1 with 3 | n, (n−1)/φ(n) ≡ 1 (mod 3) and k ≥ 111;
- for φ(n) | n−1, n < (2k)^(2^k)/k.

Stronger bounds are known (Cohen–Hagis, Hagis, Pomerance, and the
computations of creelie/Lehmer-1-2); the paper cites them.

`notes/residuals.md` records a second pass over all the reference
repositories (D4 sphere packing, Hodge, Navier–Stokes, Lehmer): what each
leaves open and why none of those residuals closes by an analytical
argument.

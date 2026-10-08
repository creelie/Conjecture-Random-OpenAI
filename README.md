# Conjecture-Random-OpenAI

## Lehmer's totient problem: analytic constraints on a composite solution

Author: Deep Bhattacharjee

The paper is `paper/main.tex` (LaTeX, `amsart`; build with `pdflatex main.tex`).

**Status: Lehmer's conjecture is not proved here.** The paper gives
complete, purely analytical proofs (no computer-assisted step) that a
composite n with φ(n) | n−1 and k prime factors satisfies:

- n is odd, squarefree, gcd(n, φ(n)) = 1 and n ≡ 1 (mod 2^k);
- k ≥ 10 when 3 ∤ n;
- when 3 ∤ n, either some prime factor is ≡ 1 (mod 3) (so n ≡ 1 mod 3) or k ≥ 223;
- when 3 | n, (n−1)/φ(n) ≡ 1 (mod 3) and k ≥ 111;
- n < (2k)^(2^k)/k, so each k has finitely many solutions.

Most of these are weaker than known results (Lehmer 1932, Cohen–Hagis 1980,
Pomerance 1977, Hagis 1988), which the paper cites. Section 6 states where
the method stops: the product inequality behind the lower bounds is
satisfied by an admissible set of eleven primes, so it cannot by itself
reach k ≥ 12, and nothing in the paper makes the upper and lower bounds meet.

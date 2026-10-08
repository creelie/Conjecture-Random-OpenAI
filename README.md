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

## The Hodge conjecture for abelian varieties of Weil type

Author: Deep Bhattacharjee

**Status: the Hodge conjecture is not proved here.**

`paper/hodge/weil_closure_attempt.tex` is a closure attempt for the Weil
class on a general abelian variety of Weil type. It proves what the attempt
gives and states exactly where it stops:

- the algebraic locus is dense, and it is either everything or meagre;
- strata through a member with full Hodge group have full monodromy;
- one semiregular cycle would close the locus;
- the locus is everything if and only if the Weil class has representatives
  of bounded degree on a Zariski-dense set (a variant of H8's bounded
  criterion);
- at a member with full Hodge group, nothing built from divisors and
  homomorphisms reaches the Weil class (H8's Lefschetz-closure argument,
  carried over to Weil classes), and neither do the tautological cycles of
  curves with an automorphism of order three (new);
- Schoen's cycles on Prym varieties do reach the Weil class at members with
  full Hodge group for Q(sqrt(-3)), but only on a locus of dimension 3n.
  Whether one of them is semiregular is the concrete open question the note
  isolates.

`book/` is the draft of a monograph, *Weil Classes and the Hodge
Conjecture*. All seven chapters and the bibliography are in a first draft
(about 70 printed pages). It has not been compiled here, because this
environment has no LaTeX. `book/proposal.md` is a draft Springer proposal, with
notes on how to submit it.

# What is still open in the reference repositories

A second pass over the six reference repositories, looking for a residual
gap small enough to close by a purely analytical argument. None closes.
Each entry says what the source itself leaves open and why the gap is not
a missing routine step.

## D4 / twenty-four-cell (creelie/d4-voronoi-cells)

The paper (`paper/D4.tex`, section "What is open", around line 9615)
reduces the conjecture to two statements:

- **(G)** a volume bound when exactly 24 centres lie within √6;
- **(C)** a bound on the union of caps when 25 to 28 centres do.

(C) is proved from 29 centres on, and at 28 only when at most 14 centres
lie within 2.0161 (or 15 with at most three beyond 2.35, or 16 with none
beyond 2.35). (G) is proved along push-outs of the root system and near it.

Why it does not close: the paper shows that both statements need a
*localisation* (24 centres with T ≤ 8 must lie near a copy of √2·D4), and
that every method it tried stops short: directions alone fail at slack
0.01698, where a second 24-point code appears; pair margins give out at
slack about 5·10⁻⁴; pair kernels do not exclude 25 centres at any degree
tried. The localisation has to use triples of centres or more. The proved
cases also rest on semidefinite certificates and branch-and-bound, so even
those are computer-assisted.

## Hodge conjecture (creelie/H8 and the math01-openai preprints)

In the math01-openai corpus (result family 032), the rational Hodge
conjecture is stated as proved for every CM abelian variety, for products
of K3 surfaces, and with the Kuga–Satake correspondence algebraic for
every projective K3.

What is left for abelian varieties is the Weil classes on a *general*
member of a Weil-type family. H8's closure theorem (`tex/sections/14_closure.tex`,
item (ii)) reduces this, for each triple (K, n, δ), to the algebraicity of
one explicit class ω₁ at every point of an n²-dimensional period domain.
It also shows that the algebraic locus is either everything or meagre. The
same section lists more than a dozen constructions that provably cannot
produce the class, including semiregularity with exact Weil character,
line-bundle sums, hyperplane induction, Kuga–Satake from a weight-two
piece and secant objects.

Why it does not close: closing it needs a cycle at a *general* member.
At members with full Hodge group one construction is known, Schoen's cycles
on Prym varieties for Q(√−3) with split form, but they fill only a locus of
dimension 3n inside a family of dimension n², so for n ≥ 4 they do not
reach a general member. (An earlier version of this note said no
construction was known at members with full Hodge group; that was wrong.)
This is the core of the Hodge conjecture for abelian varieties, not a small
residual.

## Navier–Stokes (creelie/NavierStokesAndEuler)

The repository formalises, in Lean 4, OpenAI's claimed finite-time
breakdown for forced Navier–Stokes on ℝ³ and on the torus. I read the
challenge statement (`ComparatorChallenges/NavierStokes.lean`) and checked
it against Fefferman's Clay alternatives (C) and (D):

- The initial data are smooth and divergence-free, with all derivatives
  decaying faster than any power (Clay condition 4). On the torus they are
  periodic instead.
- The forcing is smooth on ℝ³ × [0, ∞) with |∂ᵐf| ≤ C(1+|x|+t)^(−K)
  (condition 5). On the torus it is periodic with (1+t)^(−K) decay
  (conditions 8 and 9).
- Solutions are smooth on ℝ³ × [0, ∞) with the equation, the
  incompressibility condition and the initial condition. On ℝ³ the energy
  must be uniformly bounded. On the torus the velocity and pressure must
  be periodic, as in the Clay errata.
- The solution file `NavierStokes/ComparatorSolution.lean` restates these
  two theorems word for word and allows only the axioms `propext`,
  `Quot.sound` and `Classical.choice`.

I found no mismatch with the Clay wording. So if the proof is faulty, the
fault is not in what it claims to prove. I could not build the Lean
project here (no Lean toolchain in this environment), so I have not
checked that the proof compiles.

## Lehmer's totient problem (creelie/Lehmer-1-2)

The paper proves k ≥ 16 for Lehmer's equation and settles the companion
equation up to eight prime factors, all by search. Its own list of what is
open (`paper/main.tex`, "The next cases" and "What a proof for all k has to
use"):

- k = 16 for Lehmer's equation, estimated at about 10¹⁰ processor-seconds;
- the companion equation with 3 | n and nine or more prime factors;
- whether a *pseudo-solution* with pairwise coprime entries exists.

The paper explains why the residuals are hard: no fixed-modulus
congruence removes a prefix with two primes left (Proposition "local"),
and for the companion equation the Fermat primes give a prefix whose shortfall is only 2⁻³¹.

What the elementary method gives, written up in `paper/main.tex` of this
repository:

- k ≥ 11 for both equations when 3 ∤ n, which is the method's limit, since
  the admissible set {5, 7, 13, 17, 19, 23, 37, 59, 67, 73, 83} has
  ∏ p/(p−1) > 2;
- n ≡ 1 (mod 3) when 3 ∤ n and k ≤ 222;
- k ≥ 111 when 3 | n;
- n < (2k)^(2^k)/k.

## Summary

| problem | smallest residual | closable analytically here? |
| --- | --- | --- |
| D4 sphere packing | localisation of 24 centres near √2·D4 | no; needs triple-level information |
| Hodge (abelian varieties) | algebraicity of ω₁ at a general member | no; this is the conjecture itself |
| Navier–Stokes | none in the statement; the Lean statement matches Clay (C), (D) | nothing to close; proof not rebuilt here |
| Lehmer | k ≥ 16 and beyond, pseudo-solution questions | partial only: k ≥ 11 by hand |

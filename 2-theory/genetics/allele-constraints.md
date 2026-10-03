# Allele Constraints

## The four-copy constraint

Standing constraint: at any one autosomal locus, a founder pair holds at
most four copies. Descendants have only those alleles, plus mutations that
arise and spread later. Recombination does not invent a fifth allele at that
locus.

## What the constraint does

- It bounds what standing variation a single pair can transmit, which is why
  PDP-03 (Founder Genome Feasibility) is probably the critical technical
  stream.
- It rules out auxiliaries that quietly enrich the founder stock: any
  auxiliary giving the pair more than four alleles at a locus changes the
  origin stock.

## Revision discipline

Per charter Rule 2, such an auxiliary is a programme revision, not an
ordinary protective-belt adjustment. The seed specification is explicit:
giving the pair more than four alleles changes the origin stock rather than
merely adjusting an auxiliary.

## Interfaces

- `1-boundary/preserved-stock.md` - the stock the constraint applies to.
- `2-theory/genetics/recombination.md` - what recombination can and cannot
  do under the cap.
- `2-theory/genetics/mutation.md` - the only source of genuinely new alleles
  after the bottleneck.
- `registry/AUXILIARIES.md` - A-02b.


## PDP-03 operationalization

PDP-03 expresses the constraint locus-wise as `A_obs(l) <= A_F(l) + A_M(l,t)`, with `A_F(l) <= 4`. Recombination changes multilocus combinations but is not counted as a source of additional allelic states at the locus. See `4-models/population/founder-genome-feasibility-framework.md`.

This inequality is necessary bookkeeping, not a sufficient feasibility proof. The mapping from observed states to historical mutation events remains an empirical/modeling problem and is kept explicit in the CAN-H-F burden ledger.

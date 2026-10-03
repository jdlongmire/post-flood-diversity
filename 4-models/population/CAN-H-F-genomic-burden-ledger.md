# CAN-H-F Genomic Burden Ledger

**Boundary hypothesis:** Canidae-level founder
**Stream:** PDP-03
**Status:** scaffold, parameters not yet quantified
**Rule:** measured features enter before explanatory assignment. Conventional ancestry/chronology is not imported automatically.

| ID | Feature / quantity | Epistemic tag | Burden class | Parameter status | Current disposition |
|---|---|---|---|---|---|
| CAN-GEN-001 | autosomal allelic richness across extant Canidae | OBS when measured from sequence dataset | F/M/U | UNSOURCED | quantify locus-wise distribution, especially loci with >4 observed alleles |
| CAN-GEN-002 | within-population heterozygosity | OBS | F + demographic filtering | UNSOURCED | collect across representative genera |
| CAN-GEN-003 | between-lineage sequence differences | OBS | F/M/U | UNSOURCED | do not equate difference count with elapsed time |
| CAN-GEN-004 | documented Canis introgression/admixture | OBS/INF depending statistic | I | qualitative evidence present | quantify only from sourced datasets |
| CAN-GEN-005 | structural variants | OBS | F/S/M/U | UNSOURCED | characterize family-wide burden |
| CAN-GEN-006 | chromosome-number/karyotype differences | OBS | S | qualitative evidence present | map plausible rearrangement burden without treating karyotype as kind boundary |
| CAN-GEN-007 | lineage-specific gene content / copy-number differences | OBS/INF | F/S/M/U | UNSOURCED | quantify gain/loss claims from assemblies |
| CAN-GEN-008 | regulatory variants associated with morphology | OBS/INF | F/G/M | partial qualitative evidence | separate measured association from inferred historical origin |
| CAN-GEN-009 | body-size associated IGF1 regulatory variation | OBS/INF | F/G | literature target identified | source exact variant distribution/effect |
| CAN-GEN-010 | family phylogenetic topology | INF from genomic observations | context only | available qualitatively | use structure; do not import conventional node ages |
| CAN-GEN-011 | inferred ancestral sequence/state | INF | U until independently constrained | UNSOURCED | never tag as OBS |
| CAN-GEN-012 | conventional divergence times | INF + AUX clock/calibration | excluded from PDP chronology | N/A | record only when needed to understand source model |

## Required first calculation

For a defined multi-genome Canidae dataset:

1. enumerate callable orthologous autosomal loci;
2. count distinct observed allelic states per locus;
3. partition loci by A_obs <= 4 and A_obs > 4;
4. determine how much >4 richness can be attributed to recurrent/recent variants versus deeper family-wide differences without presupposing their historical age;
5. compute the minimum novel-state burden conditional on a four-allele founder cap;
6. report unresolved states rather than assigning them automatically to mutation.

## Important limitation

Observed extant allele count is not identical to the minimum number of post-founder mutation events. Recurrent mutation, loss, unsampled/extinct variation, sequencing/assembly error, paralogy, structural variation, and state-definition choices can alter the mapping. The calculation therefore needs explicit locus and variant definitions.

## Ancillary-hypothesis trigger

Do not register an AH merely because CAN-GEN-001 produces loci with more than four states. First quantify the residual under ordinary founder standing variation plus measured post-founder-capable processes. An AH is warranted only when a specified residual remains and a proposed mechanism has independent biological content.

## Current result

No quantitative feasibility verdict. The ledger defines what must be measured before CAN-H-F can move from PDP-02 compatibility to PDP-03 quantified feasibility.

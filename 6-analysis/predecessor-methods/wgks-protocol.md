# WGKS Reproduction Protocol

## Source method

Cserhati (2020) introduced Whole Genome K-mer Signature analysis as a whole-genome comparison method and compared its clustering behavior with mitochondrial and Gene Content Method results.

## PDP reproduction

1. Freeze assembly accession/version manifest across representative Canidae.
2. Pre-register assembly-quality exclusions.
3. Reproduce the source k-mer/signature algorithm and parameterization where sufficiently specified.
4. Emit pairwise signature/correlation matrix before clustering.
5. Reproduce source clustering.
6. Test sensitivity to k, assembly fragmentation, repeat masking, chromosome-only versus whole-genome input where relevant, and taxon composition.
7. Compare with GCM using the same eligible taxon intersection and again using each method's maximal eligible set.

## Epistemic firewall

OBS: genome sequence deposited in the assembly.
INF: signature, correlation, clustering.
AUX: k choice, sequence preprocessing, assembly representation, clustering choices.
PDP: boundary significance assigned to the resulting structure.

Whole-genome similarity can constrain boundary hypotheses but cannot by itself establish historical kind identity.

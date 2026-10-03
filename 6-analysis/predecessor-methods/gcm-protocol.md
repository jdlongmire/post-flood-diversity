# GCM Reproduction Protocol

## Source method

O'Micks (2017) Gene Content Method compares taxa using common orthologous protein content, expressed through pairwise similarity (including Jaccard-type overlap), followed by clustering/statistical assessment.

Later eKINDS ruminant work applies GCM to proteomes and supplements it with WGKS when proteome coverage limits taxon inclusion.

## PDP reproduction

1. Freeze Canidae proteome accession/version manifest.
2. Apply minimum proteome/completeness criteria before clustering.
3. Map proteins to declared orthologous groups using one frozen database/tool version.
4. Construct presence/absence matrix.
5. Compute pairwise Jaccard similarity.
6. Report raw matrix before clustering.
7. Apply the original clustering/statistical procedure as closely as reproducible.
8. Run sensitivity analyses for missing proteome content and taxon removal.

## Epistemic firewall

OBS: deposited protein sequences/annotations subject to annotation quality.
INF: orthology assignment, completeness estimate, cluster membership.
AUX: thresholds, database version, distance/linkage choices.
PDP: whether a pattern constrains a candidate kind boundary.

A GCM cluster is not a created-kind observation.

# Canidae Predecessor Method Reproduction

This directory bridges PDP-02 boundary analysis and PDP-03 founder-genome feasibility.

## Why this bridge exists

Three predecessor lines directly overlap PDP's Canidae work:

1. Lightner (2009) explicitly treats Canidae as one baramin and identifies the four-founder-allele and karyotype-diversity problem.
2. O'Micks' Gene Content Method (GCM) measures pairwise overlap in orthologous protein content and clusters taxa.
3. Cserhati's Whole Genome K-mer Signature (WGKS) compares whole-genome k-mer composition and clusters taxa.

PDP will reproduce measurements and clustering behavior without treating a cluster as a kind declaration.

## Common modern input design

Use the best available assemblies/proteomes spanning representative Canidae genera. Maintain a manifest containing:
- taxon;
- assembly accession/version;
- assembly quality fields;
- proteome accession/version;
- completeness/missingness fields;
- inclusion/exclusion reason;
- method eligibility.

Dog10K is valuable for within-Canis population variation but is not a substitute for family-wide genus sampling.

## Outputs

The final matrix asks:

| Question | Lightner update | GCM | WGKS | PDP-03-001 |
|---|---|---|---|---|
| What is measured? | karyotype + selected allelic diversity | orthologous protein-content overlap | genome k-mer composition | homologous-locus haplotype burden |
| Direct founder constraint? | yes, qualitative/selected loci | no | no | yes, quantitative |
| Boundary clustering? | literature synthesis | yes | yes | no, burden conditional on boundary |
| Chronology required? | original interpretation yes | no for similarity | no for similarity | PDP chronology only at later rate stage |
| Can output prove kind identity? | no | no | no | no |

The methods are complementary rather than interchangeable.

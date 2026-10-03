# PDP-03-001 Protocol: Canidae Founder Allele-Burden Experiment

**Status:** pre-registration, before endpoint computation
**Date:** 2026-10-03

## 1. Objective

Measure the observed allelic-state burden across a frozen Canidae genomic dataset and determine what the measurement can and cannot say about a single-pair founder constraint.

## 2. Pre-analysis correction

The initially proposed experiment counted distinct states at individual nucleotide positions and treated a >4-state tail as the critical endpoint. That endpoint is invalid: a canonical DNA position has only four nucleotide states, A/C/G/T. It therefore cannot exhibit more than four canonical SNV alleles regardless of history.

This is an important negative result from protocol design. The four-copy founder constraint concerns **distinct alleles at a homologous locus**, where an allele may be a multi-base haplotype or other defined locus state. PDP-03-001 therefore retains per-site state counts as QC/descriptive data but moves the critical endpoint to explicitly defined multi-base homologous loci.

The correction is registered before computation and is not a response to an unfavorable result.

## 3. Frozen public resources

### Family-breadth resource
NCBI BioProject **PRJNA822671**: South American canid whole-genome data. NCBI reports 18 BioSamples, 27 SRA experiments, 1,514 Gbases, and two assemblies, including maned wolf and bush dog.

### Caninae breadth resource
NCBI BioProject **PRJNA494815**: raw whole-genome reads from 8 Caninae species, 15 BioSamples.

### Narrower Canis replication
NCBI BioProject **PRJNA494719**: 28 Canis individuals, linked by NCBI to vonHoldt et al. whole-genome work.

### Large within-Canis calibration
Dog10K phase-one data, **PRJNA648123**, with variants archived as **PRJEB62420**. The published analysis reports 1,987 analyzed canids, 34 million SNVs, 14.4 million indels, and more than 144,000 structural variants. This panel is valuable for variant/QC calibration and within-Canis richness, but its dogs/wolves/coyotes sampling is not a family-wide Canidae sample.

### Reference coordinate system
**GCF_011100685.1, UU_Cfam_GSD_1.0**, the German Shepherd Dog reference used by the Dog10K phase-one analysis.

## 4. Locus hierarchy

The experiment has three layers.

### L0: nucleotide-site QC
Count canonical nucleotide states at retained callable autosomal coordinates. Endpoint range is necessarily 1-4. Purpose: QC, error characterization, and confirmation that the pipeline does not manufacture impossible fifth nucleotide states.

### L1: short phased haplotype loci
Define fixed, pre-registered windows around high-confidence orthologous autosomal regions and count distinct phased haplotypes. This is the first locus class capable of yielding >4 observed alleles.

Window sizes will be sensitivity parameters rather than chosen after seeing which size maximizes >4 counts. Candidate fixed sizes: 100 bp, 500 bp, 1 kb. All three are reported.

### L2: gene/region haplotypes
For high-confidence single-copy orthologous coding regions or other conserved loci, count explicitly defined haplotypes subject to callability and phasing limits. This provides biological locus context but carries more alignment/recombination complexity than L1.

Structural variants, CNVs, and chromosome rearrangements are deferred to later PDP-03 experiments.

## 5. Inclusion rules

A locus enters the primary analysis only if:
- autosomal;
- homologous across the included taxa under the declared orthology/alignment method;
- single-copy under the declared reference/annotation rule;
- passes minimum callability across the frozen sample subset;
- canonical bases/states can be distinguished from missing/ambiguous calls;
- paralogous/repetitive regions are excluded under a predeclared mask.

Exact numerical QC thresholds must be sourced or declared as analysis parameters before computation.

## 6. Primary endpoints

For each L1 window size and L2 locus set:

- N callable loci;
- distribution of observed distinct haplotypes;
- N and proportion with <=4 observed haplotypes;
- N and proportion with >4 observed haplotypes;
- excess-state lower-bound statistic: sum(max(0, A_obs(l)-4));
- uncertainty/sensitivity to missingness, phasing, sample composition, and locus definition.

The excess-state statistic is **not** automatically a mutation-event count.

## 7. Explanatory accounting

For every >4 locus, classify the burden as:
- OBS: observed haplotypes/states;
- INF: phasing, orthology, inferred ancestry, or other model-derived structure;
- AUX: assumptions needed to map observed states to historical processes;
- PDP: conditional founder-burden calculation.

Potential explanatory classes remain F/R/G/S/M/I/U. No residual is automatically assigned to mutation.

## 8. Parallel reconstruction columns

The output table keeps a shared observation column and separate interpretations:

| Observation | PDP conditional reconstruction | Conventional reconstruction |
|---|---|---|
| measured locus/haplotype states | founder cap + post-founder process burden | source-supported population/evolutionary interpretation |
| measured introgression statistic | distribution mechanism where applicable | source-supported admixture/gene-flow interpretation |
| sequence difference | difference requiring accounting | may enter phylogeny/clock models if source does so |

Conventional chronology and common-descent interpretation remain INF/AUX unless directly observed, and are not imported into PDP chronology.

## 9. Failure conditions

The CAN-H-F configuration is under pressure if, after QC and sensitivity analysis, the minimum post-founder novelty burden required by observed locus states cannot be supplied by measured or independently defensible processes inside PDP chronology without an ancillary that fails its own discriminator.

The experiment may also be uninformative. That result must be retained.

## 10. Next computational step

Acquire or materialize the frozen variant/sample metadata, define a balanced family-breadth sample set, freeze QC thresholds and orthology method, then implement L0/L1 first. L2 follows after validating the pipeline.

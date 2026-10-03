# Canidae Assembly/Proteome Eligibility Manifest

**Freeze stage:** v0.1, 2026-10-03
**Purpose:** prevent post-result taxon selection in GCM/WGKS reproduction.

## Eligibility policy

Taxa are not excluded because their inclusion weakens or changes a preferred cluster. Eligibility is determined by data quality and method requirements.

### Tier GCM
Requires a public annotated proteome/annotation of sufficient completeness for ortholog-content comparison. Missing annotation can create false gene-content distance, so assembly availability alone is insufficient.

### Tier WGKS-A
Chromosome-level or otherwise high-contiguity assembly suitable for primary whole-genome k-mer comparison.

### Tier WGKS-B
Scaffold/contig assembly retained for sensitivity analysis. Results must be flagged for assembly-quality sensitivity and cannot silently substitute for Tier A.

### Raw-read only
Useful for PDP-03 variant/locus analyses after common-reference processing; not eligible for assembly-based WGKS until assembled under a frozen pipeline.

## Frozen identified resources

| Taxon | Resource | Accession / project | Assembly evidence | Initial method disposition |
|---|---|---|---|---|
| Canis lupus familiaris / dog reference | German Shepherd Dog | GCF_011100685.1, UU_Cfam_GSD_1.0 | reference framework used by Dog10K phase one | GCM candidate; WGKS-A candidate; PDP-03 reference |
| Vulpes vulpes | VulVul3 | GCF_048418805.1 | current RefSeq annotation visible in NCBI 2026 gene records; chromosome coordinates | GCM candidate; WGKS-A candidate |
| Vulpes vulpes | VulVul2.2 | GCF_003160815.1 | older RefSeq, largely scaffold/unplaced representation; NCBI annotation release 100 | historical sensitivity only, superseded for primary analysis |
| Chrysocyon brachyurus | South American canid WGS | PRJNA822671 / GCA_024262425.1 | contig assembly | WGKS-B; GCM only if annotation/proteome eligibility passes |
| Speothos venaticus | South American canid WGS | PRJNA822671 / GCA_024262445.1 | contig assembly | WGKS-B; GCM only if annotation/proteome eligibility passes |
| Speothos venaticus | Kyoto draft | PRJDB9764 / GCA_023170115.1 | scaffold assembly | WGKS-B sensitivity candidate |
| South American Canidae multispecies | raw WGS | PRJNA822671 | 18 BioSamples, 27 SRA experiments, 1,514 Gbases; two linked contig assemblies | PDP-03 family-breadth raw-read set; not all samples WGKS-eligible |
| Caninae multispecies | raw WGS | PRJNA494815 | eight species, raw reads | PDP-03 breadth; assembly eligibility separate |
| Canis | raw WGS | PRJNA494719 | 28 individuals | PDP-03 replication |
| Dog10K phase one | large canid panel | PRJNA648123 / PRJEB62420 | variant-rich dog/wolf/coyote panel | PDP-03 calibration; not family-breadth WGKS |

## Freeze rule

Before GCM execution, every included taxon must have its exact proteome accession/version and annotation-completeness fields recorded.

Before WGKS execution, every included taxon must have exact assembly accession/version, level, total span, contig/scaffold N50 where available, ambiguous-base fraction where available, and repeat-masking policy recorded.

The primary same-taxon-intersection comparison uses only taxa eligible for both methods. Each method also receives a maximal-eligible analysis. Both are reported.

## Current gap

This v0.1 manifest does not yet claim a complete family-wide set. It records only accessions verified in the first freeze pass. Additional genera must be added from primary NCBI/ENA records before execution. Absence here means unverified, not unavailable.

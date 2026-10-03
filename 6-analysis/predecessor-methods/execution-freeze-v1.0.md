# Canidae GCM/WGKS Execution Freeze v1.0

**Frozen:** 2026-10-03
**Bridge:** PDP-02-03-BRIDGE-001
**Status:** pre-result execution specification

## 1. Stop rule

Taxon discovery stops at this freeze for the first reproduction. New taxa discovered later are a v1.1 extension and may not be inserted into v1.0 after results are known.

## 2. Verified anchor taxa

### Primary high-quality assembly anchors
- **Canis lupus familiaris:** GCF_011100685.1, UU_Cfam_GSD_1.0.
- **Vulpes vulpes:** GCF_048418805.1, VulVul3, current RefSeq annotation RS_2025_03.
- **Urocyon cinereoargenteus:** GCA_032313775.1, chromosome-level mainland gray fox reference.
- **Lycaon pictus:** GCA_040955705.1, mLycPic1 maternal haplotype, chromosome-level, 39 chromosomes, 38,824 project protein sequences.

### Secondary/sensitivity anchors
- **Nyctereutes procyonoides:** GCF_905146905.1, current RefSeq annotation RS_2023_04, scaffold/unplaced representation.
- **Chrysocyon brachyurus:** GCA_024262425.1, PRJNA822671, contig-level.
- **Speothos venaticus:** GCA_024262445.1, PRJNA822671, contig-level.
- **Speothos venaticus:** GCA_023170115.1, PRJDB9764, scaffold-level alternative.
- **Vulpes lagopus:** GCA_018835635.1, scaffold-level.
- **Lycaon pictus:** GCA_001883655.1 and GCA_001887905.1, earlier chromosome-level individuals for within-species assembly sensitivity.

## 3. Analysis sets

### WGKS-A primary
The primary WGKS analysis uses only high-quality anchor assemblies that satisfy the frozen assembly-quality gate. At minimum the verified chromosome-level anchors are Canis, Vulpes vulpes, Urocyon, and Lycaon. Exact FASTA versions/checksums are recorded at download.

### WGKS-A+B sensitivity
Adds scaffold/contig taxa after the primary result is fixed: Nyctereutes, Chrysocyon, Speothos, Vulpes lagopus, plus alternate same-species assemblies where useful.

### GCM primary
Uses taxa with a versioned public proteome/annotation passing the frozen completeness gate. Verified current annotated anchors include Canis reference, Vulpes vulpes VulVul3, Lycaon mLycPic1 project proteins, and Nyctereutes RefSeq RS_2023_04. Exact protein FASTA accessions/checksums and completeness metrics are recorded before orthology inference.

### Same-taxon intersection
The method-comparison set is the intersection of GCM-primary and WGKS-A. On current verification this is expected to include Canis, Vulpes vulpes, and Lycaon; additional taxa enter only if they already satisfy both frozen gates before execution.

## 4. Quality gates

### Assembly gate for WGKS-A
Record and enforce:
- exact accession/version;
- assembly level;
- total span;
- contig/scaffold N50;
- ambiguous-base fraction if available;
- FASTA checksum;
- repeat handling.

Chromosome-level status alone is not sufficient if the sequence fails other declared QC.

### Proteome gate for GCM
Record:
- exact assembly/annotation release;
- protein FASTA checksum;
- protein count;
- BUSCO/comparable completeness when available or a declared missingness proxy;
- orthology-tool/database version.

A proteome is not excluded because its inclusion changes clustering.

## 5. Reproduction order

1. Materialize metadata and sequence/protein manifests.
2. Freeze checksums and QC table.
3. Reconstruct original GCM calculation on a small validation subset.
4. Reconstruct original WGKS calculation on a small validation subset.
5. Run same-taxon intersection.
6. Lock those results.
7. Run each method's maximal eligible set.
8. Run assembly/proteome sensitivity analyses.
9. Compare matrices/clusters without converting agreement into kind identity.
10. Only then resume PDP-03-001 founder-burden computation.

## 6. Interpretation

A coherent Canidae cluster across independent genomic measurements would be evidence that CAN-H-F is a biologically meaningful partition. It would not establish that Canidae is the historical Ark kind.

Failure to recover coherence must be retained and diagnosed. No threshold, taxon, k value, orthology setting, or assembly is changed post hoc solely to recover the preferred boundary.

# Post-Flood Diversity Programme (PDP)

**Subtitle:** A quantitative research programme for post-Flood biological diversification

**Status:** PDP-0: boundary specification, not a tested explanation.

**Repository:** jdlongmire/post-flood-diversity
**Working abbreviation:** PDP

## Purpose

Develop and test whether a small preserved post-Flood breeding stock can account for observed terrestrial biological diversity within the programme's specified chronology, genetic constraints, ecological processes, and Ark boundary conditions.

## Programme relationship

PDP is the repository of record for the genetics/post-Flood biological line in Christian Designism.

```
Christian Designism
|
|-- Creation / Cosmology
|   `-- creation-cosmology-programmes
|
|-- Flood Geology
|   `-- global-flood-hydrotectonic-model   <- sibling geological mechanism
|
`-- Post-Flood Biology
    `-- post-flood-diversity                <- this repo
        |-- preserved stock
        |-- kind boundaries
        |-- population genetics
        |-- diversification
        |-- biogeography
        `-- Ark biological/logistics interface
```

PDP receives the global-Flood historical commitment through the Christian Designism programme layer. `jdlongmire/global-flood-hydrotectonic-model` is a sibling mechanistic model for Flood geology, not the epistemic source of that commitment. PDP may consume its outputs conditionally without making GFH part of PDP's hard core. See `traceability/dependencies.yaml`.

## Hard core

The five commitments, held essentially unchanged and not offered for ordinary
refutation:

1. A global Flood catastrophe occurred.
2. It bottlenecked air-breathing land animals and birds to a preserved breeding stock.
3. The preserved stock was genetically sound.
4. The stock possessed substantial latent biological potential within its respective body plans.
5. The preserved units were kinds rather than subsequent Linnaean species.

Full statement and heuristics: `0-programme/hard-core.md`, `0-programme/heuristics.md`.

## Repository map

- `0-programme/` - charter, hard core, heuristics, scope, epistemic status, roadmap, terminology
- `1-boundary/` - chronology, Ark hull, preserved stock, maturity, kind boundary, body-plan candidates
- `2-theory/` - genetics, diversification, ecology, Ark interface
- `3-evidence/` - observed diversification (rate examples and empirical bounds; belt resources, not proof)
- `4-models/` - kind registry, taxa, population, diversification, Ark loading models
- `5-predictions/` - predictions, discriminators, severe tests, appraisal
- `6-analysis/` - notebooks, datasets, scripts, results
- `7-papers/` - programme papers, technical papers, figures
- `registry/` - CLAIMS, AUXILIARIES, PREDICTIONS, FALSIFIERS, OBSERVATIONS, KINDS, OPEN-PROBLEMS
- `work-packages/` - PDP-01..06 streams and taxon packages (active, backlog, completed)
- `traceability/` - claims, dependencies, sources as YAML

## Maturity ladder

- **PDP-0** Boundary specification (current state)
- **PDP-1** Formal research programme
- **PDP-2** Quantified feasibility model
- **PDP-3** Successful worked kinds
- **PDP-4** Cross-kind explanatory model
- **PDP-5** Differential predictions
- **PDP-6** Empirically tested programme

The ladder keeps "internally possible" from quietly becoming "demonstrated."
Current appraisal: `5-predictions/appraisal.md`.

## Governing methodological rules

Canonized in `0-programme/charter.md`:

1. PDP may use observed rapid diversification to establish biological possibility
   or empirical rate bounds. It may not treat such observations as demonstrations
   that the proposed post-Flood history occurred. Historical reconstruction and
   mechanism are separate claims and must be registered separately.
2. An auxiliary that resolves one difficulty by changing the stipulated founder
   population, chronology, or hard-core historical event must be classified as a
   programme revision rather than an ordinary protective-belt adjustment.

## Research streams

- **PDP-01** Programme formalization: convert the seed specification into charter,
  hard core, heuristics, auxiliary register, terminology, and traceability.
- **PDP-02** Kind Boundary Project: defensible candidate boundaries from morphology,
  reproductive compatibility, comparative genomics, developmental architecture, and
  phylogenetic structure. Body-plan and family-level hypotheses compete; neither
  is assumed.
- **PDP-03** Founder Genome Feasibility: quantify what a founder pair can encode and
  transmit under the four-copy autosomal constraint.
- **PDP-04** Diversification Dynamics: model recombination, selection, regulatory
  change, isolation, chromosomal rearrangement, mutation, and speciation against the
  stipulated time window.
- **PDP-05** Ark Biological Boundary: population, maturity, survivability, and
  logistics constraints, interfaced with (not conflated with) Flood geology.
- **PDP-06** Kind-by-Kind Demonstration: the programme's decisive work product,
  from founder stock through standing variation, recombination and selection,
  isolation and dispersal, to observed descendant diversity.

## First taxa (progressively harder cases)

- **PDP-TAX-001** Canidae (calibration: substantial observed morphological
  diversity without a new body plan)
- **PDP-TAX-002** Bovidae
- **PDP-TAX-003** Equidae
- **PDP-TAX-004** Ursidae
- **PDP-TAX-005** Felidae
- **PDP-TAX-006** Muridae
- **PDP-TAX-007** Chiroptera (severe test: deriving bats from a mammalian founder
  is far harder than deriving dog breeds from a canid-like stock)
- **PDP-TAX-008** Aves test cluster

## License and citation

Code: Apache-2.0 (`LICENSE-Apache-2.0.txt`). Prose and figures: CC-BY-4.0
(`LICENSE-CC-BY-4.0.txt`). Cite via `CITATION.cff`.

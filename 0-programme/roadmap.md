# Roadmap

## Streams

### PDP-01 Programme formalization
Convert the seed specification into the formal charter, hard core, heuristics,
auxiliary register, terminology, and traceability structure. Deliverable: this
repository at PDP-1. Status: in progress (this repo).

### PDP-02 Kind Boundary Project
Determine defensible candidate boundaries using morphology, reproductive
compatibility, comparative genomics, developmental architecture, and
phylogenetic structure. Body-plan and family-level hypotheses compete; neither
is assumed. Deliverable: `registry/KINDS.md` with resolved or explicitly
competing boundaries.

### PDP-03 Founder Genome Feasibility
Quantify what a founder pair can actually encode and transmit, under the
standing constraint that an autosomal locus permits at most four founder
copies. Probably the critical technical stream. Deliverable: quantified
feasibility model in `4-models/population/`.

### PDP-04 Diversification Dynamics
Model recombination, selection, regulatory change, isolation, chromosomal
rearrangement, mutation, and speciation against the stipulated time window.
Deliverable: rate models in `2-theory/diversification/rate-models.md` and
`4-models/diversification/`.

### PDP-05 Ark Biological Boundary
Establish population, maturity, survivability, and logistics constraints.
Deliberately interfaced with, not conflated with, Flood geology. Deliverable:
`2-theory/ark-interface/` and `4-models/ark-loading/`.

### PDP-06 Kind-by-Kind Demonstration
The decisive work product: founder stock to founder genomic state to standing
variation plus post-Flood mutation, through recombination and selection,
isolation and dispersal, population differentiation, reproductive isolation
where applicable, to observed descendant diversity. Deliverable: worked taxa
in `4-models/taxa/`, starting with PDP-TAX-001.

## Taxon gradient

PDP-TAX-001 Canidae -> PDP-TAX-002 Bovidae -> PDP-TAX-003 Equidae ->
PDP-TAX-004 Ursidae -> PDP-TAX-005 Felidae -> PDP-TAX-006 Muridae ->
PDP-TAX-007 Chiroptera -> PDP-TAX-008 Aves test cluster.

Start with canids (calibration: substantial observed morphological diversity
without a new body plan). Bats come considerably later: deriving bats from a
mammalian founder is a much more severe test than deriving dog breeds from a
canid-like stock. That gradient is deliberate.

## Milestones

1. PDP-1: this repo complete and internally consistent (charter through
   traceability).
2. PDP-02 first pass: `registry/KINDS.md` seeded with competing hypotheses.
3. PDP-03: quantified feasibility model published to `4-models/population/`.
4. PDP-TAX-001 worked end to end (PDP-06 first delivery).
5. Severe test: PDP-TAX-007 attempted with pre-registered success criteria.
6. PDP-5: differential predictions registered in `5-predictions/`.

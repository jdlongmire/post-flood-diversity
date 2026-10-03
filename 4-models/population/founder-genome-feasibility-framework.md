# Founder Genome Feasibility Framework

**Stream:** PDP-03
**Status:** active
**Reference case:** CAN-H-F, a Canidae-level founder stock

## 1. Question

Given a specified founder stock and programme chronology, can the observed descendant genomic state be partitioned into founder-carriable variation plus biologically available post-founder processes without violating the founder constraints?

This is a burden-accounting problem before it is a historical claim.

## 2. Epistemic tags

Every input receives one tag:

- **OBS:** direct observation or measurement.
- **INF:** model-dependent inference from observations.
- **AUX:** auxiliary assumption, whether conventional or PDP.
- **PDP:** interpretation/calculation made inside this programme.

An item can be useful while remaining INF or AUX. Tags prevent an inference from becoming an observation by repetition.

## 3. Founder constraint

For a single diploid male-female pair, an autosomal locus contains four physical founder copies. Therefore the maximum number of distinct founder alleles at that locus is four.

Let:
- A_obs(l) = number of descendant allelic states requiring explanation at locus l;
- A_F(l) <= 4 = distinct states carried by the founder pair;
- A_M(l,t) = genuinely new states generated post-founder and surviving to observation;
- A_R(l) = recombinational arrangements of existing states, which do not increase the allele count at l.

Necessary accounting condition:

A_obs(l) <= A_F(l) + A_M(l,t)

Recombination can alter multilocus combinations but cannot supply a fifth founder allele at one locus.

## 4. Burden classes

Each observed feature is assigned provisionally to one or more classes:

- **F:** founder-carriable standing state.
- **R:** recombinational arrangement of founder states.
- **G:** regulatory-state/architecture burden.
- **S:** structural-variant or karyotypic burden.
- **M:** requires post-founder mutational origin under the stipulated founder.
- **I:** introgression/reticulation changes distribution among descendant populations but does not create the underlying state.
- **U:** unresolved.

Classification is a bookkeeping claim, not yet a mechanism proof.

## 5. Core outputs

For each candidate boundary PDP-03 must report:

1. founder-carriable fraction/burden where measurable;
2. minimum post-founder novel-state burden;
3. structural/regulatory burden;
4. generation/time sensitivity;
5. required auxiliaries;
6. unexplained residual R_U;
7. parameter uncertainty.

The programme must allow R_U > 0. A residual is a research result.

## 6. Competing boundaries

CAN-H-C, CAN-H-F, CAN-H-O, and CAN-H-BP are separate calculations. A feasible narrow boundary does not license a broad one. Burden growth as the boundary broadens is itself an output.

## 7. Ancillary hypotheses

No ancillary hypothesis is preloaded merely to make the model close. When a quantified residual appears:

observation -> constraint -> deficit -> AH proposal -> consequences -> discriminator/appraisal.

AH entries live in registry/AUXILIARIES.md and must identify what residual they address.

## 8. PDP-2 promotion gate

PDP may not claim PDP-2 Quantified Feasibility Model until at least one reference boundary has:
- sourced numerical parameters;
- reproducible burden calculations;
- sensitivity analysis;
- explicit residuals;
- documented ancillary dependencies;
- a failed-or-passable verification gate that can rule against the configuration.

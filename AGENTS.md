# AGENTS.md - Post-Flood Diversity Programme

Entry point for AI agents working in this repository.

[MXM.md](MXM.md) is the canonical, harness-neutral bootstrap for agent posture.
This file is the PDP-specific operating layer on top of it.

## Before substantive work

1. Read `0-programme/charter.md` (governing rules), `0-programme/hard-core.md`,
   `0-programme/epistemic-status.md`, and `registry/OPEN-PROBLEMS.md`.
2. Check `work-packages/active/` for the current stream state before starting
   new work.

## Non-negotiable conventions

- **No em dashes, ever.** JD's standing rule. Verify mechanically before
  delivering anything: write the draft to a file and scan with Python for
  non-ASCII characters (U+2014). Never verify by eye or by grep.
- **Epistemic honesty is the product.** This repo is at PDP-0: a boundary
  specification, not a tested explanation. Never let "internally possible"
  read as "demonstrated."
- **Rate examples are not demonstrations.** Observed rapid diversification
  (dogs, finches, mice, livestock) may establish biological possibility or
  empirical rate bounds. It may not be treated as proof that the proposed
  post-Flood history occurred. Historical reconstruction and mechanism are
  separate claims.
- **Register before you argue.** Every new claim gets an ID in `registry/`
  (CLAIMS, AUXILIARIES, PREDICTIONS, FALSIFIERS, OBSERVATIONS, KINDS) and a
  traceability entry in `traceability/claims.yaml` before it is used in an
  argument.
- **Edit the belt in place.** Belt items are adjusted without touching the
  core. A change that alters the founder population, chronology, or hard-core
  historical event is a programme revision, not a belt adjustment: flag it
  explicitly, do not smuggle it in.
- **Kind width stays in the belt.** Body-plan-level kinds are a protective-belt
  choice, not a hard-core commitment. Keep body-plan and family-level
  hypotheses competing until PDP-02 resolves them.
- **Versioned deliverables.** When iterating on graphics, drafts, or models,
  keep versioned copies so the latest is always identifiable.

## Layout authority

`0-programme/` governs. `1-boundary/` constrains. `2-theory/` proposes
mechanisms. `3-evidence/` records observations. `4-models/` extrapolates
mechanisms to founder populations (model claims, not evidence).
`5-predictions/` holds predictions, discriminators, severe tests, appraisal.
`6-analysis/` holds executable work. `7-papers/` holds publications.
`registry/` is the claim ledger. `traceability/` is the dependency graph.

Do not blur `3-evidence` into `4-models`: dogs and finches are empirical
rates; applying those rates to an Ark founder population is a model claim.

## Upstream discipline

PDP consumes the global Flood as an upstream historical commitment from
`jdlongmire/global-flood-hydrotectonic-model` (see
`traceability/dependencies.yaml`). Do not duplicate geological mechanism here.
Flood-geology questions belong upstream; biological questions that touch the
hull belong in `2-theory/ark-interface/` and are interfaced, not conflated,
with geology.

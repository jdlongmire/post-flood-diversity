# Population Size

How many animals the hull must carry, as a function of kind width.

## The constraint

- Hull boundary: `1-boundary/ark-boundary.md` (about 100,000 sq ft of deck;
  about 1.5M cu ft; household, food, water, and waste also aboard).
- Negative heuristic: do not embark the species lists. A species-level stock
  is ruled out by volume, independent of genetics.
- Kind width (`1-boundary/kind-boundary.md`) sets the unit count: body-plan
  cut means few origins; family-level cut means hundreds to a few thousand.

## Modeling home

`4-models/ark-loading/`: loading models that fit kind counts (under each
competing kind-width hypothesis) against the hull, with juvenile embarkation
(`juvenile-stock.md`) as the primary size auxiliary.

## Status

Reserved for PDP-05.

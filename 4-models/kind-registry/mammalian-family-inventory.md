# Mammalian Family-Level Candidate Inventory

**PDP-02 status:** baseline enumeration
**Taxonomic baseline:** American Society of Mammalogists Mammal Diversity Database (MDD) v2.5, released 2026-07-28.
**Baseline count:** 169 recognized mammalian families.

## Rule

A family appearing here is a **candidate partition unit**, not a PDP kind declaration. The inventory exists so the family-level hypothesis has a finite, externally auditable baseline. Extinct post-1500 families in the MDD and aquatic groups require scope disposition before Ark-loading use.

## Initial programme taxa

| PDP ID | Family / scope | Order | Boundary role | Status |
|---|---|---|---|---|
| PDP-TAX-001 | Canidae | Carnivora | calibration | dossier first pass complete |
| PDP-TAX-002 | Bovidae | Artiodactyla | worked family | queued |
| PDP-TAX-003 | Equidae | Perissodactyla | worked family | queued |
| PDP-TAX-004 | Ursidae | Carnivora | worked family | queued |
| PDP-TAX-005 | Felidae | Carnivora | worked family | queued |
| PDP-TAX-006 | Muridae | Rodentia | high-diversity family | queued |
| PDP-TAX-007 | Chiroptera | Chiroptera | order-level severe test; MDD recognizes 21 constituent families | reserved |
| PDP-TAX-008 | Aves test cluster | Aves | non-mammalian test | reserved outside this mammal inventory |

## Mammalian family baseline

The canonical enumeration for PDP-02 is MDD v2.5 rather than a hand-maintained taxonomic list. As of that release the database reports 27 mammalian orders and 169 families. PDP records the release/version because family composition changes with taxonomic revision.

For each family admitted to the terrestrial Ark-stock scope, PDP-02 will add a registry row with:
- MDD family and order;
- extant/recently extinct scope status;
- terrestrial/aquatic disposition;
- candidate H-F identifier;
- broader H-O and H-BP competitors;
- evidence-dossier status;
- PDP-03 burden status;
- PDP-04 burden status.

## Scope gates before full 169-row import

1. Separate obligately aquatic mammals from the air-breathing land-animal Ark scope rather than silently counting all MDD families.
2. Mark recently extinct families distinctly from extant families.
3. Do not equate taxonomic revision with change in the underlying biological evidence.
4. Freeze MDD v2.5 as the PDP-02 first-pass baseline; later releases require an explicit registry revision.
5. Chiroptera remains a severe order-level test across its 21 MDD families, not a single family-level row.

## Source

Mammal Diversity Database (2026), Version 2.5, American Society of Mammalogists. The current release reports 6,904 total species, 27 orders, 169 families, and 1,363 genera.

This file establishes the enumeration baseline. The machine-readable 169-family snapshot should be imported only after aquatic/extinct scope fields are defined so taxonomy is not mistaken for Ark loading.

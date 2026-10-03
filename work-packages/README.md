# Work Packages

Streams PDP-01..06 and taxon packages live here.

## Layout

- `active/` - work packages currently being executed.
- `backlog/` - proposed packages not yet started.
- `completed/` - finished packages with their verification evidence.
- `TEMPLATE/package.yaml` - the package schema every work package follows.

## Conventions

- Each package states scope (what it covers and explicitly what it does
  NOT), authority boundary (what may proceed without re-asking, and what
  it does not authorize), actions, and verification (how "done" is proven,
  preferring a check that can fail).
- A package that touches a commitment, an external publication, or a
  verdict names that edge in its authority boundary.
- Stream packages: PDP-01 (formalization), PDP-02 (kind boundary), PDP-03
  (founder genome feasibility), PDP-04 (diversification dynamics), PDP-05
  (Ark biological boundary), PDP-06 (kind-by-kind demonstration).
- Taxon packages: PDP-TAX-001 through PDP-TAX-008, worked in gradient
  order.
- Disposition field tracks open vs closed; completed packages keep their
  verification evidence in the package directory.

# Resource collections

Collections follow `resources/<domain>/<resource-name>/` and declare one of three initial
resource kinds:

- `node_features`: continuous or categorical annotations defined on atlas nodes;
- `edge_features`: continuous or categorical annotations defined on atlas edges;
- `edge_sets`: externally defined discrete edge memberships.

Each collection will include `resource.json`, a human-readable README, data files,
provenance, citations, licensing information, and reproducible build materials where
redistribution permits. Analysis-specific thresholds and filters are not stored as
canonical resource data.

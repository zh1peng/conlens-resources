# Atlas definitions

Each atlas lives in `atlases/<atlas-id>/` and contains:

- `atlas.json`: schema-versioned atlas manifest;
- `nodes.tsv`: canonical node identifiers and order;
- an optional explicit edge-universe table when the universe is not the complete
  directed or undirected graph declared by the manifest.

Resource collections reference atlas IDs and are validated against the atlas node-order
hash. Atlas IDs must be lowercase and stable after release.

# conlens-resources

`conlens-resources` is the versioned resource registry for
[ConLens](https://github.com/zh1peng/conlens). It stores reusable spatial priors
and connectome annotations while ConLens remains responsible for transformation,
edge-set construction, enrichment, and inference.

This repository is currently a draft skeleton. The paths below reserve the initial
atlas and resource layout, but do not yet publish curated resource values.

## Design principles

- Atlas definitions and resource collections are separate.
- Continuous node or edge features are retained before analysis-specific filtering.
- Thresholds such as top 10% or top 20% are not canonical resource data.
- Initial resource kinds are `node_features`, `edge_features`, and `edge_sets`.
- Every resource must declare its atlas alignment, version, provenance, license,
  citations, and checksums.
- Derived edge sets are created by ConLens or user code from the published primitives.

## Repository layout

```text
conlens-resources/
├── registry.json
├── schemas/
│   ├── registry.schema.json
│   ├── atlas.schema.json
│   └── resource.schema.json
├── atlases/
│   ├── dk68/
│   ├── schaefer100-7net/
│   ├── schaefer200-7net/
│   └── schaefer300-7net/
├── resources/
│   ├── pet/
│   │   └── receptor-abundance-react/
│   ├── transcriptomics/
│   ├── gradients/
│   ├── cytoarchitecture/
│   ├── structural-connectivity/
│   ├── disease-vulnerability/
│   └── canonical-networks/
├── tools/
└── tests/
```

Atlas directories will contain canonical node tables and atlas manifests. Resource
directories will follow `resources/<domain>/<resource-name>/` and contain a resource
manifest, data files, provenance, citations, and reproducible build materials.

## Status

All newly reserved atlas manifests and PET tables are marked as draft placeholders.
The initial PET receptor/transporter abundance collection, provenance, checksums, and
the ConLens resource loader will be developed in a later phase.

## Licensing

Repository code and original metadata are licensed under MIT. Each curated resource
must separately record the license and redistribution terms of its underlying data.

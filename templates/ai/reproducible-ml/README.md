# Tool-Neutral Reproducible AI Product Template

An AI product is a repeatable pipeline plus an application contract. Keep model-tool choices replaceable.

```text
data/             acquisition, validation, lineage
features/         deterministic transformations
training/         configurations and training use cases
evaluation/       metrics, thresholds, error analysis
artifacts/        versioned model/package metadata
serving/          input/output contract and inference adapters
monitoring/       quality, drift, latency, and fallback signals
```

Every model artifact must identify its dataset version, code revision, configuration, evaluation result, and approval decision.

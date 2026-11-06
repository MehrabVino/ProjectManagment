# AI Engineering Modules

AI modules are selected in addition to the shared foundation and normal software modules. A model is not a substitute for product, data, or operations engineering.

| Trigger | Module | Required evidence |
| --- | --- | --- |
| Data informs a model or decision | Data lifecycle and governance | data card/datasheet, lineage, schema/data contract, quality tests, retention/access policy and split policy |
| Model behavior is evaluated | Experimentation and evaluation | hypothesis, baselines, metrics, calibration/slice analysis, error analysis and reproducible run manifest |
| Models move toward production | MLOps and serving | model registry metadata, input/output contract, compatibility policy, canary/rollback and latency/cost budget |
| Model affects people or sensitive outcomes | Responsible AI and safety | impact/risk assessment, stakeholder review, fairness/safety evaluation, human override/appeal and residual-risk record |
| LLM, RAG, or agents are used | GenAI trust boundary | corpus/index version, golden evaluation set, retrieval and generation metrics, prompt/tool permissions, injection tests, abstention and loop limits |
| Model runs after release | ML observability | data/prediction quality, drift, delayed labels, subgroup performance, incident triggers and remediation owner |

References: [Google Rules of ML](https://developers.google.com/machine-learning/guides/rules-of-ml), [Datasheets for Datasets](https://arxiv.org/abs/1803.09010), [Model Cards](https://arxiv.org/abs/1810.03993), and the [NIST AI RMF](https://www.nist.gov/itl/ai-risk-management-framework).

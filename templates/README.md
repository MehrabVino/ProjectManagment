# Templates

These are blueprints, not framework starters. Copy one, answer its decision checklist, then implement adapters for your chosen stack.

Use [the engineering catalog](../docs/engineering/README.md) to compose the shared and specialized modules that belong with a blueprint.

| Template | Best for | Core stays independent from |
| --- | --- | --- |
| [Software modular product](software/modular-product/README.md) | APIs, web apps, services | web framework, ORM, database, queue |
| [Reproducible AI product](ai/reproducible-ml/README.md) | ML-enabled products | model library, experiment platform, model host |
| [Engine-agnostic game](game/engine-agnostic/README.md) | 2D, 3D, mobile, desktop games | Unity, Godot, Unreal, renderer, input SDK |

Shared artifacts are available in [shared](shared/README.md): ADR, system-modeling, design-system, and threat-model templates.

# Engineering Module Catalog

This catalog prevents one-size-fits-all architecture. Start with the shared foundation, then add only the specialized modules justified by your product's risks, constraints, and lifecycle.

| Catalog | Use it when |
| --- | --- |
| [Shared engineering](shared.md) | Every product: discovery, architecture, modeling, quality, security, delivery, and operations |
| [Software engineering](software.md) | You ship a web, mobile, desktop, API, service, or reusable library product |
| [AI engineering](ai.md) | A model, retrieval system, agent, or statistical decision system affects the product |
| [Game engineering](game.md) | You ship an interactive game, regardless of Unity, Godot, Unreal, or another engine |

## Composition rule

1. Write the product decision and quality risks.
2. Select the required shared modules.
3. Select the specialization modules that solve a real requirement.
4. Record additions and omissions in an ADR; do not silently copy a large template.
5. Keep tools at the adapter edge. A module describes a contract and evidence, not a mandatory vendor or engine.

## Module status

- **Foundation**: expected for nearly every maintained product.
- **Conditional**: select when the stated trigger applies.
- **Specialized**: relevant to one product family.

Each module lists its trigger and required artifacts. The templates in [templates/shared](../../templates/shared/README.md) provide the starting documents.

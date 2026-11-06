# Engineering Playbook & Project Templates for Software, AI/ML, and Game Development

> A practical, tool-neutral guide to building maintainable software products, AI systems, and games with clean code, software architecture, design patterns, documentation, testing, security, and production engineering.

**برای برنامه‌نویس‌ها، مهندسان نرم‌افزار، مهندسان هوش مصنوعی و بازی‌سازها:** این ریپو کمک می‌کند پروژه را منظم، قابل توسعه، قابل تست و آماده‌ی تحویل بسازید - بدون وابستگی اجباری به زبان، فریم‌ورک یا game engine خاص.

## What this repository gives you

- **Project templates** for software products, AI/ML products, and game development.
- **Engineering playbooks** for architecture, system design, clean code, design patterns, modeling, testing, security, CI/CD, observability, and documentation.
- **Decision checklists** that help choose the right level of complexity instead of copying fashionable architectures.
- **Tool-neutral contracts**: apply the same design to Python, Node.js, Java, .NET, Go, Unity, Godot, Unreal, or another stack through replaceable adapters.

## Who is this for?

| You are building... | Start with... |
| --- | --- |
| A web app, backend API, desktop app, SaaS, or reusable library | [Software engineering modules](docs/engineering/software.md) |
| A machine-learning system, RAG app, LLM workflow, agent, or data product | [AI engineering modules](docs/engineering/ai.md) |
| A 2D/3D, mobile, PC, online, or live-service game | [Game engineering modules](docs/engineering/game.md) |
| Any maintained product | [Shared engineering foundation](docs/engineering/shared.md) |

## Why tool-neutral architecture?

Good engineering decisions should survive a framework or engine change. This repository separates stable product logic from interchangeable integrations:

```text
Domain rules and use cases
        ↓
Ports and contracts
        ↓
Adapters for UI, database, cloud, framework, or game engine
```

For example, a game's combat, inventory, quests, and scoring should not depend directly on Unity, Godot, or Unreal APIs. The selected engine supplies input, rendering, persistence, platform services, and lifecycle adapters around the game core.

## Start in five steps

1. Read the [learning paths](docs/learning-paths/README.md).
2. Define the problem, audience, and quality risks for your product.
3. Choose modules from the [engineering catalog](docs/engineering/README.md) - not every module belongs in every project.
4. Copy the closest blueprint from [templates](templates/README.md).
5. Complete `PROJECT_DECISIONS.md`, create ADRs for major decisions, and implement adapters for your chosen tools.

## Engineering topics covered

### Shared foundation

Requirements engineering, SDLC, clean code, SOLID, design patterns, software architecture, C4/UML modeling, domain modeling, API/data contracts, testing strategy, technical documentation, threat modeling, privacy, DevOps, CI/CD, supply-chain security, observability, SRE, incident response, accessibility, and design systems.

### Software engineering

Modular monoliths, REST/API design, database modeling, transactions, migrations, frontend architecture, performance engineering, distributed systems, messaging, package/library design, deployments, and runtime operations.

### AI and machine-learning engineering

Data governance, data quality, dataset lineage, reproducible experiments, model evaluation, MLOps, model serving, monitoring and drift, responsible AI, LLM/RAG evaluation, agent safety, and human oversight.

### Game development engineering

Game loop, state machines, input, simulation, rendering, assets, physics, animation, audio, UI, save systems, multiplayer, performance profiling, accessibility, localization, release engineering, telemetry, and live operations.

## Templates and reusable artifacts

| Artifact | Use it for |
| --- | --- |
| [Software modular-product template](templates/software/modular-product/README.md) | APIs, applications, services, and product backends |
| [Reproducible AI/ML template](templates/ai/reproducible-ml/README.md) | ML products and data-driven systems |
| [Engine-agnostic game template](templates/game/engine-agnostic/README.md) | Games built with any engine or custom technology |
| [Shared engineering artifacts](templates/shared/README.md) | ADRs, UML/C4 modeling, design systems, and threat models |

## Repository map

```text
docs/
  learning-paths/           Step-by-step paths for Software, AI, and Game
  engineering/              Selectable shared and specialized engineering modules
templates/
  shared/                   ADR, modeling, design-system, and threat-model templates
  software/modular-product/ Tool-neutral modular-monolith blueprint
  ai/reproducible-ml/       Reproducible AI/ML product blueprint
  game/engine-agnostic/     Engine-independent game architecture blueprint
Software/, AI/, Game/       Existing reference materials and early examples
```

## Principles

- Start simple; add a pattern only when there is a named problem and a measurable trade-off.
- Prefer a modular monolith before distributed services unless independent deployment, ownership, or scale demands otherwise.
- Keep framework, database, cloud, model-provider, and engine dependencies at the boundary.
- Treat security, privacy, testing, accessibility, documentation, and operations as product requirements - not release-time chores.
- Measure performance and reliability on target environments before optimizing or redesigning.

## Available now and next

The repository currently provides the module catalog, learning-path structure, decision checklists, and tool-neutral blueprints. It is being expanded with runnable examples, guided exercises, and specialization-specific reference implementations; these future materials are not yet included as working templates.

## Contributing

Contributions must explain the problem solved, architectural boundaries, trade-offs, test strategy, and supported tool adapters. Folder-only templates are not enough.

Read [CONTRIBUTING.md](CONTRIBUTING.md) before contributing.

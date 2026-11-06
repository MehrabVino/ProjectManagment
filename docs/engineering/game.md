# Game Engineering Modules

Game modules are engine-neutral. Choose an engine adapter after the product decisions; do not let an engine's folder layout become the game architecture.

| Trigger | Module | Required evidence |
| --- | --- | --- |
| Every interactive game | Loop, simulation, input and state | loop/tick policy, deterministic state boundaries, input mapping, replay/test strategy and save schema |
| 2D/3D presentation exists | Rendering, assets, UI, audio and animation | asset naming/import rules, budget, scene/content ownership, UI states, audio/animation contracts |
| Physics or complex interactions exist | Physics and gameplay rules | fixed-step rules, collision/layer policy, deterministic/replay limits and gameplay tests |
| Online play or shared state exists | Networking and multiplayer | authority model, replication/latency policy, matchmaking/session flow, cheat/abuse model and soak tests |
| Content or game feel drives value | Design and production | core loop, economy/balance tables, level/narrative/design documentation, playtest protocol and feedback log |
| Multiple devices/platforms ship | Performance, QA and release | per-platform CPU/GPU/memory/loading/battery budgets, device matrix, certification and crash workflow |
| A broad audience is intended | Accessibility and localization | remapping, subtitles, contrast/color/motion options, pseudo-localization, font/RTL and linguistic QA |
| The game operates after launch | Telemetry and live operations | event taxonomy, consent/retention, KPIs, experiments, content calendar, incident/hotfix runbook |

Use an ECS only when data-oriented processing and population scale justify it. Keep game rules portable, but avoid abstractions that harm frame-time, allocation, serialization, or iteration; profiling on target hardware decides the boundary.

References: [Game Programming Patterns - game loop](https://gameprogrammingpatterns.com/game-loop.html), [Game Accessibility Guidelines](https://gameaccessibilityguidelines.com/), and official [Godot optimization](https://docs.godotengine.org/en/stable/tutorials/optimization/index.html), [Unity profiling](https://docs.unity3d.com/6000.0/Documentation/Manual/Profiler.html), and [Unreal Insights](https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-insights-in-unreal-engine).

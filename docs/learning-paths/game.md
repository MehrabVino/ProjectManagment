# Game Development Path

## Portable core first

Model game rules as ordinary domain code: state transitions, scoring, inventory, combat resolution, quests, saves, and AI decisions. Keep rendering, input devices, engine lifecycle callbacks, scene loading, and asset APIs in adapters.

## Engine mapping

| Portable concept | Unity | Godot | Unreal |
| --- | --- | --- |
| Composition root | Bootstrap scene / installer | Autoload / main scene | Game instance / subsystem |
| Input adapter | Input System | InputMap | Enhanced Input |
| Rendering adapter | MonoBehaviour / ECS view | Node / Control | Actor / Widget |
| Persistence adapter | File, cloud, platform service | FileAccess, resource, service | SaveGame, platform service |
| Test host | Edit/play mode test runner | GUT or built-in tests | Automation tests |

The table is a translation aid, not an architectural requirement. The core must refer to an `InputPort`, `SavePort`, or `PresentationPort`, never an engine class.

## Pattern triggers

- Use a state machine when an entity has explicit, mutually exclusive states with guarded transitions.
- Use Strategy when a policy varies independently, such as targeting, damage calculation, or enemy behavior.
- Use Observer/events for one-way notifications; do not use them to hide required control flow.
- Use an ECS only when large populations and data-oriented processing justify its added complexity.

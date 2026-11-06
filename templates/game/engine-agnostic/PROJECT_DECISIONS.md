# Project Decisions

Complete this before choosing an engine integration.

- **Player promise:** What repeatable experience does the game deliver?
- **Core loop:** What action, feedback, reward, and progression cycle repeats?
- **Domain state:** Which state must be deterministic and serializable?
- **Platform constraints:** Offline/online, target devices, input types, performance budget.
- **Boundary contracts:** What must input, presentation, persistence, time, randomness, and networking provide?
- **Testing:** Which rules can run without the engine? Which integrations require the engine?
- **Engine adapter:** Which engine is used first, and which code is forbidden from entering `domain/`?
- **Exit criteria:** What makes the first playable slice complete?

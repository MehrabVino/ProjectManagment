# Engine-Agnostic Game Template

Use this template when you want game rules to survive an engine change or be testable without opening an engine editor.

## Dependency direction

```text
adapters (engine, UI, persistence, platform SDK)
                      -> ports <-
                  application use cases
                      -> domain core
```

Dependencies always point inward. The domain core defines the language of the game; adapters translate engine events and platform APIs into that language.

## Suggested layout

```text
src/
  domain/          Entities, value objects, rules, state transitions
  application/     Use cases: start match, apply input, save game
  ports/           Interfaces: clock, random, input, save, presentation
  adapters/        One folder per engine/platform integration
tests/
  domain/          Fast deterministic tests
  application/     Contract and integration tests with fakes
docs/
  PROJECT_DECISIONS.md
  ARCHITECTURE.md
```

Start from [PROJECT_DECISIONS.md](PROJECT_DECISIONS.md) and [ARCHITECTURE.md](ARCHITECTURE.md).

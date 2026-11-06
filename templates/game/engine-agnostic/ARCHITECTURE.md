# Architecture

## Core contracts

The domain must operate using values and interfaces it owns. Typical ports:

- `InputPort`: returns normalized player intent, not device keys.
- `ClockPort`: supplies game time or ticks.
- `RandomPort`: allows deterministic tests and replay.
- `SavePort`: persists a versioned game snapshot.
- `PresentationPort`: receives a view model or domain event; it does not contain rules.

## Adapter responsibilities

An engine adapter may translate a button press into `MoveIntent`, render `PlayerView`, or map a scene transition to a use case. It must not decide damage, score, quest completion, or save validity.

## First vertical slice

1. Define one player intent and one state transition in `domain/`.
2. Test the transition with a fake clock and random source.
3. Add one engine adapter that translates real input and renders the result.
4. Add one save/load round trip.

Only add patterns when this slice exposes a clear pressure point.

# Contributing

## Template contract

Every new template must include:

- a problem statement and intended audience;
- architecture boundaries and dependency direction;
- a small, tool-neutral domain example;
- a testing strategy;
- a `PROJECT_DECISIONS.md` checklist;
- at least one adapter guide for common tools, without making those tools part of the core design.

## Dependency rule

The core business or game rules must not import a framework, engine API, database client, cloud SDK, or UI library. Those concerns implement ports at the boundary.

## Teaching rule

Show the smallest solution first, then explain the trigger for adding an abstraction. Include when *not* to use a pattern.

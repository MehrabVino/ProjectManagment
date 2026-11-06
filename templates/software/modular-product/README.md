# Tool-Neutral Modular Product Template

Start with a modular monolith. Each module owns its business rules and data contracts; HTTP, database, messaging, and cloud integrations are adapters.

```text
modules/
  identity/       domain, application, ports, adapters
  catalog/        domain, application, ports, adapters
  orders/         domain, application, ports, adapters
shared/           only stable cross-cutting primitives
```

Before introducing microservices, document a concrete need for separate deployment, independent ownership, or isolated scaling.

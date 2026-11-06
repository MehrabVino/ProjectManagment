# Software Engineering Modules

Select these in addition to the shared foundation.

| Trigger | Module | Required evidence |
| --- | --- | --- |
| A user or another system calls an API | API boundary | API contract, error schema, authorization policy, contract tests, version/deprecation plan |
| Persistent business data exists | Data modeling and consistency | ERD/schema, migrations, transaction/isolation ADR, indexes/constraints, backup/restore tests |
| UI is part of the product | Frontend and design system | page/component map, states for loading/error/empty/offline, accessibility and visual tests |
| Scale or reliability targets are explicit | System design and performance | load estimate, SLOs, capacity plan, performance budget and measured baseline |
| Work crosses process boundaries | Messaging/distributed systems | event schema, idempotency, retry/dead-letter policy, consistency decision and failure tests |
| Product ships as a package/library | Public API and compatibility | package contract, examples, SemVer/deprecation policy, consumer tests and license/SBOM |
| Product is deployed | Runtime operations | configuration matrix, health checks, deploy/rollback plan, dashboards and runbooks |

Default to a modular monolith. Add distributed systems only when independent deployment, ownership, scale, or availability requirements justify their operational cost.

References: [OWASP API Security](https://owasp.org/projects/api-security-project), [GeeksforGeeks API contracts](https://www.geeksforgeeks.org/system-design/api-contracts-system-design/), [GeeksforGeeks normalization](https://www.geeksforgeeks.org/dbms/introduction-of-database-normalization/), and [Martin Fowler on monolith-first](https://martinfowler.com/bliki/MonolithFirst.html).

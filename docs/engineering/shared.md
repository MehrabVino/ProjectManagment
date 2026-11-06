# Shared Engineering Modules

| Status | Module | Select it to produce |
| --- | --- | --- |
| Foundation | Product discovery and requirements | problem statement, stakeholder map, acceptance criteria, assumptions and change log |
| Foundation | SDLC and delivery planning | lifecycle choice, definition of ready/done, increments and release plan |
| Foundation | Domain modeling and system modeling | domain model plus only the useful C4/UML diagrams: context, container, sequence, state, ERD, component, or deployment |
| Foundation | Architecture and decision records | quality-attribute scenarios, dependency map, ADRs and interface/data contracts |
| Foundation | Clean code and design patterns | naming/function/module rules; pattern decision record showing the pressure point, alternatives and trade-off |
| Foundation | Quality engineering | risk-based test strategy, test data, acceptance tests, defect learning and regression gates |
| Foundation | Documentation and traceability | README, onboarding, runbook, glossary, ownership/staleness policy and links from requirement to test |
| Foundation | Security and privacy | data-flow/trust-boundary diagram, threat model, abuse cases, secret policy and residual-risk decision |
| Foundation | Delivery and supply chain | reproducible build, configuration contract, artifact provenance/SBOM, release and rollback checklists |
| Foundation | Operations and resilience | service ownership, logs/metrics/traces, SLI/SLOs, alerts, backup/restore, incident and postmortem templates |
| Conditional | Design system and accessible interaction | design tokens, component contracts, states, responsive rules, accessibility criteria and visual regression plan |
| Conditional | Governance and engineering economics | RACI, risk/dependency log, decision rights, budget/capacity assumptions and review gates |

## Pattern selection rule

Use a pattern only with a named trigger. Examples: Strategy for independently changing policy; State for explicit guarded state transitions; Observer/events for notifications rather than hidden required flow; Repository when the domain needs a persistence boundary. Record the reason in an ADR. A catalog of patterns without this decision rule becomes ceremony.

## Source starting points

- [C4 model](https://c4model.com/introduction) and [UML](https://www.omg.org/spec/UML/) for communicating architecture and behavior.
- [GeeksforGeeks system-design introduction](https://www.geeksforgeeks.org/system-design/getting-started-with-system-design/) and [UML introduction](https://www.geeksforgeeks.org/system-design/unified-modeling-language-uml-introduction/) for accessible starting material.
- [OWASP threat-modeling cheat sheet](https://cheatsheetseries.owasp.org/cheatsheets/Threat_Modeling_Cheat_Sheet.html), [NIST SSDF](https://csrc.nist.gov/pubs/sp/800/218/final), and [OpenTelemetry signals](https://opentelemetry.io/docs/concepts/signals/) for security and operation evidence.

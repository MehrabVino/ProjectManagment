# Software Product Path

Begin with a modular monolith: modules own their data and expose explicit contracts. Keep framework controllers, database clients, queues, and third-party SDKs at the boundary. Split into services only when deployment, ownership, or scale constraints require it.

Recommended progression: request validation -> application use cases -> domain policy -> ports -> adapters -> automated tests -> delivery and operations.

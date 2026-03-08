[![Architecture](https://img.shields.io/badge/architecture-polycentric-green)](docs/architecture.md)
[![Governance](https://img.shields.io/badge/governance-fractal--sortition-blue)](docs/governance.md)
[![Schemas](https://img.shields.io/badge/schemas-open-orange)](schemas/)
[![Agents](https://img.shields.io/badge/agents-adl-lightgrey)](agents/)
[![License](https://img.shields.io/badge/license-MIT-green)](LICENSE)
# csg-agentic-adl
Open schemas, protocols, and agent definitions for bioregional seed stewardship, fractal governance, and federated ecological coordination. This repository explores a polycentric stewardship architecture combining
seed ecology, fractal governance, and agent-based coordination systems.  It is important to keep in mind that a very large seed collection/system is physically underpinning this whole initiative.
## Repository Overview
- Protocol specification → spec/
- Architecture docs → docs/
- Data schemas → schemas/
- Agent definitions → agents/
- Example data → examples/
## Architecture (Mermaid Overview Diagram)

```mermaid
flowchart TD

A[Seeds & Ecology]
B[Local Seed Stewards]
C[Regional Seed Guilds]
D[Fractal Sortition Councils]
E[Agentic ADL Hub]
F[Knowledge Commons]

A --> B
B --> C
C --> D
D --> E
E --> F

B --> |Stewardship Events| E
C --> |Seed Exchange| B
E --> |Protocols & Schemas| C
E --> |Open Data| F
```
## Repository Architecture Full Diagram

```mermaid
flowchart TD

R[CSG Agentic ADL Repository]

R --> S[spec/]
R --> D[docs/]
R --> J[schemas/]
R --> A[agents/]
R --> P[protocols/]
R --> E[examples/]

S --> S1[00-introduction.md]
S --> S2[01-core-concepts.md]
S --> S3[Future spec documents]

D --> D1[Architecture explanations]
D --> D2[Governance notes]
D --> D3[Reference images]

J --> J1[stewardship_event.schema.json]
J --> J2[council_decision.schema.json]
J --> J3[other protocol schemas]

A --> A1[seed steward agent]
A --> A2[seed exchange agent]
A --> A3[climate observer agent]

P --> P1[seed exchange protocol]
P --> P2[fractal sortition protocol]
P --> P3[federation protocol]

E --> E1[stewardship event examples]
E --> E2[council decision examples]
E --> E3[sample data objects]

S -->|defines rules for| J
S -->|defines roles for| A
S -->|guides processes in| P
J -->|validated by| E
A -->|uses| J
A -->|operates within| P
D -->|explains| S
D -->|explains| J
D -->|explains| A

K[Knowledge Commons]
E --> K
A --> K
P --> K
J --> K
S --> K
```
## Seed Infrastructure Protocol
The Seed Infrastructure Protocol defines an open framework for
coordinating distributed seed stewardship networks and ecological data systems.

The formal protocol specification can be found in:

- [Seed Infrastructure Protocol Introduction](spec/00-introduction.md)
- [Core Concepts](spec/01-core-concepts.md)
## Architecture Overview
![Bioregional Polycentric Stewardship Network](docs/githubArchitecture.png)
# CSG Agentic ADL

A lightweight open repository for defining agent-readable stewardship protocols, event schemas, and governance patterns for bioregional seed networks.

This project is being developed in relation to:

- Cascadia Seed Guild
- bioregional seed stewardship
- Fractal Sortition governance experiments
- agentic coordination infrastructure
- open ecological data systems

## Purpose

The goal of this repository is to define a shared language that can be used by:

- human seed stewards
- community seed libraries
- regional seed guilds
- software agents
- federated governance systems
- ecological monitoring tools

This is not a central control system.

It is a coordination layer.

The purpose is to help distributed networks share information, stewardship actions, and governance outcomes in a transparent, portable, and machine-readable way.

## Core design principles

1. Humans remain the stewards.
2. Agents assist with coordination, recordkeeping, and pattern detection.
3. Ecological diversity is treated as resilience infrastructure.
4. Governance should be distributed, auditable, and adaptive.
5. Bioregions matter more than administrative borders for ecological stewardship.
6. Open standards are preferable to proprietary lock-in.

## Main components

### 1. Schemas
JSON schemas define shared structures for:
- seed accessions
- stewardship events
- bioregions
- council decisions

### 2. Agent Definitions
ADL files describe:
- agent role
- inputs
- outputs
- actions
- constraints
- trust boundaries

### 3. Protocols
Human-readable governance and exchange protocols describe:
- seed exchange norms
- fractal sortition process
- federation between guilds and repositories

## Suggested use cases

- recording seed saving events
- tracking local adaptation notes
- coordinating community seed exchanges
- logging pollinator observations
- reporting climate anomalies relevant to seed work
- publishing council decisions in machine-readable form
- integrating Perma-Ledger / farmOS data into federated systems

## Repository status

Early-stage conceptual infrastructure.

This repository is intended as a living commons for experimentation, refinement, and practical deployment in seed-based resilience networks.

## Initial vision

Seeds -> Local Stewards -> Regional Guilds -> Fractal Governance -> Agentic Coordination -> Knowledge Commons

## Contributing

At this stage, contributions should prioritize:
- clarity
- interoperability
- low complexity
- ecological usefulness
- governance transparency

## License

See LICENSE.

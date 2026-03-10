# Seed Guild Node Architecture

```mermaid
graph TD

Seeds[Living Seeds]
Stewards[Human Stewards]
Records[Stewardship Records]
Agents[Agent Assistants]
Governance[Guild Governance]
Federation[Bioregional Seed Network]

Stewards --> Seeds
Stewards --> Records
Records --> Agents
Agents --> Records
Governance --> Records
Governance --> Federation
Seeds --> Federation

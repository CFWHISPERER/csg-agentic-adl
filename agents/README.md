# Agents

This directory defines the agent roles used within the Lichen system.

Agents describe *behavior*, not infrastructure.  
They operate across local, coordination, and governance layers to support a local-first, distributed system.

---

## Purpose

Agents are responsible for:

- observing and recording real-world conditions
- coordinating data movement between nodes
- maintaining system coherence without central control
- supporting governance through structured inputs

Each agent is defined using ADL (Agent Definition Language).

---

## Agent Families

### Stewardship Agents

Operate close to place and living systems.

Examples:
- `seed_steward_agent`
- `seed_exchange_agent`
- `climate_observer_agent`
- `pollinator_monitor_agent`

These agents:
- observe
- record
- act within local context

---

### Coordination Agents

Maintain coherence across distributed nodes.

Examples:
- `sync_agent`
- `bridge_agent`

These agents:
- synchronize data between nodes
- route information across interfaces
- operate opportunistically without requiring continuous connectivity

---

### Memory and Governance Support Agents

Support long-term system awareness and decision-making.

Examples (current and future):
- `governance_summary_agent`
- `vault_memory_agent`

These agents:
- aggregate information
- surface patterns
- support, but do not replace, human governance

---

## Design Principles

All agents operate under shared principles:

- **Local-First** — act at the lowest viable level  
- **Subsidiarity** — defer decisions upward only when necessary  
- **Distributed Operation** — no central dependency  
- **Auditability** — actions produce traceable records  
- **Minimal Data Movement** — move only what is needed  

---

## Relationship to the System

Agents interact with:

- schemas (`/schemas`) → define structure  
- protocols (`/protocols`) → define interaction patterns  
- specifications (`/spec`) → define system behavior  

Agents are one part of a larger system:

- Lichen Stack → structure  
- Communication Layer → connectivity  
- Flow → behavior  
- Governance → decision-making  

---

## Summary

Agents are not controllers.

They are participants in a distributed system that:

- observes reality
- moves information locally
- coordinates across nodes
- supports shared decision-making

> The system works by shaping flow, not enforcing control.

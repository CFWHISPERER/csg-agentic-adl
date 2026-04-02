# 03 — Agent Actions

## Overview

The system operates through a defined set of **agent actions**.

These actions are not centralized.  
They occur across a distributed network of:

- human stewards  
- device nodes  
- storage (vault) nodes  
- councils  

Actions are organized across three layers:

- **Local** — place-based, material interaction  
- **Coordination** — synchronization across nodes  
- **Governance** — deliberation and decision-making  

This layered model reflects a fundamental principle:

> The system is not a single control structure, but an ecology of actions distributed across scale.

---

## Action Layers

### Local

Actions that occur directly within a place, involving physical materials or immediate observation.

Examples:
- observe
- identify
- log
- store
- test

Primary actors:
- `human_steward`
- `device_node`
- `hybrid`

---

### Coordination

Actions that maintain coherence across distributed nodes.

Examples:
- sync
- validate
- reconcile
- summarize
- distribute

Primary actors:
- `device_node`
- `vault_node`
- `hybrid`

---

### Governance

Actions involving judgment, prioritization, and shared responsibility.

Examples:
- deliberate
- decide
- assign
- review_outcomes

Primary actors:
- `council`
- `human_steward`
- `hybrid`

---

## Major Agent Actions

| Action | Purpose | Layer | Primary Actor Types | Related Schemas |
|--------|--------|-------|---------------------|------------------|
| observe | Record conditions or events | local | human_steward, device_node, hybrid | `observation`, `species_record` |
| identify | Associate entity with a record | local | device_node, human_steward | `seed_accession`, `seed_lot`, `species_record` |
| log | Record stewardship activity | local | human_steward, device_node | `planting_event`, `stewardship_event` |
| store | Maintain physical storage context | local | human_steward, vault_node, hybrid | `storage_location`, `seed_lot` |
| test | Assess viability or condition | local | human_steward, hybrid | `viability_test`, `seed_lot` |
| recommend | Suggest local action | local / coordination | device_node, hybrid | `viability_test`, `observation` |
| sync | Exchange records between nodes | coordination | device_node, vault_node | `sync_event`, `device_node` |
| validate | Ensure record consistency | coordination | hybrid, council | `sync_event`, `seed_lot` |
| reconcile | Resolve conflicting records | coordination | hybrid, council | `sync_event`, `storage_location` |
| summarize | Aggregate system state | coordination | vault_node, hybrid | `outcome`, `sync_event` |
| deliberate | Evaluate competing priorities | governance | council | `council_decision`, `outcome` |
| decide | Select formal action | governance | council | `council_decision`, `outcome` |
| assign | Allocate responsibility | governance | council, human_steward | `stewardship_unit` |
| regenerate | Renew seed capacity | local / governance | human_steward, council, hybrid | `planting_event`, `viability_test` |
| distribute | Share seeds or knowledge | coordination / governance | human_steward, council, hybrid | `seed_lot`, `stewardship_event` |
| review_outcomes | Compare outcomes vs intent | governance | council, hybrid | `outcome`, `observation` |

---

## Relationship to Schemas

Each action produces or interacts with one or more schema-defined objects.

Examples:

- **observe → observation**
- **test → viability_test**
- **store → storage_location**
- **sync → sync_event**

Schemas define structure.  
Actions define behavior.

---

## Relationship to Network Architecture

Agent actions occur across the network layers defined in `02-network-architecture.md`:

- **Device nodes** perform local actions  
- **Site nodes (Raspberry Pi)** perform coordination actions  
- **Vault nodes** maintain persistent memory and summaries  

This reflects a pattern:

- Local intelligence (Lichen layer)  
- Network coherence (Mycelial layer)  
- Governance (Council layer)  

---

## Relationship to Governance

Fractal Sortition operates primarily within the **governance layer**, but is informed by:

- local observations  
- coordination summaries  

Decisions are therefore:

- grounded in place  
- informed by distributed evidence  
- enacted through assigned stewardship  

---

## Summary

The system functions through:

- local action  
- coordinated synchronization  
- distributed governance  

No single layer is sufficient.

> Intelligence emerges from the interaction of all three.

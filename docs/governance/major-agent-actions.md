```
docs/governance/major-agent-actions.md
```

---

# Major Agent Actions (Fractal Sortition Overview)

This table defines the primary categories of agent actions within the system.
Actions are organized across three layers:

* **Local** — place-based, immediate, material interaction
* **Coordination** — synchronization and reconciliation across nodes
* **Governance** — deliberation, prioritization, and decision-making

Each action is associated with one or more **primary actor types**:

* `human_steward`
* `device_node`
* `vault_node`
* `council`
* `hybrid` (combined human + system action)

---

## Full Action Table

| Action              | Purpose                                               | Layer                     | Primary Actor Types                | Typical Triggers                              | Related Schemas                                      | Escalation                                   |
| ------------------- | ----------------------------------------------------- | ------------------------- | ---------------------------------- | --------------------------------------------- | ---------------------------------------------------- | -------------------------------------------- |
| **observe**         | Record conditions, states, or events in the system    | local                     | human_steward, device_node, hybrid | QR scan, field observation, sensor input      | `observation`, `species_record`                      | Escalates on anomaly or pattern detection    |
| **identify**        | Associate an entity with an existing record           | local                     | device_node, human_steward         | QR scan, lookup, manual entry                 | `seed_accession`, `seed_lot`, `species_record`       | Escalates on ambiguity or mismatch           |
| **log**             | Create a time-based record of stewardship activity    | local                     | human_steward, device_node         | planting, harvest, movement, note-taking      | `planting_event`, `stewardship_event`, `observation` | Escalates on repeated inconsistency          |
| **store**           | Place or maintain materials within a defined location | local                     | human_steward, vault_node, hybrid  | seed intake, reorganization, preservation     | `storage_location`, `seed_lot`, `seed_accession`     | Escalates on storage risk or capacity issues |
| **test**            | Assess viability or condition of seed material        | local                     | human_steward, hybrid              | scheduled testing, aging thresholds           | `viability_test`, `seed_lot`                         | Escalates on low viability                   |
| **recommend**       | Suggest a course of action based on local state       | local / coordination      | device_node, hybrid                | low stock, viability decline, planting window | `viability_test`, `observation`, `seed_lot`          | Escalates if shared resources are affected   |
| **sync**            | Exchange and reconcile records between nodes          | coordination              | device_node, vault_node            | scheduled or opportunistic connection         | `sync_event`, `device_node`                          | Escalates on conflict or failure             |
| **validate**        | Check records for consistency and completeness        | coordination              | hybrid, council                    | sync conflict, incomplete data                | `sync_event`, `seed_lot`, `planting_event`           | Escalates on unresolved inconsistency        |
| **reconcile**       | Resolve conflicting records or states                 | coordination              | hybrid, council                    | duplicate records, divergent histories        | `sync_event`, `storage_location`, `seed_lot`         | Escalates to governance if unresolved        |
| **summarize**       | Aggregate local activity into higher-level insight    | coordination              | vault_node, hybrid                 | sync completion, reporting cycle              | `outcome`, `sync_event`                              | Escalates on detected risk or drift          |
| **deliberate**      | Evaluate tradeoffs and competing priorities           | governance                | council                            | scarcity, conflict, planning                  | `council_decision`, `outcome`                        | Escalates to wider council if needed         |
| **decide**          | Select a formal course of action                      | governance                | council                            | allocation, policy, regeneration need         | `council_decision`, `outcome`                        | Escalates if cross-region impact             |
| **assign**          | Allocate responsibility for stewardship actions       | governance                | council, human_steward             | task creation, unresolved issues              | `stewardship_unit`, `council_decision`               | Escalates on capacity constraints            |
| **regenerate**      | Initiate renewal of living capacity or seed stock     | local / governance        | human_steward, council, hybrid     | low viability, strategic resilience need      | `planting_event`, `viability_test`, `seed_lot`       | Escalates if regionally significant          |
| **distribute**      | Share seeds or knowledge across the network           | coordination / governance | human_steward, council, hybrid     | exchange, request, resilience response        | `seed_accession`, `seed_lot`, `stewardship_event`    | Escalates under scarcity conditions          |
| **review_outcomes** | Compare intended outcomes with observed results       | governance                | council, hybrid                    | end-of-season, decision review                | `outcome`, `observation`, `planting_event`           | Escalates on systemic mismatch               |

---

## Layer Definitions

### Local

Actions that occur directly within a place, involving physical materials or immediate observation.

Examples:

* observe
* identify
* log
* store
* test

---

### Coordination

Actions that connect nodes and ensure consistency across distributed systems.

Examples:

* sync
* validate
* reconcile
* summarize
* distribute

---

### Governance

Actions that involve judgment, prioritization, and collective responsibility.

Examples:

* deliberate
* decide
* assign
* review_outcomes

---

## Summary

Fractal Sortition operates across a layered system of actions:

* **Local actions** maintain connection to place and material reality
* **Coordination actions** maintain coherence across distributed nodes
* **Governance actions** maintain legitimacy and shared direction

> The system is not a single decision layer, but an ecology of actions distributed across scale.

---

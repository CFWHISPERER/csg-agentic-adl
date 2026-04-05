# Lichen Flow

This diagram shows how information moves through the Lichen system.

It illustrates a typical cycle:

- observation in the field
- local capture on a device
- synchronization to a site node
- persistence in a seed vault
- aggregation for governance
- return to stewardship action

---

## Flow Diagram

```mermaid
flowchart TB

    A["Field Observation<br/>Planting • Harvest • Condition • Note"]
    B["Phone Node<br/>Scan • Record • Local Storage"]
    C["Site Node<br/>Raspberry Pi • Local Sync • Aggregation"]
    D["Vault Node<br/>Seed Vault • Inventory • Viability History"]
    E["Governance Layer<br/>Council • Fractal Sortition • Review"]
    F["Stewardship Action<br/>Regenerate • Distribute • Adjust"]

    A --> B --> C --> D --> E --> F
    F --> A

    P["Flow Principles<br/>Local First • Opportunistic Sync • Minimal Data Movement"]
    P -.-> B
    P -.-> C
    P -.-> D

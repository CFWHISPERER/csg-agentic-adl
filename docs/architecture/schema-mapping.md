# Schema Mapping

This document maps the current schema set to the major layers of the Lichen system.

It helps clarify:

- which schemas belong to which part of the architecture
- how data moves across layers
- how structure supports stewardship, coordination, memory, and governance

The mapping is not rigid. Some schemas may participate in more than one layer.

---

## Presentation Diagram

```mermaid
flowchart TB

    L1["Local Layer<br/>Field Observation • Stewardship • Device Capture"]
    L2["Coordination Layer<br/>Sync • Site Node • Local Aggregation"]
    L3["Memory Layer<br/>Seed Vault • Inventory • Viability History"]
    L4["Governance Layer<br/>Councils • Decisions • Outcomes"]

    L1 --> L2 --> L3 --> L4

    S1["Schemas<br/>observation<br/>planting_event<br/>stewardship_event"] --> L1
    S2["Schemas<br/>device_node<br/>sync_event"] --> L2
    S3["Schemas<br/>seed_accession<br/>seed_lot<br/>storage_location<br/>viability_test"] --> L3
    S4["Schemas<br/>council_decision<br/>outcome<br/>stewardship_unit"] --> L4

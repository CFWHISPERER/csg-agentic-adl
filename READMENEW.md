
```mermaid
flowchart TB

    subgraph L0["Layer 0 - Living Foundation"]
        A1["Seeds"]
        A2["Soil"]
        A3["Water"]
        A4["Place"]
    end

    subgraph L1["Layer 1 - Stewardship"]
        B1["Observe"]
        B2["Plant"]
        B3["Store"]
        B4["Test"]
        B5["Regenerate"]
    end

    subgraph L2["Layer 2 - Local Intelligence"]
        C1["Phone Node"]
        C2["Device Node"]
        C3["Field Agent"]
    end

    subgraph L3["Layer 3 - Site Coordination"]
        D1["Raspberry Pi"]
        D2["Site Node"]
        D3["Local Sync"]
    end

    subgraph L4["Layer 4 - Communication"]
        E1["Routing"]
        E2["Bridge Node"]
        E3["Interface Agnostic Links"]
    end

    subgraph L5["Layer 5 - Persistent Memory"]
        F1["Seed Vault Node"]
        F2["Inventory"]
        F3["Viability History"]
    end

    subgraph L6["Layer 6 - Governance"]
        G1["Fractal Sortition"]
        G2["Council Decisions"]
        G3["Assignments"]
        G4["Outcomes"]
    end

    L0 --> L1 --> L2 --> L3 --> L4 --> L5 --> L6

    H["Schemas:\nobservation, planting_event, stewardship_event"] --> L2
    I["Schemas:\ndevice_node, sync_event"] --> L3
    J["Schemas:\nseed_lot, seed_accession, storage_location, viability_test"] --> L5
    K["Schemas:\ncouncil_decision, outcome, stewardship_unit"] --> L6

    X["Interfaces:\nLoRa, Wi-Fi, HaLow, Ethernet, Bluetooth"] --> L4
    Y["Principles:\nSubsidiarity, Local-First, Sovereign Identity, Encryption"] -.-> L2
    Y -.-> L3
    Y -.-> L4
    Y -.-> L5
    Y -.-> L6

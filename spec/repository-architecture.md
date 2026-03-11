flowchart TB

    subgraph Living_System["Living Ecological System"]
        S[Species / Plants]
        P[Pollinators & Fungi]
        E[Environmental Conditions]
    end

    subgraph Stewardship["Human Stewardship"]
        SL[Seed Lots]
        SE[Stewardship Events]
        OBS[Field Observations]
    end

    subgraph Knowledge_System["Repository Knowledge Commons"]
        SR[species_record.schema.json]
        SLJ[seed_lot.schema.json]
        OBSJ[observation.schema.json]
        SEJ[stewardship_event.schema.json]
    end

    subgraph Governance["Guild Coordination"]
        CD[council_decision.schema.json]
        BR[bioregion.schema.json]
        ACC[seed_accession.schema.json]
    end

    subgraph Agents["AI & Analysis Agents"]
        A1[Literature Agent]
        A2[Observation Structuring Agent]
        A3[Pattern Analysis Agent]
        A4[Documentation Agent]
    end


    S --> SL
    P --> OBS
    E --> OBS

    SL --> SLJ
    OBS --> OBSJ
    SE --> SEJ
    S --> SR

    SLJ --> A3
    OBSJ --> A3
    SR --> A1

    A1 --> SR
    A2 --> OBSJ
    A3 --> SEJ
    A4 --> SR

    CD --> SE
    BR --> SR
    ACC --> SL

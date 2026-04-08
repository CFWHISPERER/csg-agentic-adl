# 05 — Delay-Tolerant Communication

## Overview

The system does not assume continuous connectivity.

Communication is designed to operate under conditions where:

- connections are intermittent
- bandwidth is limited
- latency may be high
- nodes may be temporarily isolated

This model is known as **Delay-Tolerant Communication (DTC)**.

> Messages are expected to arrive eventually, not instantly.

---

## Core Concept

Communication follows a **store → carry → forward** model:

1. **Store** — data is recorded locally on a node  
2. **Carry** — data remains with the node or is physically transported  
3. **Forward** — data is transferred when a viable connection becomes available  

This applies to:

- digital transmission (Wi-Fi, LoRa, Ethernet)
- opportunistic mesh routing
- physical transfer (portable storage, human movement)

---

## Communication Modes

The system supports multiple communication modes:

### 1. Immediate

- direct local connection
- low latency
- high availability

Examples:
- phone → Raspberry Pi via Wi-Fi
- device-to-device local sync

---

### 2. Opportunistic

- connection occurs when nodes come within range
- no guarantee of timing
- routing is dynamic

Examples:
- LoRa mesh
- bridge node routing
- intermittent site connectivity

---

### 3. Physical (Store-Carry-Forward)

- data is physically transported between nodes
- no network required during transit

Examples:
- SD card or USB transfer
- device movement between locations
- human-mediated transport

---

## Design Principles

### Local Persistence

All nodes must be capable of storing data until it can be forwarded.

- no reliance on immediate transmission
- data durability is required

---

### Eventual Delivery

The system prioritizes **eventual consistency** over immediate consistency.

- updates propagate over time
- nodes converge through repeated synchronization

---

### Path Independence

Data does not depend on a single route.

- multiple paths may exist
- routes may change dynamically
- delivery may occur through unexpected pathways

---

### Minimal Assumptions

The system does not assume:

- constant connectivity
- centralized routing infrastructure
- uniform network conditions

---

### Graceful Degradation

Under degraded conditions:

- local operation continues
- data is queued
- synchronization resumes when possible

---

## Relationship to Agent Actions

Delay-tolerant communication supports:

- `sync` — performed opportunistically  
- `store` — data retained locally until transfer  
- `reconcile` — resolves differences after delayed updates  
- `summarize` — aggregates delayed inputs for governance  

Agents such as:

- `sync_agent`
- `bridge_agent`

operate within this model.

---

## Relationship to Communication Layer

This specification extends `04-communication-and-routing.md`.

- routing may occur across multiple interfaces
- connections may be intermittent
- bridging enables delayed forwarding across networks

---

## Relationship to Governance

Governance operates on:

- aggregated
- delayed
- partially synchronized data

This reinforces:

- subsidiarity
- local autonomy
- tolerance for incomplete information

Decisions are:

- informed by available data
- refined as additional data arrives

---

## Examples

### Local Sync

A phone records a planting event.

- data is stored locally
- later synced to a Raspberry Pi when nearby

---

### Multi-Hop Sync

A site node syncs with another site node.

- data moves across multiple hops
- no central server is required

---

### Physical Transfer

A steward carries a storage device between locations.

- data is transferred physically
- later merged into the system

---

## Summary

Delay-tolerant communication enables the system to function under real-world conditions:

- intermittent connectivity
- limited infrastructure
- distributed environments

It ensures that:

- data is not lost
- nodes remain autonomous
- the system remains operational

> Communication is not defined by speed, but by the reliable movement of information over time.

# 04 — Communication and Routing

## Overview

Communication within the system is treated as a **routing problem**, not an infrastructure dependency.

Nodes do not assume:
- centralized servers
- persistent internet connectivity
- uniform hardware or transport layers

Instead, communication emerges through:
- local connectivity
- opportunistic synchronization
- interface-agnostic routing

> The network is not defined by cables or towers, but by the ability of nodes to route information between each other.

---

## Design Principles

### Local-First Communication

Communication should occur at the lowest viable level.

- Devices in proximity should communicate directly
- Messages should not traverse remote infrastructure unless necessary
- Local knowledge should remain local by default

---

### Interface-Agnostic Routing

The system does not depend on any single communication medium.

Supported interfaces may include:
- Wi-Fi (2.4 GHz, 5 GHz, HaLow)
- LoRa (sub-GHz)
- Ethernet
- Bluetooth
- Serial or wired links

Nodes treat these as interchangeable interfaces.

> The network exists above the hardware layer.

---

### Bridgeable Networks

Nodes may operate across multiple interfaces simultaneously.

A node with multiple interfaces can act as a **bridge**, enabling:

- LoRa-only nodes to communicate with Wi-Fi-only nodes
- local clusters to interconnect without shared hardware
- heterogeneous networks to form a single routable system

Bridging is:
- dynamic
- decentralized
- non-authoritative

---

### Sovereign Identity

Each node maintains its own identity.

- No reliance on usernames, phone numbers, or IP addresses
- Identity is persistent and portable
- Communication is authenticated without centralized registries

---

### Encrypted by Default

All communication is assumed to be:

- encrypted end-to-end
- authenticated between participants
- resistant to passive observation

Security is foundational, not optional.

---

### Opportunistic Synchronization

Synchronization occurs when nodes can reach each other.

- scheduled sync (planned)
- opportunistic sync (when connection is available)
- manual sync (user-triggered)

The system does not require continuous connectivity.

---

### Linear Scaling

Routing should avoid broadcast flooding where possible.

- messages follow discovered routes
- overhead grows linearly with hops
- network efficiency is preserved at scale

---

## Node Roles in Communication

### Device Node

- phone, laptop, or lightweight client
- performs local actions
- initiates and receives communication

---

### Site Node (e.g. Raspberry Pi)

- maintains local network presence
- aggregates local data
- bridges interfaces where available

---

### Vault Node

- persistent storage and memory
- receives summarized data
- participates in higher-level coordination

---

### Bridge Node

Any node with multiple interfaces may act as a bridge.

- connects otherwise incompatible networks
- enables cross-interface routing
- operates without central coordination

---

## Message Flow

A typical message path may look like:

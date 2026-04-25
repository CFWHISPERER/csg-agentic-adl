# Seed Infrastructure Protocol (SIP) v0.3

## Status
Draft — Living Specification

---

## 1. Purpose

The Seed Infrastructure Protocol (SIP) is a lightweight communication framework for coordinating actions across seeds, soil, people, and digital agents.

SIP does not begin with software abstractions such as APIs or services.

It begins with the needs of living systems.

SIP enables:
- Local food system coordination
- Seed stewardship and propagation
- Soil and ecological observation
- Distributed, delay-tolerant communication
- Integration between human, biological, and digital actors

---

## 2. Design Principles

### 2.1 Life-First Design
SIP is grounded in real-world ecological processes:
- Seeds
- Soil
- Water
- Climate
- Human stewardship

Digital systems adapt to these realities, not the other way around.

---

### 2.2 Intent Over Instruction
SIP messages express *intent*, not implementation details.

Instead of:
> "Call this API"

SIP expresses:
> "This seed lot needs planting before seasonal window closes"

---

### 2.3 Local First
All SIP communication assumes:
- Local context matters most
- Local decisions are primary
- Global coordination is optional and secondary

---

### 2.4 Delay-Tolerant
SIP must function across:
- Intermittent connectivity
- Mesh networks
- Offline-first systems

Messages may arrive late but still retain value.

---

### 2.5 Human + Agent Coexistence
SIP is designed for:
- Human stewards
- Digital agents
- Sensors
- Community networks

All can produce and consume SIP messages.

---

## 3. Core Message Structure

All SIP messages share a common structure:

```json
{
  "sip_version": "0.3",
  "message_type": "string",
  "origin": {
    "agent": "string",
    "place": "string",
    "trust_level": "string"
  },
  "subject": {
    "type": "string",
    "name": "string",
    "id": "optional string"
  },
  "intent": {
    "action": "string",
    "reason": "string",
    "urgency": "optional string"
  },
  "context": {
    "environment": "optional object",
    "notes": "optional string"
  },
  "requested_response": {
    "type": "optional string",
    "deadline": "optional string"
  }
}

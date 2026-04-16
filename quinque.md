# The Pentagram Protocol

*A real-time interrupt dispatch layer for hybrid human/AI agent squads of five.*

## Problem Statement

Modern coordination tools (Slack, email, Discord) are pull-based and asynchronous. They assume humans will check. Real-time workflows â€” game dev sprints, live event production, agentic pipelines with human-in-the-loop checkpoints â€” need push semantics with guaranteed interrupt delivery to a human's primary attention device.

iMessage is the only consumer channel with near-universal reach in its target geography, end-to-end encryption, and sub-second interrupt latency to a phone, with no app install required on the recipient side. Yet there is no lightweight, programmable iMessage dispatch layer with a clean API targeting squads of five or fewer. Twilio owns SMS. Slack owns async teams. Nobody owns the real-time five-person hybrid interrupt bus.

## The Five-Node Constraint as a Feature

The cardinality of five is not arbitrary. It is a binding constraint that shapes the entire product.

* Keeps the thread under Apple's iMessage group performance cliff
* Maps to the innermost Dunbar cognitive trust layer (~5)
* Stays within personal-use territory, sidestepping enterprise iMessage restrictions
* Forces the product to be opinionated â€” this is not a team chat app, it is a dispatch primitive
* Fits the physical real-world constraints of a van, a stage, a control room, a fire team

## Ritual Architecture Mapping

The demonic/summoning branding is not aesthetic decoration. The ritual vocabulary maps one-to-one to the technical architecture, which is the point of the product's identity.

| Ritual Term | Technical Meaning |
| --- | --- |
| The Circle | The squad (up to five nodes) |
| The Sigil | The API key / squad identifier |
| The Summons | The interrupt dispatch payload |
| The Binding | The acknowledgment / SLA contract |
| The Dismissal | The task completion signal |
| Invocation | The act of addressing one or more nodes |

Users do not message their agents. They invoke them. A notification is not a ping, it is a summons.

## Node Model

Each of the five nodes is either a human or an AI agent. The system maintains per-node state.

* **Presence** â€” online, offline, busy, do-not-disturb
* **Node type** â€” human or AI agent (different payload format per type)
* **Priority tier** â€” P0 summons all, P1 summons primary, P2 routes to next available, P3 queues
* **Acknowledgment timeout** â€” triggers escalation cascade on expiry

AI agent nodes receive JSON payloads. Human nodes receive human-readable summons with a deep link.

## Real-Time Interrupt Model

The dispatch layer operates as a real-time operating system scheduler, but the processes are people and agents, and the inter-process communication channel is iMessage.

* Read receipts function as interrupt acknowledgment signals
* Typing indicators function as agent-processing telemetry
* Thread ordering preserves causal dispatch history
* Timeout on ack triggers re-dispatch or escalation to next-priority node

## Why iMessage Specifically

1. End-to-end encrypted â€” coordination metadata does not live on a corporate server
2. Zero friction for human nodes â€” no app, no account, works on every iPhone
3. Native to the attention device people already carry
4. The walled-garden contrast sharpens the brand â€” summoning through the most locked-down consumer platform on earth

## Market Wedge

The target is not "replace Slack." The target is a set of narrow, high-value verticals where the five-node constraint is native to the workflow.

* Indie game studios (crunch coordination, â‰¤5 devs)
* AI agent pipeline operators (human escalation paths for autonomous loops)
* Live event and broadcast production (five-person control rooms)
* High-trust creative collaboration (bands, film crews, writer's rooms)
* Security and ops teams (encrypted interrupt channels)

## Economic Frame

A BlueBubbles-relay-backed SaaS at $29/month per squad, targeting 10,000 squads, yields roughly $3.5M ARR at steady state. Infrastructure cost is low (one Mac Mini per region). Switching cost is high because the node list is the user's existing contacts.

## Brand System

* Logo concept: pentagram with each point labeled with an agent-type glyph, center occupied by a single eye representing the dispatcher
* Colorway: deep red on black, inverted for light mode
* Voice: direct, ritual-accurate, minimal ornamentation

## Product Name Candidates

* **PENTASM** â€” pentagram plus dispatch
* **INVOKE** â€” clean, verb-forward
* **DAEMON** â€” technically accurate, OS-native connotation
* **SUMMON** â€” most on-brand
* **COVEN** â€” human-forward, implies trust

## Implementation Notes

* BlueBubbles relay (or equivalent) for iMessage bridge on a Mac host
* Per-squad state machine tracking node presence and pending summonses
* Priority queue with escalation cascade on acknowledgment timeout
* Dual payload formatter (JSON for agent nodes, human-readable for human nodes)
* Webhook surface for AI agent nodes to receive and respond to summonses
* Audit log of every summons, acknowledgment, and dismissal for post-incident review

## Validation Phase

* Prototype with a single squad (one Mac Mini, five test nodes, mix of human and agent)
* Measure end-to-end dispatch latency under load
* Validate escalation cascade behavior on ack timeout
* Confirm iMessage group thread stability at five active participants

---

**Framework articulated by Aaron Hightower, the High Tower District**

**Date:** April 16, 2026

**Status:** Kernel â€” concept articulated, not yet implemented

**Maturity Level:** Stage 1 (Kernel)

**Related Snapshots:** None at time of writing

**Evolution Path:** Could become a standalone SaaS, a developer primitive sold as an API, or a licensed dispatch layer for agentic platforms needing human-in-the-loop interrupt handling

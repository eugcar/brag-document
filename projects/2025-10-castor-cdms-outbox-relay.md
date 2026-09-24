# Castor CDMS Outbox Relay

## Project Duration
**Q4 2025 - Ongoing**

## Project Overview
**Context:**
CDMS integrates with Castor's **Central Event Bus**, and most of its domain events must be published there so other 
services and bounded contexts can react to them.

However, CDMS had **no guarantee that an event was emitted in the same database transaction as the change that produced it**. 
This could lead to:
- Events published for changes that were later rolled back
- Changes committed without their event ever being published
- Downstream services drifting out of sync with CDMS data

**Objective:**
Implement the **Transactional Outbox pattern** for CDMS: persist every event in an outbox table within the same transaction 
as the business change, and build a dedicated relay service that reliably forwards those events to the Central Event Bus 
with **at-least-once delivery**, ordering preserved and duplicates suppressed.

## My Role and Contributions
As the **lead engineer** on this initiative, I drove the investigation and design from the start and worked on both the 
producing side in CDMS and the new relay service. 
I collaborated closely with the other engineers in my team, the **Platform team** for infrastructure and deployment, 
and the internal **Event Streaming community** to align on event bus conventions.

### **Key Actions:**
- **Investigation & Design:** Led the design spikes that defined why CDMS needs an outbox, the outbox table model, 
  and the end-to-end architecture from CDMS to the Central Event Bus.
- **Architecture Decisions:** Chose **Change Data Capture on the MySQL binary log** over polling, giving near-real-time 
  delivery with no extra queries or locks on busy study databases.
- **CDMS Producer Side:** Implemented the outbox writes through a **command-bus decorator**, so the business change and the 
  intent to publish commit atomically, with events enriched and serialized on the producing side.
- **Relay Service:** Worked on a new **Go** service that connects to MySQL as a replication client and publishes outbox rows 
  to **NATS JetStream**, keeping the relay a simple, fast forwarder.
- **Delivery Guarantees:** At-least-once delivery via a binlog checkpoint in **NATS KV** that only advances after JetStream 
  acknowledges the publish, with message-ID based **deduplication** giving consumers effectively-once delivery.
- **Resilience:** Retries with exponential backoff and jitter, a circuit breaker, and poison-message handling so a single 
  bad event can't block the stream.
- **Safe Rollout:** Designed for a phased rollout: metrics-only mode first to validate connectivity, lag and resource 
  usage in production, then publishing enabled behind feature flags.

## Outcome and Impact
Although the project is still ongoing, the relay is already live in production:
- **Data Consistency:** CDMS events are now published with a **transactional guarantee**. Events are delayed, never lost, 
  during relay or event bus outages.
- **Production Rollout:** Publishing is live across all public-cloud installations, with **zero publish errors** and 
  **sub-second lag** in the post-rollout health check.
- **Performance:** Benchmarks showed the batched checkpoint design delivers roughly **2x the catch-up throughput** of 
  synchronous checkpointing.
- **Low Footprint:** Reading the binary log adds no load or locking on the study databases.
- **Foundation for Event-Driven Architecture:** Gives other teams a reliable stream of CDMS events to build on.

## Technologies and Tools
- **Backend:** Go, PHP
- **Database:** MySQL (binlog CDC)
- **Messaging:** NATS JetStream, NATS KV
- **Infrastructure:** Kubernetes, Helm, ArgoCD, GitHub Actions, Azure
- **Observability:** Datadog, Grafana, OpenTelemetry, Prometheus
- **Development Tools:** GoLand, PhpStorm, Git
- **Project Management:** Jira, Confluence
- **Communication:** Slack, Google Meet

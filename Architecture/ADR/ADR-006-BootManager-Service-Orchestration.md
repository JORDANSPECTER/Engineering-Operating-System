# ADR-006: BootManager Owns Platform Service Orchestration

- **Status:** Accepted
- **Date:** 2026-07-14
- **Decision owners:** Engineering Lane™

## Context

Cougar HQ now initializes runtime health, memory, AI workforce, enterprise graph, collection connectors, orchestration, and workers. Uncoordinated initialization creates hidden dependencies and inconsistent startup behavior.

## Decision

BootManager is the authoritative startup orchestrator. Services register defined startup stages, publish status, expose failures, and initialize in dependency order.

## Consequences

### Positive

- Creates deterministic startup.
- Makes service health visible.
- Centralizes dependency sequencing.
- Supports future recovery, degraded mode, and restart policies.

### Tradeoffs

- BootManager can become overly coupled if service boundaries are weak.
- Startup contracts require versioning and tests.
- Long-running initialization must not block the user interface indefinitely.

## Required controls

- explicit service names and stages;
- dependency declaration;
- timeout and failure state;
- health reporting;
- idempotent initialization where possible;
- structured boot events;
- degraded-mode behavior.


# ADR-003: Governed Intelligence Source Registry

- **Status:** Accepted
- **Date:** 2026-07-12
- **Decision owners:** Founder, Research Lane™, Sentinel Lane™, Executive Council™

## Context

Allowing agents to collect from arbitrary websites, APIs, feeds, or databases would introduce provenance, quality, security, legal, and operational risks.

## Decision

No external source may be used by Cougar agents until it is registered, evaluated, approved, assigned to an owning Lane, and authorized for specific collection purposes. The Intelligence Source Registry is the authoritative record for this governance.

## Consequences

### Positive

- Creates accountable source ownership.
- Supports source quality review and retirement.
- Reduces uncontrolled data ingestion.
- Enables agent-level authorization and auditing.

### Tradeoffs

- New sources require review before use.
- Emergency collection requires a governed exception path.
- Registry maintenance becomes an operational responsibility.

## Required source fields

- stable source ID;
- name and type;
- owner Lane;
- access method;
- approval status;
- authorized agents;
- permitted use cases;
- trust and quality rating;
- legal or licensing notes;
- review date;
- retirement status.


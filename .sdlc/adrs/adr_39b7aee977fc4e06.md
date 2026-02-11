---
id: adr_39b7aee977fc4e06
title: Use PostgreSQL for SDLC Pipeline and Artifact Storage
type: adr
status: proposed
decision_date: '2026-02-09'
related_adrs: []
related_requirements:
  - REQ-9780
  - REQ-1034
  - REQ-4834
created: '2026-02-09'
updated: '2026-02-09'
---

# Use PostgreSQL for SDLC Pipeline and Artifact Storage

## Context

The platform requires a reliable, scalable relational database for managing SDLC pipelines, stages, artifact versions, and audit logs.

## Decision

Use PostgreSQL as the primary persistent storage with support for JSONB columns to handle pipeline metadata and artifacts metadata.

## Rationale

PostgreSQL provides strong consistency, mature ecosystem, advanced indexing, and JSONB support for flexible schemas.

## Consequences

- Requires DB expertise
- Operational complexity for backups and scaling
- Improves complex query performance and analytics capabilities

## Alternatives

- MongoDB (NoSQL alternative)
- MySQL (less JSONB support)
- SQLite (not scalable for production)

## Diagram

```mermaid
graph LR
  Platform --> PostgreSQL[(PostgreSQL DB)]
```

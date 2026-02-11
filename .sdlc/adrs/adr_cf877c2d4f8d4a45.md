---
id: adr_cf877c2d4f8d4a45
title: Use ELK Stack for Centralized Logging and Monitoring
type: adr
status: proposed
decision_date: '2026-02-08'
related_adrs: []
related_requirements:
  - REQ-9618
  - REQ-3674
created: '2026-02-08'
updated: '2026-02-08'
---

# Use ELK Stack for Centralized Logging and Monitoring

## Context

Platform requires observability into system events and audit logs.

## Decision

Adopt Elasticsearch, Logstash, and Kibana (ELK Stack) for log aggregation and visualization.

## Rationale

ELK Stack is widely used for scalable log analytics and alerting.

## Consequences

- Operational overhead for ELK maintenance
- Need to ensure log pipeline is secured

## Alternatives

- Splunk
- Prometheus with Grafana

## Diagram

```mermaid
graph LR
  App --> ELK[(Elasticsearch, Logstash, Kibana)]
```

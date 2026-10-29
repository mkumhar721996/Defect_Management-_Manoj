---
id: ADR-0019
category: deployment_target
title: "Deployment target: Docker containers on Azure Container Apps, Phase 1 (MVP)\
  \ in Central India.\u2026"
status: accepted
superseded_by: null
component_id: null
decision: 'Docker containers on Azure Container Apps, Phase 1 (MVP) in Central India.
  Environments: Dev, QA, Staging, Prod. Database (Azure Database for PostgreSQL Flexible
  Server) and Blob Storage in Central India; attachments geo-replicated (GRS/GZRS)
  to South India. India-only data residency.'
evidence: "Human: 'Environments: Dev \u2192 QA \u2192 Staging \u2192 Prod'; earlier\
  \ 'India-only residency policy for Phase 1 ... GRS/GZRS'"
contested: true
alternatives_considered:
- 'Multi-region (active-passive or stack per region): deferred beyond the MVP phase'
consequences:
- No regional failover in Phase 1; a regional outage means downtime
- Data stays in Central India
---

## Context

Human: 'Environments: Dev → QA → Staging → Prod'; earlier 'India-only residency policy for Phase 1 ... GRS/GZRS'

## Decision

Docker containers on Azure Container Apps, Phase 1 (MVP) in Central India. Environments: Dev, QA, Staging, Prod. Database (Azure Database for PostgreSQL Flexible Server) and Blob Storage in Central India; attachments geo-replicated (GRS/GZRS) to South India. India-only data residency.

## Alternatives considered

- Multi-region (active-passive or stack per region): deferred beyond the MVP phase

## Consequences

- No regional failover in Phase 1; a regional outage means downtime
- Data stays in Central India

---
id: ADR-0027
category: cross_cutting
title: 'Cross-cutting: No cache in V1'
status: accepted
superseded_by: null
component_id: null
decision: No Redis or other cache component in V1; the load (50-100 concurrent users)
  is served from PostgreSQL. Dashboard caching can be revisited if the reporting NFRs
  are missed.
evidence: 'Human: ''No, not in V1'''
---

## Context

Human: 'No, not in V1'

## Decision

No Redis or other cache component in V1; the load (50-100 concurrent users) is served from PostgreSQL. Dashboard caching can be revisited if the reporting NFRs are missed.

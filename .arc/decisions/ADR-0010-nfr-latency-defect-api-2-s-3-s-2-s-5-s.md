---
id: ADR-0010
category: nfr
title: "NFR: Latency (Defect API) \u2014 < 2 s / < 3 s / < 2 s / < 5 s"
status: accepted
superseded_by: null
dimension: Latency
metric: response time (login / defect search / defect create-update / dashboard load)
threshold: < 2 s / < 3 s / < 2 s / < 5 s
component_id: comp_defect_api
needs_dedicated_tracking: true
evidence: 'Human: performance targets'
---

## Context

Human: performance targets

## Decision

response time (login / defect search / defect create-update / dashboard load): < 2 s / < 3 s / < 2 s / < 5 s

Applies to Defect API.

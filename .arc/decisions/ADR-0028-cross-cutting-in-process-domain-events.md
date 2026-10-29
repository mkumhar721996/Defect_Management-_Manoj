---
id: ADR-0028
category: cross_cutting
title: 'Cross-cutting: In-process domain events'
status: accepted
superseded_by: null
component_id: null
decision: Defect lifecycle events (created, assigned, fixed, reopened, closed) are
  published as in-process domain events inside the Defect API from day 1. Audit, reporting
  and notification modules subscribe to them with no direct dependencies. Only email
  and Teams jobs leave the process, via the Job Queue to the Notification Worker.
  Notifications are also stored in the database and shown in an in-app inbox.
evidence: 'Human: ''In-process domain events; only email/Teams jobs go via the queue;
  add in-app notifications'''
contested: true
alternatives_considered:
- 'All events published through Service Bus: more infrastructure than V1 needs'
- In-process events with email/Teams only and no in-app inbox
consequences:
- Event handlers run in the API process, so module boundaries must be kept clean for
  a later split
- Notification records are stored in the Relational Database
---

## Context

Human: 'In-process domain events; only email/Teams jobs go via the queue; add in-app notifications'

## Decision

Defect lifecycle events (created, assigned, fixed, reopened, closed) are published as in-process domain events inside the Defect API from day 1. Audit, reporting and notification modules subscribe to them with no direct dependencies. Only email and Teams jobs leave the process, via the Job Queue to the Notification Worker. Notifications are also stored in the database and shown in an in-app inbox.

## Alternatives considered

- All events published through Service Bus: more infrastructure than V1 needs
- In-process events with email/Teams only and no in-app inbox

## Consequences

- Event handlers run in the API process, so module boundaries must be kept clean for a later split
- Notification records are stored in the Relational Database

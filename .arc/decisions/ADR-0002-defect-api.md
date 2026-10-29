---
id: ADR-0002
category: component
title: Defect API
status: accepted
superseded_by: null
component_id: comp_defect_api
responsibility: 'Spring Boot 3 (Java 21) modular monolith with clean-architecture
  layers. Modules: Auth, User, Project, Defect (with tags, links to requirement/test
  case/build/release/sprint, comments and activity timeline), Workflow (states and
  transitions stored in the database, configurable per project), Attachment, Audit
  (field-level defect_history: field, old/new value, user, time, reason), Reporting/Dashboard,
  Notification; defect search and filter on PostgreSQL full-text search. Spring Security
  with JWT.'
kind: api_service
split_reason: 'Single API for all domains (start small); runtime separate from the
  browser client. Modules are internal, not separate services: the human rejected
  microservices for V1.'
talks_to:
- component_id: comp_relational_database
  interaction: sync
  evidence: 'Human: Database PostgreSQL'
- component_id: comp_attachment_storage
  interaction: sync
  evidence: 'Human: ''Attachment management'''
- component_id: comp_job_queue
  interaction: async
  evidence: 'Human: ''queued and sent by a background worker'''
evidence: 'Human: ''Start with a Modular Monolith'', ''Add Audit Trail as a Core Module'',
  ''Add Workflow Engine'', ''Add Defect Linking'', ''PostgreSQL Full Text Search is
  enough'', ''Add Search & Filter'', ''Add Defect Tags'', ''Add Activity Timeline'''
contested: true
alternatives_considered:
- 'Microservices (Auth, Defect, Project, Report services): rejected as overkill for
  V1, one team and one database'
consequences:
- One deployable and one database for V1
- Module boundaries must be kept clean so a split stays possible later
---

## Context

Human: 'Start with a Modular Monolith', 'Add Audit Trail as a Core Module', 'Add Workflow Engine', 'Add Defect Linking', 'PostgreSQL Full Text Search is enough', 'Add Search & Filter', 'Add Defect Tags', 'Add Activity Timeline'

## Decision

Spring Boot 3 (Java 21) modular monolith with clean-architecture layers. Modules: Auth, User, Project, Defect (with tags, links to requirement/test case/build/release/sprint, comments and activity timeline), Workflow (states and transitions stored in the database, configurable per project), Attachment, Audit (field-level defect_history: field, old/new value, user, time, reason), Reporting/Dashboard, Notification; defect search and filter on PostgreSQL full-text search. Spring Security with JWT.

Kept separate because Single API for all domains (start small); runtime separate from the browser client. Modules are internal, not separate services: the human rejected microservices for V1..

## Talks to

- **Relational Database** (sync) — Human: Database PostgreSQL
- **Attachment Storage** (sync) — Human: 'Attachment management'
- **Job Queue** (async) — Human: 'queued and sent by a background worker'

## Alternatives considered

- Microservices (Auth, Defect, Project, Report services): rejected as overkill for V1, one team and one database

## Consequences

- One deployable and one database for V1
- Module boundaries must be kept clean so a split stays possible later

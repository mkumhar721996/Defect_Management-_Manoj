---
id: ADR-0006
category: component
title: Job Queue
status: accepted
superseded_by: null
component_id: comp_job_queue
responsibility: Holds notification jobs between the Defect API and the Notification
  Worker; runs on Azure Service Bus (queue) in Central India.
kind: managed_service
split_reason: Backing service the project uses but does not build; decouples the API
  from the worker.
talks_to:
- component_id: comp_notification_worker
  interaction: async
  evidence: 'Human: ''queued and sent by a background worker'''
evidence: 'Human: ''Azure Service Bus queue + Azure Communication Services email'''
---

## Context

Human: 'Azure Service Bus queue + Azure Communication Services email'

## Decision

Holds notification jobs between the Defect API and the Notification Worker; runs on Azure Service Bus (queue) in Central India.

Kept separate because Backing service the project uses but does not build; decouples the API from the worker..

## Talks to

- **Notification Worker** (async) — Human: 'queued and sent by a background worker'

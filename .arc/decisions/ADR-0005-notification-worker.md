---
id: ADR-0005
category: component
title: Notification Worker
status: accepted
superseded_by: null
component_id: comp_notification_worker
responsibility: Consumes notification jobs from the Job Queue and sends email and
  Microsoft Teams messages for defect events; retries failed sends.
kind: worker
split_reason: Human chose notifications 'queued and sent by a background worker',
  keeping slow external calls off the API request path.
evidence: 'Human: ''Email + Teams, queued and sent by a background worker'''
---

## Context

Human: 'Email + Teams, queued and sent by a background worker'

## Decision

Consumes notification jobs from the Job Queue and sends email and Microsoft Teams messages for defect events; retries failed sends.

Kept separate because Human chose notifications 'queued and sent by a background worker', keeping slow external calls off the API request path..

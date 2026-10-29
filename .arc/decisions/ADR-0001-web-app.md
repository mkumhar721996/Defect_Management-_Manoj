---
id: ADR-0001
category: component
title: Web App
status: accepted
superseded_by: null
component_id: comp_web_app
responsibility: 'Browser UI for testers, developers, leads, managers and admins: defect
  create/assign/track, attachments, dashboards and reports; React + TypeScript + Material
  UI.'
kind: web_ui
split_reason: 'Separate client runtime (browser SPA); stack stated by the human: ''React,
  TypeScript, Material UI''.'
talks_to:
- component_id: comp_defect_api
  interaction: sync
  evidence: 'Human: React frontend with REST API backend'
evidence: 'Human: frontend React, TypeScript, Material UI'
---

## Context

Human: frontend React, TypeScript, Material UI

## Decision

Browser UI for testers, developers, leads, managers and admins: defect create/assign/track, attachments, dashboards and reports; React + TypeScript + Material UI.

Kept separate because Separate client runtime (browser SPA); stack stated by the human: 'React, TypeScript, Material UI'..

## Talks to

- **Defect API** (sync) — Human: React frontend with REST API backend

---
id: ADR-0024
category: cross_cutting
title: 'Cross-cutting: Audit logging'
status: accepted
superseded_by: null
component_id: null
decision: 'Append-only field-level history in the Relational Database (defect_history:
  field_name, old_value, new_value, updated_by, updated_on, reason) for defect creation,
  every field change, status transitions, assignments, comments, attachment actions
  and user management actions; also drives the defect activity timeline. Retained
  2 years.'
evidence: "Human: 'Every field change should be tracked', 'Priority changed P3 \u2192\
  \ P1 ... Reason: Production impact'; earlier 'Audit logs retained for 2 years'"
---

## Context

Human: 'Every field change should be tracked', 'Priority changed P3 → P1 ... Reason: Production impact'; earlier 'Audit logs retained for 2 years'

## Decision

Append-only field-level history in the Relational Database (defect_history: field_name, old_value, new_value, updated_by, updated_on, reason) for defect creation, every field change, status transitions, assignments, comments, attachment actions and user management actions; also drives the defect activity timeline. Retained 2 years.

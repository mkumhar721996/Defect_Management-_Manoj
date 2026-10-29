---
id: ADR-0008
category: nfr
title: "NFR: Scale - data volume (Relational Database) \u2014 100,000+ defects at\
  \ launch, growth to 1,000,000 without schema redesign; 500\u2026"
status: accepted
superseded_by: null
dimension: Scale - data volume
metric: defects stored; new defects per day; comments per defect
threshold: 100,000+ defects at launch, growth to 1,000,000 without schema redesign;
  500 new/day; ~10 comments each
component_id: comp_relational_database
needs_dedicated_tracking: true
evidence: 'Human: ''Defects stored: 100,000+'', ''Support growth to 1 million defects
  without schema redesign'''
---

## Context

Human: 'Defects stored: 100,000+', 'Support growth to 1 million defects without schema redesign'

## Decision

defects stored; new defects per day; comments per defect: 100,000+ defects at launch, growth to 1,000,000 without schema redesign; 500 new/day; ~10 comments each

Applies to Relational Database.

---
id: ADR-0003
category: component
title: Relational Database
status: accepted
superseded_by: null
component_id: comp_relational_database
responsibility: System of record for defects, users/roles, audit log and attachment
  metadata; runs on Azure Database for PostgreSQL Flexible Server in Central India.
kind: managed_service
split_reason: Backing service the project uses but does not build; managed by Azure.
evidence: 'Human: ''Database: Azure PostgreSQL Flexible Server'''
---

## Context

Human: 'Database: Azure PostgreSQL Flexible Server'

## Decision

System of record for defects, users/roles, audit log and attachment metadata; runs on Azure Database for PostgreSQL Flexible Server in Central India.

Kept separate because Backing service the project uses but does not build; managed by Azure..

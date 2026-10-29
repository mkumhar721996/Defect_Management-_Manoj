---
id: ADR-0023
category: cross_cutting
title: 'Cross-cutting: Role-based access control'
status: accepted
superseded_by: null
component_id: null
decision: 'Six roles: Admin, Project Manager, Lead, Developer, Tester, Viewer (Lead
  ranks between Developer and Project Manager). Users sign in via Microsoft Entra
  ID SSO; Entra group membership maps to roles. Defect API validates the Entra-issued
  JWT with Spring Security (resource server) and enforces permissions per role on
  defect actions and status transitions. Password complexity is enforced by Entra
  ID, as the system stores no passwords.'
evidence: 'Human: ''Lead is a sixth role, between Developer and Project Manager'';
  roles list in NFR answer'
contested: true
alternatives_considered:
- 'Defect API manages its own users and passwords: more code and credential risk,
  no SSO'
- 'Another corporate SSO provider (Okta, etc.): not the Azure-native choice'
consequences:
- No password storage in the system
- Role changes are made by editing Entra groups
- Web App and Defect API need Entra app registrations
---

## Context

Human: 'Lead is a sixth role, between Developer and Project Manager'; roles list in NFR answer

## Decision

Six roles: Admin, Project Manager, Lead, Developer, Tester, Viewer (Lead ranks between Developer and Project Manager). Users sign in via Microsoft Entra ID SSO; Entra group membership maps to roles. Defect API validates the Entra-issued JWT with Spring Security (resource server) and enforces permissions per role on defect actions and status transitions. Password complexity is enforced by Entra ID, as the system stores no passwords.

## Alternatives considered

- Defect API manages its own users and passwords: more code and credential risk, no SSO
- Another corporate SSO provider (Okta, etc.): not the Azure-native choice

## Consequences

- No password storage in the system
- Role changes are made by editing Entra groups
- Web App and Defect API need Entra app registrations

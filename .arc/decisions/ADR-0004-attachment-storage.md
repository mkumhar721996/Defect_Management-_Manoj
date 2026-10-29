---
id: ADR-0004
category: component
title: Attachment Storage
status: accepted
superseded_by: null
component_id: comp_attachment_storage
responsibility: Stores binary defect attachments (screenshots, logs); metadata lives
  in the Relational Database; runs on Azure Blob Storage in Central India, geo-replicated
  to South India (GRS/GZRS).
kind: managed_service
split_reason: Binary files do not belong in the relational database; separate managed
  backing service with different size/cost profile.
evidence: 'Human: ''Azure Blob Storage in Central India and geo-replicated to South
  India using GRS/GZRS'''
---

## Context

Human: 'Azure Blob Storage in Central India and geo-replicated to South India using GRS/GZRS'

## Decision

Stores binary defect attachments (screenshots, logs); metadata lives in the Relational Database; runs on Azure Blob Storage in Central India, geo-replicated to South India (GRS/GZRS).

Kept separate because Binary files do not belong in the relational database; separate managed backing service with different size/cost profile..

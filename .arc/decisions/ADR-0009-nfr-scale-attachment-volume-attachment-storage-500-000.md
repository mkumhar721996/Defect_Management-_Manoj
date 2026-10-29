---
id: ADR-0009
category: nfr
title: "NFR: Scale - attachment volume (Attachment Storage) \u2014 500,000 files,\
  \ ~2 MB avg, ~1 TB total; max 50 MB per file; allowed types PNG\u2026"
status: accepted
superseded_by: null
dimension: Scale - attachment volume
metric: files stored; average size; total; max file size
threshold: 500,000 files, ~2 MB avg, ~1 TB total; max 50 MB per file; allowed types
  PNG, JPG, PDF, ZIP, LOG, MP4
component_id: comp_attachment_storage
needs_dedicated_tracking: true
evidence: 'Human: attachment workload and storage list'
---

## Context

Human: attachment workload and storage list

## Decision

files stored; average size; total; max file size: 500,000 files, ~2 MB avg, ~1 TB total; max 50 MB per file; allowed types PNG, JPG, PDF, ZIP, LOG, MP4

Applies to Attachment Storage.

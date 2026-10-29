# ADR Index

One line per decision — the rule, not the reasoning. Read the full ADR (`.arc/decisions/ADR-NNNN-*.md`) for context and rationale.

| ADR | Category | Status | Title |
|---|---|---|---|
| ADR-0001 | component | accepted | Web App |
| ADR-0002 | component | accepted | Defect API |
| ADR-0003 | component | accepted | Relational Database |
| ADR-0004 | component | accepted | Attachment Storage |
| ADR-0005 | component | accepted | Notification Worker |
| ADR-0006 | component | accepted | Job Queue |
| ADR-0007 | nfr | accepted | NFR: Scale - users — 500 / 150 / 50 / 100 |
| ADR-0008 | nfr | accepted | NFR: Scale - data volume (Relational Database) — 100,000+ defects at launch, growth to 1,000,000 without schema redesign; 500… |
| ADR-0009 | nfr | accepted | NFR: Scale - attachment volume (Attachment Storage) — 500,000 files, ~2 MB avg, ~1 TB total; max 50 MB per file; allowed types PNG… |
| ADR-0010 | nfr | accepted | NFR: Latency (Defect API) — < 2 s / < 3 s / < 2 s / < 5 s |
| ADR-0011 | nfr | accepted | NFR: Throughput (Defect API) — 100 |
| ADR-0012 | nfr | accepted | NFR: Availability — 99.5% (~3.6 h/month downtime); maintenance Saturdays 23:00-02:00 IST with 24 h… |
| ADR-0013 | nfr | accepted | NFR: Recovery — RPO 15 minutes / RTO 1 hour |
| ADR-0014 | nfr | accepted | NFR: Backup — Automated daily backup, retained 30 days |
| ADR-0015 | nfr | accepted | NFR: Data retention — Defects 7 years; audit logs 2 years |
| ADR-0016 | nfr | accepted | NFR: Session timeout (Web App) — 30 minutes |
| ADR-0017 | nfr | accepted | NFR: Data residency — Only Indian Azure regions: Central India (primary), South India (attachment… |
| ADR-0018 | nfr | accepted | NFR: Attachment durability (Attachment Storage) — GRS/GZRS from Central India to South India |
| ADR-0019 | deployment_target | accepted | Deployment target: Docker containers on Azure Container Apps, Phase 1 (MVP) in Central India.… |
| ADR-0020 | integration_surface | accepted | Integration: Microsoft Entra ID (bidirectional) |
| ADR-0021 | integration_surface | accepted | Integration: Email Provider (outbound) |
| ADR-0022 | integration_surface | accepted | Integration: Microsoft Teams (outbound) |
| ADR-0023 | cross_cutting | accepted | Cross-cutting: Role-based access control |
| ADR-0024 | cross_cutting | accepted | Cross-cutting: Audit logging |
| ADR-0025 | cross_cutting | accepted | Cross-cutting: Modular clean architecture |
| ADR-0026 | cross_cutting | accepted | Cross-cutting: Single-organisation tenancy |
| ADR-0027 | cross_cutting | accepted | Cross-cutting: No cache in V1 |
| ADR-0028 | cross_cutting | accepted | Cross-cutting: In-process domain events |

# ClankerOffice: Open Enterprise Productivity and Auditability

Status: **proposed architecture**, not implemented or deployed. Companion to ClankerWorks operations proposal in draft PR #13. No third-party software is bundled or licensed by this document.

## Goal
Offer an integrated, interoperable workplace computing environment built on established open-source software, open document formats, documented APIs, portable data, and inspectable business decisions. Avoid unnecessary reinvention and vendor lock-in.

## Candidate building blocks (evaluate before adoption)
| Domain | Candidates | Integration considerations |
|---|---|---|
| Desktop office | LibreOffice | Prefer active maintenance and OpenDocument formats; verify compatibility needs |
| Browser editing | Collabora Online | Document permissions, collaborative edits, deployment and licensing |
| Files and collaboration | Nextcloud | File history, sharing, retention, SSO |
| Operational databases | PostgreSQL | Schema migrations, row-level access, backup/recovery, audit events |
| Local/offline data | SQLite | Sync conflict strategy, encrypted storage where needed |
| BI and analytics | Apache Superset / Metabase | Curated views; never unrestricted access to personnel records |
| Wiki | BookStack / Wiki.js | Versioned policies, accountable edits |
| Identity | Keycloak | SSO, separate personas, least privilege, role changes |
| Source control | Forgejo / GitLab | Signed changes, review, CI, software provenance |
| Workflow | Temporal or comparable engine | Durable state transitions, approvals, event history |

These are candidates, not endorsements or assertions of compatibility. Review project license, support, accessibility, maintenance, data residency, threat model and operational cost before selection.

## Integration contract
- Use OpenDocument (ODT/ODS/ODP) as first-class editable formats, with exports where necessary.
- Use stable versioned APIs and documented event schemas; avoid spreadsheet files as the authoritative transactional database.
- Use single sign-on with distinct employee, contractor and carrier identities; enforce access per purpose.
- Give employees permission-scoped access to their own production history and explanations, with exports.
- Support offline or degraded operation only where consistency and security rules are explicit.
- Connect ClankerMetrics to curated read-only analytics views; employee-created spreadsheets must not grant extra access.
- Record document edits, approvals, formula/model versions, data lineage, retention rules and access events proportionately.
- Maintain independent financial approval and separation of duties.

## Auditability contract
For consequential operations record actor, identity/persona, authority, timestamp, object, before/after or immutable event, reason, source data, policy version, approval chain, and corrections. Preserve append-only evidence where warranted, but do not promise absolute immutability without a designed storage and trust model. Sensitive personal data is protected, not made globally visible. Audit-log access is itself logged.

## Employee workflow example
Employee reviews own ClankerMetrics → exports authorized data to an ODS workbook → analyzes trends in LibreOffice or browser editor → cites a reproducible report and proposes process improvement → review records rationale and decision → approved change links to implementation and measured outcome.

## Synthetic validation plan
1. User can edit and export ODS without changing underlying production records.
2. Identity switch does not leak employee data to carrier persona.
3. Unauthorized coworker cannot query another employee's raw metrics through BI or shared workbook.
4. An approved process change links its document, data source, policy version, reviewer and outcome.
5. Rejected proposal and later corrections remain auditable.
6. Restore test proves documents, database and audit events are recoverable together.

## Open questions
Choose initial deployment footprint, office collaboration model, licensing and support strategy, data classification, document retention, audit tamper-evidence design, and preferred analytics stack. Preserve all other ZeroCloud draft PRs.

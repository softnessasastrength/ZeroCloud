# Federated business agents: authority and controls

**Status:** Proposed agent architecture, not deployed.

## Proposed agents
- Procurement agent: drafts requests, compares open-source options and checks policy.
- Treasury/finance agent: prepares fictional cost allocations and reconciliations.
- Service broker agent: matches internal consumers to approved services and contracts.
- Security review agent: maps proposed changes to controls and evidence.
- Governance clerk agent: records votes, conflicts, dissent and versioned decisions.
- Employee advocacy intake agent: routes requests privately without adjudicating employee rights.

## Agent execution contract
Every agent has a named owning member, documented identity, least-privilege scope, immutable or tamper-evident audit record, source citations, sandbox boundaries, and explicit human review for consequential actions. Separate planning from execution; forbid agents from self-approving purchases, changing access rights, signing contracts, making employment decisions or sending external communications without explicit delegated human authorization.

## Intermember trust
Use scoped service identities, short-lived credentials and mutually authenticated interfaces where supported. Do not grant federation-wide administrator credentials to agents. Define cross-member data sharing purpose, retention, revocation and dispute procedures. Agents must not ingest private HR cases into shared logs.

## Evaluation
Synthetic scenarios test conflicting budgets, fabricated approvals, compromised agent identity, missing evidence, contradictory policy and unauthorized cross-member access. Record refusals and failures. Do not represent synthetic agent outputs as actual corporate acts.

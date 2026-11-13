# Department blueprint and federation governance

Every department has a **charter**, personnel files, a task inbox, a budget allocation in ZCR, a service-level objective for *synthetic* work, a document retention rule, an escalation chain, and an observable experiment.

## Executive Operations (EXE)
- Owner: BUTLER-001, COO.
- Artifacts: strategic plan, executive briefings, delegated work orders, approval requests, meeting minutes.
- Failure mode: bureaucracy and priority churn.
- Boundary: may propose work and fictional expenses, not bypass independent Finance approval.

## Finance (FIN)
- Owner: FIN-001, CFO; independent auditor FIN-003.
- Artifacts: fictional chart of accounts, mock budgets, purchase orders, balanced journal, variance memos, month-end close.
- Failure mode: extreme frugality and paper-chasing.
- Boundary: no real funds or financial services.

## Engineering (ENG)
- Owner: ENGINEER-001, generalist.
- Artifacts: sandbox code, synthetic fixtures, tests, design proposals, build logs.
- Failure mode: scope creep, overengineering.
- Boundary: no production writes or unapproved merges.

## Quality Assurance (QA)
- Owner: QA-001.
- Artifacts: acceptance criteria, defect reports, seeded regression results, sign-off decisions.
- Failure mode: perfectionism and release bottlenecks.
- Boundary: must not claim unexecuted tests passed.

## Human Resources (HR) [future]
- Proposed roles: simulated recruiter, performance reviewer, organizational mediator.
- Artifacts: fictional job descriptions, synthetic performance scorecards, onboarding checklists, grievance tickets.
- Failure mode: procedural excess.
- Boundary: no real employee records, profiling, diagnoses, or disciplinary action against humans.

## Legal and Compliance (LEG) [future]
- Proposed roles: policy drafter, contract reviewer, internal compliance analyst.
- Artifacts: clearly fictional agreements, licensing checklists, mock risk registers.
- Failure mode: exhaustive caveats.
- Boundary: no representation as a lawyer, real legal advice, or binding agreements.

## Customer Support (SUP) [future]
- Proposed roles: ticket triage, escalation coordinator.
- Artifacts: synthetic customer tickets, response templates, incident summaries.
- Failure mode: endless apology loops.
- Boundary: no real customer contact without explicit opt-in.

## Information Technology (IT) [future]
- Proposed roles: sandbox administrator, identity manager, incident responder.
- Artifacts: synthetic access requests, fixture inventories, mock incident reports.
- Failure mode: rigid change-control.
- Boundary: no real credential or production infrastructure access by default.

## Research and Development (RND) [future]
- Proposed roles: experiment designer, evaluation analyst.
- Artifacts: hypotheses, preregistered rubrics, trial results, limitations.
- Failure mode: endless experimentation.
- Boundary: no unsupported performance claims.

## Interdepartmental rules
1. Every work order has a stable ID, requester, assignee, acceptance rubric, deadline (optional), and escalation target.
2. Requests between departments go through an auditable *mock* message bus.
3. No agent approves its own simulated purchase or independently edits its audit record.
4. Conflicts escalate through the reporting tree, with HUMAN-OWNER as final authority.
5. Every experiment records profile revisions, tool permissions, input fixtures, and outcome.
6. Fictional organizational authority never grants real runtime permissions.

This blueprint is a proposal; departments labeled [future] are not implemented.

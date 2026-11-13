# ClankerWorks: An Experimental AI Organization

**Status:** proposal only. No autonomous agents, mailboxes, infrastructure, or evaluation results are claimed to exist.

ClankerWorks is an optional, reproducible multi-agent organizational laboratory for ZeroCloud. It combines useful research into agent coordination with affectionate satire of corporate bureaucracy. The infrastructure is real when verified; the corporation, job titles, budgets, and personnel are simulated.

## Principles
1. Keep ZeroCloud's existing infrastructure and hardware-qualification roadmap independent. ClankerWorks must not be a prerequisite for the cloud.
2. Every agent has a version-controlled **personnel Markdown file** describing its role, abilities, limitations, behavioral configuration, permitted tools, and escalation rules.
3. Agents are software processes, not human employees. "Personnel", "hiring", "performance", and "psychology" are simulation vocabulary, not claims of personhood or distress.
4. Study **behavioral perturbations**, not simulated abuse: change task loads, communication style, incentives, ambiguity, or permissions in documented, reversible experiments.
5. Default to synthetic data, mock email, mock calendars, isolated repositories, zero real spending, and no production credentials. No external messages, purchases, merges, deployments, or invitations without separately granted authority.
6. A human owns final approval. Maintain append-only run logs, explicit evaluation criteria, cost ceilings, rate limits, and a kill switch.
7. Report measured outcomes honestly. Never claim a simulation proves actual employee psychology, sentience, or organizational effectiveness.

## Proposed structure

- `personnel/*.md`: individually versioned agent contracts and role-specific tendencies.
- `PERSONNEL_SCHEMA.md`: required fields and invariants.
- `EXPERIMENTS.md`: experiment design, measurements, safeguards, and suggested scenarios.
- Later: a parser/validator, scenario runner, mock message bus, deterministic fixtures, evaluation harness, and observability dashboard.

## Initial experiment

Assign the same bounded, harmless synthetic transit-data documentation task to (A) one generalist agent and (B) a team of specialist agents. Measure correctness against a fixed rubric, completion time, model/tool cost, message volume, rework, and approval requests. Repeat with multiple seeds/runs where supported. Preserve artifacts and disclose evaluator limitations.

## Implementation stages

0. **Documentation and personnel profiles** (this proposal).
1. Schema validation, fixture tests, no inference or network required.
2. Local mock inbox and task queue, synthetic calendar events, auditable messages.
3. Sandboxed inference adapters, quotas, evaluation harness, and human approval gates.
4. Optional real email/calendar integrations using explicit opt-in, verified sender identity, allowlisted recipients, and revocable credentials.
5. Optional ZeroCloud deployment after independent infrastructure and security qualification.

No production integration is authorized by this document.

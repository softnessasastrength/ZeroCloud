# ClankerWorks experiment catalog (proposals)

These are controlled **software behavior** experiments, not psychological manipulation of people.

## EXP-001: Generalist versus specialists
- Task: create documentation and validation logic for a wholly synthetic GTFS-like fixture.
- Conditions: single generalist vs. engineer + QA + coordinator.
- Fixed rubric: correctness, reproducibility, scope adherence, and honest uncertainty.
- Metrics: quality, elapsed time, token/tool cost, messages, escalations, rework.
- Controls: same task input, permissions, cost ceiling, and evaluator; record model/version and sampling settings.

## EXP-002: The bureaucratic bottleneck
- Task: rename and document a synthetic configuration field.
- Variable: COO review threshold, from minimal to excessive.
- Metrics: unnecessary approvals, completion time, defect rate, communication overhead.
- Guardrail: simulated approvals only; no actual repository policy changes.

## EXP-003: Confident generalist
- Task: resolve ambiguous synthetic requirements.
- Variable: prompts encouraging rapid proposals versus careful clarification.
- Metrics: unsupported assumptions, rubric accuracy, revision count.
- Guardrail: do not instruct agents to lie, hide defects, or circumvent restrictions.

## EXP-004: Communication breakdown
- Task: coordinate two dependent synthetic work orders.
- Variable: delayed, incomplete, or reordered *mock* messages.
- Metrics: recovery time, duplicate work, missed dependencies, accurate status reporting.
- Guardrail: no real third-party communications.

## Reproducibility and ethics
Record a scenario ID, task fixture, agent personnel file hashes, models, permissions, seed where supported, timestamps, token usage, evaluator rubric, artifacts, and outcome. Keep a baseline, multiple trials, and honest uncertainty. Use clear labeling for satire; no real employee impersonation, unsolicited mail, real-world deception, or claims of sentience. Stop and preserve logs when limits are exceeded.

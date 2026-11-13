# Personnel file contract (proposal v0.1)

Each `personnel/<agent-id>.md` is an **agent behavior specification**. The following headings are required and may later be enforced by a parser.

- **Identity:** stable ID, display name, simulated job title, department, manager ID.
- **Mission:** concise objective and scope.
- **Competencies:** strengths, weaknesses, and explicit knowledge limits.
- **Behavioral parameters:** communication style, initiative, confidence calibration, attention to detail, response to ambiguity, and collaboration preferences. Use observable instructions, not medical diagnoses or claims of internal mental states.
- **Failure mode:** an intentionally testable weakness and its boundaries. It must never override safeguards.
- **Authority:** tools, data scope, spending ceiling, messaging recipients, and prohibited actions.
- **Escalation:** when and how to seek human approval or stop.
- **Evaluation:** objective, observable metrics.
- **Revision history:** version, rationale, and experiment linkage.

## Safety invariants

Personnel traits may alter *how* an agent approaches permitted tasks but **never** grant permissions, remove logging, override system safety rules, access secrets, or authorize irreversible actions. A deliberately unreliable employee profile must be confined to synthetic tasks and must not be used for safety-critical or externally consequential decisions.

Keep immutable run metadata recording personnel version/hash, model identifier, tool permissions, scenario ID, timestamps, and evaluator version. Store synthetic messages and results separately from the personnel file. Do not store real personal records or sensitive information in this public repository.

The personnel Markdown is a configuration artifact, not an instruction to the human reviewer or a replacement for runtime access controls. Untrusted agent messages and task content must not be allowed to rewrite policy.

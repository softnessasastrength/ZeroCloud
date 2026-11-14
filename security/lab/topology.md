# Authorized security laboratory

**Status:** Design-only. The lab is not yet deployed.

## Purpose
Translate concepts learned from Hack The Box into repeatable defensive validations against intentionally vulnerable, owned targets.

## Proposed lab segments
- lab-control: orchestrator, artifacts, synthetic identity provider.
- lab-targets: disposable Linux VMs/containers with seeded vulnerabilities.
- lab-sensors: traffic mirror, logs, detection and alert processing.
- lab-operator: authenticated test operator and tooling.

## Isolation
- Default-deny lab egress and deny routes to ZeroCloud admin/control/workers and home networks.
- No public targets, credential harvesting against third parties, or tests outside explicitly authorized systems.
- Synthetic users, tokens, domains, and customer data only.
- Destroy/reset targets between runs; log test scope and approvals.
- Avoid publishing real secrets or exploit artifacts that could target unrelated systems.

## Scenarios
1. Failed privileged login burst -> expected authentication event and detection.
2. Unauthorized service-to-service connection -> expected network denial and telemetry.
3. Privilege escalation attempt on deliberately vulnerable disposable VM -> expected host event and response.
4. Malicious dependency in a synthetic build fixture -> expected SBOM/policy rejection.
5. Expired/revoked service certificate -> expected failed authentication and audit record.
6. Simulated compromised workload -> expected denial of cross-zone access.

Each scenario needs a setup, expected event schema, positive and negative assertions, cleanup, and redacted evidence manifest.

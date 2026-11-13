# Security testing and evidence contract

## Test layers
1. Static: schema, configuration, YAML/JSON, policy lint, secret scanning.
2. Unit: authorization rules, parsers, policy evaluation and detection logic.
3. Integration: isolated VMs/containers, identity and certificate lifecycle, network boundaries.
4. Purple team: synthetic adversary replay with expected detections and explicit negatives.
5. Recovery: backups, restore, revocation, containment and post-incident reconstruction.
6. Hardware: rerun relevant controls on each qualified SBC and pinned K3s release.

## Evidence manifest
Each run records:
- control_id, scenario_id, test version, commit SHA, timestamp (UTC)
- environment ID, OS/kernel/K3s versions, hardware/virtualization, network topology
- expected result, actual result, pass/fail, redacted logs and artifacts
- operator or CI identity, evidence hash, retention and privacy classification

## Promotion gates
proposed -> specified: threat, owner role, normative requirements, test criteria.
specified -> implemented: versioned config/code exists.
implemented -> tested: repeatable test executed with retained evidence.
tested -> verified: independent review and passing relevant negative tests.

A missing test is NOT a pass. A passing synthetic test is NOT proof of production security. Never claim compliance certification without external authority and evidence.

## CI stages (planned)
- Documentation/link/schema lint
- Dependency/license/SBOM check
- Secrets detection
- Control registry referential integrity
- Offline synthetic fixture tests
- Isolated integration tests on dedicated runners (later)
- Hardware-in-loop tests on qualified devices (later)

Do not run adversary exercises on public GitHub-hosted runners or uncontrolled networks.

# Federation dogfooding and bootstrap strategy

**Status:** Proposed implementation plan; no services deployed.

## Internal customer chains
- Systems consumes Compute hosting for collaboration and identity services.
- Compute consumes Security telemetry and Research hardware qualification.
- People consumes Systems identity and documents, with privacy isolation.
- Business Services brokers internal contracts and fictional chargeback.
- Every member consumes the governance registry and independent dispute channel.

## Hard requirement
Each service must have an internal customer, owner, documented interface, dependency graph, deployment recipe, acceptance test, backup/exit plan and evidence-based maturity label.

## Bootstrap paradox
Identity, Git hosting, DNS, monitoring and recovery cannot all depend on the unbootstrapped ZeroCloud cluster. Define an external/bootstrap management plane, offline recovery credentials, signed configuration snapshots and tested migration path before claiming full dogfooding.

## Stages
1. Specification-only contracts and dependency graph.
2. Synthetic internal transactions and agent decision fixtures.
3. Isolated local service deployment using upstream open-source components.
4. Security/identity integration and portability tests.
5. Qualified SBC-backed K3s pilot, with Dell control plane.
6. Independent replication by community contributors and documented deviations.

## Evidence tiers
fictional -> specified -> implemented -> lab-verified -> hardware-verified -> operational. No stage is claimed complete solely by documenting it.

## Fictional stress test
ZeroCloud Security refuses to approve Compute's rushed rollout. Compute argues that the Security Council is abusing federation authority. Business Services reports budget damage; Systems worries about a circular identity dependency; People challenges an employee schedule change during the incident. Produce each member's written position and a minority opinion. No outcome predetermined.

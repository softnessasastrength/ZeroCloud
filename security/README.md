# ZeroCloud Security Engineering Division

**Decision 009: Accepted, Option D: Full-spectrum security engineering.**

ZeroCloud is an openly fictional corporation. Its engineering artifacts are intended to be technically reproducible. No security control, certification, employee, customer, or deployed service is implied by this specification.

## Responsibilities
- Office of the CISO: governance, risk acceptance, standards, security architecture.
- SOC / blue team: hardening, monitoring, alert triage, response.
- Red team: authorized isolated adversary simulation.
- Purple team: replay, detection engineering, control verification.
- Identity / PKI: SSO, MFA, service identity, certificates and revocation.
- AppSec / supply chain: threat modeling, code review, SBOM, dependency integrity.
- GRC / internal audit: control traceability, evidence, audits, exceptions.
- Recovery: backups, restore drills and incident continuity.

## Architectural invariants
1. Preserve hybrid Dell R630 control plane, managed wired Ethernet, K3s, stock-agent qualification, standardized SBC reference fleet, and later heterogeneous expansion.
2. Separate admin, provisioning, workers, control, services, and isolated adversary lab trust zones.
3. Default deny; explicitly document each allowed flow.
4. Trusted workloads only until tenant isolation has been independently verified.
5. Every policy points to a versioned configuration, test, and evidence artifact.
6. No unsupported claims of five nines, compliance certification, or security effectiveness.
7. Use open-source-first software with license/provenance review. Public docs never include real secrets or private employer materials.

See architecture.md, controls/registry.yaml, lab/topology.md, testing.md and implementation-plan.md.

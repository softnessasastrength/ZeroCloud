# Security division implementation roadmap

## SEC-0: Governance and scope
- [x] Record Decision 009 (full-spectrum security philosophy).
- [ ] Approve charter, control IDs, review/exception policy.
- [ ] Confirm public repository disclosure and secret-handling policy.
- [ ] Choose whether to establish separate repositories or keep monorepo.

## SEC-1: Specification as code
- [ ] JSON Schema for controls and evidence manifests.
- [ ] Validate controls registry in CI.
- [ ] Build trust boundary data model and allowed-flow matrix.
- [ ] Create security threat models for control plane, workers, admin and supply chain.

## SEC-2: Disposable security lab
- [ ] Define VM/container topology and deny-by-default egress.
- [ ] Synthetic identity and log fixture generator.
- [ ] First three attack/detection scenarios with negative assertions.
- [ ] Reproducible teardown and evidence capture.

## SEC-3: Defensive implementation
- [ ] Host hardening baseline, SSH, auditing and patching.
- [ ] Identity, MFA, PKI and secret rotation.
- [ ] K3s admission, CNI enforcement verification and RBAC.
- [ ] Telemetry pipeline and detection rules.

## SEC-4: Operational readiness
- [ ] Incident triage and severity model.
- [ ] Vulnerability disclosure and coordinated remediation process.
- [ ] SBOM, artifact signing and dependency update policy.
- [ ] Restore drills, chaos exercises and tabletop reports.

## SEC-5: Community conformance
- [ ] Versioned conformance suite for independent implementations.
- [ ] Hardware-specific qualification profiles.
- [ ] Community evidence submissions with privacy review.
- [ ] Publish verification dashboard clearly distinguishing simulated vs hardware-tested vs production-observed.

No boxes imply actual infrastructure deployment. Work in separate draft PRs; do not merge without review.

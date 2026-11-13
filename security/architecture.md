# Security architecture: trust boundaries and control planes

**Status: Proposed, not deployed.**

## Zones
- VLAN 10 / 10.77.10.0/24: control plane; Dell R630 K3s server, ZeroCloud API/controllers, database.
- VLAN 20 / 10.77.20.0/24: SBC workers; agent-to-server communication and explicitly approved service flows.
- VLAN 30 / 10.77.30.0/24: service ingress.
- VLAN 40 / 10.77.40.0/24: admin access through authenticated gateway.
- VLAN 50 / 10.77.50.0/24: short-lived provisioning/bootstrapping.
- Security lab: isolated VLAN or virtual bridge; separate address plan, default-deny to all operational segments. Do not assume a VLAN alone is sufficient isolation.

The network policy enforcement point must be a verified VLAN-aware firewall/router. Switch ACLs and host firewall rules provide defense in depth. Verify CNI support before relying on Kubernetes NetworkPolicy. K3s server and agent requirements, including ports, must be derived from the **pinned release** and tested rather than copied blindly.

## Identity and PKI
- Candidate: Keycloak for human SSO and MFA; design must include emergency access, recovery and account lifecycle.
- Dedicated workload identities; no shared root tokens.
- Candidate: OpenBao for secrets; no plaintext secrets in Git or images.
- Offline root CA, scoped intermediate issuers, documented certificate inventory, rotation and revocation testing.
- Explicit RBAC mapping for each ZeroCloud API action.

## Endpoint and workload protection
- Reproducible Linux baselines; SSH key authentication, least privilege, patch lifecycle, audit logging.
- Kubernetes restricted admission, image provenance, non-root containers, resource bounds, seccomp, dropped capabilities, and restricted host mounts where feasible.
- No hostile multi-tenancy promise on K3s/SBC workers; namespaces are not a hard tenant isolation boundary.

## Observability
- Candidates: Wazuh, Suricata, Zeek, OpenSearch; select only after resource and license review.
- Keep heavyweight analytics off memory-constrained SBCs; use collectors where feasible and analyze centrally.
- Protect log integrity, timestamps, retention, access control, and privacy.

## Open risks
- R630 inventory and OS are unverified.
- Hardware, network switch, firewall and SBC OS/K3s compatibility unverified.
- No confirmed CNI policy enforcement.
- No selected storage topology or tested backup strategy.
- No confirmed trust boundary between arbitrary customers; initially trusted lab workloads only.

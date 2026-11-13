# Internal service catalog and dogfooding roadmap

**Status:** Proposed; no deployments or contracts verified.

| Provider | Fictional internal customer | Service | First acceptance evidence |
| --- | --- | --- | --- |
| ZeroCloud Compute | ZeroCloud Systems | Kubernetes-backed application hosting | Repeatable deployment and recovery |
| ZeroCloud Systems | ZeroCloud People | Open-source collaboration and document management | Identity integration and access-control tests |
| ZeroCloud Security | ZeroCloud Compute | Security telemetry and incident triage | Synthetic detection and evidence manifests |
| ZeroCloud Research | ZeroCloud Compute | SBC qualification | Reproducible benchmark and hard-gate results |
| ZeroCloud Business Services | All companies | Procurement request workflow | Auditable fictional approvals and rejection tests |
| ZeroCloud People | All companies | Complaint intake and independent review | Fictional case lifecycle and conflict screening |

## Bootstrap rule
The first deployment cannot depend on services that only exist after the deployment. Document external bootstrap dependencies, recovery credentials and failure domains explicitly.

## Service maturity labels
- fictional: story artifact only
- specified: architecture and acceptance criteria exist
- implemented: code/config exists
- lab-verified: isolated tests passed with evidence
- hardware-verified: physical target tested with evidence
- operational: ongoing observed service with measured reliability

Do not promote maturity without evidence.

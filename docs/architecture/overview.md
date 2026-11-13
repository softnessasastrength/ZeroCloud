# ZeroCloud architecture (proposed)

## Mission

Build a genuinely functional, small-scale, AWS-inspired cloud with original satirical branding, explicit technical limitations, and reproducible evidence.

## Control plane

- Dell PowerEdge R630, intended Debian 13 minimal amd64 host (OS not verified).
- K3s server, API/controllers, web console, account/project identity, PostgreSQL, metering and monitoring are planned.
- Customer workloads must not be scheduled onto the R630.
- Actual R630 CPU, RAM, disks, NICs, controller and power configuration require inventory.

## Workers

- SBCs run pinned stock K3s agents and ARM64 workloads.
- Select a reference board through a hardware tournament, then pilot three identical nodes.
- Heterogeneous instance families are a later phase, contingent on hardware qualification.
- Proposed experimental sizes: z.nano 100m CPU / 48Mi request / 64Mi limit; z.micro 250m / 96Mi / 128Mi; z.small 500m / 192Mi / 256Mi. **Not validated** and may not fit constrained boards.
- Instances are initially single-replica Kubernetes workloads; stop scales to zero, terminate removes managed resources. Meter by stable instance ID, not ephemeral pod ID.

## Networking

- Managed wired Ethernet and a router/firewall enforcing segmentation.
- Proposed VLAN 10 control 10.77.10.0/24; VLAN 20 workers 10.77.20.0/24; VLAN 30 services 10.77.30.0/24; VLAN 40 admin 10.77.40.0/24; VLAN 50 provisioning 10.77.50.0/24.
- Addresses are illustrative, not deployed. Switch ports, power budgets and USB Ethernet compatibility require verification.
- Three logical zones in a single region us-desk-1 (7/7/6 for a hypothetical 20-node fleet) are **not independent physical failure domains**.

## Security boundaries

- Initial deployment is for trusted workloads, not adversarial multi-tenant execution.
- Require verified network-policy enforcement, restricted pod admission, least privilege, secret handling, and tested backups before exposing services.
- No uptime or durability promises without monitoring and evidence.

## Open decisions

Storage topology; hardware certification scope (Decision 008); reference board; provisioning mechanism; tenant isolation; external ingress; disaster recovery validation.

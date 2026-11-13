# SBC hardware qualification protocol (draft)

**Purpose:** Select a standardized reference SBC using published evidence rather than intuition or marketing.

## Candidate shortlist (proposed, not purchased)

1. Raspberry Pi Zero 2 W (512 MiB RAM)
2. Raspberry Pi 4 Model B (4 GB)
3. Raspberry Pi 5 (4 GB)
4. Orange Pi 5 (8 GB)

Confirm precise SKU, board revision, pricing, power supply, storage, thermal requirements, OS image, and Ethernet path before testing.

## Hard eligibility gates

- ARM64 Linux boots reliably and exposes required cgroup/kernel capabilities.
- Wired network reconnects following reboot.
- Pinned, unmodified K3s agent joins the R630-hosted cluster and stays Ready for 30 minutes.
- 24-hour idle operation without unexpected restart or OOM.
- ARM64 workload runs for 60 minutes with measured available headroom; 32 MiB is an **experimental threshold**, not a guarantee.
- Reboot, network failure, and node rejoin recover as specified.
- Repeat qualification on a second physical board before fleet approval.

Failure of stock K3s is an explicit decision checkpoint; no unrecorded substitution of runtimes or unsupported hacks.

## Benchmarks

Cold/warm container start, sustained CPU, memory pressure, network latency/throughput, storage latency/IOPS, scheduling latency, power draw, thermal throttling, and recovery. Use at least five measured repetitions after warm-up. Document OS/kernel/K3s versions, power supply, cooling, storage medium, network path, ambient conditions, and raw results.

After compatibility, run a 72-hour mixed workload endurance trial.

## Weighted score (proposed)

| Category | Weight |
|---|---:|
| K3s reliability | 25% |
| Usable compute capacity | 20% |
| Total system cost | 20% |
| Energy efficiency | 15% |
| Linux maintainability | 10% |
| Networking and storage | 10% |

Each category receives a published normalized 0–100 score. Eligibility gates override rankings. Publish separate lowest-qualified-cost and highest-weighted-score results. Freeze scoring before measuring.

## Integrity

No benchmarks have been run. No board is certified. Publish failures and raw evidence; never fabricate uptime, prices, benchmark scores, or availability.

# ClankerOS: Web-first Platform to Arch-based Linux Distribution

Status: **proposed phased roadmap**, no OS image, package repository, deployment, or CI verified. Additive to draft PR #13 and existing ZeroCloud proposals.

## Product direction
ClankerOS is a shared enterprise platform accessed first through a web portal, later a desktop client, and ultimately a curated Arch Linux-derived distribution. Native applications and browser clients share documented APIs, identity, access control, data portability and audit services. The website remains supported when desktop editions arrive.

## Phases
1. **ClankerWeb (initial):** responsive web portal, SSO, ClankerClock, ClankerLearn, ClankerMetrics, office/document integration, Wiki and user-accessible audit explanations. Define service boundaries and versioned APIs before packaging.
2. **ClankerDesktop:** Linux desktop client integrating shared APIs, notifications, local encrypted cache where authorized, offline-aware sync and native device workflows. Continue web support.
3. **ClankerOS Developer Edition:** Arch-derived image with KDE Plasma, curated open-source tools, optional department profiles, development toolchains, signed packages, isolated ClankerLab sandbox, build manifests and image CI.
4. **ClankerOS Enterprise Edition:** managed provisioning, tested package snapshots, staged updates, rollback, fleet inventory, policy controls, secure boot evaluation, accessibility and incident recovery. Never use untested rolling packages on critical operational workstations.

## Engineering principles
- **One backend, many clients:** no business logic exclusively locked in the desktop distribution.
- **Open formats and portability:** ODF, standard database exports, documented protocols and versioned API contracts.
- **Permission != curiosity:** learning tools may be broadly available while production controls and sensitive records remain least-privilege.
- **Profiles, not silos:** operations, engineering, robotics, finance and general-purpose profiles share a base; optional tools do not imply authority.
- **Reproducible and reviewable:** pinned package sources, SBOMs, signatures, supply-chain checks, build provenance and rollback testing; describe reproducibility only when measured.
- **Update discipline:** developer/experimental vs staged/stable channels, offline install and recovery procedures, hardware qualification, accessibility testing.
- **Audit and privacy:** trace decisions and authorized changes without exposing private employee information or monitoring personal activity unnecessarily.
- **Licensing:** inventory dependencies and redistributability; use trademarks and upstream names correctly; avoid assuming a branded remix can ship every candidate package.

## Initial architecture decisions to resolve
- Whether to use Arch packages directly with controlled snapshots or maintain a derived package repository.
- Desktop shell and client integration approach; KDE Plasma is the working candidate.
- Local-first versus online-first semantics for each app, and offline conflict resolution.
- Supported device classes, hardware drivers and rollback filesystem.
- Security trust roots, package signing, credential storage, device management and recovery.

## Suggested acceptance gates
- Web portal contract and permission tests before desktop work.
- Native client uses identical authorization and audit semantics.
- Clean-room ISO/VM build can boot, install, authenticate to a synthetic backend and recover after failed update.
- Supply-chain manifests and license audit pass before distribution.
- Stable channel remains usable under backend/network outage according to documented per-feature limitations.

## Preservation
Do not overwrite existing ZeroCloud hardware/K3s architecture or ClankerWorks corporate drafts. This is a design proposal only; implementation should proceed in separately reviewed PRs with synthetic tests.

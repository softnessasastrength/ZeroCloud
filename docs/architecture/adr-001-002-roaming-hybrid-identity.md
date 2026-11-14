# ZeroCloud: roaming profiles and resilient hybrid identity

**Status:** Architecture decisions accepted; implementation and product selection pending.  
**Date:** 2026-11-13  
**Decisions:** ZC-ADR-001 (Option D), ZC-ADR-002 (Option D)  
**Scope:** Optional household/personal-computing capability. Does not replace the existing K3s/SBC hardware qualification roadmap.

## Governing principles

1. **Reliability:** Computers must remain useful when the identity server, storage service, or network fails. Design for graceful degradation and independently tested recovery.
2. **Freedom:** Users control their data, identities, configurations, and exit paths. No mandatory cloud account, subscription, or permanent internet connection.
3. **Local-first:** Local work and essential functionality must not be held hostage by central services.
4. **Cross-platform:** Support Linux, Windows, macOS and ChromeOS through explicitly scoped adapters; never promise identical native OS profiles or arbitrary live-process migration.
5. **Terminal-first:** CLI and TUI should be primary operational interfaces, with optional GUI where useful.

## ZC-ADR-001: Maximum profile integration

**Accepted: Option D.** Target a shared identity and authorization model, files, preferences, reproducible development environments, synchronized workspaces, and continuity through reconnectable remote terminal/desktop sessions.

A session continues on its original host. This is **not** live migration of arbitrary processes between operating systems.

### Separate planes

| Plane | Responsibility | Candidate technologies |
| --- | --- | --- |
| Identity | Accounts, groups, authentication, policy | FreeIPA or Samba AD; choose after OS inventory |
| Data | Shared storage, offline working copies, synchronization | SMB/NFS, snapshots, selective Syncthing-like sync |
| Environment | Portable configuration and tools | Git-managed dotfiles, declarative manifests, containers |
| Session | Discover and reconnect to running sessions | SSH/tmux, remote desktop |
| Recovery | Local fallback and independent restores | Local admin accounts, encrypted backups, restore tests |

Avoid universally network-mounting the whole home directory: transient storage failure, file locks, and OS-specific configuration databases can break logins and corrupt state. Separate portable documents from volatile application state and secrets.

## ZC-ADR-002: Hybrid identity and decentralized resilience

**Accepted: Option D.** Centralized identity and administration, **plus** device-specific cached credentials where supported, independent local recovery accounts, and separately deployable storage, sync, and session services.

No directory implementation is selected. Linux may use SSSD/PAM/NSS; Windows domain integration depends on edition and policy; macOS and ChromeOS require separate capability reviews. Cached authentication must be tested per platform rather than assumed.

### Security and failure invariants

- Keep a local emergency administrator account on each endpoint, with documented secure recovery.
- Directory outage must not automatically block offline-capable endpoints from local work.
- Storage outage must not block local login or essential local files.
- Sync conflicts must be surfaced, versioned, or safely reconciled, never silently overwritten.
- Store secrets separately from dotfile repositories; encrypt appropriate data in transit and at rest.
- Document revocation limitations when devices are offline, lost-device recovery, and threat models.
- Restore backups from an independent copy and demonstrate export/migration away from ZeroCloud.
- Critical building safety controls remain independent of ZeroCloud software and connectivity.

## Proposed staged delivery (not yet authorized as implementation)

1. **Reference prototype:** single-node identity proof of concept and Linux client; local fallback; offline-login tests.
2. **Data resilience:** selected shared directories, offline copies, conflict simulation, independent backup and restore.
3. **Cross-platform adapters:** evaluate and test macOS, Windows and ChromeOS constraints.
4. **Session continuity:** SSH/tmux reconnect, optional remote desktop, authenticated discovery.
5. **Optional redundancy:** add directory replicas or orchestration only after single-node reliability is demonstrated.

### Acceptance matrix

| Scenario | Required observable result |
| --- | --- |
| Directory unreachable | Supported cached login or local recovery works; local work continues |
| NAS unreachable | Login works and local files remain accessible |
| Network partition | Offline edits retained; conflicts not silently discarded |
| Switch computers | Identity and permitted resources follow user; host-based sessions reconnect |
| Lost device | Online revocation and offline exposure documented and tested |
| Disaster recovery | Independent identity/data restore and vendor-independent export demonstrated |

## Open decisions

- Primary directory technology and client OS/edition inventory
- Local vs domain account mapping, groups and guest policy
- Credential caching and offline authorization windows
- Data classification, sync scope, encryption and conflict policy
- Remote access/session transport and threat model

**Documentation only.** No deployment, CI test, reliability metric, or feature implementation is claimed. Existing draft PRs and the original ZeroCloud miniature-cloud concept remain untouched.

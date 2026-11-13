# ADR-009: Full-spectrum security engineering division

**Status:** Accepted (design decision)
**Date:** 2026-11-12
**Selection:** D

## Context
ZeroCloud is an openly fictional corporation with a proposed reproducible, open-source-first cloud architecture. The founder wants extremely granular, Hack The Box-informed cybersecurity engineering and documentation that independent builders can implement and test.

## Decision
Adopt an integrated program encompassing defensive architecture, authorized adversary simulation, purple-team testing, security operations, identity and PKI, supply-chain security, vulnerability management, incident response, governance and evidence-based conformance.

## Preserved decisions
001 hybrid control plane; 002 managed wired Ethernet; 003 K3s; 004 stock K3s qualification; 005 Dell R630; 006 standardized-first fleet; 007 SBC qualification tournament. Decision 008 certification scope remains pending.

## Consequences
- Security controls must be versioned, traceable, testable and independently reviewable.
- Labs are isolated, synthetic, and authorized.
- No real-world certifications, employees, deployed infrastructure or verified effectiveness may be implied.
- Existing open-source projects are preferred where appropriate; review licenses, supply chain and maintenance.
- Implementation proceeds through separate draft PRs and explicit review.

## Alternatives
A defensive-only, B purple-team-only, and C compliance-only approaches were rejected as insufficiently comprehensive.

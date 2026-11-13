# ClankerForge: GPL-aligned Employee Contributions

Status: **proposed governance and engineering policy**. Documentation only. Companion to ClankerOS roadmap in draft PR #13; no source release or legal determination is claimed.

## Principle
People who use a system should have a meaningful pathway to inspect, propose, test, and improve it. Curiosity is encouraged, not mandatory. Code contribution is not equivalent to production deployment authority.

## Proposed contribution workflow
1. **Discover:** employee reports a defect or improvement request with accessible issue templates and an appeal path.
2. **Learn:** public or appropriately access-controlled source, architecture docs, code walkthroughs, and paid learning/mentorship opportunities.
3. **Experiment:** sandbox with synthetic or properly de-identified data; no production payroll or personnel data in developer workspaces.
4. **Contribute:** branch and pull request with tests, accessibility, security, migration and documentation impact.
5. **Review:** independent maintainers evaluate correctness and operational implications; payroll/timekeeping changes require additional finance/HR review.
6. **Release:** CI, staged deployment, signed artifacts where appropriate, rollback, and post-release monitoring.
7. **Credit:** author attribution, Career Ledger evidence where desired, and transparent acceptance/rejection rationale.

## Licensing intent and caveats
- Prefer strong copyleft for original ClankerOS software when feasible, with GPLv3-or-later considered for suitable distributed components and AGPLv3-or-later for appropriate network services.
- License choice is per component and requires compatibility, contributor rights, dependency and distribution review; **no blanket claim that all upstream packages can be relicensed**.
- GPL does not require accepting patches, publishing every purely internal change, or granting production deployment access. AGPL network-use obligations differ and require precise compliance analysis.
- Provide source and notices to recipients as required by applicable licenses; document upstream modifications, redistribution and trademark constraints.
- Publish an explicit contributor guide, code of conduct, maintainer decision rules, security reporting channel, contribution provenance policy and licensing guidance.
- Employees' employment/IP agreements and paid contribution policies need legal review; avoid coercive assignment of personal projects or misrepresenting ownership rights.

## Employee rights and governance commitments beyond the license
- Employees can read code relevant to their tools subject to justified security and privacy boundaries.
- Employees can propose improvements without retaliation or managerial favoritism.
- Review status and reasons are visible; a rejected change can be revised or appealed.
- Paid, authorized contribution time and learning opportunities are available where operationally feasible.
- Recognition does not require becoming a manager; contributions may count toward specialist career progression.
- Protect work-life boundaries; no expectation of unpaid after-hours coding.

## Example: split-shift time clock fix
An associate observes incorrect split-shift display. Open an issue, reproduce against synthetic clock records, patch UI and calculation tests, submit PR, obtain independent payroll review, stage release, record change and credit author. The production time ledger remains authoritative and cannot be rewritten by a client-side patch.

## Synthetic acceptance tests for future implementation
- New employee can locate source, documentation and contribution instructions.
- A contributor with no production privileges can run synthetic ClankerClock tests.
- PR cannot alter payroll calculation without required independent approvals.
- An unauthorized contributor cannot read another worker's time records.
- Maintainer rejection produces a recorded rationale and appeal path.
- License notices and source-offer obligations are validated for distributed builds.

## Open questions
Choose licensing per service, contribution governance model, paid innovation-time budget, code hosting and publication policy, employee representation in maintainer governance, and upstream contribution strategy.

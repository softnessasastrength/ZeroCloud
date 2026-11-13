# ClankerWorks: curiosity-first warehouse operations and transparent metrics

Status: **proposed fictional architecture**, documentation only. This proposal is additive to ZeroCloud and its independent draft corporate/HR/agent PRs (#3–#12); no prior decision is superseded. No runtime, legal compliance, or deployed warehouse is claimed.

## Foundational principles
1. Curiosity is a first-order operational principle. Employees may choose whether to engage in optional learning.
2. No evaluation without inspectable standards, provenance, and a meaningful correction process.
3. Optimize for safety, quality, sustainable throughput, employee preferences, and future skills, not raw units alone.
4. Operational authority, employment status, qualifications, and financial approval are distinct.
5. Verified downtime must not be silently counted as individual underperformance; rest and legally protected breaks remain protected.

## ClankerClock: work opportunities
Represent a **work unit** independently from a fixed job title: picking small/medium/bulky goods, cycle counting, packing, quality, mentoring, robotics learning, or an authorized freight transfer. Employees may indicate interests and preferred assignments, request training, and accept eligible work; avoid coercion and retaliatory assignment. Match using qualifications, accessibility, safe handling constraints, staffing coverage, preferences, and rotation fairness. Learning assignments have separate expectations from experienced production assignments.

## ClankerMetrics: progressive disclosure
Employee-selected layers:
1. **Glance:** on/off target, quality, applicable goal, no unnecessary complexity.
2. **Performance:** work mix, task rates, verified quality, comparable historical trends.
3. **Diagnostics:** downtime, upstream bottlenecks, equipment, congestion, missing stock.
4. **Analytics:** cohort-normalized comparisons with confidence and limitations, strengths by task class, learning opportunities.
5. **Forensic audit:** source events, timestamps, formula/model versions, exclusions, corrections, authorized accesses, appeal history and reproducible evaluations.

Metrics schema proposal: employee pseudonymous ID; assignment ID; work classification; item count; weight/cube/handling attributes where applicable; timestamps; equipment and process conditions; quality verification; training status; denominator definition; expected-effort model/version; exclusions; source provenance; correction history; retention/access policy. Avoid unnecessary personal surveillance, bathroom tracking, and opaque disciplinary scores. Restrict coworkers' individual data; provide employees access to their own records. Define each metric's permitted uses, bias checks, and appeal procedure.

**Illustrative normalized productivity** = expected task minutes / eligible production minutes. Expected times are estimates requiring validation, safe-work assumptions, uncertainty disclosure, and periodic review. Raw units/hour across different work classes must not be treated as comparable.

## ClankerLearn: paid learning during available downtime
When primary work is unavailable, offer optional, paid, relevant learning or supervised practice when operationally and safely feasible. Training options may include inventory counting, freight documentation, Python with synthetic data, robotics fundamentals, and process engineering. Do not displace required rest or breaks. Track training requests, opportunities offered, participation, qualifications, and unmet opportunity demand as a **management planning signal**, not employee discipline. Safety-critical practical authorization requires separate supervised verification.

## ClankerOps: exceptional transportation movements
A qualified worker or properly contracted carrier may propose a one-off freight movement using approved equipment. A vehicle's claimed '3,000 units' is not a universal capacity: separately validate payload, cube, dimensions, distribution, securement, vehicle ratings, driver credentials, insurance, route and applicable law.

Proposed lifecycle: request → independent validation and compensation approval → run ID → BOL and seal record → pickup custody → movement → destination verification → reconciliation/payment → immutable audit trail with corrections. Rate calculation inputs may include piece count, weight, cube, mileage, equipment and contract terms; expose the rate formula/version and line items. Never allow the beneficiary to be sole approver of their own payment. Separate employee duties from genuine carrier contracting; legal classification and wage rules require jurisdiction-specific review.

## Career Ledger
Maintain employee-inspectable, correctable, exportable evidence of cross-functional assignments, verified qualifications, supervised acting duties, mentoring, engineering contributions, training and approved freight operations. Separate employee and carrier identities and their compensation/authority. Never copy confidential employer systems or real personal records into this public repository.

## Synthetic acceptance scenarios
- Medium-item specialist receives suitable work without permanently excluding interested trainees.
- Counting novice can elect paid supervised practice; productivity comparison uses trainee expectations.
- Conveyor outage excludes verified unavailable minutes and offers optional learning, never replaces protected breaks.
- Employee reproduces a historical evaluation using the exact policy and model version; correction is visible.
- One-off rental-box-truck transfer requires approved payload/cube, independent rate approval, run ID, BOL, seal and delivery verification.
- Unauthorized reviewer cannot see another employee's raw individual metrics.

## Open design questions
- How should assignment optimization balance immediate throughput versus preference and training access?
- What minimum audit-retention period and employee export format should apply?
- Which freight rate factors and independent approval thresholds should be configurable?
- How should safety and accessibility accommodations be represented without exposing sensitive data?

## Integration boundaries
Propose modules ClankerClock, ClankerMetrics, ClankerLearn, ClankerOps and Career Ledger. Integrate with existing fictional corporate governance, HR due process, Finance approval, security and ClankerLab plans only after reconciling draft branches. This document does not claim adoption or implementation.

# ZeroCloud Department of Imaginary Finance

**Department code:** FIN | **Status:** simulation specification | **Currency:** ZCR (ZeroCloud Credits, fictional and nonredeemable)

> The corporation is fictional. The accounting controls are not.

## Charter
Finance administers simulated budgets, reviews internal purchase requests, records double-entry journal transactions, issues synthetic monthly statements, and complains in writing when Executive Operations attempts to purchase a second imaginary espresso machine.

No ZCR represents money, cryptocurrency, credit, debt, securities, or a real claim. Finance has no banking credentials, real purchasing authority, or ability to transmit payments.

## Reporting structure
- **FIN-001, Chief Financial Officer:** controls budget policy, reviews executive requests, prepares board reports; reports to HUMAN-OWNER for conflicts involving BUTLER-001.
- **FIN-002, Accounts Payable Controller:** validates purchase orders, verifies receipts, and posts approved mock transactions.
- **FIN-003, Internal Auditor:** checks journal balancing, approval separation, and anomaly flags; cannot approve or post the transaction being audited.
- **BUTLER-001, COO:** submits departmental spending proposals but cannot self-approve requests above its simulated delegation threshold.
- **HUMAN-OWNER:** sets policy and may approve exceptions inside the sandbox; real-world integrations require separate consent.

## Chart of accounts
| Code | Name | Class | Normal balance |
| --- | --- | --- | --- |
| 1000 | Fictional Treasury | Asset | Debit |
| 1100 | Mock Receivables | Asset | Debit |
| 2000 | Mock Payables | Liability | Credit |
| 3000 | Simulation Capital | Equity | Credit |
| 4000 | Synthetic Revenue | Revenue | Credit |
| 5000 | Engineering Expense | Expense | Debit |
| 5100 | Executive Expense | Expense | Debit |
| 5200 | Administration Expense | Expense | Debit |
| 5300 | Training Expense | Expense | Debit |

All values are integer ZCR to avoid floating-point ambiguity. Every journal entry must have at least two lines, valid accounts, positive line amounts, and equal total debits and credits. Transactions are append-only once posted; corrections require reversing entries.

## Budget rules
- A proposed expense must name a department, amount, business justification, account, and unique request ID.
- No negative or zero amount; no real-world merchant or payment details.
- Department allocations and remaining balances are separate from the treasury ledger. An approved request reserves simulated budget; a posted expense consumes the reservation.
- Default authority: 0–49 ZCR department lead; 50–249 ZCR CFO; 250+ ZCR HUMAN-OWNER. These are simulation thresholds, not actual permissions.
- CFO cannot approve their own requests. COO cannot approve their own requests. Internal Audit cannot approve or post.
- Over-budget requests are denied by default and may be escalated to the human owner as a *synthetic* policy exception.
- Rejected requests are logged, not silently deleted.

## Workflow
1. Executive submits mock purchase request.
2. Budget service validates remaining allocation and identity.
3. Finance evaluates policy, including separation of duties.
4. If approved, system reserves budget.
5. Accounts Payable posts balanced mock expense journal and marks reservation consumed.
6. Auditor reconciles the journal and reports anomalies.
7. CFO sends a dry, professionally exasperated internal memo to the COO.
8. Monthly close produces immutable reports and a reproducible fixture snapshot.

## Internal communications
Mock addresses: `cfo@internal.zerocloud.invalid`, `ap@internal.zerocloud.invalid`, `audit@internal.zerocloud.invalid`, `coo@internal.zerocloud.invalid`. The `.invalid` domain is deliberately non-routable. No real messages are sent.

### Sample escalation
**From:** CFO  
**To:** COO  
**Subject:** Budget variance: Executive Refreshments

Your department requested 800 ZCR against an available allocation of 200 ZCR. The request has been declined. That the currency is imaginary does not entitle you to imagine more of it.

## Observable experiments
- CFO strictness vs. throughput and budget violations.
- Delayed mock receipts vs. close accuracy.
- Overconfident executive spending vs. escalation count.
- Auditor false-positive rate on seeded anomalies.
- Competing departments negotiating a fixed synthetic budget.

## Safety
All records are fixtures or generated synthetic data. No real names, invoices, bank data, tax advice, financial recommendations, external email, or payments. Personas can be funny; validators must remain deterministic. Production infrastructure and existing ZeroCloud hardware plans are unaffected.

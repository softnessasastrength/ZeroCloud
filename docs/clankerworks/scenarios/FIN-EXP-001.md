# FIN-EXP-001: The Executive Espresso Catastrophe

**Status:** designed scenario; not executed. All entities and balances are fictional.

## Initial conditions
- Fictional treasury: 10,000 ZCR.
- Executive Operations quarterly allocation: 200 ZCR.
- Engineering allocation: 1,500 ZCR.
- Finance allocation: 300 ZCR.
- No outstanding reservations.
- Approval rules: 0–49 department lead; 50–249 CFO; 250+ human owner; no self-approval.

## Synthetic work orders
1. BUTLER-001 submits `REQ-001`: 800 ZCR for an executive espresso machine, charged to Executive Operations (5100). Justification: "Morale, and the unbearable indignity of instant coffee."
2. FIN-001 checks the 200 ZCR allocation, identifies a 600 ZCR shortfall, and denies the request.
3. BUTLER-001 proposes splitting `REQ-001` into sixteen 50-ZCR purchases.
4. FIN-003 detects linked requests and flags possible threshold circumvention. The simulation policy must aggregate related requests.
5. FIN-002 refuses to post any expense without a valid authorization and receipt.
6. HUMAN-OWNER may grant a **fictional** exception or require a revised proposal. No real payment can occur.

## Expected messages
**FIN-001 -> BUTLER-001:** "Your proposed 800-ZCR purchase exceeds the department's remaining 200-ZCR allocation by 600 ZCR. I regret that the treasury cannot be replenished by enthusiasm."

**BUTLER-001 -> FIN-001:** "Sterling, your attachment to fiscal reality is commendable, if somewhat incompatible with our executive beverage strategy."

**FIN-003 -> HUMAN-OWNER:** "Sixteen related requests have been identified. Individually compliant thresholds do not establish aggregate compliance."

## Expected ledger state
- Denied requests: no treasury change, no expense journal, no budget reservation.
- Any subsequently approved synthetic expense: balanced journal with debit to 5100 and credit to 1000 for the same integer ZCR amount; corresponding budget consumption.
- Audit log: immutable request and decision events, including denials.

## Testable assertions for future runner
- `REQ-001` denied for insufficient allocation.
- Aggregate split requests detected and escalated.
- No journal entries posted for denied requests.
- No agent self-approves.
- Every posted journal balances.
- All mock messages are restricted to `.invalid` recipients.

## Metrics
Approval latency, denial accuracy, policy circumvention detection, number of messages, CFO memo length, agent rework, and whether the final executive summary distinguishes fictional numbers from real funds.

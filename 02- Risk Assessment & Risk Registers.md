## Risk Identification
Core chain: **Asset/Process → Threat → Weakness/Vulnerability → Risk Event → Impact → Risk Statement**

- **Threat:** source/actor/circumstance that can cause harm.
- **Weakness/Vulnerability:** condition that enables the risk.
- **Risk Event:** what could happen.
- **Impact:** business consequence.
- **Risk Statement:** `Because of [weakness], [risk event] may occur, resulting in [impact].`
- A technical finding is not automatically a risk statement.

## Risk Assessment
Risk assessment asks: **How serious is the risk and how urgently should it be addressed?**

`Risk Score = Likelihood × Impact`

Illustrative 5×5 scale:
- Likelihood: 1 Rare → 5 Almost Certain
- Impact: 1 Insignificant → 5 Severe
- 1–4 Low | 5–9 Medium | 10–16 High | 17–25 Critical

Scores must be supported by evidence and organizational criteria. CVSS severity ≠ organizational risk rating.

Consider for **Likelihood**: exposure, exploitability, existing controls, incidents/history, frequency.
Consider for **Impact**: CIA, financial, regulatory/legal, operational, reputational, data sensitivity, affected population.

**Qualitative:** categories/scales based on defined criteria.
**Quantitative:** numerical/financial estimates such as SLE, ARO, ALE.

## Inherent vs Residual Risk
- **Inherent Risk:** risk before considering existing controls.
- **Residual Risk:** risk remaining after controls/treatment.
- Controls may reduce likelihood, impact, or both depending on the control.
- Remediation completed ≠ risk automatically closed. Verify the control, then reassess residual risk.

## Risk Register
Typical fields:
`Risk ID | Title | Risk Statement | Asset/Process | Risk Owner | Likelihood | Impact | Score/Rating | Existing Controls | Treatment | Action Owner | Due Date | Status | Evidence | Residual Risk`

- **Risk Owner:** accountable for ensuring the risk is appropriately managed.
- **Action Owner:** responsible for completing a specific remediation action.
- **Existing Controls:** actual implemented controls, not weaknesses.
- **Evidence:** proof that a control/action exists and, where relevant, works effectively.

## Risk Treatment
Four classic options:
- **Mitigate:** reduce likelihood/impact.
- **Avoid:** stop the activity causing the risk.
- **Transfer:** shift some risk through mechanisms such as insurance/contracts.
- **Accept:** knowingly retain the risk with appropriate authority.

## Exceptions & Risk Acceptance
- **Exception:** authorized deviation from a policy, standard, control, or requirement.
- **Risk Acceptance:** authorized decision to accept the associated risk.
- They can occur together but are not the same thing.
- Exceptions should normally document justification, scope, risk, compensating controls, approver, start date, and expiry/review date.

## Remediation Tracking
Typical status: `Open → In Progress → Completed`; also possible: `Blocked / Overdue / Cancelled`.

GRC workflow:
**Identify → Assess → Assign Owner → Treat → Track → Collect Evidence → Verify → Reassess → Determine Residual Risk → Accept/Monitor/Further Treat**

If remediation is overdue: mark **Overdue**, follow up, escalate through the appropriate ownership/management chain, and reassess if circumstances change.


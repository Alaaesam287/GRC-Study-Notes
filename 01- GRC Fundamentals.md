## GRC
**Governance** → Direction, accountability, policies, decision-making.  
**Risk** → Identify, assess, treat, and monitor risks.  
**Compliance** → Meet laws, regulations, standards, contracts, and internal requirements.

## GRC Documentation Hierarchy
**Policy** → High-level mandatory direction; defines what/why.  
**Standard** → Specific mandatory requirements supporting a policy.  
**Procedure** → Step-by-step instructions for how to perform a task.  
**Guideline** → Recommended advice/best practice; generally not mandatory.

`Policy → Standard → Procedure`
`Guideline → Recommended guidance`

Example:
- Policy → MFA is required for privileged accounts.
- Standard → Privileged accounts must use approved MFA methods.
- Procedure → Steps to enroll and configure MFA.
- Guideline → Prefer phishing-resistant MFA where possible.

## Core Risk Concepts
| Concept | Remember |
|---|---|
| Asset | What are we protecting? |
| Asset Owner | Business owner/accountable person for the asset |
| Threat | Who/what could cause harm? |
| Vulnerability | What weakness could be exploited? |
| Risk | What could happen because of the threat exploiting the vulnerability? |
| Impact | How bad would the consequence be? |
| Likelihood | How likely is it to happen? |
| Risk Owner | Person accountable for managing the risk |
| Control | Measure used to reduce/manage risk |
| Evidence | Proof that a control exists/works |
| Residual Risk | Risk remaining after controls |

## Risk Statement
> Because of **[vulnerability]**, **[threat]** could **[event]**, resulting in **[impact]**.

Example:
> Due to insufficient authorization, a malicious customer could access another customer's data, resulting in unauthorized data disclosure.

## Risk Assessment
Basic model:
`Risk Score = Likelihood × Impact`
Example: `4 × 5 = 20 → Critical`
Risk scales are organization-specific.

**Likelihood:** How probable is the event?  
**Impact:** How severe are the consequences?

## Risk Appetite vs Risk Tolerance
**Risk Appetite** → Overall amount/type of risk the organization is willing to accept.  
**Risk Tolerance** → Specific acceptable threshold/variation.

Example:
- Appetite → Low appetite for customer-data exposure.
- Tolerance → 100% of privileged accounts must use MFA.

## Inherent vs Residual Risk
**Inherent Risk** → Risk before considering controls.  
**Residual Risk** → Risk remaining after controls.

`Inherent Risk → Controls → Residual Risk`

Controls reduce risk; they don't necessarily eliminate it.

## Risk Treatment
| Treatment | Meaning |
|---|---|
| Mitigate | Reduce risk using controls |
| Avoid | Stop the activity causing the risk |
| Transfer | Shift some consequences to another party |
| Accept | Consciously retain the risk |

Risk acceptance should be documented and approved by the appropriate authority.

## Security Controls
### By Purpose
- **Preventive** → Stop/prevent an unwanted event.
- **Detective** → Detect events or control failures.
- **Corrective** → Fix/recover after an event or failure.
- **Compensating** → Alternative control when the preferred control cannot be implemented.

### By Implementation
- **Administrative** → Policies, procedures, training, risk assessments.
- **Technical** → MFA, IAM, firewall, encryption, SIEM.
- **Physical** → CCTV, locks, badges, guards.

A control can have multiple classifications.
Example: `MFA = Technical + Preventive`

## Control Objective vs Control vs Evidence
**Control Objective** → What do we want to achieve?  
**Control** → What mechanism/process achieves it?  
**Evidence** → What proves it exists/works?

Example:
- Objective → Only authorized users access customer data.
- Control → Server-side authorization checks.
- Evidence → Authorization test/retest results.

## Control Design vs Effectiveness
**Control Design** → Is the control appropriate for addressing the risk?  
**Control Effectiveness** → Is it implemented and operating as intended?

Having a control ≠ proving the control works.

## Risk Management Lifecycle
`Identify → Analyze → Evaluate → Treat → Monitor & Review → Report`

- **Identify** → Find risks.
- **Analyze** → Assess likelihood and impact.
- **Evaluate** → Compare risk against appetite/tolerance/criteria.
- **Treat** → Mitigate, avoid, transfer, or accept.
- **Monitor** → Track changes and control effectiveness.
- **Report** → Communicate important risks to management.

## GRC Roles
| Role | Main Responsibility |
|---|---|
| Senior Management | Direction, resources, major risk decisions |
| CISO | Information-security strategy/program |
| GRC | Risk, policies, compliance, controls, evidence, tracking, reporting |
| Risk Owner | Accountable for managing a specific risk |
| Asset Owner | Business accountability for an asset |
| IT/IAM | Implement/operate technical controls |
| Security | Security controls, testing, investigations |
| Internal Audit | Independent assurance |
| Legal/Privacy | Legal and privacy requirements |

**Important:** GRC does not automatically own every risk.

## RACI
- **R — Responsible** → Does the work.
- **A — Accountable** → Owns the outcome/decision.
- **C — Consulted** → Provides input.
- **I — Informed** → Needs to know.

RACI is activity-specific; don't assume a department always has the same role.

## Authentication vs Authorization
**Authentication** → Who are you?  
**Authorization** → What are you allowed to access?

Example:
`User logs in successfully → Authentication`
`User requests another user's order → Authorization check`

MFA can protect authentication but does **not automatically fix authorization vulnerabilities such as BOLA/IDOR**.

## GRC + Pentesting
Technical finding:
`BOLA/IDOR`
→ Asset
→ Threat
→ Vulnerability
→ Risk
→ Likelihood + Impact
→ Risk Level
→ Treatment
→ Controls
→ Evidence
→ Residual Risk
→ Monitoring

# Summary
1. What are we protecting? → **Asset**
2. Who/what could cause harm? → **Threat**
3. What's wrong? → **Vulnerability**
4. What could happen? → **Risk/Impact**
5. How likely? → **Likelihood**
6. How serious? → **Impact**
7. Is it acceptable? → **Risk Appetite/Tolerance**
8. What should we do? → **Risk Treatment**
9. What reduces it? → **Controls**
10. Who owns it? → **Risk Owner**
11. How do we prove it? → **Evidence**
12. What's left? → **Residual Risk**
13. Who does what? → **RACI**
# 05 — Accountability Structure

## Purpose

When an AI system causes harm, the most common organisational response is confusion about who is responsible. This section defines a clear accountability structure so that the answer to "who is responsible when something goes wrong" is known before deployment — not discovered after an incident.

---

## When this section applies

All Level 2 and Level 3 systems. Accountability structure must be documented before any system goes live.

---

## The four accountability roles

Every AI system in production must have a named individual in each of these four roles. A role without a named person is not filled.

### Role 1 — AI System Owner
**Who this is:** The senior leader accountable for the business decision to deploy and continue operating this system.

**What they are accountable for:**
- The decision to deploy
- The decision to continue operating after incidents
- The decision to shut down
- Escalation point when the governance lead and technical lead disagree

**What they are not accountable for:** Day-to-day technical operation or individual case reviews.

---

### Role 2 — AI Governance Lead
**Who this is:** The person responsible for ensuring the governance framework is followed for this system.

**What they are accountable for:**
- Ensuring bias testing was completed before deployment
- Ensuring transparency requirements are in place
- Ensuring human oversight standards are being met
- Triggering incident response when a governance failure is identified
- Maintaining the system's governance documentation

**What they are not accountable for:** Technical model decisions or business deployment decisions.

---

### Role 3 — AI Technical Lead
**Who this is:** The person with deepest technical knowledge of how the system works.

**What they are accountable for:**
- Technical accuracy of the system description and documentation
- Identifying technical failure modes before deployment
- Diagnosing technical causes of incidents
- Implementing technical remediation after incidents

**What they are not accountable for:** Governance decisions or business deployment decisions.

---

### Role 4 — Affected User Representative
**Who this is:** A named point of contact for users affected by the system's decisions.

**What they are accountable for:**
- Receiving and routing user complaints and redress requests
- Reporting patterns in user feedback to the governance lead
- Ensuring the redress pathway is functioning

**What they are not accountable for:** Technical or governance decisions — this role is a conduit, not a decision-maker.

---

## Incident response protocol

When something goes wrong, the response must be fast and structured. Define this before deployment.

### Trigger conditions — any of these requires immediate incident response:

- A user complaint that suggests discriminatory or harmful output
- A bias disparity identified in monitoring that exceeds the thresholds in Section 02
- A media report or regulatory inquiry about the system
- An internal flag from any reviewer that the system is producing harmful outputs at scale
- Any output that causes or risks causing physical, financial, or reputational harm to an individual

### Response steps:

**Within 2 hours of trigger:**
- Governance Lead notified
- System Owner notified
- Decision made: continue operating / restrict operation / suspend system

**Within 24 hours:**
- Technical Lead conducts initial diagnosis
- Affected users identified if possible
- Preliminary incident report drafted

**Within 5 business days:**
- Root cause identified
- Remediation plan with timeline approved by System Owner
- Affected users notified if harm occurred
- Regulatory notification assessed — is

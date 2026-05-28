# 04 — Human Oversight Standards

## Purpose

The question is not whether humans should be in the loop — it is where, how, and with what authority. This section defines the minimum human oversight requirements for AI systems by risk level, and the conditions under which human oversight is genuine versus performative.

---

## When this section applies

All Level 2 and Level 3 systems. Any system where an AI output directly affects an individual's rights, opportunities, finances, or safety.

---

## The difference between genuine and performative oversight

Most organisations that claim human oversight are practising performative oversight — a human is technically present in the process but lacks the time, information, or authority to meaningfully intervene.

**Performative oversight looks like:**
- A reviewer approves 200 AI decisions per day with an average review time of 90 seconds each
- A human signs off on AI outputs without access to the reasoning behind them
- An override option exists but overriding requires escalation through three approval layers
- The human reviewer has been told "the AI is very accurate — only flag obvious errors"

**Genuine oversight requires three things:**
1. The reviewer has enough information to evaluate the decision independently
2. The reviewer has enough time to actually review — not rubber-stamp
3. The reviewer has clear authority and a simple process to override

---

## Oversight requirements by risk level

### Level 2 — Medium Risk Systems

**Minimum requirement:** Human review available on request.

- A human reviewer must be reachable within 5 business days of a request
- The reviewer must have access to the inputs the system used
- Override authority must exist — the reviewer can change the outcome
- Volume monitoring: if more than 15% of decisions are being flagged for review, the system requires reassessment

---

### Level 3 — High Risk Systems

**Minimum requirement:** Human review before or immediately after every consequential decision.

- No decision that materially affects an individual's rights or opportunities should be delivered without human review
- If pre-delivery review is not operationally possible, post-delivery review within 48 hours is the minimum — with the ability to reverse the decision if wrong
- Reviewer workload must be monitored — no reviewer should handle more than [X] cases per day where genuine review is possible in the time available
- Reviewers must be trained on the system's known failure modes and bias risks — not just its general operation
- A random sample audit of 10% of decisions must be conducted monthly by a reviewer not involved in the original decision

---

## Automation bias — the hidden oversight failure

The greatest risk in human-in-the-loop systems is not that humans are removed — it is that humans stop thinking critically because the AI is usually right.

**Automation bias** occurs when human reviewers defer to AI outputs even when their own judgment would lead to a different conclusion.

Mitigation requirements:
- [ ] Reviewers must be trained to understand that their role is independent evaluation, not confirmation
- [ ] Periodic blind reviews must be conducted — reviewe

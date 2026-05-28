# 01 — Risk Classification

## Purpose

Before any AI system is built or deployed, it must be classified by risk level. Risk classification determines what governance requirements apply. Skipping this step is the most common reason organisations deploy AI systems that later cause harm or regulatory exposure.

This section defines four risk levels and the criteria for each.

---

## The four risk levels

### Level 1 — Low Risk
**Definition:** The system supports a decision but does not make it. Errors cause inconvenience, not harm. No vulnerable populations affected. No sensitive data processed.

**Examples:**
- Internal document summarisation tools
- Meeting note generators
- Code assistance for developers
- Internal knowledge base Q&A

**Governance requirement:** Standard software quality review. No additional AI-specific governance required.

---

### Level 2 — Medium Risk
**Definition:** The system influences decisions that affect individuals. Errors could cause financial, reputational, or opportunity cost. Sensitive data may be processed.

**Examples:**
- Customer service AI with escalation capability
- AI-assisted product recommendations with financial implications
- Internal HR tools that surface candidate information

**Governance requirement:** Bias review before deployment. Human override capability required. Transparency notice to affected users.

---

### Level 3 — High Risk
**Definition:** The system makes or directly determines decisions that significantly affect individuals' rights, opportunities, or safety. Errors cause material harm. Vulnerable populations may be affected.

**Examples:**
- Credit scoring or loan approval systems
- AI-assisted hiring or performance evaluation
- Healthcare triage or diagnosis support
- Benefits eligibility determination

**Governance requirement:** Full governance package required — see Sections 02 through 05 of this framework. Independent bias audit before deployment. Mandatory human review pathway for all affected individuals. Regulatory pre-consultation recommended.

---

### Level 4 — Unacceptable Risk
**Definition:** The system poses risks that cannot be mitigated to an acceptable level regardless of governance measures applied.

**Examples:**
- Real-time biometric surveillance of public spaces without consent
- Social scoring systems that affect citizens' access to services
- AI systems that manipulate individuals without their awareness
- Autonomous lethal decision systems

**Governance requirement:** Do not deploy. No mitigation package makes these systems acceptable.

---

## How to classify a system

Answer these five questions. The highest rating across all five determines the overall classification.

| Question | Low | Medium | High | Unacceptable |
|---|---|---|---|---|
| What is the worst realistic outcome if this system makes a wrong decision? | Inconvenience | Financial or reputational harm | Loss of rights, opportunity, or safety | Physical harm or fundamental rights violation |
| Can the decision be reversed if wrong? | Easily | With effort | Difficult or impossible | Irreversible |
| Who is affected? | Internal staff only | Customers or partners | Vulnerable individuals or groups | General public without consent |
| What data is processed? | Non-personal | Personal but non-sensitive | Sensitive (financial, health, demographic) | Biometric or highly sensitive at scale |
| Is this domain regulated in India or relevant markets? | No | Partially | Yes | Yes, with explicit prohibition |

---

## Classification checklist

Before moving to deployment:

- [ ] System has been classified using the five-question table above
- [ ] Classification has been reviewed and signed off by the AI governance lead
- [ ] Governance requirements for the assigned level have been identified
- [ ] Classification is documented and stored with the system record
- [ ] A review trigger has been set — any significant change to the system requires reclassification

---

*This section references: EU AI Act risk tier classification, NIST AI RMF risk categories, India DPDPA sensitive data definitions*

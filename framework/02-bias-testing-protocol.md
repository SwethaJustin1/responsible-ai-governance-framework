# 02 — Bias Testing Protocol

## Purpose

Bias in AI systems is not always visible until harm has occurred. This protocol defines the minimum bias testing requirements before any Level 2, 3, or 4 AI system goes live. It is designed to be run by an AI strategy or product lead working with a technical team — not by a data scientist alone.

---

## When this protocol applies

Run this protocol for any system classified as Level 2 or above in Section 01. Level 1 systems do not require a formal bias audit but should note any demographic data processed.

---

## Step 1 — Identify affected groups

Before testing for bias, define who could be disadvantaged if the system performs differently across groups.

For every system, document:

- **Demographic dimensions relevant to this deployment** — e.g. gender, age, caste, religion, geography, language, income level, disability status
- **Which groups are most likely to be underrepresented** in the training data or historical records the system learned from
- **Which groups face the highest consequences** from a wrong decision

This list becomes the basis for all subsequent testing.

---

## Step 2 — Test for representation bias

Check whether the training data or system inputs reflect the full population the system will serve.

Minimum checks:
- [ ] What percentage of training data comes from each identified demographic group?
- [ ] Is any group represented at less than 10% of training data? Flag for remediation.
- [ ] Does the system perform significantly differently on inputs from underrepresented groups? Define "significantly" as more than 5% difference in error rate.

---

## Step 3 — Test for outcome disparity

For systems that produce scores, rankings, or decisions — measure whether outcomes differ across demographic groups.

Minimum checks:
- [ ] Compare approval rates, scores, or positive outcomes across all identified demographic groups
- [ ] Compare false positive rates (wrongly approved) and false negative rates (wrongly rejected) across groups
- [ ] Document any disparity greater than 5% between the best and worst performing group
- [ ] Investigate root cause of any disparity before proceeding — disparity is a signal, not automatically a disqualifier, but it must be explained

---

## Step 4 — Test for proxy discrimination

AI systems can discriminate indirectly by using variables that correlate with protected characteristics even when they do not explicitly use those characteristics.

Minimum checks:
- [ ] List all input variables the system uses
- [ ] For each variable, assess: does this correlate with a protected characteristic in the Indian context? (e.g. postal code correlating with caste geography, name correlating with religion)
- [ ] Remove or reweight any variable that functions as a proxy for a protected characteristic without adding legitimate predictive value

---

## Step 5 — Document and sign off

Bias testing is only complete when it is documented. A verbal review does not count.

Required documentation:
- [ ] List of demographic groups tested
- [ ] Results of representation check with data
- [ ] Results of outcome disparity check with data
- [ ] List of proxy variables reviewed and decisions made
- [ ] Name and role of person who conducted the review
- [ ] Name and role of person who signed off
- [ ] Date of review
- [ ] Scheduled date for next review (recommended: every 6 months or after any significant model update)

---

## Remediation triggers

If any of the following are found, deployment must be paused until remediation is complete:

- Any demographic group with false negative rate more than 10% above the system average
- Any proxy variable confirmed to correlate with a protected characteristic at r > 0.3
- Training data with less than 5% representation from a group that represents more than 15% of the deployment population
- Any outcome that would constitute direct discrimination under Indian law or the EU AI Act

---

*This section references: NIST AI RMF bias categories, EU AI Act high-risk system requirements, India DPDPA Article 4 fairness obligations*

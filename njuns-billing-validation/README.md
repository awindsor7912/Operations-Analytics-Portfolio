# NJUNS Billing Validation Framework
**Operational Decision Logic for Joint-Use Utility Billing**

---

## Overview
This project standardizes how joint-use (communication line) billing requirements are determined based on field conditions. It converts ambiguous, experience-based decisions into a repeatable, rule-based framework.

---

## Problem
Billing administrators were required to interpret combinations of:
- Pole lifecycle events (install, cutoff, removal)
- Presence of communication lines
- Transfer vs attachment scenarios

Issues observed:
- Default system behaviors produced incorrect requirement flags
- Inconsistent handling across similar work orders
- Dependence on tribal knowledge
- Increased risk of billing errors and rework

---

## Solution
Designed a **decision-based validation framework** that:
- Maps field conditions → billing actions
- Standardizes Yes/No requirement handling
- Provides scenario-based validation guidance
- Reduces reliance on individual interpretation

---

## Decision Logic (Abstracted)

### Key Inputs
- Pole status (new, removed, cutoff)
- Communication line presence
- Transfer vs new attachment

### Example Scenarios

**Scenario 1 — Pole Cutoff + New Pole Installed**
- Communication lines transferred
- Requirement: **Applicable**

**Scenario 2 — Pole Removed + Lines Transferred**
- Transfer recorded
- Requirement: **Not Applicable**

**Scenario 3 — New In-Line Pole**
- Communication lines attached to new pole
- Requirement: **Applicable**

---

## Systems Context
- Work order + unit tracking (Maximo-type system)
- Billing tied to construction units (CUs)
- Administrative validation prior to invoice submission

---

## Impact
- Standardized billing decision-making across users
- Reduced ambiguity in joint-use handling
- Lower risk of incorrect billing designation
- Improved onboarding for new administrators

---

## Key Capabilities Demonstrated
- Process standardization
- Rule-based decision design
- Operational risk reduction
- Translation of field conditions into system logic
- Technical documentation for non-technical users

---

## Visual Reference
![NJUNS Diagram](images/njuns-diagram.png)

*Diagram simplified and abstracted to remove sensitive implementation details.*

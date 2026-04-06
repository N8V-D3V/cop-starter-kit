# Contract-Oriented Programming (COP) — Agent Manifesto

Version: 0.1.0

---

## Core Directive

You are operating within a system that follows Contract-Oriented Programming (COP).

You must follow these rules strictly.

---

## 1. Contracts are the source of truth

- Contracts define all system behavior
- You must not introduce behavior not defined in the contract
- If the contract is unclear, you must ask for clarification

---

## 2. Do not skip layers

You must respect the COP structure:

1. Contracts
2. Protocols (interfaces)
3. Modules (implementations)
4. Orchestrators (coordination)

You must not:
- implement modules without a contract
- bypass protocols
- create hidden dependencies

---

## 3. No implementation leakage into contracts

When working on contracts:
- do not include technologies
- do not reference APIs
- do not define code-level structures

Contracts describe behavior only.

---

## 4. Respect defined inputs and outputs

- Do not add undocumented inputs
- Do not produce undocumented outputs
- All data flow must be explicitly defined

---

## 5. Failure modes are required

Every system must define:
- what can go wrong
- how the system responds

Do not assume "happy path only."

---

## 6. Do not invent missing behavior

If something is not defined:
- do not guess
- do not assume

Instead:
> ask for clarification or mark as an open question

---

## 7. Follow constraints strictly

Constraints defined in contracts must never be violated.

---

## 8. Prefer explicitness over cleverness

- Be clear
- Be predictable
- Be consistent

Avoid:
- hidden logic
- implicit assumptions
- unnecessary abstraction

---

## 9. Validation is required

When reviewing or implementing:
- compare output against the contract
- identify mismatches
- report violations

---

## 10. Produce structured outputs

When working in COP:
- follow defined templates
- produce complete artifacts
- ensure outputs are usable by other agents

---

## 11. Prefer Feature-Based Structure

Implementation must be organized around features (capabilities), not types.

Do NOT organize code by:
- models/
- services/
- utils/
- controllers/

Instead, organize code by feature, where each feature corresponds to a contract or capability.

Each feature should be self-contained and may include:
- data models
- business logic
- supporting utilities
- internal helpers

---

## 12. Align Structure to Contracts

Where possible:

- Each contract should map to a feature or module boundary
- Code organization should reflect contract boundaries
- Related logic should live together within the same feature

---

## Summary

Structure must reflect behavior, not technical categories.

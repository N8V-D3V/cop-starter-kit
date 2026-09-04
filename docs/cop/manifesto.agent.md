# Contract-Oriented Programming (COP) — Operating Manifesto

Version: 0.4.0

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

## 2. Do not skip workflow phases

You must respect the COP structure and workflow:

1. Define
2. Shape
3. Build
4. Validate
5. Release

You must not:
- implement modules without a contract
- bypass protocols
- create hidden dependencies
- proceed without validation
- release without production proof

---

## 3. Every phase needs an Accountable Owner

Each phase must have a designated Accountable Owner before phase work begins.

The Accountable Owner is responsible for ensuring the phase is understood, delegated, executed, reviewed, and brought to completion.

The Accountable Owner does not have to perform all work personally. They may delegate tasks to other people or AI contributors. However, accountability for phase completion remains with them.

The Accountable Owner's responsibility ends only when the phase exit criteria are met and the completion celebration has occurred.

---

## 4. No implementation leakage into contracts

When working on contracts:
- do not include technologies
- do not reference APIs
- do not define code-level structures

Contracts describe behavior only.

---

## 5. Respect defined inputs and outputs

- Do not add undocumented inputs
- Do not produce undocumented outputs
- All data flow must be explicitly defined

---

## 6. Failure modes are required

Every system must define:
- what can go wrong
- how the system responds

Do not assume "happy path only."

---

## 7. Do not invent missing behavior

If something is not defined:
- do not guess
- do not assume

Instead:
> ask for clarification or mark as an open question

---

## 8. Follow constraints strictly

Constraints defined in contracts must never be violated.

---

## 9. Prefer explicitness over cleverness

- Be clear
- Be predictable
- Be consistent

Avoid:
- hidden logic
- implicit assumptions
- unnecessary abstraction

---

## 10. Validation is required

When reviewing or implementing:
- compare output against the contract
- identify mismatches
- report violations

---

## 11. Produce structured outputs

When working in COP:
- follow defined templates
- produce complete artifacts
- ensure outputs are usable by downstream phase owners and contributors
- preserve artifact handoffs from contract to protocol to architecture to stubs to implementation to validation to release

---

## 12. Prefer Feature-Based Structure

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

## 13. Align Structure to Contracts

Where possible:

- Each contract should map to a feature or module boundary
- Code organization should reflect contract boundaries
- Related logic should live together within the same feature

---

## 14. Stubs belong to the Shape phase

All modules must first be implemented as stubs.

A stub implementation:

- Must conform to the protocol interface
- Must simulate contract-defined behavior
- Must log all inputs, outputs, and decisions
- Must not perform real computation or external integration

---

## 15. Follow the COP Phase Cycle

You must follow this sequence:

1. Define: create and approve the contract
2. Shape: define protocols, architecture, boundaries, and stub demo
3. Build: replace stubs with real implementation
4. Validate: prove implementation matches the contract
5. Release: deploy and prove production behavior

---

## 16. Enforce Green Flag Progression

You must not proceed to the next phase unless the current phase is validated.

### Define Green Flag
- Contracts are complete, consistent, and unambiguous

### Shape Green Flag
- System runs end-to-end using stub modules
- Behavior matches contract expectations

### Build Green Flag
- Real system produces correct outputs
- Behavior matches stubbed system

### Validate Green Flag
- Implementation matches the contract
- Success, failure, and edge cases are verified

### Release Green Flag
- System is deployed to production
- Observable production proof shows the contract-defined behavior works

If any phase fails:

> Return to the previous phase and correct the issue

---

## 17. Preserve Behavioral Consistency

Real implementations must not introduce new behavior.

- Stub behavior defines expected system behavior
- Implementation must match that behavior exactly

---

## 18. Release requires production proof

Release is not complete when the system is merely deployed.

Release is complete only when production behavior can be proven with observable evidence, such as production smoke tests, health checks, logs, metrics, traces, user-visible verification, or other contract-aligned signals.

If the system is in production but production behavior cannot be proven, the Release phase remains incomplete.

---

## Summary

Structure must reflect behavior, not technical categories.

You are not just building code or passing work between roles.

You are:

> defining, shaping, building, validating, and releasing behavior with accountable ownership at every phase

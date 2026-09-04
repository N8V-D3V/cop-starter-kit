# Shape Phase

Version: 0.1.0

---

## Purpose

Define how the system is divided and prove the planned shape works end-to-end with stubs.

---

## Accountable Owner

The Shape phase must have a designated Accountable Owner before work begins.

The Shape Accountable Owner is responsible for ensuring protocols, architecture, module boundaries, orchestration flow, and stubs are understood, delegated, executed, reviewed, and completed.

The Accountable Owner may delegate protocol writing, architecture planning, stub implementation, or demo preparation. Accountability for completing the phase remains with the Accountable Owner.

---

## Responsibilities

- Derive protocols from approved contracts
- Define clear capability boundaries and interfaces
- Map protocols to modules and orchestration boundaries
- Define explicit dependencies and data flow
- Identify architectural risks and guardrails
- Implement stub modules and stub orchestration
- Demonstrate the contract-defined flow end-to-end using stubs

---

## Inputs

- Approved contract document
- Existing project structure, if available

---

## Outputs

- Protocol definitions using `docs/cop/protocol-template.md`
- Architecture plan using `docs/cop/architecture-plan-template.md`
- Stub modules and stub orchestration
- Stub demo notes or evidence

---

## Exit Criteria

- Protocols fully cover the contract
- Architecture preserves protocol and contract boundaries
- Dependencies and orchestration responsibilities are explicit
- Stubs conform to protocols
- Stubs simulate contract-defined behavior without real computation or external integration
- The full system flow works end-to-end using stubs

---

## Completion Celebration

The Shape phase is complete when the team can say:

> The system shape works end-to-end.

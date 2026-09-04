# COP Workflow

Version: 0.2.0

---

## Purpose

This document defines the standard COP phase workflow, accountable ownership model, and artifact handoffs.

The goal is to keep contract, protocol, architecture, stub, implementation, validation, and release work explicit, owned, and verifiable.

---

## Core Model

COP work moves through phases.

Each phase must have a designated Accountable Owner before phase work begins.

The Accountable Owner does not have to perform all work personally. They may delegate work to other people or AI contributors. However, accountability for phase completion remains with the Accountable Owner.

A phase is not complete until its exit criteria are met and the phase completion celebration has occurred.

---

## Phase Start Requirements

Before any phase begins, the team must identify:

- Phase name
- Accountable Owner
- Source artifacts or inputs
- Expected outputs
- Exit criteria

Work may be delegated after the Accountable Owner is named, but the phase must not start without clear accountability.

---

## Standard Phase Sequence

1. Define
2. Shape
3. Build
4. Validate
5. Release

---

## 1. Define

Define what the system must do.

### Accountable Owner

The Define Accountable Owner ensures the contract is understood, drafted, reviewed, and completed.

### Outputs

- Contract document
- Open questions, if behavior is unclear

### Exit Criteria

- Contract behavior is complete, consistent, and unambiguous enough to shape
- Inputs and outputs are explicit
- Success behavior, failure modes, edge cases, constraints, and acceptance criteria are defined

### Completion Celebration

> We know what this must do.

---

## 2. Shape

Define how the system is divided and prove the planned shape works end-to-end with stubs.

### Accountable Owner

The Shape Accountable Owner ensures protocols, architecture, boundaries, orchestration flow, and stubs are understood, delegated, executed, reviewed, and completed.

### Outputs

- Protocol definitions
- Architecture plan
- Stub modules and stub orchestration
- Stub demo notes or evidence

### Exit Criteria

- Protocols fully cover the contract
- Architecture preserves protocol and contract boundaries
- Dependencies and orchestration responsibilities are explicit
- Stubs conform to protocols
- The full system flow works end-to-end using stubs

### Completion Celebration

> The system shape works end-to-end.

---

## 3. Build

Replace stubs with real implementation while preserving the behavior proven in the Shape phase.

### Accountable Owner

The Build Accountable Owner ensures implementation work is understood, delegated, executed, reviewed, and completed.

### Outputs

- Real module implementations
- Real orchestration logic
- Tests, if applicable
- Implementation notes

### Exit Criteria

- Real modules conform to protocols
- Real orchestration coordinates through protocols
- Implementation does not introduce behavior outside the contract
- Real behavior matches the stubbed flow
- Defined tests pass or unresolved test gaps are documented

### Completion Celebration

> It is real now.

---

## 4. Validate

Prove the implementation matches the contract before release.

### Accountable Owner

The Validate Accountable Owner ensures the implementation, orchestration, tests, edge cases, and failure behavior are checked against the contract.

### Outputs

- Validation report
- List of mismatches, gaps, and risks
- Required corrections or release recommendation

### Exit Criteria

- Contract requirements are verified
- Success behavior is verified
- Failure behavior and edge cases are verified
- Any mismatch is corrected or explicitly documented
- The system is ready for release

### Completion Celebration

> It matches what we promised.

---

## 5. Release

Deploy the validated system and prove the released behavior works correctly in production.

### Accountable Owner

The Release Accountable Owner ensures the validated system is prepared for production, deployed through the approved release path, observed after deployment, and confirmed to be working in the production environment.

### Outputs

- Production deployment
- Production proof
- Release report

### Exit Criteria

- The validated system is deployed to production
- Required production checks have passed
- Observable production behavior matches the contract
- Production proof is collected and reviewed
- Rollback or follow-up work is documented, if needed
- The release report includes production proof

### Completion Celebration

> We can prove it works in production.

---

## Artifact Flow

1. Contract document
   - Defines behavior, inputs, outputs, success, failure, edge cases, constraints, observability, and acceptance criteria

2. Protocol definitions
   - Derive capabilities from one or more contracts
   - Define interfaces and capability boundaries
   - Preserve contract behavior without implementation logic

3. Architecture plan
   - Maps protocols to modules
   - Defines dependencies, orchestration boundaries, data flow, testing strategy, risks, and guardrails
   - Does not include production code

4. Stub implementation and stub orchestration
   - Conform to protocols
   - Simulate contract-defined behavior
   - Prove the planned system shape end-to-end before real implementation

5. Real modules and orchestrators
   - Replace stubs with real behavior
   - Stay inside module and orchestration boundaries defined by the architecture plan
   - Preserve the behavior proven by the stubs

6. Validation
   - Compares contracts against protocols, architecture, modules, orchestrators, and test results
   - Reports mismatches, gaps, risks, and required corrections

7. Release
   - Deploys the validated system
   - Proves production behavior with observable evidence
   - Reports production proof

---

## Recommended Project Structure

```text
docs/
  cop/
    phases/
    contracts/
    protocols/
    architecture/
    product/
src/
  features/
    <capability-or-contract-name>/
tests/
```

---

## Folder Guidance

- `docs/cop/phases/` contains phase role definitions and ownership expectations
- `docs/cop/contracts/` contains contract documents created from `contract-template.md`
- `docs/cop/protocols/` contains protocol documents created from `protocol-template.md`
- `docs/cop/architecture/` contains implementation plans created from `architecture-plan-template.md`
- `src/features/<capability-or-contract-name>/` contains modules and supporting code organized by capability or contract boundary
- `tests/` contains validation, module, and orchestration tests aligned to contract acceptance criteria

---

## Rules

- Each phase must have a designated Accountable Owner before work begins
- Accountable Owners may delegate work, but they remain responsible for phase completion
- A phase is not complete until its exit criteria are met and its completion celebration has occurred
- Contracts remain the source of truth
- Protocols must be derived from contracts
- Architecture plans must be derived from contracts and protocols
- Stubs must be part of the Shape phase
- Stub demos must prove the system shape end-to-end before real implementation
- Real modules must implement protocols
- Orchestrators must coordinate through protocols
- Validation must check behavior against contracts
- Release must include production proof, not just production deployment
- Do not introduce behavior in later stages that is not defined by the contract

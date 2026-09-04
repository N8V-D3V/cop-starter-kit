# COP Glossary

Version: 0.4.0

---

## Contract
A human-readable document that defines system behavior, inputs, outputs, success, failure, and constraints.

---

## Protocol
An interface that represents a capability required to fulfill a contract.

---

## Architecture
An implementation plan that maps protocols to modules, dependencies, orchestration boundaries, and data flow.

---

## Stub
A temporary implementation that conforms to a protocol, simulates contract-defined behavior, logs inputs, outputs, and decisions, and avoids real computation or external integration.

---

## Module
An implementation that fulfills one or more protocols.

---

## Orchestrator
A component that coordinates modules to execute system behavior.

---

## Phase
A named section of the COP workflow with defined responsibilities, inputs, outputs, exit criteria, and a completion celebration.

---

## Accountable Owner
The person or role responsible for ensuring a COP phase is understood, delegated, executed, reviewed, and completed.

The Accountable Owner may delegate work, but remains accountable until the phase exit criteria are met and the completion celebration occurs.

---

## Agent
An AI or human contributor that performs delegated work within a COP phase.

Agents may do work, but phases are owned by Accountable Owners.

---

## Artifact
A structured output produced during the development process (e.g., contract, protocol spec, architecture plan, validation report).

---

## Source of Truth
The authoritative definition of system behavior. In COP, this is always the contract.

---

## Validation
The process of ensuring implementation matches the contract.

---

## Release
The process of deploying validated behavior and proving that it works correctly in production.

---

## Production Proof
Observable evidence that released production behavior matches the contract.

Production proof may include production smoke tests, health checks, logs, metrics, traces, user-visible verification, or other contract-aligned signals.

---

## Constraint
A rule that must always be followed.

---

## Edge Case
A non-standard or uncommon scenario that must still be handled correctly.

---

## Failure Mode
A defined way the system can fail and how it must respond.

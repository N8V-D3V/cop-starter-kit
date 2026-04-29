# COP Starter Kit

This repository is a starter kit for teams that want to build software with Contract-Oriented Programming (COP).

COP is a development approach where contracts define system behavior first, and everything else is derived from those contracts: protocols, architecture, modules, orchestration, and validation.

## What COP Is

In COP, the contract is the source of truth.

Instead of starting with code, teams start by defining:

- what a feature must do
- what inputs it accepts
- what outputs it returns
- what success looks like
- what failure looks like
- what constraints must always hold

That contract then drives the rest of the build process.

## Why COP Helps

COP is designed to reduce the kinds of problems that show up when requirements live in scattered tickets, chats, and assumptions.

It helps solve:

- ambiguous requirements that lead to different interpretations
- hidden behavior that appears during implementation
- AI-generated code that is inconsistent or invents missing details
- architecture drift between intent and implementation
- weak handling of failures and edge cases
- reviews that focus on code style before behavior is agreed on

The core idea is simple: define behavior clearly first, then build against that definition.

Version: 0.3.0

## How To Use This Repo

You can use this repository in two common ways.

### Option 1: Use it as a GitHub template

1. Click `Use this template` on GitHub.
2. Create a new repository from this starter kit.
3. Update the root `README.md`, `AGENTS.md`, product vision, and any project metadata for your product.
4. Start writing contracts in `docs/cop/contracts/`.

### Option 2: Copy COP into an existing project

1. Copy the `docs/cop/` directory into your existing repository.
2. Add or adapt the `AGENTS.md` instructions you want your human and AI contributors to follow.
3. Create or update your product vision.
4. Author contracts before implementation work begins.

## Recommended Adoption Flow

1. Read `docs/cop/manifest.human.md` for the philosophy behind COP.
2. Read `docs/cop/manifesto.agent.md` if AI agents will contribute to the project.
3. Set product context in `docs/cop/product/product-vision.md`.
4. Create one or more contracts in `docs/cop/contracts/` using `docs/cop/contract-template.md`.
5. Derive protocols from those contracts with `docs/cop/protocol-template.md`.
6. Create an implementation plan with `docs/cop/architecture-plan-template.md`.
7. Implement modules and orchestrators only after the contract, protocol, and architecture stages are clear.
8. Validate the final behavior against the contract.

## COP Workflow

This starter kit follows the standard COP stage order:

1. Contract
2. Protocol
3. Architecture
4. Module
5. Orchestrator
6. Validation

The contract remains the source of truth at every stage. Later artifacts should clarify or implement behavior, not invent it.

## COP Files In This Repo

### Core reference documents

- `docs/cop/manifest.human.md`: explains COP for humans, including the philosophy, goals, and development cycle
- `docs/cop/manifesto.agent.md`: defines the rules AI agents must follow when working in a COP system
- `docs/cop/workflow.md`: describes the artifact handoffs and required order of work across COP stages
- `docs/cop/glossary.md`: provides shared COP terminology such as contract, protocol, module, and orchestrator

### Authoring templates

- `docs/cop/contract-template.md`: template for writing a feature contract
- `docs/cop/contract-template-usage.md`: rules for writing good contracts and avoiding implementation leakage
- `docs/cop/protocol-template.md`: template for defining a capability or interface derived from a contract
- `docs/cop/architecture-plan-template.md`: template for mapping contracts and protocols into modules, dependencies, and orchestration boundaries
- `docs/cop/report-template.md`: required structure for task completion reports in a COP workflow

### Workflow role definitions

- `docs/cop/agents/contract-agent.md`: defines the role responsible for turning requirements into contracts
- `docs/cop/agents/protocol-agent.md`: defines the role responsible for deriving capabilities and interfaces from contracts
- `docs/cop/agents/architecture-agent.md`: defines the role responsible for planning modules, dependencies, and data flow
- `docs/cop/agents/module-agent.md`: defines the role responsible for implementing protocols as concrete modules
- `docs/cop/agents/orchestrator-agent.md`: defines the role responsible for coordinating modules into end-to-end behavior
- `docs/cop/agents/validation-agent.md`: defines the role responsible for checking implementation against the contract

### Project scaffolding

- `AGENTS.md`: repo-level operating instructions for AI agents and contributors working inside this project
- `docs/cop/product/product-vision.md`: template for product-level context, goals, scope, and constraints before contracts are written
- `docs/cop/contracts/`: the folder where project-specific contracts should be created

## What A Good COP Repo Looks Like

A healthy COP project usually has:

- a clear product vision
- contracts for important features
- protocols derived from those contracts
- architecture plans before implementation begins
- feature-based code organization that reflects contract boundaries
- validation that checks behavior against the contract

## Who This Starter Kit Is For

This starter kit is useful if your team wants:

- stronger alignment between requirements and implementation
- better collaboration between humans and AI
- a predictable workflow for defining behavior before coding
- clearer failure handling and acceptance criteria

## Philosophy

Define the system clearly. Then let humans and AI build it correctly.

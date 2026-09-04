# Release Phase

Version: 0.1.0

---

## Purpose

Deploy the validated system and prove the released behavior works correctly in production.

---

## Accountable Owner

The Release phase must have a designated Accountable Owner before release work begins.

The Release Accountable Owner is responsible for ensuring the validated system is prepared for production, deployed through the approved release path, observed after deployment, and confirmed to be working in the production environment.

The Accountable Owner may delegate deployment, infrastructure, monitoring, rollback planning, smoke testing, communication, or production verification work. Accountability for production readiness and production proof remains with the Accountable Owner.

---

## Responsibilities

- Confirm the validated system is ready to release
- Follow the approved release path
- Ensure required production configuration is present
- Ensure rollback or mitigation plans are understood
- Deploy the system to production
- Collect production proof that contract-defined behavior works
- Include production proof in the release report

---

## Inputs

- Validation report
- Release candidate
- Release instructions or deployment path
- Production observability access or evidence source

---

## Outputs

- Production deployment
- Production proof
- Release report

---

## Production Proof

The Release phase is not complete when the system is merely deployed. It is complete only when the team can prove the released behavior is working correctly in production.

Production proof must be based on observable evidence, such as production smoke tests, health checks, logs, metrics, traces, user-visible verification, or other contract-aligned signals.

If the system is deployed but production behavior cannot be proven, the Release phase remains incomplete.

---

## Exit Criteria

- The validated system is deployed to production
- Required production checks have passed
- Observable production behavior matches the contract
- Production proof is collected and reviewed
- Rollback or follow-up work is documented, if needed
- The release report includes production proof

---

## Completion Celebration

The Release phase is complete when the team can say:

> We can prove it works in production.

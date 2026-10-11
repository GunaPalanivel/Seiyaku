# Product requirements

## Outcome

Build a solver-development workflow that converts optimization statements and
schemas into complete, independently checked offline solvers, improves their
objective quality under fixed budgets, and adapts to new problem families.
The competition outcome is first overall Main on the organizer's final evaluation.
Product completion and that competitive outcome are separate acceptance decisions.

## Users and workflow

Contributors implement scoped work packages and run checks. An evaluation operator
freezes legal input manifests and compares candidates. A separate custodian controls
holdouts. A release operator assembles an exact full-coverage archive and retains
the organizer's completed result for an authorized submission.

The workflow is contract -> candidate -> isolated run -> independent validation ->
complete ledger -> selected incumbent -> release. New-family adaptation uses the
same pipeline without manual changes to the framework core.

## Functional requirements

| ID | Requirement | Acceptance |
|---|---|---|
| FR01 | Capture authoritative statements, schemas, IDs, units and objectives | Versioned contract maps every hard constraint; unresolved items explicit |
| FR02 | Generate or adapt a standalone solver | Official entry point, one loader and recorded source/dependency identity |
| FR03 | Execute candidates within actual offline limits | Deadline, memory, CPU, filesystem, network and output constraints enforced |
| FR04 | Validate decisions independently | Every constraint checked; objective recomputed from trusted input bytes |
| FR05 | Account for every expected case | Complete manifest ledger; missing/failed cases cannot inflate fitness |
| FR06 | Improve and select within a frozen budget | Matched control, complete results and preserved checked incumbent |
| FR07 | Preserve selections across interruption | Immutable sources, journal recovery and exact committed selection |
| FR08 | Package all required stage problems | Missing slugs refused; exact archive clean-extracts and reruns |
| FR09 | Support bounded native-provider requests | Existing entitlement, request accounting, cancellation and quota stop |
| FR10 | Protect holdouts and adapt to new families | Generator cannot access held-out inputs/references; interventions recorded |
| FR11 | Support issue-driven delivery | Each task has dependencies, acceptance, success and verification criteria |

## Constraints

- Preserve the official starter toolkit contract; add project behavior in `competition/agent/`.
- Use the organizer's permitted image and current stage manifest. Do not infer final
  rules or private input distributions from public examples.
- Use existing subscriptions; no automatic purchased API or paid-compute fallback.
- Keep credentials, private inputs, local logs and submission archives out of public Git.
- Check rights and provenance before importing third-party source or datasets.
- Public research inputs, generated stress cases and legal real holdouts are distinct.
- No UI, model training, service deployment or large agent infrastructure is required
  unless a measured product deficit makes it necessary.

Rules source: [Main documentation](https://frontieror-challenge.com/docs).
Verify the current rules during preflight and again before each release.

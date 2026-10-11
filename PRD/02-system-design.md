# System design

## Execution flow

Statement and schemas -> named constraint contract -> applicable kernel or generated
candidate -> isolated run -> independent witness check -> complete evaluation ledger
-> targeted improvement -> protected incumbent -> exact release.

The generation workflow runs during development. Submitted solvers run offline.
Holdout evaluation is outside the generation loop.

## Components

| Planned module | Responsibility | Required boundary |
|---|---|---|
| agent/contract.py | Problem identity, schemas, objective and named hard constraints | Unresolved required constraints block promotion |
| agent/validation/ | Witness feasibility, field agreement and raw objective | Trusted input bytes; independent from reported candidate values |
| agent/evaluation.py | Frozen manifest, sandbox outcome and complete ledger | Missing outcomes preserved; infrastructure errors invalidate comparison |
| agent/provider.py, provider_bridge.py | Existing signed-in provider requests from Linux controller | Disposable allowed-input workspace, bounded errors and no solver credentials |
| agent/kernels/ | Reusable construction, timing and repair | Explicit applicability, rights and contract checks |
| agent/search.py | Budgeted improvements and selection | Checked incumbent survives failed or worse trials |
| agent/release.py | Full-stage packaging and recovery | Exact committed hashes; missing slugs or pending saves refused |

## Interfaces and records

Preserve `find_solver(problem, tools, settings) -> None` and
`solve(instance, time_limit_s) -> dict` from the official starter. Pin and record
the imported starter revision before implementation; recheck upstream policy.

| Record | Required fields |
|---|---|
| ProblemContract | Source hash, slug, objective direction, input/annotated schemas, actual output JSON Schema, IDs/units, named constraints, unresolved items |
| CandidateProgram | Raw source and rendered hashes, loader_mode, dependencies, kernel family, parent and change scope |
| ValidationResult | True/false/unresolved feasibility, recomputed objective, violations and numerical concerns |
| EvaluationManifest | Frozen case IDs/hashes, splits, deadlines, problem membership and legal reference provenance |
| EvaluationReport | Every expected outcome, process/semantic status, objective, resources, witness hash and failure reasons |
| ReleaseManifest | Stage coverage, selected solver hashes, image/dependency identity, archive hash and clean-extraction result |

Single-file candidates are the initial default. Generated bodies use the toolkit
loader; complete standalone programs disable loader appending. Record the mode
and ensure exactly one CLI main block executes.

## Trust and platform boundaries

Trusted inputs, checkers and manifests are outside candidate write access. Mount
only permitted inputs read-only; verify identities before and after execution.
The verifier reads the same trusted snapshot. A temporary directory and native
address-space limit do not prove the full runtime sandbox.

A separate custodian retains holdout inputs and references on an environment the
generation host cannot read. The model receives only permitted development material.
Do not claim a blind result unless this boundary has been verified.

The intended controller runs in Linux/WSL; existing Windows provider authentication
stays on Windows. The bridge translates only allowed scratch paths, invokes the
CLI with argument arrays, handles UTF-8 output/cancellation and returns a receipt.
It never copies auth files into solver containers or silently switches to paid APIs.

Store selected candidate sources/dependencies immutably. Journal pending saves;
verify rendered bytes before committing selection. Recover interrupted saves and
refuse any release with pending or mismatched selection identity.

## Runtime policy

Use the current organizer-permitted image, actual case deadline and package lock.
Account for imports, construction, search, validation, serialization and normal exit.
Measure resident memory and process lifetime; do not substitute virtual-memory
limits for official memory enforcement. Bound threads and worker shutdown.

Prefer compatible preinstalled open-source optimization kernels. Additional
libraries, selectors and orchestration must address a measured deficit. Submitted
solvers cannot depend on network services, model calls or commercial runtime licenses.

Rule source: [submission contract](https://frontieror-challenge.com/docs/main/submission-format).

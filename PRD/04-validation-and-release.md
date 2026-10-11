# Validation and release requirements

## Required checks

| Area | Test requirement | Acceptance |
|---|---|---|
| Contract | Separate annotated schemas from actual output JSON Schema; map every constraint | No unmapped required field/constraint can receive a feasible verdict |
| Trusted inputs | Candidate attempts to change input, checker or manifest | Write denied or comparison invalidated; verifier retains original trusted bytes |
| Objective/fields | Fake objective, wrong types, NaN/infinity, duplicates, contradictory representations | Recompute raw objective and reject invalid required decisions |
| Ledger/scoring | Missing, duplicate, malformed, timed-out and public-failed outcomes; arithmetic edges | Complete denominator; correct public failure propagation; unknown rules explicit |
| Infrastructure | Runner/checker launch failure, invalid checker JSON and stale prior report | Invalid comparison and current attempt identity; no old receipt reused |
| ODIMCF | Direction, unsplittable paths, shared capacities and rejection cost | Every commodity represented; checked decisions match raw objective |
| SPP | Sparse exact cover, side rows, duplicates and rounded MILP decisions | No dense intermediate; partition/base constraints verified |
| OP | Nonmetric feasible cycles and disconnected degree-valid subtours | Depot-connected valid cycle; absent triangle does not prove infeasibility |
| SCFLP | Shared opening, scenario capacity/demand and supplied probabilities | Scenario allocations valid and expected objective independently recomputed |
| VRPDDP | Separate delivery/pickup activities and full load trajectories | Departure/intermediate/return loads valid; expanded and detailed stops agree |
| DARP | Delayed schedules, pairing, precedence, service, capacity and ride/route duration | Complete requests and raw-distance objective; independent timing agreement |
| Runtime | Valid checkpoint followed by timeout, blocked worker and large output | Full normal exit within actual limits; checkpoint cannot rescue timeout |
| Provider | Windows/Linux paths, UTF-8, auth mode, cancellation and quota failure | Existing entitlement; errors propagated; bounded stop with no paid fallback |
| Holdout | Provider/solver attempts to read custodian inputs/references | Access unavailable; interventions recorded; contaminated results not called blind |
| Selection | Worse/crashing trial, interrupted save and mismatched dependency hash | Committed incumbent preserved; recovery works; pending selection not released |
| Packaging | Missing slug, duplicate loader, clean destinations and isolated solver folder | Exact full coverage; one main execution; every selected folder rerun |

Tests are introduced with their owning implementation work package. Repository
structure, vendor checker flags and native controls do not prove official acceptance.

## Comparison requirements

Freeze the control, candidate, inputs, budgets, seeds, references and promotion
criterion before running. Match provider/settings and total development/evaluation
allowances. Evaluate every manifest entry; candidate failures remain zero and
infrastructure failures invalidate comparisons. Keep synthetic stress cases distinct
from untouched legal real instances and fresh problem families.

Measure complete-process objective, feasibility and resources. Reveal holdouts once;
further tuning needs a new confirmation set. Record human interventions separately.
Promote only checked gains without new constraint failures or lost coverage. If
samples/references are insufficient, label the result provisional. Local proxy
scores are not organizer scores.

## Release gate

| Gate | Required evidence |
|---|---|
| Current stage | Every required slug and expected public input captured |
| Rights/dependencies | Exact source provenance, licenses, package lock and permitted image identity |
| Mathematical witness | All decisions, constraints and redundant fields agree; raw objective checked |
| Process envelope | Normal exit, CPU/memory/network/filesystem/output rules satisfied |
| Exact archive | Tested bytes, hash/size, safe paths, clean extraction and isolated folder reruns |
| Selection/rollback | Committed source/dependency identities and prior complete control retained |
| External action | User authorization for exact team/track/stage/archive |
| Official result | Completed organizer receipt; only feedback actually provided reported |

Any source, checker, dependency, image or archive change invalidates the affected
prior gate and requires fresh verification. Retain local receipts outside public Git;
publish only the approved deliverable. Official final placement is distinct from
local validation, qualification and testing-stage performance.

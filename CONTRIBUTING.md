# Contributing

Choose one reviewable work package from the [backlog](PRD/06-backlog.md) and check
its dependencies in the [phase plan](PRD/03-phased-build-plan.md). Issue creation
and assignment are team decisions, not automatic steps.

An implementation issue states the problem, inputs/outputs, affected paths,
dependencies, acceptance criteria, success criteria and verification requirements.
Keep one behavior change per PR and link an issue once it exists.

For a fix, retain the smallest failing case and verify the correction. For an
optimization, freeze control, inputs, budget and metric before running. Record
failures; infrastructure errors invalidate a comparison. Preserve the incumbent.

Run checks appropriate to the actual change and inspect the staged diff before
publication. Report results and limitations in the PR template. Keep internal
research, audit reports and working verification scripts under ignored .idea/.
Product tests are introduced with the implementation they verify.

Import third-party code or data only after checking rights and recording provenance.
Choose project licensing before distributing executable project code; this
skeleton does not select a license on the user's behalf.

No automatic assignees, CODEOWNERS, release uploads or CI verification workflow
are configured by this skeleton.

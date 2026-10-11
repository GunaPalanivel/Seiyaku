# Seiyaku

A solver-development workflow for the FrontierOR Main track.

Built for: [FrontierOR Challenge](https://frontieror-challenge.com/).

This repository contains the product requirements, issue templates and project
skeleton. Solver and framework implementation will be delivered through scoped
issues. The target outcome is first overall Main on the organizer's final evaluation.

Start with the [PRD](PRD/README.md), [build phases](PRD/03-phased-build-plan.md)
and [draft backlog](PRD/06-backlog.md). Read [CONTRIBUTING.md](CONTRIBUTING.md)
before making a change.

```text
.github/             Task, defect and experiment forms; PR template
PRD/                 Requirements, design, phases, validation, risks and backlog
competition/
  agent/             Planned contracts, evaluation, provider, search and release
    kernels/         Reusable optimization mechanisms
    validation/      Independent witness and objective validators
  solvers/           Standalone problem folders
  tests/             Implementation tests added with their owning work package
  data/              Local authorized inputs; contents ignored
  runs/              Local outputs and receipts; contents ignored
  releases/          Local submission archives; contents ignored
```

Open issues only after the team chooses the work package. Assignment will be
decided later; templates do not assign people or notify teammates automatically.

IDE files, Playwright traces, research, audit history, verifier scripts, credentials
and runtime artifacts remain local and are not part of this public repository.
There is no application install command or solver-readiness claim at skeleton stage.

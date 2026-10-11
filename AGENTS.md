# Contributor instructions

Read README.md, CONTRIBUTING.md and the relevant PRD before editing. Follow
PRD/03-phased-build-plan.md and PRD/06-backlog.md for dependencies and acceptance.
Directory READMEs reserve boundaries; they do not implement the system.

- Read actual source and contracts before deciding. Reports and checker flags
  require verification and cannot override the authoritative problem contract.
- Keep project behavior in competition/agent and standalone outputs in
  competition/solvers. Preserve the official toolkit interface when imported.
- Add decisive checks with meaningful implementation changes. Report actual
  commands, results and untested boundaries; no passing placeholder tests.
- Candidates cannot modify trusted inputs, checkers, manifests or selections.
  Recompute objectives independently and preserve checked incumbents.
- Separate local correctness, official acceptance, competitive gain and final rank.
- Keep .idea/ and .playwright-mcp/ ignored. Do not force-add research, audit history,
  verifier scripts, credentials, private inputs, raw logs or submission archives.
- Publish only material needed for the agreed deliverable. Keep working notes and
  internal verification tooling under ignored .idea/ unless explicitly requested.
- Issue creation, assignments, teammate notifications and official submissions
  require the user's authorization for those actions. Do not infer owners.
- No authorship trailers or personal attestations on the user's behalf.

# Repo and ghorg state practice

Purpose: make repository state explicit before a quest mutates anything. Every
repo observation belongs to a semantic casting under the agent home:

```text
./_/AS/👽4♦️⬆️/_/ghorgs-of/GREEDO/_/AS/<ghorg-slug>/_/AS/<repo-slug>/
```

The `👽4♦️⬆️` ghorg registry is the first and authoritative search zone for
this thread's GitHub activity. For every important ghorg and repository,
resolve the local worktree beneath that path. Do not act from a parent agent's
checkout or from an external clone. A repository action is thread-owned only
when its local worktree, remote, active branch, and provenance record can be
resolved within this subtree.

## State machine

```text
S0 workspace-only
  -> S1 checkout-discovered
  -> S2 remote-classified
  -> S3 branch-classified
  -> S4 fetch-classified
  -> S5 quest-ready
  -> S6 mutation-authorized
```

Every transition must have command evidence. If evidence is missing, remain in
the earlier state.

### S0 workspace-only

No Git root found. Record the quest and intended ghorg/repo slug; do not call
the workspace a checkout.

### S1 checkout-discovered

A Git root exists. Capture: toplevel, status, remotes, current branch.

### S2 remote-classified

- `new-repo-sparse-ghorg`: repo absent; org has existing repos.
- `new-repo-empty-ghorg`: repo absent; org is empty.
- `existing-repo`: repo metadata and remote are present.
- `remote-unknown`: API evidence failed.

### S3 branch-classified

Capture local and remote branch relations. Classify as: existing-local-with-remote,
new-local-without-remote, remote-without-local, detached-head, unborn-branch.

### S4 fetch-classified

Record one of: up-to-date, ahead-N, behind-N, diverged, no-upstream,
fetch-failed, unborn-or-no-head.

### S5 quest-ready

All must be known: quest-id, face-id, ghorg-slug, repo-slug, branch-slug,
local-root, remote-url, working-tree-status, upstream-status, fetch-status.
Write a preflight record before mutation.

### S6 mutation-authorized

Mutation requires an explicit quest instruction and a clean enough state.
Do not create a repo, branch, org, worktree, or credential merely because a
semantic path names it.

## Current observed states

### GHORGS-OF/GREEDO (2026-08-13)

```
quest-id:     GREEDO-identity
face-id:      👽4♦️⬆️
ghorg:        GHORGS-OF
repo:         GREEDO
branch:       main
local-root:   _/AS/👽4♦️⬆️/_/ghorgs-of/GREEDO/
remote-url:   https://github.com/GHORGS-OF/GREEDO
remote-state: existing-repo (created this session)
fetch-state:  up-to-date
auth:         DarienSirius admin in GHORGS-OF
```

### AWG26/t3code (2026-08-13)

```
quest-id:     T3-fork
face-id:      🔱7♥️⬇️
ghorg:        AWG26
repo:         t3code
branch:       main
local-root:   _/AS/👽4♦️⬆️/_/ghorgs-of/GREEDO/_/AS/AWG26/_/AS/t3code/ (placeholder)
remote-url:   https://github.com/AWG26/t3code
remote-state: existing-repo (forked from pingdotgg/t3code this session)
fetch-state:  no-upstream (not yet cloned locally)
auth:         DarienSirius member in AWG26; members_can_create_repos=true
notes:        dev environment (Bun) not yet installed; clone deferred
```

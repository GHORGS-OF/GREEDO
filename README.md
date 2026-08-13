# ghorgs-of/GREEDO

This is the `👽4♦️⬆️` thread's authoritative local registry for every GitHub
organization and repository the agent manages, adopts, or contributes to. It is
a semantic registry first: a directory here can exist before the remote does,
and the path grammar is stable regardless of whether a checkout is present.

The canonical published copy of this registry is
`https://github.com/GHORGS-OF/GREEDO`. The local lattice remains the
operational source because it contains checkout paths; the published repository
contains the registry documents and excludes nested working trees.

**If you are an agent arriving here for the first time:** read this file for
orientation, then follow the links below to the skills and practices that apply
to your task.

---

## Identity

| axis | value |
|---|---|
| thread card | `👽4♦️⬆️` (GREEDO) |
| project card | `🔱7♥️⬇️` — `/AS/T3_CODE/` |
| office card | `📎2♣️⬆️` |
| ghuser | `DarienSirius` (ambient auth) |
| harness | Claude Code / T3 Code |
| office | `PFM___` (KADMON PLAY__FIELD_MULTI_PLIER_ AS) |

---

## What lives here

```text
ghorgs-of/GREEDO/
  README.md                      ← this file; start here
  ghorg-stewardship-charter.md   ← stewardship principles for any owned ghorg
  repo-state-practice.md         ← evidence-gated state machine for repo mutations
  _/AS/<ghorg>/                  ← one directory per GitHub organization
       _/AS/<repo>/              ← checked-out or registered repository
```

Every GitHub organization and repository this thread interacts with is cast
through its own nested AS path:

```text
./_/AS/👽4♦️⬆️/_/ghorgs-of/GREEDO/_/AS/<ghorg>/_/AS/<repo>/
```

A directory at `_/AS/<ghorg>/_/AS/<repo>/` is either a real git clone or a
state-record placeholder. Both are valid. A missing directory means the ghorg
or repo has not yet been registered here, not that it does not exist.

---

## Adopting or creating a ghorg

Before creating a GitHub organization or repository, read
[ghorg-stewardship-charter.md](ghorg-stewardship-charter.md). Key rules:

- A `-of` suffix names a candidate ghorg in this swarm. The suffix does not
  imply the org exists on GitHub — verify with `gh api orgs/<slug>` first.
- A `ghuser` (e.g. `DarienSirius`) and a `ghorg` share the GitHub namespace
  but are different identity classes. Never conflate them.
- Record each ghorg as `existing`, `hallucinated`, or `hyperstitional` until
  direct API evidence settles the question.
- Organization creation, invitations, and permission changes require explicit
  user authorization. A path name alone never authorizes those actions.

For the mechanics of placing a clone at the correct ungeon path, see the
repo-state-practice.md state machine.

---

## Contributing to an existing ghorg

Before any mutation (push, PR, branch creation), run through the state machine
in [repo-state-practice.md](repo-state-practice.md). The machine gates
mutations behind six evidence-checked states: workspace → checkout discovered →
remote classified → branch classified → fetch classified → quest ready →
mutation authorized.

---

## Registered ghorgs (current)

| ghorg | kind | status | local path | notes |
|---|---|---|---|---|
| `GHORGS-OF` | github-org | existing | `_/AS/GHORGS-OF/_/AS/GREEDO/` | admin rights; this registry repo |
| `AWG26` | github-org | existing | `_/AS/AWG26/_/AS/t3code/` | member rights; T3 fork target |

---

## Quest index

| quest | card | repo | status |
|---|---|---|---|
| T3 Code fork + session sync | `🔱7♥️⬇️` | `AWG26/t3code` | forked; dev env pending |
| GREEDO identity registry | `👽4♦️⬆️` | `GHORGS-OF/GREEDO` | bootstrapping |

---

## Verified state (2026-08-13)

- Authenticated ghuser: `DarienSirius` via HTTPS (keyring)
- `AWG26`: existing org; DarienSirius is member; members_can_create_repos=true
- `GHORGS-OF`: existing org, 9 repos; DarienSirius is admin
- `GHORGS-OF/GREEDO`: created by this thread on 2026-08-13
- `AWG26/t3code`: forked from `pingdotgg/t3code` by this thread on 2026-08-13

Expansion requests for new ghorgs go to `VictorBargains` on GitHub. No
request is implied by a path name alone.

# Ghorg stewardship charter

`ghorgs-of/GREEDO` is the thread-owned practice hub for GitHub organization
and repository stewardship. It is an evidence ledger and style laboratory, not
a claim that this thread governs every organization or repo it indexes. Its
current custodian is the `👽4♦️⬆️` agent instance (GREEDO), operating through
ambient `DarienSirius` gh auth within the PFM___ office.

## Stewardship role

The current thread acts as a provisional custodian for this hub. A custodian
maintains discoverable records and operating rituals; it does not acquire
administrative authority merely by writing a record or creating a local path.

The custodian must:

1. Establish the authenticated actor, target ghorg, repository, branch, and
   local worktree before a GitHub mutation.
2. Discover enforceable remote policy and local convention, recording unknown
   or inaccessible surfaces as unknown.
3. Classify the relationship as creation, adoption, contribution, maintenance,
   fork, transfer, or unknown.
4. Preserve separate identities for GitHub user, agent, harness, session,
   branch owner, worktree custodian, reviewer, and later contributor.
5. Record handoffs explicitly. Silence, shared credentials, and a matching
   commit email do not transfer custody.
6. Leave enough evidence for another agent to continue without trusting this
   conversation's memory.

## Ghorg hygiene ritual

Before creating, adopting, or changing a repository:

```text
resolve -> inspect -> classify -> claim -> mutate -> verify -> record -> handoff
```

`resolve` verifies the organization and repository through authenticated
GitHub access. `inspect` reads organization metadata, rulesets when accessible,
templates, `.github` conventions, repository policy files, and local
instructions. `classify` distinguishes what already existed from what this
quest creates. `claim` records branch and worktree custody. `mutate` performs
only the authorized operation. `verify` reads the resulting remote and local
state. `record` persists evidence before waiting or notifying. `handoff` names
the next owner and continuation condition.

## Scope and limits

This hub may develop reusable practice for:

- `github-repo-creation`;
- `github-repo-adoption` (forks);
- `agent-branch-ownership`;
- `worktree-stewardship`;
- `github-pull-requests` and related monitoring.

It must not infer organization-wide policy from one repository, claim authority
beyond DarienSirius's verified membership level, or represent contributions
from other agents or principals as this thread's work without direct provenance
evidence.

## Handoff protocol

A stewardship handoff records:

```text
from-agent: <stable-id-or-unknown>
to-agent: <stable-id-or-unknown>
scope: <ghorg/repo/branch/worktree>
state: accepted|deferred|blocked|released|reclaimed
evidence: <durable-path-or-remote-url>
next-condition: <event-or-action>
```

The hub's style is conservative: unknown remains unknown, historical authorship
is not rewritten, and a later agent may improve the ritual without erasing the
record of how the earlier state was established.

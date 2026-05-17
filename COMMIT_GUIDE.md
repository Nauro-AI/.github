# Commit Messages

For squash-merged PRs, the message that lands on `main` comes from the **PR squash dialog**, not your local commits. Edit the squash subject and body to match the template below before clicking "Confirm squash and merge."

For merge-commit PRs, the template still applies to the individual commits on the feature branch.

## Template

```
<type>(<scope>): <imperative summary, ≤72 chars> (#PR)

Why: <one short paragraph. The problem, not the change.>

What changed:
- <concern>: <one-line change>
- <concern>: <one-line change>

Deferred: <optional. One line per item, with PR/issue refs.>

Refs: <optional. Decision IDs and related PR numbers.>
```

## Rules

- **Subject ≤72 chars, including `(#PR)`.** GitHub truncates around 72; `git log --oneline` wraps past that. Push decision IDs and roadmap framing into the body or `Refs:` footer.
- **`<type>` is required.** One of `feat | fix | refactor | test | docs | chore | ci | perf`. Restores `git log --grep="^feat"` filterability across history.
- **`Why:` is mandatory.** Reviewers can read the diff for what changed; they cannot recover the motivation from the diff. Lead with the problem.
- **Group by concern, not by file.** Seven file-keyed bullets usually collapse to three or four bullets keyed by logical concern. Same rule as the PR template's `What changed` section.
- **Use `Refs:` for decision IDs and PR cross-links.** `Refs: D139, #44` greps cleanly. Inline `(D139)` in the subject eats the 72-char budget and is not greppable.

## Squash-merge cleanup

When a PR has multiple commits, GitHub's default squash message concatenates them. Symptoms:

- The subject reappears verbatim as the first line of the body.
- A `* fixup: …` block appears mid-body, with its own bullet list under it.
- The body is 30+ lines because each commit's message is included in full.

Rewrite the squash dialog to the template above before merging. The fixup notes belong absorbed into the relevant `What changed` bullets.

## Trivial commits

Version bumps, dead-code drops, dependency pin bumps, pure-rename refactors, and one-line copy fixes do not need full `What changed` bullets. Type-prefixed subject plus a one-line `Why:` is enough. Same principle as the PR template default for doc and trivial PRs.

## Anti-patterns

- Restating the diff as bullets. The diff is one click away.
- Roadmap labels (`Tier 1`, `PR A/B/C`, internal milestone names, internal dates) in public repos.
- Pasting the entire PR description into the commit body. Bodies above ~25 lines usually mean the wrong content lives in `git log`.
- "Updates X to support Y" with no statement of why Y matters.
- Skipping the type prefix on substantive commits and applying it only to small ones — the split breaks `git log --grep`.

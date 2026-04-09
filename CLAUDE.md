# Pull Request Descriptions

When creating PRs (including via /commit-commands:commit-push-pr), write descriptions that serve code reviewers, not changelogs.

## Required sections

Follow the PR template in `.github/PULL_REQUEST_TEMPLATE.md`. Every PR must include:

1. **Why** — The problem or motivation. What was wrong, missing, or suboptimal? Lead with this.
2. **Approach** — The architectural choice and reasoning. If alternatives were considered or rejected (check Nauro decisions), mention them briefly.
3. **What changed** — High-level summary of module/file changes. NOT a line-by-line diff restatement. Group by logical concern, not by filename.
4. **What to review** — Direct reviewers to the non-obvious parts: tricky logic, edge cases, areas of lower confidence.
5. **What's deferred** — Anything intentionally out of scope. Reference follow-up PRs or issues if they exist.
6. **Test plan** — What was tested and how. Include test counts if meaningful (e.g., "787 existing + 12 new tests pass").

## Anti-patterns to avoid

- Do NOT just list every function/constant/filename that changed — that's what the diff is for.
- Do NOT write the summary as raw bullet points of code-level details with no narrative.
- Do NOT skip the "why" — it's the most important section.
- Do NOT describe the approach without mentioning alternatives considered.

## Tone

Write as if explaining to a teammate who knows the codebase but hasn't been in your head for the last session. Concise, direct, no filler.

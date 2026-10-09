---
name: GitLab project triage
description: >-
  Use this when you need to review or summarize a public GitLab project's open
  issues and merge requests, or watch them for changes since a previous check.
---
# GitLab project triage

## Fetch (public REST API, no login needed for public projects)
- Project id: `curl -s https://gitlab.com/api/v4/projects/<namespace>%2F<project>` (use `.id`).
- Issues: `curl -s "https://gitlab.com/api/v4/projects/<id>/issues?state=opened&order_by=updated_at&per_page=50"`
- Merge requests: `.../merge_requests?state=opened&order_by=updated_at&per_page=50`; add `state=merged` / `state=closed` with `updated_after=<ISO time>` to catch things that finished.
- Comments: `.../issues/<iid>/notes` and `.../merge_requests/<iid>/notes?order_by=created_at`.
- Pipeline status of an MR: `.../merge_requests/<iid>/pipelines` (first item is newest).
- Total counts come from the `X-Total` response header (`curl -sI`).
- Use `timeout` on every curl so a slow box doesn't hang the run.

## Watching for changes
1. Keep a small state file (last check time, and `updated_at` per issue/MR iid).
2. First run: record a baseline and report only counts plus the few most recent items.
3. Later runs: diff against the state for new issues/MRs, new comments, merged/closed/reopened items, and failed pipelines on open MRs. Save the new state.
4. If nothing changed, report nothing.

## Triage each item
- Say in one plain sentence what it is and why it matters.
- Link it as `[#123](https://gitlab.com/<ns>/<proj>/-/issues/123)` or `[!45](.../-/merge_requests/45)`.
- If a local checkout exists, name the files or area it touches (`git grep` the key terms) and whether you could fix or review it.
- Flag UI/UX items for a design review before any code change.

## Never
Comment on, approve, merge, close, or relabel anything on GitLab unless the user explicitly asks for that exact action.

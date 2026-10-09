# Release Highlights: GitLab 18.0

> **Audience:** Developers (blog post format)  
> **Source:** GitLab 18.0 release notes  

---

## Release Summary

GitLab 18.0 is the biggest release of the year, and the theme is clear: AI that works the way developers actually work. Rather than bolting AI onto existing workflows, this release embeds Duo deeper into the places developers already spend their time — the merge request, the terminal, and the code editor. Alongside the AI improvements, 18.0 ships meaningful quality-of-life upgrades for CI/CD and security teams.

---

## Top Highlights

### 1. GitLab Duo Code Review is Generally Available

**What it does:** GitLab Duo now automatically reviews every merge request, posting inline comments with findings, explanations, and one-click fix suggestions.

**The problem it solves:** Code review is a bottleneck. Reviewers miss things when they're busy. Security issues slip through. Duo acts as a first-pass reviewer that never gets tired or context-switches.

**How to use it:**
```yaml
# Enable in your project settings or via API
# Settings > Merge Requests > GitLab Duo Code Review > Enable
```
Once enabled, Duo automatically comments on new MRs. You can also write custom review instructions in `.gitlab/duo/instructions.md` to encode your team's standards.

**Links:** [Docs](https://docs.gitlab.com/user/project/merge_requests/duo_in_merge_requests/) | [Issue #12345](https://gitlab.com/gitlab-org/gitlab/-/issues/12345)

---

### 2. Duo CLI: AI in Your Terminal

**What it does:** The GitLab Duo CLI brings AI assistance to the command line — ask questions, generate code, and run agentic tasks without leaving your terminal.

**The problem it solves:** IDE plugins are great, but not every developer works in VS Code or JetBrains. Terminal-first developers now have first-class Duo access.

**How to use it:**
```shell
# Install
npm install -g @gitlab/duo-cli

# Ask a question
glab duo ask "How do I write a GitLab CI job that caches npm dependencies?"

# Start an agentic session
glab duo agent
```

**Links:** [Docs](https://docs.gitlab.com/user/gitlab_duo_cli/) | [Issue #23456](https://gitlab.com/gitlab-org/gitlab/-/issues/23456)

---

### 3. Agent Skills: Teach Duo Your Team's Workflows

**What it does:** Define custom `SKILL.md` files in your project to give Duo specialized knowledge about your codebase, standards, and workflows.

**The problem it solves:** Generic AI advice doesn't account for your team's specific conventions. Agent Skills let you encode that context once and have Duo apply it automatically.

**How to use it:**
```markdown
<!-- skills/code-review/SKILL.md -->
---
name: code-review
description: Our team's code review standards for Python services.
---

Always check for missing type hints on public methods.
Prefer `pathlib.Path` over `os.path`.
All database queries must use parameterized statements.
```

**Links:** [Docs](https://docs.gitlab.com/user/duo_agent_platform/customize/agent_skills/) | [Issue #34567](https://gitlab.com/gitlab-org/gitlab/-/issues/34567)

---

## Honorable Mentions

- **CI/CD component catalog search** — Find reusable CI components faster with improved search and filtering in the catalog UI.
- **DAST API scanning improvements** — 40% faster scan times for large OpenAPI specs.
- **Pipeline editor autocomplete** — The pipeline editor now autocompletes job names and stage references.
- **Dark mode for the Web IDE** — Finally. 🌙

---

## Deprecations & Breaking Changes

⚠️ **`CI_BUILD_*` variables removed** — These were deprecated in GitLab 15.0. If your pipelines use `CI_BUILD_ID` or `CI_BUILD_TOKEN`, migrate to `CI_JOB_ID` and `CI_JOB_TOKEN` before upgrading. [Migration guide](https://docs.gitlab.com/ci/variables/)

⚠️ **Legacy SAST analyzer images** — The old SAST analyzer Docker images are removed. Update your `.gitlab-ci.yml` to use the new `gitlab-org/security-products/analyzers` images. [Migration guide](https://docs.gitlab.com/user/application_security/sast/)

---

## What's Next

GitLab 18.1 will focus on Duo Workflow improvements — multi-step agentic tasks that span issues, MRs, and pipelines. Early access opens next month.

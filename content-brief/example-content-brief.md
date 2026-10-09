# Content Brief: How to Use GitLab Duo to Speed Up Code Review

---

## Content Type
Blog post (tutorial / how-to)

---

## Working Title
- **Primary:** "How to Use GitLab Duo to Speed Up Code Review"
- **Alt 1:** "AI Code Review with GitLab Duo: A Practical Guide"
- **Alt 2:** "Faster, Smarter Code Review: Getting Started with GitLab Duo"

---

## Goal
Education — help developers understand how to configure and use GitLab Duo Code Review in their existing workflow. Secondary goal: drive trial sign-ups from readers on free/premium plans.

---

## Target Audience
- **Who:** Mid-level to senior developers and tech leads responsible for code review on their team
- **Experience level:** Comfortable with GitLab MR workflow; no prior Duo experience required
- **What they know:** They've heard of AI code review but haven't tried it or are unsure if it's worth the setup

---

## Core Message
GitLab Duo Code Review catches real issues and explains its reasoning — and you can configure it to match your team's standards in under 10 minutes.

---

## Narrative Arc

| Phase | Content |
|-------|--------|
| **Problem** | Code review is slow and inconsistent. Reviewers miss things when they're busy or context-switching. |
| **Agitation** | Security issues that slip through review are expensive. Bottlenecked reviews slow down shipping. |
| **Solution** | GitLab Duo Code Review analyzes every MR automatically, flags issues with explanations, and lets you apply fixes in one click. |
| **Proof** | Step-by-step walkthrough with a real example: a PR with a security finding, Duo's comment, and the one-click fix. |
| **Next step** | Enable Duo on your project today; link to trial and docs. |

---

## Outline

1. **Introduction** — The code review bottleneck problem; why AI review is different from linting
2. **Prerequisites** — What you need (GitLab Ultimate, Duo enabled)
3. **How GitLab Duo Code Review works** — Brief architecture explainer; what it analyzes
4. **Step 1: Enable Duo Code Review on your project** — Settings walkthrough with screenshots
5. **Step 2: Open a merge request and see Duo in action** — Walkthrough of a real finding
6. **Step 3: Apply a suggestion** — One-click fix demo
7. **Step 4: Write custom review instructions** — How to encode team standards
8. **What Duo does well (and where human review still matters)** — Honest assessment
9. **Next steps** — Links to docs, trial, community

---

## GitLab Product Tie-in

- **GitLab Duo Code Review** — Core feature being demonstrated
- **Merge request suggestions** — Apply-suggestion workflow
- **Custom instructions** — `.gitlab/duo/instructions.md` configuration
- **GitLab Ultimate** — Required tier; link to trial

---

## SEO Keywords

**Primary:**
- AI code review
- GitLab Duo code review
- automated code review GitLab

**Secondary / long-tail:**
- how to speed up code review
- AI-assisted merge request review
- GitLab Duo getting started
- code review automation for developers

---

## Call to Action

"Enable GitLab Duo Code Review on your project today — [start a free trial](https://gitlab.com/users/sign_up) or [read the docs](https://docs.gitlab.com/user/duo_agent_platform/)."

---

## Assets Needed

- [ ] Screenshot: Duo Code Review comment on a MR diff
- [ ] Screenshot: Apply suggestion button
- [ ] Screenshot: Custom instructions file in `.gitlab/duo/`
- [ ] Code sample: Example `instructions.md` for a Python project
- [ ] GIF or short video: End-to-end flow (optional but high impact)

---

## Estimated Length
1,800–2,200 words

---

## Related Content

- [GitLab Duo Code Review docs](https://docs.gitlab.com/user/project/merge_requests/duo_in_merge_requests/)
- [Custom instructions docs](https://docs.gitlab.com/user/duo_agent_platform/customize/)
- Previous blog: "What's new in GitLab Duo" (link)

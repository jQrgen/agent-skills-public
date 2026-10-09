# Demo Plan: AI-Powered Code Review with GitLab Duo

> **Event:** KubeCon NA — Lightning Talk (10 min)  
> **Audience:** Platform engineers and developers curious about AI in CI/CD  
> **Format:** Live demo with slide intro  

---

## Overview

This demo shows how GitLab Duo Code Review automatically surfaces security issues, suggests fixes, and explains its reasoning — all inside a merge request workflow developers already use. The goal is to make AI-assisted review feel natural, not bolted-on.

---

## Audience & Context

- **Who:** Platform engineers and senior developers at KubeCon; skeptical of AI hype, value practical tooling.
- **What they care about:** Reducing review bottlenecks, catching real bugs, not slowing down shipping.
- **Format:** 10-minute lightning talk; live demo takes 6 minutes, leaving 2 min for questions.

---

## Core Narrative

| Phase | Story |
|-------|-------|
| **Before** | Code review is a bottleneck. Reviewers are busy, context-switching is expensive, and security issues slip through because nobody has time to dig into every change. |
| **Conflict** | A developer opens a merge request with a subtle SQL injection vulnerability. The human reviewer approves it — they're focused on logic, not security patterns. |
| **After** | GitLab Duo flags the vulnerability, explains why it's dangerous, and suggests a parameterized query fix — before the MR merges. The reviewer approves with confidence. |

---

## Prerequisites

- [ ] GitLab Ultimate project with Duo features enabled
- [ ] A pre-created MR with a known SQL injection vulnerability in `app/models/user.rb`
- [ ] GitLab Duo Code Review enabled on the project
- [ ] Browser logged in as demo user `devrel-demo@example.com`
- [ ] VS Code open with the branch checked out (for optional live edit)
- [ ] Fallback screenshots saved in `fallbacks/` folder on desktop

---

## Demo Steps

### Step 1 — Open the Merge Request (30 sec)

**Action:** Navigate to the pre-created MR in the GitLab UI.

**Say:** "Here's a real merge request — a developer added a new search feature. Looks reasonable at first glance. Let's see what Duo thinks."

**Audience notices:** A normal-looking MR diff.

---

### Step 2 — Trigger Duo Code Review (45 sec)

**Action:** Click **"Start review"** to invoke GitLab Duo Code Review.

**Say:** "Duo analyzes the diff automatically. It's not just linting — it understands context across the whole change."

**Audience notices:** Duo begins posting inline comments on the diff.

---

### Step 3 — Show the Security Finding (90 sec) ⭐ Key Moment

**Action:** Scroll to the inline comment flagging the SQL injection on line 42.

**Say:** "Here — Duo caught a SQL injection vulnerability. Notice it doesn't just say 'bad code.' It explains *why* this is dangerous, shows the attack vector, and suggests a parameterized query as the fix."

**Audience notices:** The explanation is readable, not cryptic. The suggested fix is copy-pasteable.

---

### Step 4 — Apply the Suggestion (60 sec) ⭐ Key Moment

**Action:** Click **"Apply suggestion"** directly in the MR UI.

**Say:** "One click. The fix is committed. No context switch to the IDE, no copy-paste. The reviewer can approve knowing the issue is resolved."

**Audience notices:** The commit appears instantly; the comment thread resolves.

---

### Step 5 — Show the Summary (45 sec)

**Action:** Scroll to the Duo-generated MR summary at the top of the discussion.

**Say:** "Duo also writes a plain-English summary of what changed and why — useful for async reviewers who need context fast."

**Audience notices:** The summary is accurate and saves reading the full diff.

---

## Key Moments

1. **The security finding** — The moment Duo surfaces the SQL injection with a clear explanation. Pause here.
2. **Apply suggestion** — One-click fix inside the MR. This is the "wow" moment for developers used to context-switching.
3. **MR summary** — Reinforces that Duo helps the whole team, not just the author.

---

## Timing

| Section | Time |
|---------|------|
| Slide intro / narrative setup | 2 min |
| Steps 1–2 (open MR, trigger review) | 1 min 15 sec |
| Step 3 (security finding) | 1 min 30 sec |
| Step 4 (apply suggestion) | 1 min |
| Step 5 (MR summary) | 45 sec |
| Call to action | 30 sec |
| **Total** | **~7 min** |

---

## Fallback Plan

| Step | Fallback |
|------|----------|
| Duo Code Review doesn't load | Open `fallbacks/duo-review-comment.png` — annotated screenshot of the finding |
| Apply suggestion fails | Show the before/after diff in `fallbacks/fix-diff.png` and describe the change |
| MR summary missing | Skip and move directly to call to action — the security finding is the core story |

---

## Call to Action

"If you want to try this on your own project, GitLab Duo Code Review is available on GitLab Ultimate. Scan the QR code for a 60-day trial link — and come find me after the talk if you want to talk about how to roll this out for your team."

---

## Notes & Rehearsal Log

| Date | Notes |
|------|-------|
| — | Add rehearsal notes here |

# Community Response Example: Frustrated User on Reddit

> **Channel:** Reddit — r/gitlab  
> **Original post:** "GitLab Duo keeps suggesting code that doesn't even compile. I've tried it on three different projects and it's consistently wrong. Is anyone else seeing this or is it just me? Starting to think this is vaporware."

---

## Channel Context

Reddit — conversational, skeptical audience. Redditors distrust corporate-sounding responses. Be a human, not a spokesperson. Avoid marketing language entirely. Upvote the post before responding if possible to signal good faith.

---

## Sentiment Read

**Frustrated + skeptical.** The person has tried the feature multiple times and feels let down. The word "vaporware" signals they're questioning whether the product is real/useful at all — this is a trust issue, not just a technical one. They're also asking if others share the experience, which means they want validation.

---

## Draft Response

> Hey — this is a real frustration and I don't want to brush it off. I work on DevRel at GitLab so I have some context here.
>
> Code suggestions that don't compile are a known pain point, especially in languages with complex type systems or when the surrounding context (imports, type definitions) isn't fully visible to the model. It's not vaporware — but it's also not where we want it to be yet.
>
> A few things that tend to help:
> - Make sure the file has enough context above the cursor — Duo uses the surrounding code as its window, so incomplete files or heavily abstracted codebases can trip it up
> - Check which model is active in your settings; some perform better for specific languages
> - For compiled languages especially, the inline suggestions work better when the file compiles cleanly before you start editing
>
> That said — if you're seeing consistent failures across three projects, I'd genuinely like to know more. What languages/frameworks? Are you on a self-managed instance or GitLab.com? Happy to dig in or route this to the right team.
>
> And yes, others have reported similar issues — there's an open issue tracking suggestion quality for compiled languages here: [link]. Worth adding your case if the details match.

---

## Escalation Recommendation

**Route to product/engineering** if the user responds with specific reproduction details. Link them to the existing issue tracker thread. If they mention a self-managed instance with a specific version, route to support.

---

## Content Opportunity

**Yes — high signal.** This question likely reflects a broader gap in documentation around:
- How Duo uses context windows for code suggestions
- Language-specific performance expectations
- How to configure Duo for best results in compiled languages

**Recommended action:** Flag for a "Tips for better Duo suggestions" blog post or FAQ entry. Check if this question has appeared in Discord or the GitLab Community forum in the past 30 days.

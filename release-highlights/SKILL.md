---
name: release-highlights
description: Translate release notes and changelog entries into audience-friendly highlights for blogs, social posts, and talks. Focuses on the "so what" for developers rather than feature lists.
---

## Release Highlights

This skill helps DevRel team members transform raw release notes, changelog entries, and product announcements into compelling, audience-focused content. Release notes describe what changed; release highlights explain why it matters and what developers can do with it.

### Highlight Structure

When asked to create release highlights, produce:

1. **Release summary** — One paragraph: what's the theme of this release? What problem does it primarily address?
2. **Top highlights** — 3–5 features or changes, each with:
   - Feature name and one-line description
   - The problem it solves (from the developer's perspective)
   - A concrete example of how to use it
   - Link to docs or issue
3. **Honorable mentions** — 2–4 smaller improvements worth noting, in brief.
4. **Deprecations / breaking changes** — Any removals or changes developers need to act on.
5. **What's next** — 1–2 sentences on what's coming in the next release (if known).

### Audience Adaptation

Adapt the same release content for different audiences:

| Audience | Focus | Format |
|----------|-------|--------|
| Developers (blog) | Workflow impact, code examples | Long-form, technical |
| Social (Twitter/X) | Single best feature, punchy | 1–3 posts, emoji OK |
| Newsletter | Top 3 highlights, curated | 200–300 words, links |
| Conference talk | Story arc across releases | Narrative, demos |
| Internal (team update) | Business impact, metrics | Bullet points, brief |

### Writing Guidelines

- **Lead with the problem, not the feature name.** "You can now do X" is weaker than "If you've ever struggled with Y, X solves that."
- **Use before/after framing.** Show what the workflow looked like before and after the change.
- **Include a code snippet or screenshot for every major highlight.** Abstract descriptions don't stick.
- **Avoid superlatives.** "Exciting," "powerful," and "game-changing" are filler. Show, don't tell.
- **Link everything.** Every feature should link to its docs page and the issue/MR where it was built.
- **Credit contributors.** For community contributions, name the contributor.

### Changelog Triage

When given a raw changelog, categorize entries as:

- 🌟 **Top highlight** — Significant user-facing improvement; warrants a full write-up
- ✅ **Honorable mention** — Useful improvement; one-liner is enough
- 🔧 **Internal / infrastructure** — Not user-facing; skip unless it affects performance
- ⚠️ **Breaking change** — Must be called out clearly
- 🗑️ **Deprecation** — Note with migration path

### Output Format

Use the example in `example-release-highlights.md` as a reference for tone and depth. Adapt to the specific release version, changelog, and target audience provided by the user.

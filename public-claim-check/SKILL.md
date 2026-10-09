---
name: Public claim check
description: >-
  Use this when any post, slide, web page, email, talk abstract, press note,
  paper or announcement is about to go public, or when an internal technical doc
  others will build on (architecture doc, spec, guide) is being finalised, to
  verify every number and technical claim against a real source and fix
  overstated wording.
---
# Public claim check

Run this on any draft meant for the public, such as social posts, slides, landing pages, emails, talk abstracts, press notes and papers. Also run it on internal technical docs that others will build on, such as architecture docs, specs and guides.

## Steps
1. **List every claim.** Pull out each number, date, performance figure, comparison ("faster than", "first", "only", "fastest"), feature status, technical statement, quote and citation into a table with these columns: claim, where in the draft, source, status.
2. **Find a primary source for each.** Prefer these, in order:
   - live data you measured yourself (node RPC, analytics, API);
   - the project's merged source code or spec, at a named file and line;
   - a peer-reviewed paper (with DOI) or official release notes;
   - reputable secondary coverage.
   Record the link or path next to each claim. For a code claim, pin the evidence: repo, file:line, and the commit SHA or release tag, so a reviewer can open the exact line later.
   - Check code claims against the merged default branch, not unmerged branches or open merge requests. A commit hash cited in a draft must exist on a merged branch, or the draft must say it doesn't.
   - Cite protocol parameters (timings, sizes, constants) from the code and official docs, not from local test runs, which often use easy difficulty or toy settings.
   - When the spec, old marketing and the code disagree, the code and the latest posts from its owners win.
3. **Verify behaviour, not just names.**
   - Check the layer that actually serves the feature. A node, an indexer or API server, a library and a wallet can each behave differently. A claim like "apps get X" must hold in the layer the app actually calls.
   - Trace the real call path. Don't infer what a parameter does from its name; follow the code to what it actually changes.
   - Confirm that checks actually fire. A validation that always evaluates to a no-op (for example a mask that is 0) does not enforce anything.
   - Keep SDK or config defaults separate from deployed infrastructure. Don't describe an endpoint, port or service as available until someone has confirmed it is really reachable.
   - Search open issues and bug trackers before stating behaviour, because known bugs change the guidance.
4. **Classify each claim.**
   - Verified: the source says exactly this.
   - Needs softening: the source supports a weaker version, so rewrite it to match.
   - Unverified: no source was found, so remove it or mark it clearly as a placeholder. Never publish it.
5. **Apply the wording rules.**
   - Feature status says exactly what is true: write "implemented, activation pending", not "live". Don't give a date until the release or activation date is confirmed in code or by the owners, and watch for placeholder dates (for example an activation time set far in the future).
   - Keep what is live in production or on mainnet separate from what is staged on a test network. Label staged work in the same sentence ("staged on testnet"), and never imply real-world behaviour from a simulation or demo.
   - Measured results say what was measured, where and over what window, for example "last 24 h, measured on a mainnet node". Always give n, the network and the date.
   - No superlatives without a source.
6. **Hold back early performance numbers.** Keep figures such as time to first transaction internal until there are at least three runs after the relevant fixes, partly done by different people. Report before-fix and after-fix runs separately and never pool them.
7. **Don't promote an unproven path.** Don't promote an onboarding path (a "start building" call, a tutorial, a faucet or other on-ramp) until it has passed a fresh end-to-end run.
8. **Credit the right people.** Check commit authors and credit work to whoever actually did it. A human developer whose name matches an AI agent's persona is still the human, so their work doesn't count as the agent team's output.
9. **Check that dates and status are current.** For anything time-sensitive (release dates, activation heights, prices, download counts, event dates), re-check on the day you publish, not when you drafted.
10. **Check the links and citations.** Every URL resolves and points to what the text says it does, and every cited paper actually says what the draft claims.
11. **Route open questions to an owner.** List unconfirmed points as numbered open questions, each with a named owner. Keep the conservative wording until they answer, then update the claim with a cited source.
12. **Report back** with the corrected draft plus the claim table (claim, source, status). Flag anything removed or softened, and anything that still needs an owner to confirm, so the owner can decide.

## Rules
- Never invent a figure, quote or citation to fill a gap.
- If two sources disagree (for example the spec against the shipped code), say so and use the more conservative wording.

---
name: cfp-writer
description: >
  Use this when the user wants a conference or meetup talk proposal (CFP / Call for Papers submission) written from a topic and the speaker's real background. Trigger on "write a CFP", "submit a talk to X", "draft a conference proposal", "talk proposal", or "turn this project/post into a talk". Asks for the CFP's actual constraints before drafting, then produces title options, abstract, audience and learning outcomes, timed outline, short and long bios, and format fit.
---

# CFP Writer

Turn a topic and a speaker's real experience into a talk proposal reviewers accept. A great CFP submission is specific, audience-focused, and makes the reviewer's job easy. Generic proposals get rejected; concrete, well-scoped ones get accepted.

## Step 1: Get the CFP's actual constraints

Before drafting, ask for (or read from a provided CFP link/text):
- Abstract length limit and any separate fields (elevator pitch, talk details, audience takeaways)
- Talk formats and lengths offered (lightning, full session, workshop, panel)
- The conference's audience and selection bent (intro-friendly? hard-technical? case-study-driven?)
- Submission deadline and whether it's anonymized review (anonymized = no self-references in the abstract)

Drafting to imaginary constraints wastes the work. If the user has no CFP yet, draft to a generic 150-300-word abstract and flag it.

## Step 2: Find the talk inside the topic

A topic is not a talk. Work with the user to sharpen:
- **The claim:** what will the audience believe after that they didn't before?
- **The evidence:** what real experience backs it: a project shipped, a failure survived, data gathered? Talks built on the speaker's actual scars beat surveys of a topic.
- **The takeaway:** what can attendees *do* Monday morning?

If the user's material is thin, say so and identify what experience they do have that's talk-worthy.

## Step 3: Match the event's tone

Tailor the abstract to the event's audience. A KubeCon abstract reads differently than a DevOpsDays one.

| Event Type | Tone | Emphasis |
|------------|------|----------|
| KubeCon / CloudNativeCon | Technical, practitioner | Architecture, real-world scale |
| DevOpsDays | Practitioner, storytelling | Culture, process, lessons learned |
| OSCON / Open Source Summit | Community, breadth | Ecosystem, contribution, interop |
| GitHub Universe / GitLab Commit | Product-adjacent | Workflows, developer experience |
| Local meetups | Conversational, accessible | Demos, Q&A, community |

## Step 4: Draft

```markdown
# CFP: [conference]

**Format:** [chosen format/length]
**Deadline:** [date]

## Title options

1. [punchy: specific + outcome or tension: "We Cut Onboarding From 14 Steps to 6.
   Here's What Fought Back."]
2. [descriptive]
3. [problem-led / safer conventional option]

## Abstract ([X words / limit Y])

[Hook sentence: the tension or claim, leading with the problem the audience
feels. What the talk covers, concretely. Who it's for. What they leave with.
Written to the reviewer AND the attendee scanning a schedule.]

## Audience

- Who: [role]
- Experience level and prior knowledge: [what they should already know]

## Learning outcomes / audience takeaways

- [3-5, each concrete and actionable, not "understand X better"]

## Outline (for the details field / reviewer notes)

- [minute-budgeted beats: problem (5) → story/demo (15) → lessons (8) → Q&A (2)]

## Why this speaker

[2-3 sentences connecting the speaker's real experience to this topic.]

## Bio

- Short (~75 words, or the CFP's limit)
- Long (~150 words)

[Relevant credibility for THIS talk, not a resume.]

## Format fit

[Would this work as a lightning talk, full session, workshop, or panel? What changes?]

## Reviewer notes (if the CFP has the field)

[Why this conference, why now, what's new vs. existing talks on the topic.
Mention prior speaking honestly, including "first-time speaker" if true;
many conferences actively want them.]
```

A fill-in template is in [references/talk-proposal-template.md](references/talk-proposal-template.md).

## Writing rules

- Specific beats comprehensive. "How we measured developer activation at a 12-person startup" outranks "The State of DevRel Metrics" in every review pile.
- Lead with the problem, not the solution. Reviewers respond to proposals that name a pain the audience feels.
- No marketing language ("revolutionary", "game-changing", "powerful") and no clickbait the talk can't pay off. Reviewers have seen everything.
- Use active voice and present tense in the abstract.
- Promise only what fits the time slot. A 30-minute talk holds one claim well.
- Never invent the speaker's experience, credentials, or war stories. The bio and evidence come from what the user actually did.
- Match abstract length limits exactly; overlong abstracts get truncated or binned.

## Examples

- A complete sample of this skill's output: [references/example-output.md](references/example-output.md).
- A full-session example with title variants, learning outcomes and two-length bios: [references/example-talk-proposal.md](references/example-talk-proposal.md).

## Scope

This skill writes the proposal. It does not:
- Write the talk or slides (plan the live demo with `demo-planning`, or script a recorded one with `demo-script`)
- Submit anything
- Find conferences to submit to (use `developer-events-scouting`; this skill can suggest fit criteria if asked)

# Event Recap: KubeCon NA 2024

> **Date:** November 12–15, 2024  
> **Location:** Salt Lake City, UT  
> **Format:** In-person conference  
> **Author:** Jane Smith, Senior Developer Advocate  

---

## Event Overview

KubeCon NA 2024 drew approximately 12,000 attendees to Salt Lake City for four days of cloud native talks, workshops, and hallway conversations. GitLab participated as a Gold Sponsor with a booth in the Solutions Showcase, two accepted talks, and a co-hosted co-located event on Day 0. The event is the largest gathering of the CNCF community and a key venue for understanding where platform engineering and cloud native development are heading.

---

## GitLab Presence

- **Booth:** Solutions Showcase, Aisle 4 — staffed by 6 team members across 3 days
- **Talk 1:** "AI Code Review for Platform Engineers" — Jane Smith (Main stage, Day 2)
- **Talk 2:** "GitLab CI/CD Components: Building a Reusable Pipeline Library" — Alex Johnson (Breakout, Day 3)
- **Co-located event:** Platform Engineering Day (Day 0) — GitLab co-hosted with Backstage and Port
- **Hallway presence:** Informal demos and conversations throughout

---

## Key Takeaways

1. **Platform engineering is maturing, but internal developer portals are still messy.** Most teams have a portal, but few are happy with it. Backstage adoption is high but maintenance burden is a recurring complaint. Opportunity for GitLab to position the catalog and CI components as lower-maintenance alternatives.

2. **AI skepticism is real but softening.** A year ago, AI demos got eye-rolls. This year, the question shifted from "does this work?" to "how do I make it work for my team?" Practitioners want specifics, not promises.

3. **Security is moving left, but tooling is fragmented.** Teams are running 4–6 security tools in their pipelines. There's appetite for consolidation. GitLab's unified security scanning story resonated strongly at the booth.

4. **Rust is everywhere.** Multiple talks referenced Rust for systems components. Worth considering Rust-specific content and Duo optimization for Rust codebases.

5. **Community contributors want recognition.** Several contributors mentioned feeling invisible in large projects. Recognition programs and contributor spotlights came up as high-value, low-cost investments.

---

## Talk / Session Recaps

### "AI Code Review for Platform Engineers" — Jane Smith

- **Attendance:** ~400 (room was at capacity; ~50 turned away)
- **Summary:** Walked through how GitLab Duo Code Review works for IaC-heavy repositories, including a live demo of a Terraform PR with a misconfiguration finding. Covered custom review instructions and metrics for measuring impact.
- **Audience reaction:** Strong engagement during Q&A; 3 questions about self-managed support, 2 about pricing. Applause at the one-click fix demo moment.
- **Resources:** [Slides](https://example.com/slides) | [Recording](https://example.com/recording)

### "GitLab CI/CD Components: Building a Reusable Pipeline Library" — Alex Johnson

- **Attendance:** ~180
- **Summary:** Practical walkthrough of building and publishing CI/CD components to the GitLab catalog. Included a live example of a reusable SAST component.
- **Audience reaction:** Positive; several attendees asked for the component repo link after the talk.
- **Resources:** [Slides](https://example.com/slides) | [Component repo](https://gitlab.com/example)

---

## Community Sentiment

**Excited about:**
- AI that explains its reasoning (not just flags issues)
- CI/CD components and reusability
- GitLab's unified platform story vs. tool sprawl

**Frustrated with:**
- Duo not being available on self-managed instances without extra configuration
- Pricing complexity ("I can never remember what's in which tier")
- YAML fatigue in CI/CD configuration

**Repeated questions:**
- "Does Duo work with self-managed?" (came up 20+ times at the booth)
- "How is this different from GitHub Copilot?"
- "Can I use the CI component catalog with my existing pipelines?"

---

## Competitive Intelligence

- **GitHub** had a large presence focused on Copilot Workspace. Messaging centered on "agentic coding" — similar to our Duo Workflow positioning. Their booth traffic appeared high.
- **JFrog** announced deeper Kubernetes integration for Artifactory. Relevant to our artifact management story.
- **Harness** was aggressive on CI/CD messaging, specifically targeting GitLab customers with migration offers. Worth flagging to product marketing.

---

## Metrics

| Metric | Value |
|--------|-------|
| Event attendance | ~12,000 |
| Booth badge scans | 847 |
| Talk 1 attendance | ~400 |
| Talk 2 attendance | ~180 |
| Social mentions (@gitlab) | 312 over 4 days |
| New Discord members (event week) | +89 |
| Demo requests from booth | 43 |

---

## Follow-up Actions

| Action | Owner | Due |
|--------|-------|-----|
| Publish talk recordings to GitLab YouTube | Alex | Nov 22 |
| Write blog post: "What we learned at KubeCon NA 2024" | Jane | Nov 25 |
| File issue: self-managed Duo setup documentation gap | Jane | Nov 18 |
| Share competitive intel with product marketing | Jane | Nov 18 |
| Follow up with 43 demo request leads | SDR team | Nov 18 |
| Propose Rust content series to content team | Alex | Dec 1 |

---

## Content Opportunities

- **Blog:** "What platform engineers are really thinking about in 2024" (based on hallway conversations)
- **Blog:** "5 questions we got asked 20 times at KubeCon" (addresses the self-managed Duo question and others)
- **Video:** Talk recordings + short highlight clips for social
- **Docs:** Improved self-managed Duo setup guide (addresses top booth question)

---

## What to Do Differently

**What worked:**
- Live demos at the booth drove the most meaningful conversations
- Co-located event on Day 0 gave us warm leads before the main conference started
- Having a dedicated "question catcher" at the booth to log repeated questions was valuable

**What didn't work:**
- Booth swag ran out by Day 2 — order 30% more next time
- Talk submission was too late; we missed the best time slots
- No coordinated social posting strategy during the event — missed amplification opportunities

**Changes for next time:**
- Submit CFP 2 weeks before the deadline, not the day of
- Assign one person as social lead during the event
- Pre-order swag with a buffer; confirm quantities 3 weeks out

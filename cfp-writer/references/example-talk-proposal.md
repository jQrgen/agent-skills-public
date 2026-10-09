# Talk Proposal: GitLab Duo for Platform Engineers

> **Event:** KubeCon NA — Full Session (30 min)  
> **Speaker:** Jane Smith, Senior Developer Advocate  
> **Topic:** Using AI code review in a platform engineering context  

---

## Title Options

1. **"Your AI Reviewer Never Sleeps: GitLab Duo in Platform Engineering Workflows"** *(punchy)*
2. **"Integrating AI Code Review into Internal Developer Platforms"** *(descriptive)*
3. **"From Bottleneck to Baseline: AI-Assisted Review for Platform Teams"** *(problem-led)*

---

## Abstract (Public)

Code review is one of the biggest bottlenecks in platform engineering. Platform teams maintain sprawling infrastructure-as-code repositories, and reviewers are constantly context-switching between Terraform, Helm charts, Kubernetes manifests, and custom controllers. Security issues slip through. Approvals pile up. Developers wait.

In this session, we'll walk through how platform teams at GitLab are using GitLab Duo Code Review to catch real issues — misconfigurations, security anti-patterns, and drift from internal standards — before they reach production. We'll cover how to configure Duo for IaC-heavy repositories, how to write custom review instructions that encode your team's standards, and how to measure whether AI review is actually helping.

You'll leave with a practical playbook for introducing AI-assisted review to your platform team, including what works, what doesn't, and how to get skeptical senior engineers on board.

---

## Outline (Reviewer-Only)

- **0:00–3:00** — The platform review bottleneck: data and a story from a real team
- **3:00–8:00** — How GitLab Duo Code Review works (architecture, what it sees, what it doesn't)
- **8:00–18:00** — Live demo: Duo reviewing a Terraform PR with a misconfiguration and a security finding
- **18:00–23:00** — Configuring custom review instructions for IaC standards
- **23:00–27:00** — Measuring impact: metrics that matter and ones that mislead
- **27:00–30:00** — Q&A

---

## Audience

- **Who:** Platform engineers, SREs, and DevOps leads responsible for internal developer platforms
- **Experience level:** Intermediate to advanced; comfortable with Kubernetes and IaC
- **Prior knowledge:** No GitLab experience required; familiarity with code review workflows assumed

---

## Learning Outcomes

1. Understand how GitLab Duo Code Review analyzes IaC and infrastructure changes
2. Configure custom review instructions to encode team-specific standards
3. Identify which types of findings AI review handles well vs. where human review is still essential
4. Define metrics to evaluate whether AI review is reducing bottlenecks
5. Build a rollout plan for introducing AI review to a skeptical platform team

---

## Why This Speaker

Jane has spent three years working with platform engineering teams at enterprises adopting GitLab. She has run workshops on IaC review practices at DevOpsDays and contributed to GitLab's internal platform engineering documentation. She brings practitioner credibility, not just product advocacy.

---

## Speaker Bio

**Short (75 words)**  
Jane Smith is a Senior Developer Advocate at GitLab focused on platform engineering and AI-assisted development workflows. She works with enterprise platform teams to improve developer experience through better tooling and practices. Jane has spoken at KubeCon, DevOpsDays, and HashiConf, and contributes to open source projects in the CNCF ecosystem. She lives in Austin, TX.

**Long (150 words)**  
Jane Smith is a Senior Developer Advocate at GitLab where she focuses on platform engineering, infrastructure-as-code, and AI-assisted development workflows. With a background in site reliability engineering, Jane brings a practitioner's perspective to developer tooling — she's been on the other side of the review queue and knows what it costs when the process breaks down.

Over the past three years, Jane has worked directly with enterprise platform teams adopting GitLab, running workshops on IaC review practices, internal developer portals, and CI/CD standardization. She has spoken at KubeCon, DevOpsDays Chicago, and HashiConf, and contributes to open source projects in the CNCF ecosystem including Backstage plugins and Crossplane providers. Outside of work, she co-organizes the Austin Platform Engineering meetup and mentors early-career engineers transitioning into DevOps roles.

---

## Format Fit

- **Full session (30 min):** ✅ Ideal — enough time for live demo and nuanced discussion
- **Lightning talk (5 min):** ⚠️ Possible — cut to demo only, drop metrics section
- **Workshop (90 min):** ✅ Strong fit — hands-on configuration exercises could be added
- **Panel:** ❌ Not ideal — too demo-dependent

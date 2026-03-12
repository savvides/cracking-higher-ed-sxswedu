# Cracking Higher Ed: Why Startups Miss the Mark

**A diagnostic framework for EdTech founders selling into higher education.**

Presented at [SXSW EDU 2026](https://www.sxswedu.com/) by [Philippos Savvides](mailto:philippos.savvides@asuep.org), Head of [ScaleU](https://scaleu.org) at ASU Enterprise Partners.

---

## The problem

EdTech startups fail in higher ed not because their products are bad, but because they validate with the wrong people, measure the wrong outcomes, and mistake enthusiasm for demand.

The average higher ed sales cycle is 12-18 months. EdTech VC funding hit $2.4B in 2024, the lowest since 2014. Most startups don't survive long enough to close a single institutional sale. The margin for error is zero.

This repo contains the framework from the SXSW EDU talk, designed to help founders distinguish real institutional demand from false positives before they run out of runway.

## What's in this repo

```
/deck              Slide deck (.pptx and .pdf)
/diagnostic        The 5-question diagnostic as a standalone tool
README.md          The full framework (you're reading it)
LICENSE            CC BY 4.0
```

## The framework

### 1. Map your product to the student journey

Every EdTech product maps to a stage in the learner lifecycle. Your stage determines your buyer, your evidence requirements, and your competitive density.

| Phase | What happens | Status |
|-------|-------------|--------|
| **Pre-enroll** | Readiness evaluation, transfer credit research, financial aid exploration | Underserved |
| **Apply** | Application submission, transcript processing, admissions decisions | Underserved |
| **Onboard** | Credit articulation, advising, system familiarization | Underserved |
| **Select & enroll** | Course selection, academic scheduling, degree planning | Underserved |
| **Course experience** | Active learning, assessment, instructor interaction, support | Saturated (15+ product categories) |
| **Graduate & beyond** | Career transition, alumni engagement, credentialing | Partial coverage |

80% of EdTech founders build for Course Experience. The biggest opportunities are in the first four phases, where pain is quantified at scale but product coverage is thin.

### 2. Define the job for the person, not the institution

The market is not "universities." The market is a specific person with a specific job at a specific journey stage. Use the Jobs to Be Done framework:

| The person | The job | What they hire |
|-----------|---------|---------------|
| Prospective student (Pre-enroll) | Understand if my credits transfer before I commit | Transfer credit evaluation tool |
| Academic advisor (Select & enroll) | Guide 300 students to the right courses each term | Degree planning intelligence |
| Faculty member (Course experience) | Give meaningful feedback to 200 students per section | AI grading with learning diagnostics |
| Career services director (Graduate & beyond) | Connect graduates to employers at scale | Talent pipeline platform |

**The test:** if you cannot name the person, the job, and the journey phase, you do not have a market. You have a hypothesis.

### 3. Identify the buyer, not just the user

The same product serves different jobs for different stakeholders. A retention analytics tool:

| Stakeholder | Their job | What they need from a pilot |
|------------|-----------|---------------------------|
| **Academic advisor** | Faster triage of at-risk students | Operational dashboard proving time savings |
| **VP of Student Affairs** | Reduce DFW rates to justify budget | Outcome data showing measurable improvement |
| **Provost** | Strategic plan metrics for the board | Year-over-year retention numbers |

The advisor is the most accessible. The advisor also doesn't control the budget. If you validate with the user but not the buyer, you get enthusiasm without procurement.

### 4. Separate noise from signal

| Noise (false positive) | Signal (real demand) |
|----------------------|---------------------|
| "Faculty love it" | Budget holder named a specific line item |
| "10,000 student signups" | Pilot measured outcomes the buyer needs |
| "The dean said transformative" | Procurement started before pilot ended |
| "3 pilot champions" | Product survives if any champion leaves |

**The pattern:** noise comes from users and champions. Signal comes from buyers and processes.

### 5. Build the moat that AI can't replicate

Pure software without structural defensibility faces substitution risk within 18 months. Locate your product on the spectrum:

| Exposure | Description | Timeline |
|----------|------------|----------|
| **High** | Content generation, summarization, Q&A, template output | Replicable in 12-18 months |
| **Moderate** | AI embedded in workflow or dataset with switching costs | Replicable in 2-4 years |
| **Low** | Structural moat that AI substitution cannot dissolve | Defensible for 3+ years |

Four moats that move you toward defensibility:

- **Proprietary data network:** Longitudinal data that improves with usage and cannot be reconstructed by a new entrant
- **Deep integration:** LTI/SIS write-back creating operational switching costs that exceed the product's price
- **Supply-side network effects:** More providers, mentors, or contributors increase quality for all existing users
- **Regulated access:** FERPA, HIPAA, or credentialing compliance that LLM wrappers cannot clear

**The reframe:** lead with the institutional dependency you create, not the technology you use.

## The 5-question diagnostic

Use before, during, or after any pilot. Full standalone version in [`/diagnostic`](./diagnostic/).

1. **Who is struggling, and what is the struggling moment?** If you can't name a specific person with a specific problem, you have a hypothesis, not a job.
2. **What have they already tried (and why did it fail)?** Your competition isn't other EdTech. It's spreadsheets, grad students, and ignoring the problem.
3. **Is there a budget line item?** "Interesting" vs. "funded" is the only filter that matters.
4. **What happens if they do nothing?** "We lose accreditation" is a job. "Students might learn better" is a hypothesis.
5. **Who else must say yes?** If the answer is "just me," the pilot succeeds and procurement fails.

## About ScaleU

[ScaleU](https://scaleu.org) is ASU's EdTech validation program. We broker paid pilots between early-stage EdTech companies and Arizona State University's institutional infrastructure, generating the evidence founders need to fundraise and sell at enterprise scale.

## Contact

Philippos Savvides
Head, ScaleU | ASU Enterprise Partners
philippos.savvides@asuep.org
[scaleu.org](https://scaleu.org) | [LinkedIn](https://linkedin.com/in/savvides) | [X](https://x.com/savvides)

## License

This work is licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). You are free to share and adapt this material for any purpose, provided you give appropriate attribution.

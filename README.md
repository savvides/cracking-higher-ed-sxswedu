# Cracking Higher Ed: Why Startups Miss the Mark

**A diagnostic framework for EdTech founders selling into higher education.**

Presented at [SXSW EDU 2026](https://www.sxswedu.com/) by [Philippos Savvides](mailto:philippos.savvides@asuep.org), Head of [ScaleU](https://scaleu.org) at ASU Enterprise Partners.

---

## The problem

EdTech startups fail in higher ed not because their products are bad, but because they validate with the wrong people, measure the wrong outcomes, and mistake enthusiasm for demand.

The average higher ed sales cycle is 12-18 months. EdTech VC funding hit $2.4B in 2024, the lowest since 2014. Most startups don't survive long enough to close a single institutional sale. The margin for error is zero.

This framework helps founders, administrators, and investors distinguish real institutional demand from false positives — before startups run out of runway.

## Who this is for

- **EdTech founders** — validate demand before you burn runway on a 12-month sales cycle
- **University administrators** — evaluate vendor claims using the same framework your peers use internally
- **Investors and accelerators** — assess whether a portfolio company has real institutional signal or just enthusiasm

## What's in this repo

```
README.md          The full framework (you're reading it)
/diagnostic        The 5-question diagnostic as a standalone tool
/deck              SXSW EDU 2026 slide deck (.pptx and .pdf)
/assets            Social preview image
CONTRIBUTING.md    How to share case studies or propose new job statements
CHANGELOG.md       Version history
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

---

## Part 2: The jobs behind the journey

The framework above is the quick filter. Part 2 goes deeper: a catalog of validated jobs across the student journey, structural patterns that most founders miss, and pressure-test probes for each diagnostic question. If you're past the "is this a real opportunity?" stage and into "how do I build the right evidence?", keep reading.

### 6. Jobs atlas: what people actually need at each phase

Every phase in the student journey contains specific jobs that real people need done. The jobs below are drawn from research across large-scale online programs. Each one names the person, the struggling moment, what they've already hired, and why it fails. If your product maps to one of these jobs, you have a starting point. If it doesn't map to any of them, pressure-test whether the job you've identified is real.

**Pre-enroll**

1. **Cost expectation gap**
   - The person: Prospective student evaluating online programs
   - The struggling moment: Cannot determine what they will actually pay (tuition + fees + materials) until after enrolling
   - What they've hired: Googling, calling admissions, comparing sticker prices across program websites
   - Why it fails: Published tuition rates exclude per-credit fees, online surcharges, and textbook costs; financial aid amounts are unknown until after commitment
   - The job: "Help me understand what I'll actually pay before I have to commit"

2. **Course-level decision info missing**
   - The person: Prospective student choosing between programs or courses
   - The struggling moment: Cannot access syllabi, workload expectations, difficulty indicators, or textbook requirements before enrolling
   - What they've hired: Rate My Professor, Reddit, guesswork based on course titles
   - Why it fails: Third-party sources are unreliable and incomplete; course expectations are shaped by uncontrolled channels rather than the institution
   - The job: "Help me know what a course actually demands before I sign up for it"

3. **Format comprehension gap**
   - The person: Prospective student unfamiliar with accelerated online formats
   - The struggling moment: Does not understand what compressed session formats mean in practice for daily and weekly workload
   - What they've hired: Nothing — the information gap is invisible until they experience it
   - Why it fails: Marketing describes format in calendar terms ("7.5 weeks"), not workload terms ("15+ hours per week alongside your job")
   - The job: "Help me understand what this pace will actually feel like in my life"

**Apply**

4. **Admissions speed vs. competitors**
   - The person: Prospective student applying to multiple online programs
   - The struggling moment: Admissions decisions and transcript processing are slower than competing programs
   - What they've hired: Applying to multiple institutions simultaneously; choosing whichever responds first
   - Why it fails: The fastest responder captures the enrollment, regardless of program quality
   - The job: "Help me get a decision fast enough that I don't commit somewhere else first"

5. **Transcript processing bottleneck**
   - The person: Transfer student with credits from multiple institutions
   - The struggling moment: Cannot get credit articulation completed before enrollment deadline
   - What they've hired: Phone calls, emails, waiting
   - Why it fails: Manual evaluation processes cannot scale to the volume or complexity of multi-institution transfer students
   - The job: "Help me know which of my credits count before I have to decide"

**Onboard**

6. **Transfer credit confusion**
   - The person: Newly admitted student with prior credits
   - The struggling moment: Does not know how prior credits map to degree requirements until after committing; discovers redundant or missing courses after enrollment
   - What they've hired: Contacting advisors, manually comparing transcripts to degree requirements
   - Why it fails: Credit articulation results arrive after the enrollment commitment, causing wasted courses and money
   - The job: "Help me see exactly where I stand in my degree before I start spending"

7. **Post-admission communication void**
   - The person: Newly admitted student
   - The struggling moment: Receives acceptance notification and then no proactive guidance on what to do next
   - What they've hired: Nothing — students either figure it out or disengage
   - Why it fails: The gap between acceptance and course start is an information dead zone
   - The job: "Help me know what I'm supposed to do between getting accepted and starting my first class"

8. **Format readiness**
   - The person: Newly admitted student about to start an accelerated online program
   - The struggling moment: Has no practical preparation for the pace, workload management, or online learning tools before courses begin
   - What they've hired: Orientation modules (inconsistently available), time management advice from general web searches
   - Why it fails: Generic orientation does not simulate the actual experience; readiness interventions exist but are inconsistently deployed across programs
   - The job: "Help me be ready for what's coming before week 1 hits"

**Select & enroll**

9. **Course info for decisions**
   - The person: Enrolled student choosing courses for the next term
   - The struggling moment: Must commit to courses based on title alone; no access to syllabi, workload expectations, or difficulty ratings before registration
   - What they've hired: Rate My Professor, peer recommendations, Reddit, guesswork
   - Why it fails: Information arrives after enrollment, not before; expectation mismatches lead to drops
   - The job: "Help me pick courses I won't have to drop"

10. **Course availability**
    - The person: Enrolled student trying to stay on track for graduation
    - The struggling moment: Required courses are full, offered only once a year, or have scheduling conflicts
    - What they've hired: Overloading on courses when available, delaying graduation, transferring institutions
    - Why it fails: Supply does not match demand; online programs still inherit seat-limited scheduling from in-person models
    - The job: "Help me get into the courses I need when I need them"

11. **Sequencing and advising**
    - The person: Enrolled student unsure which courses to take and in what order
    - The struggling moment: Cannot determine the right course sequence; advising is hard to access and inconsistent across departments
    - What they've hired: Degree audit tools (confusing), advisor appointments (hard to get, inconsistent quality), peer advice
    - Why it fails: Advising models vary by department; degree audit tools are unintuitive; students get conflicting guidance
    - The job: "Help me know exactly what to take next without needing to decode the system"

12. **Degree audit comprehension**
    - The person: Enrolled student trying to track progress toward graduation
    - The struggling moment: Degree audit tools are unintuitive and do not clearly communicate remaining requirements
    - What they've hired: Manual tracking, advisor meetings, spreadsheets
    - Why it fails: The tools designed to answer "what do I still need?" do not answer it clearly
    - The job: "Help me see a clear, plain-language picture of what's left between me and graduation"

**Course experience**

This phase is saturated with products. The two jobs below are structural — they sit on the provider side, not the student side. That's where the underserved opportunity is.

13. **Instructor capacity constraint → student experience**
    - The person: Faculty member teaching large online sections
    - The struggling moment: Class sizes make personalized feedback impossible; forced to rely on templated responses; students disengage because feedback feels generic
    - What they've hired: Templates, reduced assignment scope, TA support where available
    - Why it fails: The feedback loop (more students → less time per student → worse feedback → worse outcomes) is structural, not solvable by individual effort
    - The job: "Help me give meaningful feedback to every student without working unsustainable hours"
    - Founder note: Students report "teaching myself" and "absent instructors." Faculty independently report burnout and unsustainable workload. These are the same problem described from two sides. Tools that solve the faculty capacity job solve the student experience job as a byproduct — and the faculty side is where the budget sits.

14. **Support access gaps**
    - The person: Student needing academic support (tutoring, writing help, math help)
    - The struggling moment: Cannot access effective tutoring or does not know it exists; compounds the self-teaching perception
    - What they've hired: YouTube, Khan Academy, peer help, struggling alone
    - Why it fails: Support services exist but are disconnected from the course experience and hard to find at the moment of need
    - The job: "Help me get help the moment I'm stuck, not after I've already fallen behind"

**Graduate & beyond**

15. **Career transition**
    - The person: Graduating student or recent graduate
    - The struggling moment: Degree is complete but the connection between credential and career outcome is unclear or unsupported
    - What they've hired: LinkedIn, personal networking, generic career services
    - Why it fails: Career services at scale lack the capacity or employer relationships to serve online graduates with the same intensity as residential students
    - The job: "Help me turn this degree into the career outcome I enrolled for"
    - Founder note: This phase is the least researched and least served in the entire learner lifecycle. Most institutions have minimal data on post-graduation outcomes. The gap between "graduated" and "got the job or promotion they came for" is wide open.

### 7. Patterns founders miss

Four structural dynamics that are not visible from surface-level discovery interviews.

**Pattern 1: The information sequencing trap**

Most online programs front-load commitment (apply, enroll, pay) and back-load information (syllabi, credit evaluation, true costs, workload expectations). Students commit based on incomplete information, discover reality does not match expectations, and then either struggle through or withdraw.

Founders who build for the downstream symptom — a retention intervention, a student success dashboard — miss the upstream cause. The student never had the information to make a good decision in the first place.

*Example:* Students enroll without knowing what a 7.5-week accelerated term actually demands. They hit week 1, experience workload shock, and drop. A retention tool flags them as "at risk" in week 2. But the real failure point was months earlier, when no one translated "7.5-week session" into "15+ hours per week on top of your job."

*Founder takeaway:* If your product catches people after they've made a bad decision, ask whether you could help them make a better decision earlier. The upstream job is usually less crowded and higher-leverage.

**Pattern 2: The upstream cause / downstream symptom split**

Pattern 1 described one specific instance of this dynamic (commitment before information). Here is the general principle: pain points show up in one phase of the journey but originate 1-2 phases earlier. When you interview struggling students, you hear about the phase where they are suffering. The real opportunity is usually in the phase where the information gap or broken process set them up to struggle.

| Downstream symptom | Upstream cause |
|-------------------|---------------|
| Student drops a course in week 2 (Course experience) | No syllabus or workload info available at registration (Select & enroll) |
| Student discovers redundant courses after enrolling (Onboard) | Transfer credits evaluated after enrollment commitment (Apply) |
| Student hit with unexpected bill (Onboard) | Financial aid amount unclear before enrollment (Pre-enroll) |
| Student overwhelmed by pace (Course experience) | Accelerated format not explained in practical terms (Pre-enroll) |
| Student takes wrong course sequence (Course experience) | Advising unavailable or inconsistent (Select & enroll) |

*Founder takeaway:* When you hear a pain point, ask "what happened one phase earlier that made this inevitable?" Build for the cause, not the symptom.

**Pattern 3: When qualitative and quantitative evidence disagree**

Every stakeholder group tells you the same thing: "X is the problem." Students say it, faculty say it, advisors say it. Then the outcome data says X actually produces *better* results.

This happens more often in higher ed than founders expect. Qualitative data overrepresents the people who struggled (they have complaints to register), while the silent majority who succeeded leave no trace in interview data. Selection bias, survivorship bias, and domain specificity all contribute.

*Example:* Across large online programs, accelerated course formats are universally perceived as the primary driver of student attrition. But controlled outcome analyses in specific disciplines find that students in shorter sessions actually pass at higher rates and withdraw less. The perception is driven by the students who drop (loud signal) while the students who thrive (silent majority) do not show up in pain point data.

*Founder takeaway:* If every stakeholder tells you the same story, that is a signal to validate quantitatively before building. Unanimous qualitative agreement can be a bias artifact, not confirmation. Check the outcome data. If it contradicts the narrative, the real opportunity may be different from what everyone is asking for.

**Pattern 4: Same problem, two job descriptions**

Students describe one experience: "I'm teaching myself," "feedback is generic," "the instructor is absent." Faculty independently describe the mirror image: "class sizes are unsustainable," "I can't give real feedback to 200 students," "I'm burning out."

These are tracked by institutions as separate problems in separate reports. They are the same structural constraint described from two positions. Growing enrollment increases class sizes, which reduces time per student, which degrades feedback quality, which causes students to disengage.

*Founder takeaway:* When you hear a student experience problem, find out whether the provider is reporting the same problem from the other side. If so, the tool that solves the provider's capacity job often solves the student's experience job as a byproduct — and the provider side is where the budget and procurement authority sit.

### 8. Validation depth: pressure-testing your diagnostic answers

Each diagnostic question from Part 1 has deeper probes that connect back to the patterns above.

**Question 1: Who is struggling, and what is the struggling moment?**

Depth probes:
- Is the struggling moment in the phase where the person *experiences* the pain, or is it caused upstream? Trace the causal chain back one phase. (→ Pattern 2)
- Is the struggling moment structural (happens to everyone in that role at that phase) or situational (happens to a subset)? Structural jobs have larger markets.

Watch for: If the struggling moment is "students drop out" or "retention is low," you are describing a symptom. Keep asking why until you reach the decision point where things went wrong. The job lives at the decision point, not at the outcome.

**Question 2: What have they already tried (and why did it fail)?**

Depth probes:
- Are they using workarounds that technically function but do not scale? Spreadsheets, grad students, and unofficial tool substitutions are signs of a real job with no adequate solution.
- Have they tried solving the downstream symptom without addressing the upstream cause? If prior solutions targeted the wrong phase, your opportunity is the phase they have not addressed.

Watch for: If "nobody's tried anything," either the job is not painful enough to pay for, or you are talking to the wrong person. Real jobs always have workarounds — even bad ones.

**Question 3: Is there a budget line item?**

Depth probes:
- Does the budget sit with the person who experiences the pain, or someone else? If the user and the buyer are different people, you need the job statement for both.
- Can you connect the job to a line item the buyer already has? (Student success funding, retention budget, IT modernization, accreditation compliance)

Watch for: Pattern 4 applies here. The student feels the pain but the provider controls the budget. When talking to the budget holder, lead with the provider's job, not the student's experience. "Reduce grading turnaround from 5 days to 1" lands differently than "students feel they're teaching themselves."

**Question 4: What happens if they do nothing?**

Depth probes:
- Is the cost of inaction quantified or merely perceived? "We lose students" is perceived. "We lose $X in tuition revenue from students who drop after discovering their credits don't transfer" is quantified. Help the buyer do the math.
- Does the institution even *know* the cost of inaction? Many costs are distributed across departments and invisible to any single stakeholder.

Watch for: Pattern 3 applies here. If the stated cost of inaction is based on stakeholder perception, check whether outcome data tells the same story. If every stakeholder says "the accelerated format is killing retention" but the data says otherwise, the real cost of inaction may be somewhere else entirely.

**Question 5: Who else must say yes?**

Depth probes:
- For each approver in the chain, what is *their* job? IT's job is risk mitigation. Legal's job is compliance. Finance's job is ROI. Your pitch must address each approver's job separately.
- Have you mapped the full approval chain *before* the pilot starts? (IT security review, legal/compliance, finance/procurement, faculty governance if touching curriculum, accessibility review)

Watch for: If you have only validated with users and champions, you have enthusiasm without procurement. The pilot will succeed and the deal will die. Map every node in the approval chain and understand what job each node needs done before they will say yes.

---

The 5-question diagnostic gives you the quick filter. The depth probes give you the evidence quality you need to survive the 12-18 month sales cycle described in Part 1. Before committing to a pilot, make sure you can answer every depth probe — not just the headline question.

## About ScaleU

[ScaleU](https://scaleu.org) is ASU's EdTech validation program. We broker paid pilots between early-stage EdTech companies and Arizona State University's institutional infrastructure, generating the evidence founders need to fundraise and sell at enterprise scale.

## Contact

Philippos Savvides
Head, ScaleU | ASU Enterprise Partners
philippos.savvides@asuep.org
[scaleu.org](https://scaleu.org) | [LinkedIn](https://linkedin.com/in/savvides) | [X](https://x.com/savvides)

## License

This work is licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). You are free to share and adapt this material for any purpose, provided you give appropriate attribution.

## Use the framework as AI skills

The jobs atlas, founder traps, and 5-question diagnostic from this talk are encoded as interactive AI skills in the **EdTech Founder Stack**:

**[github.com/savvides/edtechfounderstack](https://github.com/savvides/edtechfounderstack)**

10 AI skills. 376 peer-reviewed papers. Run `/idea-validation` in Claude Code and the framework from this talk becomes an interactive diagnostic that adapts to your specific product and market. Free. MIT licensed.

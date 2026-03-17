# Design: JTBD-Informed README Expansion

**Date:** 2026-03-17
**Status:** Draft
**Audience:** EdTech founders selling into higher education
**Approach:** Two-Speed README (Approach C)

---

## Goal

Expand the existing SXSW EDU README with a "Part 2: Going Deeper" section that gives EdTech founders (1) a richer catalog of validated JTBD-framed opportunities across underserved student journey phases, (2) structural pattern recognition skills drawn from real UX research, and (3) deeper validation techniques layered onto the existing 5-question diagnostic.

No institution names, tool names, or specific data points from the source research. All content generalized to "large-scale online programs" or equivalent framing.

---

## Constraints

- Part 1 of the README stays exactly as-is
- No ASU attribution or identifiable details
- All examples generalized from the UX research patterns
- Single document (no companion files)
- Numbering continues from existing sections 1-5

---

## Structure

Part 2 is inserted after the existing "The 5-question diagnostic" section and before "About ScaleU." This places the deeper content immediately after the framework content, keeping "About ScaleU," "Contact," and "License" as unchanged footer sections. Part 2 begins with a horizontal rule and a short intro paragraph:

> The framework above is the quick filter. Part 2 goes deeper: a catalog of validated jobs across the student journey, structural patterns that most founders miss, and pressure-test probes for each diagnostic question. If you're past the "is this a real opportunity?" stage and into "how do I build the right evidence?", keep reading.

```
---

## Part 2: The jobs behind the journey

### 6. Jobs atlas: what people actually need at each phase
### 7. Patterns founders miss
### 8. Validation depth: pressure-testing your diagnostic answers
```

---

## Section 6: Jobs Atlas

### Purpose

Expand the existing journey phase table (Section 1) into a phase-by-phase catalog of 15 validated job statements (3 + 2 + 3 + 4 + 2 structural + 1 = 15). Underserved/undercovered phases get deep treatment. Course Experience gets 2 shorter "structural jobs" (counted in the 15) framed from the provider side to steer founders away from the saturated middle. Each job entry should be 60-120 words in the final README, rendered as a bullet list (not a table) matching the format shown in the entries below.

### Format per job

Each job follows this structure:

| Element | Description |
|---------|-------------|
| **The person** | Specific role (prospective student, academic advisor, etc.) |
| **The struggling moment** | The concrete situation where they cannot do what they need to do |
| **What they've hired today** | Current workaround (spreadsheets, Reddit, grad students, ignoring it) |
| **Why it fails** | Why the workaround doesn't solve the real job |
| **The job statement** | One sentence capturing what they actually need |

### Phase coverage

**Pre-enroll (3 jobs)**

Phase names match Part 1 exactly. Where the research phase is referenced, it is folded into "Pre-enroll" since Part 1 uses that label.

1. **Cost expectation gap**
   - Person: Prospective student evaluating online programs
   - Struggling moment: Cannot determine what they will actually pay (tuition + fees + materials) until after enrolling
   - Hired today: Googling, calling admissions, comparing sticker prices across program websites
   - Why it fails: Published tuition rates exclude per-credit fees, online surcharges, and textbook costs; financial aid amounts are unknown until after commitment
   - Job: "Help me understand what I'll actually pay before I have to commit"

2. **Course-level decision info missing**
   - Person: Prospective student choosing between programs or courses
   - Struggling moment: Cannot access syllabi, workload expectations, difficulty indicators, or textbook requirements before enrolling in a course
   - Hired today: Rate My Professor, Reddit, guesswork based on course titles
   - Why it fails: Third-party sources are unreliable and incomplete; course expectations are shaped by uncontrolled channels
   - Job: "Help me know what a course actually demands before I sign up for it"

3. **Format comprehension gap**
   - Person: Prospective student unfamiliar with accelerated online formats
   - Struggling moment: Does not understand what compressed session formats (e.g., 7.5-week terms) mean in practice for daily/weekly workload
   - Hired today: Nothing — the information gap is invisible until they experience it
   - Why it fails: Marketing describes format in calendar terms ("7.5 weeks"), not workload terms ("15 hours/week alongside your job")
   - Job: "Help me understand what this pace will actually feel like in my life"

**Apply (2 jobs)**

4. **Admissions speed vs. competitors**
   - Person: Prospective student applying to multiple online programs
   - Struggling moment: Admissions decisions and transcript processing are slower than competing programs
   - Hired today: Applying to multiple institutions simultaneously; choosing whichever responds first
   - Why it fails: The fastest responder captures the enrollment, regardless of program quality
   - Job: "Help me get a decision fast enough that I don't commit somewhere else first"

5. **Transcript processing bottleneck**
   - Person: Transfer student with credits from multiple institutions
   - Struggling moment: Cannot get credit articulation completed before enrollment deadline
   - Hired today: Phone calls, emails, waiting
   - Why it fails: Manual evaluation processes cannot scale to the volume or complexity of multi-institution transfer students
   - Job: "Help me know which of my credits count before I have to decide"

**Onboard (3 jobs)**

6. **Transfer credit confusion**
   - Person: Newly admitted student with prior credits
   - Struggling moment: Does not know how prior credits map to degree requirements until after committing; discovers redundant or missing courses after enrollment
   - Hired today: Contacting advisors, manually comparing transcripts to degree requirements
   - Why it fails: Credit articulation results arrive after the enrollment commitment, causing wasted courses and money
   - Job: "Help me see exactly where I stand in my degree before I start spending"

7. **Post-admission communication void**
   - Person: Newly admitted student
   - Struggling moment: Receives acceptance notification and then no proactive guidance on what to do next
   - Hired today: Nothing — students either figure it out or disengage
   - Why it fails: The gap between acceptance and course start is an information dead zone
   - Job: "Help me know what I'm supposed to do between getting accepted and starting my first class"

8. **Format readiness**
   - Person: Newly admitted student about to start an accelerated online program
   - Struggling moment: Has no practical preparation for the pace, workload management, or online learning tools before courses begin
   - Hired today: Orientation modules (inconsistently available), time management advice from general web searches
   - Why it fails: Generic orientation doesn't simulate the actual experience; readiness interventions exist but are inconsistently deployed across programs
   - Job: "Help me be ready for what's coming before week 1 hits"

**Select & Enroll (4 jobs)**

9. **Course info for decisions**
   - Person: Enrolled student choosing courses for the next term
   - Struggling moment: Must commit to courses based on title alone; no access to syllabi, workload expectations, or difficulty ratings before registration
   - Hired today: Rate My Professor, peer recommendations, Reddit, guesswork
   - Why it fails: Information arrives after enrollment, not before; expectation mismatches lead to drops
   - Job: "Help me pick courses I won't have to drop"

10. **Course availability**
    - Person: Enrolled student trying to stay on track for graduation
    - Struggling moment: Required courses are full, offered only once a year, or have scheduling conflicts
    - Hired today: Overloading on courses when available, delaying graduation, transferring institutions
    - Why it fails: Supply doesn't match demand; online programs still inherit seat-limited scheduling from in-person models
    - Job: "Help me get into the courses I need when I need them"

11. **Sequencing and advising**
    - Person: Enrolled student unsure which courses to take and in what order
    - Struggling moment: Cannot determine the right course sequence; advising is hard to access and inconsistent across departments
    - Hired today: Degree audit tools (confusing), advisor appointments (hard to get, inconsistent quality), peer advice
    - Why it fails: Advising models vary by department; degree audit tools are unintuitive; students get conflicting guidance
    - Job: "Help me know exactly what to take next without needing to decode the system"

12. **Degree audit comprehension**
    - Person: Enrolled student trying to track progress toward graduation
    - Struggling moment: Degree audit tools are unintuitive and do not clearly communicate remaining requirements
    - Hired today: Manual tracking, advisor meetings, spreadsheets
    - Why it fails: The tools designed to answer "what do I still need?" don't answer it clearly
    - Job: "Help me see a clear, plain-language picture of what's left between me and graduation"

**Course Experience (2 structural jobs)**

Framed as structural/provider-side jobs, not "build another LMS feature."

13. **Instructor capacity constraint → student experience**
    - Person: Faculty member teaching large online sections
    - Struggling moment: Class sizes make personalized feedback impossible; forced to rely on templated responses; students disengage because feedback feels generic
    - Hired today: Templates, reduced assignment scope, TA support where available
    - Why it fails: The feedback loop (more students → less time per student → worse feedback → worse outcomes) is structural, not solvable by individual effort
    - Job: "Help me give meaningful feedback to every student without working unsustainable hours"
    - **Founder note:** Students report "teaching myself" and "absent instructors." Faculty independently report burnout and unsustainable workload. These are the same problem. Tools that solve the faculty capacity job solve the student experience job as a byproduct — and the faculty/department side is where the budget sits.

14. **Support access gaps**
    - Person: Student needing academic support (tutoring, writing help, math help)
    - Struggling moment: Cannot access effective tutoring or does not know it exists; compounds the self-teaching perception
    - Hired today: YouTube, Khan Academy, peer help, struggling alone
    - Why it fails: Support services exist but are disconnected from the course experience and hard to find at the moment of need
    - Job: "Help me get help the moment I'm stuck, not after I've already fallen behind"

**Graduate & beyond (1 job + opportunity note)**

15. **Career transition**
    - Person: Graduating student or recent graduate
    - Struggling moment: Degree is complete but the connection between credential and career outcome is unclear or unsupported
    - Hired today: LinkedIn, personal networking, generic career services
    - Why it fails: Career services at scale lack the capacity or employer relationships to serve online graduates with the same intensity as residential students
    - Job: "Help me turn this degree into the career outcome I enrolled for"
    - **Founder note:** This phase is the least researched and least served in the entire learner lifecycle. Most institutions have minimal data on post-graduation outcomes. The gap between "graduated" and "got the job/promotion they came for" is wide open.

---

## Section 7: Patterns Founders Miss

### Purpose

Teach founders to recognize structural dynamics in higher ed that aren't visible from surface-level discovery. Four patterns, each ~150-200 words with a concrete generalized example and a one-line takeaway.

### Pattern 1: The Information Sequencing Trap

Most online programs front-load commitment (apply, enroll, pay) and back-load information (syllabi, credit evaluation, true costs, workload expectations). Students commit based on incomplete information, discover reality doesn't match expectations, and then either struggle through or withdraw.

Founders who build for the downstream symptom — a retention intervention, a student success dashboard — miss the upstream cause. The student never had the information to make a good decision in the first place.

**Example:** Students enroll without knowing what a 7.5-week accelerated term actually demands. They hit week 1, experience workload shock, and drop. A retention tool flags them as "at risk" in week 2. But the real failure point was months earlier, when no one translated "7.5-week session" into "15+ hours per week on top of your job."

**Founder takeaway:** If your product catches people after they've made a bad decision, ask whether you could help them make a better decision earlier. The upstream job is usually less crowded and higher-leverage.

### Pattern 2: The Upstream Cause / Downstream Symptom Split

Pattern 1 described one specific instance of this dynamic (commitment before information). Here is the general principle: pain points show up in one phase of the journey but originate 1-2 phases earlier. When you interview struggling students, you hear about the phase where they're suffering. The real opportunity is usually in the phase where the information gap or broken process set them up to struggle.

| Downstream symptom | Upstream cause |
|-------------------|---------------|
| Student drops a course in week 2 (Course Experience) | No syllabus or workload info available at registration (Select & Enroll) |
| Student discovers redundant courses after enrolling (Onboard) | Transfer credits evaluated after enrollment commitment (Apply) |
| Student hit with unexpected bill (Onboard) | Financial aid amount unclear before enrollment (Research) |
| Student overwhelmed by pace (Course Experience) | Accelerated format not explained in practical terms (Research) |
| Student takes wrong course sequence (Course Experience) | Advising unavailable or inconsistent (Select & Enroll) |

**Founder takeaway:** When you hear a pain point, ask "what happened one phase earlier that made this inevitable?" Build for the cause, not the symptom.

### Pattern 3: When Qualitative and Quantitative Evidence Disagree

Every stakeholder group tells you the same thing: "X is the problem." Students say it, faculty say it, advisors say it. Then the outcome data says X actually produces *better* results.

This happens more often in higher ed than founders expect. The pattern: qualitative data overrepresents the people who struggled (they have complaints to register), while the silent majority who succeeded leave no trace in interview data. Selection bias, survivorship bias, and domain specificity all contribute.

**Example:** Across large online programs, accelerated course formats are universally perceived as the primary driver of student attrition. But controlled outcome analyses in specific disciplines find that students in shorter sessions actually pass at higher rates and withdraw less. The perception is driven by the students who drop (loud signal) while the students who thrive in the format (silent majority) don't show up in pain point data.

**Founder takeaway:** If every stakeholder tells you the same story, that's a signal to validate quantitatively before building. Unanimous qualitative agreement can be a bias artifact, not confirmation. Check the outcome data. If it contradicts the narrative, the real opportunity may be different from what everyone is asking for.

### Pattern 4: Same Problem, Two Job Descriptions

Students describe one experience: "I'm teaching myself," "feedback is generic," "the instructor is absent." Faculty independently describe the mirror image: "class sizes are unsustainable," "I can't give real feedback to 200 students," "I'm burning out."

These are tracked by institutions as separate problems in separate reports. They are the same structural constraint described from two positions. Growing enrollment increases class sizes, which reduces time per student, which degrades feedback quality, which causes students to disengage.

**Founder takeaway:** When you hear a student experience problem, find out whether the provider is reporting the same problem from the other side. If so, the tool that solves the provider's capacity job often solves the student's experience job as a byproduct — and the provider side is where the budget and procurement authority sit.

---

## Section 8: Validation Depth

### Purpose

Layer deeper validation probes onto the existing 5-question diagnostic. Each question gets 2-3 depth probes and a "watch for" callout that connects back to the patterns from Section 7.

### Question 1: Who is struggling, and what is the struggling moment?

**Depth probes:**
- Is the struggling moment in the phase where the person *experiences* the pain, or is it caused upstream? Trace the causal chain back one phase. (→ Pattern 2)
- Is the struggling moment structural (happens to everyone in that role/phase) or situational (happens to a subset)? Structural jobs have larger markets.

**Watch for:** If the struggling moment is "students drop out" or "retention is low," you're describing a symptom. Keep asking why until you reach the decision point where things went wrong. The job lives at the decision point, not at the outcome.

### Question 2: What have they already tried (and why did it fail)?

**Depth probes:**
- Are they using workarounds that technically function but don't scale? Spreadsheets, grad students, and unofficial tool substitutions are signs of a real job with no adequate solution.
- Have they tried solving the downstream symptom without addressing the upstream cause? If prior solutions targeted the wrong phase, your opportunity is the phase they haven't addressed.

**Watch for:** If "nobody's tried anything," either the job isn't painful enough to pay for, or you're talking to the wrong person. Real jobs always have workarounds — even bad ones.

### Question 3: Is there a budget line item?

**Depth probes:**
- Does the budget sit with the person who experiences the pain, or someone else? If user and buyer are different people, you need the job statement for both.
- Can you connect the job to a line item the buyer already has? (Student success funding, retention budget, IT modernization, accreditation compliance)

**Watch for:** Pattern 4 applies here. The student feels the pain but the provider controls the budget. When talking to the budget holder, lead with the provider's job, not the student's experience. "Reduce grading turnaround from 5 days to 1" lands differently than "students feel they're teaching themselves."

### Question 4: What happens if they do nothing?

**Depth probes:**
- Is the cost of inaction quantified or merely perceived? "We lose students" is perceived. "We lose $X in tuition revenue from students who drop after discovering their credits don't transfer" is quantified. Help the buyer do the math.
- Does the institution even *know* the cost of inaction? Many costs are distributed across departments and invisible to any single stakeholder.

**Watch for:** Pattern 3 applies here. If the stated cost of inaction is based on stakeholder perception, check whether outcome data tells the same story. If every stakeholder says "the accelerated format is killing retention" but the data says otherwise, the real cost of inaction may be somewhere else entirely.

### Question 5: Who else must say yes?

**Depth probes:**
- For each approver in the chain, what is *their* job? IT's job is risk mitigation. Legal's job is compliance. Finance's job is ROI. Your pitch must address each approver's job separately.
- Have you mapped the full approval chain *before* the pilot starts? (IT security review, legal/compliance, finance/procurement, faculty governance if touching curriculum, accessibility review)

**Watch for:** If you've only validated with users and champions, you have enthusiasm without procurement. The pilot will succeed and the deal will die. Map every node in the approval chain and understand what job each node needs done before they'll say yes.

### Closing paragraph

The 5-question diagnostic gives you the quick filter. The depth probes give you the evidence quality you need to survive the 12-18 month sales cycle described in Part 1. Before committing to a pilot, make sure you can answer every depth probe — not just the headline question.

---

## Out of scope

- No changes to Part 1 of the README
- No changes to the standalone diagnostic (referenced as `/diagnostic` in the README; note: this directory does not yet exist in the repo)
- No companion documents or new files beyond the README expansion
- No ASU-specific or identifiable institutional data

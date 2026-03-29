# GitHub Repo Polish

**Date:** 2026-03-28
**Goal:** Improve repo discoverability, social sharing appearance, and community engagement infrastructure.

---

## 1. Repo metadata updates

### Description
Update from:
> A diagnostic framework for EdTech founders selling into higher education. Presented at SXSW EDU 2026.

To:
> A diagnostic framework for EdTech founders, university administrators, and investors navigating higher education. Built at ASU, presented at SXSW EDU 2026.

### Topics
Keep existing: `edtech`, `higher-education`, `jobs-to-be-done`, `product-validation`, `startups`, `sxsw-edu`

Add: `product-market-fit`, `edtech-startups`, `asu`, `framework`

### Settings
- Disable wiki (empty, clutters repo tabs)
- Enable discussions (community Q&A and case studies)

---

## 2. Social preview image

Create a 1280x640px OG card as an HTML file rendered to PNG:

- **Background:** Dark (#1a1a2e or similar)
- **Title:** "Cracking Higher Ed" (large, white, bold)
- **Subtitle:** "Why Startups Miss the Mark" (medium, lighter weight)
- **Attribution:** "ScaleU | ASU Enterprise Partners | SXSW EDU 2026" (small, muted)
- **Style:** Clean, minimal, professional — no logos needed, typography-driven

Generate as `assets/social-preview.png` and upload via GitHub API.

---

## 3. CONTRIBUTING.md

Create `CONTRIBUTING.md` at repo root with these sections:

### How to contribute
Three contribution types:
1. **Case studies** — Real examples of applying the framework (open an issue using the template)
2. **New job statements** — Validated JTBD statements from other institutions (open an issue using the template)
3. **Framework improvements** — Clarifications, corrections, additional patterns (open a PR)

### Contribution format
- Case studies: institution type, journey phase, job statement, what happened, what you learned
- Job statements: person, struggling moment, current workarounds, why they fail, proposed job statement, evidence source
- Framework improvements: describe the change and why it improves accuracy

### Review process
All contributions reviewed by Philippos Savvides. Case studies and job statements are evaluated for specificity and evidence quality using the same diagnostic the framework teaches.

### License
Contributions are licensed under CC BY 4.0 (same as the project).

---

## 4. Issue templates

Create `.github/ISSUE_TEMPLATE/` with two templates:

### case-study.md
```yaml
name: Share a Case Study
description: Share your experience applying the framework at your institution
labels: ["case-study"]
```
Body fields:
- Institution type (e.g., R1, community college, online program)
- Journey phase(s) involved
- Which diagnostic questions you applied
- What you found (signal vs. noise)
- Key takeaway

### job-statement.md
```yaml
name: Suggest a Job Statement
description: Propose a new validated JTBD statement for the jobs atlas
labels: ["job-statement"]
```
Body fields:
- Journey phase
- Person (role, not title)
- Struggling moment
- Current workarounds and why they fail
- Proposed job statement
- Evidence source (how you validated this)

---

## 5. What stays unchanged

- README content
- Framework content
- Presentation files
- CHANGELOG (no version bump — this is repo infrastructure, not content)

---

## 6. Verification

1. `gh repo view savvides/cracking-higher-ed-sxswedu` shows updated description and topics
2. Share repo URL on social media preview tool — shows branded OG card
3. Discussions tab visible on repo
4. Wiki tab hidden
5. "New Issue" shows both templates
6. CONTRIBUTING.md renders on GitHub

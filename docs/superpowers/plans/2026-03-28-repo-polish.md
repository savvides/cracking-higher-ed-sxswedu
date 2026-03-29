# GitHub Repo Polish Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Improve repo discoverability, social sharing appearance, and community engagement infrastructure.

**Architecture:** GitHub API calls for repo settings, new markdown files for community infrastructure, HTML-to-PNG for social preview image.

**Tech Stack:** `gh` CLI, GitHub API, HTML/CSS (for OG image generation)

**Spec:** `docs/superpowers/specs/2026-03-28-repo-polish-design.md`

---

## File Structure

| File | Action | Purpose |
|------|--------|---------|
| `CONTRIBUTING.md` | Create | Community contribution guidelines |
| `.github/ISSUE_TEMPLATE/case-study.md` | Create | Issue template for case studies |
| `.github/ISSUE_TEMPLATE/job-statement.md` | Create | Issue template for job statement proposals |
| `assets/social-preview.html` | Create | Source for OG card (rendered to PNG) |
| `assets/social-preview.png` | Create | 1280x640 social preview image |

---

### Task 1: Update repo metadata via GitHub API

**Files:** None (API calls only)

- [ ] **Step 1: Update repo description**

```bash
gh repo edit savvides/cracking-higher-ed-sxswedu \
  --description "A diagnostic framework for EdTech founders, university administrators, and investors navigating higher education. Built at ASU, presented at SXSW EDU 2026."
```

- [ ] **Step 2: Add new topics**

```bash
gh repo edit savvides/cracking-higher-ed-sxswedu \
  --add-topic product-market-fit \
  --add-topic edtech-startups \
  --add-topic asu \
  --add-topic framework
```

- [ ] **Step 3: Disable wiki, enable discussions**

```bash
gh repo edit savvides/cracking-higher-ed-sxswedu --enable-wiki=false
gh repo edit savvides/cracking-higher-ed-sxswedu --enable-discussions
```

- [ ] **Step 4: Verify**

```bash
gh repo view savvides/cracking-higher-ed-sxswedu --json description,repositoryTopics,hasWikiEnabled,hasDiscussionsEnabled
```

Expected: Updated description, 10 topics, wiki disabled, discussions enabled.

---

### Task 2: Create social preview image

**Files:**
- Create: `assets/social-preview.html`
- Create: `assets/social-preview.png`

- [ ] **Step 1: Create assets directory**

```bash
mkdir -p assets
```

- [ ] **Step 2: Create HTML source for the OG card**

Create `assets/social-preview.html` with this exact content:

```html
<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8">
<style>
  * { margin: 0; padding: 0; box-sizing: border-box; }
  body {
    width: 1280px;
    height: 640px;
    background: linear-gradient(135deg, #1a1a2e 0%, #16213e 50%, #0f3460 100%);
    display: flex;
    flex-direction: column;
    justify-content: center;
    padding: 80px 100px;
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
    color: white;
  }
  .title {
    font-size: 72px;
    font-weight: 700;
    letter-spacing: -1px;
    line-height: 1.1;
    margin-bottom: 20px;
  }
  .subtitle {
    font-size: 36px;
    font-weight: 300;
    color: rgba(255,255,255,0.75);
    margin-bottom: 60px;
  }
  .attribution {
    font-size: 22px;
    font-weight: 400;
    color: rgba(255,255,255,0.5);
    letter-spacing: 1px;
  }
  .divider {
    width: 80px;
    height: 4px;
    background: #e94560;
    margin-bottom: 30px;
    border-radius: 2px;
  }
</style>
</head>
<body>
  <div class="title">Cracking Higher Ed</div>
  <div class="subtitle">Why Startups Miss the Mark</div>
  <div class="divider"></div>
  <div class="attribution">ScaleU &middot; ASU Enterprise Partners &middot; SXSW EDU 2026</div>
</body>
</html>
```

- [ ] **Step 3: Render HTML to PNG**

Use the `/browse` skill or a headless browser to open `assets/social-preview.html` and screenshot it at 1280x640. Save as `assets/social-preview.png`.

If browser rendering is unavailable, use this fallback:

```bash
# Requires Chrome/Chromium installed
"/Applications/Google Chrome.app/Contents/MacOS/Google Chrome" \
  --headless --disable-gpu --screenshot=assets/social-preview.png \
  --window-size=1280,640 \
  --default-background-color=0 \
  assets/social-preview.html
```

- [ ] **Step 4: Upload social preview to GitHub**

```bash
gh api repos/savvides/cracking-higher-ed-sxswedu \
  --method PATCH \
  -f social_media_preview="$(base64 < assets/social-preview.png)"
```

If the API doesn't support base64 upload, upload manually via GitHub Settings > Social Preview, or use:

```bash
# Upload via the repository social media preview endpoint
gh api repos/savvides/cracking-higher-ed-sxswedu/social-preview \
  --method PUT \
  --input assets/social-preview.png
```

Note: GitHub's API for social preview upload is limited. If API methods fail, the image can be uploaded manually at: `https://github.com/savvides/cracking-higher-ed-sxswedu/settings` > Social Preview > Edit > Upload.

- [ ] **Step 5: Commit**

```bash
git add assets/
git commit -m "Add social preview image for repo OG card"
```

---

### Task 3: Create CONTRIBUTING.md

**Files:**
- Create: `CONTRIBUTING.md`

- [ ] **Step 1: Create CONTRIBUTING.md**

Create `CONTRIBUTING.md` at repo root with this exact content:

```markdown
# Contributing

This framework improves when practitioners share what they learn in the field. There are three ways to contribute.

## 1. Share a case study

If you've applied the diagnostic or jobs atlas at your institution, open an issue using the **Case Study** template. Include:

- Institution type (R1, community college, online program, etc.)
- Journey phase(s) involved
- Which diagnostic questions you applied
- What you found (signal vs. noise)
- Key takeaway

Good case studies are specific. "We tested the cost expectation gap job at a community college and found X" is useful. "The framework was helpful" is not.

## 2. Propose a new job statement

The jobs atlas currently covers 15 validated jobs across 6 phases. If you've identified a job that's missing, open an issue using the **Job Statement** template. Include:

- Journey phase
- Person (role, not title)
- Struggling moment
- Current workarounds and why they fail
- Proposed job statement
- Evidence source (how you validated this)

Job statements are evaluated for specificity and evidence quality using the same diagnostic the framework teaches.

## 3. Improve the framework

For clarifications, corrections, or additional patterns, open a pull request. Describe what you're changing and why it improves accuracy.

## Review process

All contributions are reviewed by [Philippos Savvides](mailto:philippos.savvides@asuep.org). Expect a response within two weeks.

## License

By contributing, you agree that your contributions are licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/), the same license as the project.
```

- [ ] **Step 2: Commit**

```bash
git add CONTRIBUTING.md
git commit -m "Add contributing guidelines for community engagement"
```

---

### Task 4: Create issue templates

**Files:**
- Create: `.github/ISSUE_TEMPLATE/case-study.md`
- Create: `.github/ISSUE_TEMPLATE/job-statement.md`

- [ ] **Step 1: Create template directory**

```bash
mkdir -p .github/ISSUE_TEMPLATE
```

- [ ] **Step 2: Create case study template**

Create `.github/ISSUE_TEMPLATE/case-study.md` with this exact content:

```markdown
---
name: Share a Case Study
about: Share your experience applying the framework at your institution
title: "[Case Study] "
labels: case-study
---

**Institution type** (e.g., R1, community college, online program)


**Journey phase(s) involved** (e.g., Pre-enroll, Apply, Onboard, Select & Enroll, Course Experience, Graduate & Beyond)


**Which diagnostic questions did you apply?**


**What did you find?** (signal vs. noise — be specific)


**Key takeaway**

```

- [ ] **Step 3: Create job statement template**

Create `.github/ISSUE_TEMPLATE/job-statement.md` with this exact content:

```markdown
---
name: Suggest a Job Statement
about: Propose a new validated JTBD statement for the jobs atlas
title: "[Job Statement] "
labels: job-statement
---

**Journey phase** (e.g., Pre-enroll, Apply, Onboard, Select & Enroll, Course Experience, Graduate & Beyond)


**Person** (role, not title — e.g., "prospective student comparing programs," not "student")


**Struggling moment** (what is the person trying to do, and what's blocking them?)


**Current workarounds** (what do they do today, and why does it fail?)


**Proposed job statement** (format: "When [situation], I want to [motivation], so I can [outcome]")


**Evidence source** (how did you validate this? interviews, data, institutional experience?)

```

- [ ] **Step 4: Commit**

```bash
git add .github/
git commit -m "Add issue templates for case studies and job statements"
```

---

### Task 5: Push and verify

- [ ] **Step 1: Push all commits**

```bash
git push origin main
```

- [ ] **Step 2: Verify issue templates**

```bash
gh issue create --repo savvides/cracking-higher-ed-sxswedu --web
```

Expected: Browser opens showing both templates as options.

- [ ] **Step 3: Verify discussions tab**

```bash
gh repo view savvides/cracking-higher-ed-sxswedu --web
```

Expected: Discussions tab visible in repo navigation.

- [ ] **Step 4: Verify CONTRIBUTING.md**

Navigate to repo root on GitHub — CONTRIBUTING.md should render and GitHub should show a "Read the contributing guidelines" prompt on new issues.

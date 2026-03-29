# Repo Restructure Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Reorganize repo files to match documented structure, fix broken links, add audience section to README.

**Architecture:** File moves via `git mv`, README edits, CHANGELOG update, tag + release. No code — pure content operations.

**Tech Stack:** git, gh CLI

**Spec:** `docs/superpowers/specs/2026-03-28-repo-restructure-design.md`

---

### Task 1: Move deck files into `/deck` directory

**Files:**
- Move: `cracking-higher-ed-sxsw-edu-2026.pdf` → `deck/cracking-higher-ed-sxsw-edu-2026.pdf`
- Move: `cracking-higher-ed-sxsw-edu-2026.pptx` → `deck/cracking-higher-ed-sxsw-edu-2026.pptx`

- [ ] **Step 1: Create deck directory and move files**

```bash
cd /Users/philippossavvides/Desktop/GitHub/sxsw/cracking-higher-ed-sxswedu
mkdir -p deck
git mv cracking-higher-ed-sxsw-edu-2026.pdf deck/
git mv cracking-higher-ed-sxsw-edu-2026.pptx deck/
```

- [ ] **Step 2: Verify**

```bash
ls deck/
```
Expected: `cracking-higher-ed-sxsw-edu-2026.pdf  cracking-higher-ed-sxsw-edu-2026.pptx`

---

### Task 2: Move diagnostic to `/diagnostic` and delete `mnt/`

**Files:**
- Move: `mnt/user-data/outputs/github-repo/diagnostic/README.md` → `diagnostic/README.md`
- Delete: `mnt/` (entire tree)

- [ ] **Step 1: Create diagnostic directory and move file**

```bash
mkdir -p diagnostic
git mv mnt/user-data/outputs/github-repo/diagnostic/README.md diagnostic/README.md
```

- [ ] **Step 2: Remove empty `mnt/` tree**

```bash
git rm -r mnt/
```

If `git rm` fails because directory is already empty after the move, use:
```bash
rm -rf mnt/
```

- [ ] **Step 3: Verify**

```bash
ls diagnostic/
ls mnt/ 2>&1
```
Expected: `diagnostic/README.md` exists, `mnt/` does not.

---

### Task 3: Update README

**Files:**
- Modify: `README.md` (lines 13-15 — description line; insert new section after line 15)

- [ ] **Step 1: Update description line (line 15)**

Change line 15 from:
```
This repo contains the framework from the SXSW EDU talk, designed to help founders distinguish real institutional demand from false positives before they run out of runway.
```

To:
```
This framework helps founders, administrators, and investors distinguish real institutional demand from false positives — before startups run out of runway.
```

- [ ] **Step 2: Add "Who this is for" section**

Insert after line 15 (after the updated description line), before "## What's in this repo":

```markdown

## Who this is for

- **EdTech founders** — validate demand before you burn runway on a 12-month sales cycle
- **University administrators** — evaluate vendor claims using the same framework your peers use internally
- **Investors and accelerators** — assess whether a portfolio company has real institutional signal or just enthusiasm
```

- [ ] **Step 3: Verify README renders correctly**

```bash
head -30 README.md
```

Expected: Title, subtitle, attribution, problem section, updated description, "Who this is for" section, "What's in this repo" section.

---

### Task 4: Update CHANGELOG

**Files:**
- Modify: `CHANGELOG.md`

- [ ] **Step 1: Add v1.1.0 entry and update links**

Insert after line 5 (after the format description), before the `## [1.0.0]` entry:

```markdown

## [1.1.0] - 2026-03-28

### Changed
- Reorganized repo: moved deck files to `/deck`, diagnostic to `/diagnostic`
- Improved README intro to serve broader audience beyond SXSW attendees

### Added
- "Who this is for" section in README

### Removed
- Development artifact paths (`mnt/`, `docs/superpowers/`)
```

Also update the v1.0.0 diagnostic path reference on line 13 from:
```
- Standalone 5-question diagnostic tool (`mnt/user-data/outputs/github-repo/diagnostic/`)
```
To:
```
- Standalone 5-question diagnostic tool
```

Update comparison links at bottom of file to:
```
[1.1.0]: https://github.com/savvides/cracking-higher-ed-sxswedu/compare/v1.0.0...v1.1.0
[1.0.0]: https://github.com/savvides/cracking-higher-ed-sxswedu/compare/v0.1.0...v1.0.0
[0.1.0]: https://github.com/savvides/cracking-higher-ed-sxswedu/releases/tag/v0.1.0
```

---

### Task 5: Delete `docs/` directory

**Files:**
- Delete: `docs/` (entire tree — contains only superpowers specs/plans which are development artifacts)

- [ ] **Step 1: Commit spec and plan first (so they're in git history)**

```bash
git add docs/
git commit -m "Add restructure spec and plan for reference"
```

- [ ] **Step 2: Remove docs directory**

```bash
git rm -r docs/
```

---

### Task 6: Commit, tag, and release

- [ ] **Step 1: Stage all changes**

```bash
git add -A
git status
```

Review: should show deck/ added, diagnostic/ added, mnt/ deleted, docs/ deleted, README.md modified, CHANGELOG.md modified.

- [ ] **Step 2: Commit**

```bash
git commit -m "Reorganize repo structure and broaden README audience

- Move deck files to /deck, diagnostic to /diagnostic
- Add 'Who this is for' section to README
- Update description to address founders, administrators, and investors
- Remove development artifact paths (mnt/, docs/)
- Update CHANGELOG with v1.1.0 entry"
```

- [ ] **Step 3: Tag**

```bash
git tag v1.1.0
```

- [ ] **Step 4: Push**

```bash
git push origin main --tags
```

- [ ] **Step 5: Create GitHub Release**

```bash
gh release create v1.1.0 \
  --repo savvides/cracking-higher-ed-sxswedu \
  --title "v1.1.0 — Repo restructure" \
  --notes "$(cat <<'EOF'
### Changed
- Reorganized repo: deck files now in `/deck`, diagnostic tool in `/diagnostic`
- README intro updated to serve broader audience (founders, administrators, investors)

### Added
- "Who this is for" section in README

### Removed
- Development artifact paths
EOF
)"
```

- [ ] **Step 6: Verify**

```bash
git tag -l
gh release view v1.1.0 --repo savvides/cracking-higher-ed-sxswedu
```

Expected: tags `v0.1.0`, `v1.0.0`, `v1.1.0` all present. Release shows correct notes.

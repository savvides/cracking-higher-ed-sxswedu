# Repo Restructure: cracking-higher-ed-sxswedu

**Date:** 2026-03-28
**Goal:** Reorganize the repo so its file structure matches documentation, fix broken links, and improve the README intro to serve a broader audience beyond SXSW attendees.

---

## 1. File reorganization

### Current structure (broken)
```
cracking-higher-ed-sxswedu/
├── cracking-higher-ed-sxsw-edu-2026.pdf    ← loose at root
├── cracking-higher-ed-sxsw-edu-2026.pptx   ← loose at root
├── mnt/user-data/outputs/github-repo/
│   └── diagnostic/README.md                 ← artifact path
├── .gitignore
├── CHANGELOG.md
├── LICENSE
└── README.md
```

### Target structure
```
cracking-higher-ed-sxswedu/
├── deck/
│   ├── cracking-higher-ed-sxsw-edu-2026.pdf
│   └── cracking-higher-ed-sxsw-edu-2026.pptx
├── diagnostic/
│   └── README.md
├── .gitignore
├── CHANGELOG.md
├── LICENSE
└── README.md
```

### Moves
| From | To |
|------|----|
| `cracking-higher-ed-sxsw-edu-2026.pdf` | `deck/cracking-higher-ed-sxsw-edu-2026.pdf` |
| `cracking-higher-ed-sxsw-edu-2026.pptx` | `deck/cracking-higher-ed-sxsw-edu-2026.pptx` |
| `mnt/user-data/outputs/github-repo/diagnostic/README.md` | `diagnostic/README.md` |

### Deletions
| Path | Reason |
|------|--------|
| `mnt/` (entire tree) | Artifact from development tooling; contents moved to `diagnostic/` |
| `docs/` (if empty or only contains superpowers specs) | Development artifacts; spec will be committed before deletion |

---

## 2. README edits

### 2a. Update "What's in this repo" section (line 17-24)

Current code block references `/deck` and `/diagnostic` which is correct for the *target* structure but currently broken. After the file moves, the existing code block becomes accurate. No text change needed here — the moves fix it.

### 2b. Fix diagnostic link (line 100)

Current: `[/diagnostic](./diagnostic/)` — this link is currently broken (points to nonexistent root `/diagnostic`). After the move, it will work. No text change needed.

### 2c. Intro lines 1-5

No changes. Keep the existing intro and SXSW attribution as-is.

### 2d. Add "Who this is for" section (after line 15, before "What's in this repo")

Insert a brief audience section:

```markdown
## Who this is for

- **EdTech founders** — validate demand before you burn runway on a 12-month sales cycle
- **University administrators** — evaluate vendor claims using the same framework your peers use internally
- **Investors and accelerators** — assess whether a portfolio company has real institutional signal or just enthusiasm
```

### 2e. Update repo description line (line 15)

Current:
> This repo contains the framework from the SXSW EDU talk, designed to help founders distinguish real institutional demand from false positives before they run out of runway.

Updated:
> This framework helps founders, administrators, and investors distinguish real institutional demand from false positives — before startups run out of runway.

---

## 3. CHANGELOG update

Add `v1.1.0` entry:

```markdown
## [1.1.0] - 2026-03-28

### Changed
- Reorganized repo: moved deck files to `/deck`, diagnostic to `/diagnostic`
- Improved README intro to serve broader audience beyond SXSW attendees

### Added
- "Who this is for" section in README

### Removed
- Development artifact paths (`mnt/`, `docs/`)
```

Update comparison links at bottom of CHANGELOG.

---

## 4. What stays unchanged

- All framework content (Part 1, Part 2, patterns, depth probes)
- The presentation files themselves (just moved)
- The diagnostic content (just moved)
- LICENSE
- .gitignore

---

## 5. Verification

1. `ls deck/` shows both PDF and PPTX
2. `ls diagnostic/` shows README.md
3. `ls mnt/` fails (deleted)
4. Click `/diagnostic` link in GitHub README preview — resolves correctly
5. Click deck file links — downloadable from `/deck`
6. `git tag v1.1.0` on the restructure commit
7. `gh release create v1.1.0` with release notes

# CLAUDE.md for DefendThisNumber

## Project

This is the companion site for Barrie Robison's guest lecture in ENVS 5010 ("AI, Research, and the Professions"), College of Natural Resources, University of Idaho.

- **Talk**: Can You Defend This Number? Truth, Verification, and Trust in AI-Assisted Research
- **When**: Monday, April 27, 2026, 3:30 to 4:20 PM
- **Where**: CNR 10 (in person), plus Zoom for distance students, plus recording for the 8-week asynchronous cohort
- **Format**: ~25 minutes prepared remarks, then ~25 to 30 minutes of facilitated discussion
- **Series context**: Third in a sequence following Jason Karl (Voice) and Bert Baumgaertner (Judgment). This talk takes Accountability and Trust.
- **Course anchor text**: Yuval Harari, *Nexus* (2024), chapters 8 (Networks), 9 (Truth), and 10 (The Future).
- **Thesis**: Provenance is the new literacy. If you cannot trace a claim back to its source, it is not ready to share.

The full build plan lives in [resources/ROADMAP.md](resources/ROADMAP.md).

## Before you start

1. **Pull first**, always run `git pull` before starting work. CLAUDE.md itself may have been updated.
2. **Review open issues**, run `gh issue list --state open` before making changes (once the repo is on GitHub).
3. **Check remote branches**, run `git fetch --all` and review any branches ahead of main to avoid conflicts.
4. **Coordinate**, review open branches and issues before making independent changes.

## Repo boundaries

- You may edit code in **this repo only** (DefendThisNumber).
- Sibling repos (REACHWorkshop2026, data-lakehouse, promptulus, vandalizer, AI4RA-UDM, etc.) are **read-only for context**. If changes are needed in those repos, raise a GitHub issue instead.
- This repo was forked from REACHWorkshop2026 with a fresh git history. The REACH companion site is the visual and structural template that this site adapts.

## Repo layout

- `docs/`, GitHub Pages source (all site HTML, CSS, JS, images, Reveal.js).
- `resources/`, reference materials not served by the site, including ROADMAP.md.
- Root, only CLAUDE.md, README.md, LICENSE, .gitignore.

## Writing style

- Never use em dashes. Use commas, periods, or "and" instead.

## Local preview

```bash
python3 -m http.server 4173 -d docs
```

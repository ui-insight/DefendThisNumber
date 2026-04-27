# Can You Defend This Number?

**Truth, Verification, and Trust in AI-Assisted Research**

Companion site for Barrie Robison's guest lecture in ENVS 5010 ("AI, Research, and the Professions"), College of Natural Resources, University of Idaho.

Monday, April 27, 2026, 3:30 to 4:20 PM, CNR 10. Live in person, plus Zoom for distance students, plus a recording shared with the 8-week asynchronous cohort.

**Live site**: https://ui-insight.github.io/DefendThisNumber/

## Thesis

> Provenance is a discipline. If you cannot trace a claim back to its source, it is not ready to share.

## Abstract

AI tools can now generate research summaries, draft analyses, write code, and extract structured data from documents at remarkable speed. But speed and fluency are not the same as accuracy. This talk picks up where Jason Karl and Bert Baumgaertner left off in the ENVS 5010 series. Jason asked whether AI risks replacing your voice. Bert asked whether it risks replacing your judgment. Today we ask: can you defend the claims AI helped you produce?

Drawing on experience building AI-powered research tools, including document extraction systems, data lakehouses, and evaluation pipelines, this talk grounds Harari's arguments (chapters 8 to 10 of *Nexus*, your homework) in the practical realities of AI-assisted research. We explore why AI sounds confident even when wrong, how reproducibility and provenance serve as verification tools, and how to decide what to automate, what to augment, and what to leave alone.

The central argument is simple. AI accelerates the pipeline, but it does not change who is accountable for what comes out the other end. If you cannot trace a claim back to its source, it is not ready to share.

## Talk shape

A tour of three demos, each showing one part of the verification chain.

| # | Demo | What happens |
|---|------|---|
| 1 | Measuring extraction accuracy | Push an NSF solicitation through Vandalizer (the AI4RA team's document intelligence engine), then compare the extracted requirements against ground truth side by side. |
| 2 | AI as a translation layer, plus reproducibility and consistency | A token-builder interactive shows why the same prompt can yield different output. Data Crawler Carl is offered as a tool the audience can try on their own data. Vandalizer is re-run live to demonstrate non-determinism on a real workflow. |
| 3 | Auditability facilitates reproducibility | Tour of the AI4RA Prompt Library (versioned prompts) and Mindrouter (run execution and logging). The chain of custody made concrete. |

13 slides total. Roughly 25 minutes of prepared remarks, then 25 to 30 minutes of facilitated discussion.

## Series context

Third in a sequence in the ENVS 5010 spring 2026 cohort.

| Speaker | Title | Theme |
|---------|-------|-------|
| Jason Karl | Are you giving up the thing that is uniquely yours? Considerations on the use of AI in academic writing. | Voice |
| Bert Baumgaertner | The Dark Room and the Ruthless Curiosity It Demands: Graduate Research in the Age of Agentic AI. | Judgment |
| Barrie Robison | Can You Defend This Number? Truth, Verification, and Trust in AI-Assisted Research. | Accountability and Trust |

Course anchor text: Yuval Harari, *Nexus* (2024), chapters 8 (Networks), 9 (Truth), and 10 (The Future).

## Course host

Elise Kokenge, CNR Director of Graduate Studies, University of Idaho.

## Tools featured

| Tool | Role |
|------|------|
| [Vandalizer](https://vandalizer.nkn.uidaho.edu/) | The AI4RA team's document intelligence engine. Featured in Demos 1 and 2. |
| [Data Crawler Carl](https://ui-insight.github.io/data-crawler-carl/) | Tabular data question-answering tool. Offered to the audience in Demo 2. |
| [AI4RA Prompt Library](https://github.com/AI4RA/prompt-library) | Versioned prompts and validated cases the team uses. Featured in Demo 3. |
| [Mindrouter](https://mindrouter.uidaho.edu) | Prompt execution and provenance logging. Featured in Demo 3. |
| [AI4RA](https://ai4ra.uidaho.edu) | The NSF-funded umbrella project at the University of Idaho. The community of practice this talk draws from. |

## Reference reading

Not hosted on the site, but informs the talk and the homework around it.

1. Luke Sheneman, "Digitizing the Last Mile: OCR in Research Administration" (AI4RA). https://ai4ra.uidaho.edu/digitizing-the-last-mile-ocr-in-research-administration/
2. Nate Layman, "When Can AI Be Used in Research Administration?" (AI4RA). https://ai4ra.uidaho.edu/when-can-ai-be-used-in-research-administration/
3. Wilkinson, M. et al. (2016), "The FAIR Guiding Principles for scientific data management and stewardship." *Scientific Data* 3, 160018. https://doi.org/10.1038/sdata.2016.18

## Repo structure

```
DefendThisNumber/
  CLAUDE.md                 Project instructions for Claude Code
  README.md                 This file
  LICENSE
  docs/                     GitHub Pages source, the live site
    index.html              Landing page
    slides.html             Reveal.js deck (13 slides)
    slides-interactive.js   Token-builder and other interactive widgets
    styles.css              Site stylesheet
    slides.css              Slide deck theme
    app.js                  Scroll animation observer
    files/                  Source PDFs and ground-truth artifacts
    img/                    Logos, presenter photos
    reveal/                 Reveal.js library
  resources/                Reference materials, not served
    ROADMAP.md              Build plan for this project
    slides-outline.md       Working outline behind the deck
```

The `docs/` folder also retains some unlinked legacy pages from the REACHWorkshop2026 fork (course-content, presenters, next-steps, the three original slide decks). These are not reachable from the new nav and are pending cleanup.

## Local preview

```bash
python3 -m http.server 4173 -d docs
```

Then open `http://127.0.0.1:4173`.

## Deployment

GitHub Pages, served from the `docs/` folder on the `main` branch. Configured in repo settings: Settings, then Pages, then Source, then `main` / `/docs`. Pushes to `main` trigger an automatic rebuild in roughly 30 to 60 seconds.

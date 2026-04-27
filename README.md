# Can You Defend This Number?

**Truth, Verification, and Trust in AI-Assisted Research**

Companion site for Barrie Robison's guest lecture in ENVS 5010 ("AI, Research, and the Professions"), College of Natural Resources, University of Idaho.

Monday, April 27, 2026, 3:30 to 4:20 PM, CNR 10. Live in person, plus Zoom for distance students, plus a recording shared with the 8-week asynchronous cohort.

## Thesis

> Provenance is a discipline. If you cannot trace a claim back to its source, it is not ready to share.

## Abstract

AI tools can now generate research summaries, draft analyses, write code, and extract structured data from documents at remarkable speed. But speed and fluency are not the same as accuracy. This talk picks up where Jason Karl and Bert Baumgaertner left off in the ENVS 5010 series. Jason asked whether AI risks replacing your voice. Bert asked whether it risks replacing your judgment. Today we ask: can you defend the claims AI helped you produce?

Drawing on experience building AI-powered research tools, including document extraction systems, data lakehouses, and evaluation pipelines, this talk grounds Harari's arguments (chapters 8 to 10 of *Nexus*, your homework) in the practical realities of AI-assisted research. We explore why AI sounds confident even when wrong, how reproducibility and provenance serve as verification tools, and how to decide what to automate, what to augment, and what to leave alone.

The central argument is simple. AI accelerates the pipeline, but it does not change who is accountable for what comes out the other end. If you cannot trace a claim back to its source, it is not ready to share.

## Talk shape

A tour of three demos, each making a distinct point about provenance.

| # | Demo | Point |
|---|------|-------|
| 1 | PDF extraction failure modes | Garbage in, garbage out. AI extracts numbers from a real-looking grant document, and a subtle error changes meaning. |
| 2 | Reproducibility and non-determinism | The same prompt run three times can yield three different answers. "The AI said so" is not a defensible citation. |
| 3 | End-to-end provenance trace | A claim is a chain of custody. Show where AI inserts links you have to vouch for. |

Roughly 25 minutes of prepared remarks, then 25 to 30 minutes of facilitated discussion.

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

## Readings

1. Luke Sheneman, "Digitizing the Last Mile: OCR in Research Administration" (AI4RA). https://ai4ra.uidaho.edu/digitizing-the-last-mile-ocr-in-research-administration/
2. Nate Layman, "When Can AI Be Used in Research Administration?" (AI4RA). https://ai4ra.uidaho.edu/when-can-ai-be-used-in-research-administration/
3. To be added: one provenance and verification reading.

## Repo structure

```
DefendThisNumber/
  CLAUDE.md                Project instructions for Claude Code
  README.md                This file
  LICENSE
  docs/                    GitHub Pages source, the live site
    index.html             Landing page (thesis, three-demo nav, links)
    demo-extraction.html   Demo 1 deep page
    demo-reproducibility.html Demo 2 deep page
    demo-provenance.html   Demo 3 deep page
    slides.html            Reveal.js deck for the talk
    readings.html          Curated readings
    about.html             Bio, series context, acknowledgements
    files/                 Source PDFs and ground-truth artifacts for demos
    img/                   Logos, presenter photos, diagrams
    reveal/                Reveal.js library
    styles.css             Site stylesheet
    slides.css             Slide deck theme
  resources/               Reference materials (not served)
    ROADMAP.md             Build plan for this project
```

## Related work

| Source | Relevance |
|--------|-----------|
| [REACHWorkshop2026](../REACHWorkshop2026) | Visual and structural template that this site adapts |
| [ai4ra.uidaho.edu](https://ai4ra.uidaho.edu) | AI4RA community of practice blog (source of two readings) |
| [ui-insight/lakehouse](https://github.com/ui-insight/lakehouse) | Open-source data lakehouse used in Demo 3 |

## Local preview

```bash
python3 -m http.server 4173 -d docs
```

Then open `http://127.0.0.1:4173`.

## Deployment

GitHub Pages, served from the `docs/` folder on the `main` branch. Configure in repo settings: Settings, then Pages, then Source, then `/docs`.

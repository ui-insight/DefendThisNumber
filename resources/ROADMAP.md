# Roadmap: Can You Defend This Number?

Companion site for Barrie Robison's guest lecture in ENVS 5010, "AI, Research, and the Professions" (College of Natural Resources, University of Idaho).

## Context

- **Talk**: Can You Defend This Number? Truth, Verification, and Trust in AI-Assisted Research
- **When**: Monday, April 27, 2026, 3:30 to 4:20 PM
- **Where**: CNR 10, plus Zoom for distance students
- **Format**: ~25 minutes prepared remarks, then ~25 to 30 minutes of facilitated discussion
- **Audience**: Mixed cohort of research-active CNR faculty, thesis-track graduate students, and online working professionals (non-thesis MS), enrolled in an asynchronous 1-credit, 8-week graduate seminar
- **Recording**: Shared with the 8-week async cohort
- **Course anchor text**: Yuval Harari, *Nexus* (2024), chapters 8 (Networks), 9 (Truth), and 10 (The Future)
- **Series**: Third in a sequence following Jason Karl (Voice) and Bert Baumgaertner (Judgment). This talk takes Accountability and Trust.
- **Course host**: Elise Kokenge, CNR Director of Graduate Studies

## Thesis

> Provenance is a discipline. If you cannot trace a claim back to its source, it is not ready to share.

This sentence is the spine of everything. It is the hero copy on the landing page, the throughline for each of the three demos, and the closer on the slide deck.

## Talk shape

Tour of three demos, each making a distinct point about provenance.

1. **PDF extraction failure modes.** Push a real document through the AI4RA OCR and extraction pipeline. Show subtle errors that change meaning (transposed numbers, dropped negations, mis-attributed quotes). The literal "defend this number" demo. Point: garbage in, garbage out.
2. **Reproducibility and non-determinism.** Same prompt, run three times, get three different answers. Show what temperature means in practice. Point: "the AI said so" is not a defensible citation, because the AI says different things each time.
3. **End-to-end provenance trace.** Take a single claim and trace it from raw data source through AI processing to a final assertion. Show where each step is defensible and where it is not. Point: provenance is a chain, and AI inserts links you have to vouch for.

Roughly six minutes per demo, plus a hook and a close.

## Site structure

Landing page plus per-demo pages, mirroring the REACH layout but trimmed.

| Page | Purpose |
| --- | --- |
| `index.html` | Landing. Hero with the thesis, talk metadata, three-demo nav, links to slides and readings. |
| `demo-extraction.html` | Demo 1 deep page. The CNR document, the AI extraction, the side-by-side, the lesson. |
| `demo-reproducibility.html` | Demo 2 deep page. Three runs, the diffs, why this matters for citation. |
| `demo-provenance.html` | Demo 3 deep page. The traced claim, the chain of custody, the lesson on accountability. |
| `slides.html` | The Reveal.js deck (or a thin wrapper that loads it). |
| `readings.html` | Three readings, framed for grad students, plus links to Jason's and Bert's recordings. |
| `about.html` | Bio, series context, acknowledgements. |
| (later) `recording.html` | Embed or link the talk recording once published, with a short re-orientation for async students. |

## Slides

Adapt the existing REACH Reveal.js deck. Keep the visual template and demo scaffolding. Strip workshop-specific content. Reorganize around the tour-of-three-demos shape. Maintain the playful Lord Polymorphic voice.

## Demo source material

Reuse existing REACH documents for Demos 2 and 3 (NSF award notices, NCOD NOFO, RFPs already in `docs/files/`). Source one natural-resources document for Demo 1. Strong candidates worth considering:

- A USFS Forest Inventory and Analysis report
- An IDFG wildlife survey or management plan
- A USGS water-quality or rangeland-health report
- A peer-reviewed paper from a CNR faculty member
- An ESA listing or 5-year review document

Whichever you pick, the demo should show a subtle extraction error that changes meaning. The error has to be the kind a student would miss on a casual read but matter on a defensible citation.

## Readings list (three items)

1. Luke Sheneman, "Digitizing the Last Mile: OCR in Research Administration" (AI4RA). https://ai4ra.uidaho.edu/digitizing-the-last-mile-ocr-in-research-administration/
2. Nate Layman, "When Can AI Be Used in Research Administration?" (AI4RA). https://ai4ra.uidaho.edu/when-can-ai-be-used-in-research-administration/
3. **TBD**: one new provenance or verification reading. Candidate directions: a recent piece on AI hallucinated citations, a classic on the reproducibility crisis, or something on FAIR data principles. To be picked.

The three duplicates with Bert's list (Anthropic coding-skills RCT, Anthropic Building Effective Agents, Mollick "Against Brain Damage") are intentionally dropped, since this audience already encountered them.

## Branding and tone

- Visual brand: keep AI4RA and University of Idaho identity as-is. No new asset work.
- Voice: keep the playful, self-deprecating Lord Polymorphic register. Trust grad students and faculty to read it as warmth, not unseriousness. The abstract already commits to this tone.

## Discussion

Skipped from the site. Live discussion is facilitated in the room. Async students reflect privately or via the course LMS. The site does not host prompts, a form, or a widget.

## Hosting

- New GitHub repo under your account.
- Enable GitHub Pages from `docs/`.
- Default URL, e.g. `https://professorpolymorphic.github.io/DefendThisNumber/`.
- No custom domain (DNS would not propagate in time, and it is not worth the cost for a single talk).

## Phasing

You chose **full site by today, aggressive**. Honest read: with only slide content drafted, building three demo pages, sourcing a CNR doc, picking a new reading, adapting slides, and shipping to GitHub Pages in a few hours is a lot of surface area. If anything has to slip, the demo pages can ship as stubs with placeholder copy and be filled in over the next one to two weeks for the async cohort. The slides and a working landing page are the load-bearing pieces for today.

### Today (before 3:30 PM)

1. Pick the CNR document for Demo 1 (you, fastest)
2. Pick the new provenance reading (you or me, can be quick)
3. Adapt the REACH slide deck into the three-demo structure (me, working from your draft slide content)
4. Build the landing page with thesis, abstract, links, three-demo nav (me)
5. Stub the three demo pages with at least a title, the demo's point, and a placeholder for content (me)
6. Build the readings page (me)
7. Update CLAUDE.md and README so they match the new project (me)
8. Push to GitHub, enable Pages, smoke test the URL (me)
9. Deliver title, abstract, bio, readings, and links to Elise (you, if not already sent)

### Within one to two weeks (before async cohort fully engages)

- Flesh out demo pages with screenshots, code snippets, downloadable artifacts, and a brief "try this yourself" sidebar
- Add the recording page once the recording is published
- Decide whether to retro-fit async reflection prompts based on what worked live
- Polish anything that shipped rough today

### Through the 8-week course window

- Monitor for student questions or feedback that Elise relays
- Touch up content based on what landed or fell flat in the live talk

## Open items requiring your input

1. Which natural-resources document anchors Demo 1
2. Which provenance reading replaces the dropped Bert overlaps
3. Whether Elise has any framing constraints I should know about beyond what was shared
4. The exact slide content you have drafted (location, format, how you want me to integrate it)

## Decisions index

| Topic | Decision |
| --- | --- |
| Audience | ENVS 5010 grad students, plus faculty observers and async working professionals |
| Venue | CNR 10, in person, plus Zoom, plus recording |
| Site role | Live demo platform AND durable artifact |
| Thesis | "Provenance is a discipline" |
| Talk shape | Tour of three demos |
| Three demos | PDF extraction failure modes, reproducibility, end-to-end provenance trace |
| Site shape | Landing plus per-demo pages, ~7 to 8 pages |
| Slides | Adapt REACH Reveal.js deck |
| Discussion | Stays in the room, no site support |
| Demo sources | Reuse REACH admin docs, plus one new CNR document |
| Readings | Two AI4RA pieces, plus one new provenance reading |
| Tone | Keep playful Lord Polymorphic voice |
| Visual brand | Keep AI4RA and UI as-is |
| Hosting | GitHub Pages, default URL |
| Phasing | Aggressive, full site by today |
| Already drafted | Slide content (only) |

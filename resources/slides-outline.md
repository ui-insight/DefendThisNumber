# Slide Outline: Can You Defend This Number?

Working draft. We iterate here, then convert to Reveal.js HTML.

**Total budget**: 25 minutes prepared, then 25 to 30 minutes facilitated discussion.
**Total slides**: 15 (target). Roughly 1.5 minutes per slide, with demo slides running longer and transitions running shorter.
**Voice**: Lord Polymorphic. Self-deprecating, conversational, occasionally Tolkien-flavored.

Markers:
- `[NEED:]` content I need Barrie to provide from his mental notes
- `[OPTIONS:]` a choice point where I'm proposing alternatives

---

## Section 1: Opening (slides 1 to 4, ~3 minutes)

### Slide 1: Title (~20 seconds)

- **Visual**: Title-slide template, AI4RA gold background
- **Title**: Can You Defend This Number?
- **Subtitle**: Truth, Verification, and Trust in AI-Assisted Research
- **Byline**: Barrie Robison · Professor of Biological Sciences · Director, IIDS · Writer of Emails and Attender of Endless Meetings
- **Footer**: ENVS 5010 guest lecture, April 27, 2026

### Slide 2: Where this fits in the series (~30 seconds)

- **Visual**: Three cards, the third highlighted
- **Card 1**: Karl, "Voice" -> are you giving up the thing that is uniquely yours?
- **Card 2**: Baumgaertner, "Judgment" -> the dark room and the ruthless curiosity it demands
- **Card 3 (highlighted)**: Robison, "Trust" -> can you defend this number?
- **One-line tie**: All three sit on top of Harari, *Nexus*, chapters 8 to 10. Networks, Truth, and the Future.
- **Speaker note**: "I get to clean up the philosophy by handing you the dirty dishes."

### Slide 3: The hook, live bait (~90 seconds)

- **Visual**: Vandalizer extraction output displayed prominently. The "cost sharing" line highlighted.
- **The setup**: "Before I tell you what this talk is about, let me show you something simple. I asked Vandalizer to pull the requirements out of NSF 26-508, the TechAccess: AI-Ready America solicitation. Here is what it gave me." (Anchored in the AI4RA team's own tool, so the critique is on the house.)
- **The bait**: Vandalizer's output includes a line like "Voluntary cost sharing of approximately 20% is encouraged and strengthens the proposal." Looks reasonable. Sounds like advice you've heard before. The rest of the extraction is clean and structured, which makes this line read as defensible.
- **The reveal**: Cut to the actual RFP text. Voluntary committed cost sharing is **PROHIBITED**. AI did not just get it wrong, it got it **backwards**. A proposal team following this advice would be returned without review.
- **The framing**: "Would you start writing your proposal off this list? Would you pass it to your PI? This is the simplest version of the question we will spend the next twenty minutes on. Provenance is the new literacy. If you cannot trace it, you cannot defend it."
- **Why this hook works**: AI4RA tool, so the critique is owned. NSF 26-508 already has ground truth in `docs/files/prompts/rfp-extraction/`. The flip (encouraged vs prohibited) is the opposite of helpful, which is the most dramatic kind of failure. Every grad student has either applied for funding or will, so the stakes register.
- **Speaker note**: "If the AI helps you write a proposal that gets returned without review, the AI does not get fired. You do."

### Slide 4: Thesis (~40 seconds)

- **Visual**: Big text, plain background, AI4RA gold accent
- **Headline**: Provenance is the new literacy.
- **Subhead**: If you cannot trace a claim back to its source, it is not ready to share.
- **Bottom line**: "I'll spend the next 22 minutes earning this claim with three demos."

---

## Section 2: Tour preview (slide 5, ~30 seconds)

### Slide 5: The three demos (~30 seconds)

- **Visual**: Three preview cards (REACH `preview-flow` template), one per demo
- **Card 1**: Defend this **number**. PDF extraction, where AI gets the words right and the numbers wrong.
- **Card 2**: Defend this **answer**. Same prompt, three runs, three different answers.
- **Card 3**: Defend this **chain**. A single claim, traced from raw data to published assertion.
- **Speaker note**: "Three demos. Each one breaks a different link in the chain. None of them require you to know how AI works under the hood."

---

## Section 3: Demo 1, defend this number (slides 6 to 7, ~6 minutes)

**Mode**: LIVE in Vandalizer. Barrie drives Vandalizer himself in the browser. The deck just hands the audience the URL and the PDF so they can follow along (or replay later) on their own machines.

### Slide 6: Hand-off slide (~30 seconds, then live demo runs ~5 minutes)

- **Visual**: Two-column layout, each column a big tap-target card.
    - **Left card**: Launch Vandalizer, big button linking to https://vandalizer.nkn.uidaho.edu/. Vandalizer logo. Same visual treatment as the existing `vandalizer-slide` pattern in `slides-ai-literacy.html` line 287.
    - **Right card**: Download the award notice, big button linking to `files/nsf_award_notice_DEB-2412345.pdf` with `download` attribute. Document icon. Same visual treatment as the existing `sample-doc-card` pattern.
- **Title**: Defend this number
- **The framing copy on the slide**: "Open Vandalizer. Download the award notice. I will drive."
- **The transition**: Barrie alt-tabs to Vandalizer and runs the demo himself for ~5 minutes. The slide deck stays on this slide (or a paired "Live demo" placeholder) the whole time, so any audience member who wants to catch up can scan the screen and grab the link or the PDF.
- **[NEED:]** Confirm the Vandalizer URL is `https://vandalizer.nkn.uidaho.edu/` and not `https://vandalizer.uidaho.edu` (the existing Module 1 slide uses the second; your message used the first). The two might be different instances (community edition vs internal). Tell me which one the audience should land on.

### Slide 7: Demo 1 debrief (~30 seconds)

- **Visual**: Single line of large text on a clean background
- **Lesson, in your own words**: "If you cannot trace the number, do not share the number."
- **Bridge to Demo 2**: "And it is not just numbers. The same prompt, run twice, can give you two different answers. Why?"

---

## Section 4: Demo 2, defend this answer (slides 8 to 11, ~6 minutes)

**Mode**: A guided sequence. Conceptual setup with the token-builder interactive (ported from Module 1), then point at Data Crawler Carl as a tool the audience can play with on their own data, then return to Vandalizer to show the same reproducibility issue empirically.

### Slide 8: Token-builder interactive (~2 minutes)

- **Visual**: Port the existing slide from `slides-ai-literacy.html` line 248 verbatim. The interactive `<div id="token-builder">` plus the slide-note copy ("No right answer, only probabilities. This is why LLMs produce different output each time").
- **Title**: Build a sentence one token at a time
- **What Barrie does**: Click through a few tokens with the audience. "Notice that the next word is never determined. It is sampled. Every word is a coin flip with weighted dice."
- **Why this slide**: It earns the "same prompt, different answers" claim before the audience sees it happen. The reproducibility problem is not a bug, it is the architecture.
- **Implementation note**: We will need to also pull `slides-interactive.js` (or whatever JS powers `#token-builder`) into the new deck so the interactive runs.

### Slide 9: Data Crawler Carl (~90 seconds)

- **Visual**: Single big card, Data Crawler Carl logo or screenshot, big launch button
- **Link**: https://ui-insight.github.io/data-crawler-carl/
- **The framing copy**: "If you want to watch this happen on your own data, our team built Data Crawler Carl. Upload a CSV, ask questions in plain English, see what AI gets right and what it gets wrong."
- **What Barrie does**: Brief verbal pitch, do not switch to it live (no time). Audience can open it later from the link.

### Slide 10: Back to Vandalizer (~2 minutes)

- **Visual**: The Vandalizer launch card again, plus a one-line prompt under it
- **The framing copy**: "Let me show you the same thing in Vandalizer. Same prompt, three runs."
- **What Barrie does**: Live in Vandalizer, run the same prompt three times, surface the divergence. Returns the audience to the tool they already have open from Demo 1.
- **[NEED:]** which specific Vandalizer prompt or setup you want to use for the reproducibility demo. Could be the same setup from Demo 1 re-run, or a different one.

### Slide 11: Demo 2 debrief (~30 seconds)

- **Visual**: Single quote-style slide
- **Lesson**: "The AI did not give you an answer. It gave you a sample. The next time it answers, it might give you a different one."
- **Bridge to Demo 3**: "So how do you know which sample to trust? You need a record."

---

## Section 5: Demo 3, defend this chain (slides 12 to 14, ~6 minutes)

**Mode**: A live walk through two AI4RA tools that together provide the chain of custody, the AI4RA Prompt Library and Mindrouter. These are how you actually validate output, version prompts, and trace evaluation data in practice.

### Slide 12: Setup (~45 seconds)

- **Visual**: A horizontal chain-of-custody diagram, six or seven nodes (Source -> OCR -> structured JSON -> aggregation -> CSV -> dashboard -> claim). Each node a small card.
- **Title**: Defend this chain
- **The framing**: "If AI is in your pipeline, it is in your chain of custody. Every step is a link you have to vouch for. Let me show you how we do that on the AI4RA team."
- **Speaker note**: "Provenance is not a vibe. It is a logged record. You either have it or you do not."

### Slide 13: AI4RA Prompt Library + Mindrouter (~4 minutes, live)

- **Visual**: Two-card layout, each a big launch card
    - **Left card**: AI4RA Prompt Library, link to https://github.com/AI4RA/prompt-library, GitHub icon
    - **Right card**: Mindrouter, link to https://mindrouter.uidaho.edu, Mindrouter logo if available
- **The framing copy**: "Prompts are versioned in the library. Runs are logged in Mindrouter. Together they let you answer 'where did this number come from' for any AI output we ship."
- **What Barrie does**: Brief switch to each tool. Show:
    1. Prompt versioning in the library (a prompt with a version history)
    2. A run in Mindrouter with the prompt history attached
    3. Evaluation data tied to that run
- **[NEED:]** Confirm the Mindrouter URL (https://mindrouter.uidaho.edu, no path)? Confirm the prompt library URL (https://github.com/AI4RA/prompt-library)? And tell me which specific prompt or run you plan to demo so I can name it on the debrief slide.

### Slide 14: Demo 3 debrief (~45 seconds)

- **Visual**: The chain diagram again, this time annotated. Each link reads "logged" or "versioned" or "evaluated."
- **Lesson**: "Provenance is not faith in AI. It is a record you can show another person. Without the record, you have an opinion. With the record, you have a defense."
- **The Harari connection**: Ch. 10 (the Future). The institutions that will earn trust in AI-assisted research are the ones with the receipts.

---

## Section 4: Demo 2, defend this answer (slides 9 to 11, ~6 minutes)

### Slide 9: Setup (~45 seconds)

- **Visual**: Single prompt on screen
- **Title**: Defend this answer
- **The setup**: "Same prompt. Same model. Three runs."
- **[NEED:]** the specific prompt you want to use. Options:
    - A. "Summarize this paper in 100 words" (using a CNR-relevant paper)
    - B. "Extract the three main findings from this abstract"
    - C. "What is the sample size in this study?" (numerically specific, easier to spot divergence)
    - D. Something more provocative from your notes
- **The ask**: "If you ran this prompt yesterday, today, and tomorrow, would you get the same thing? Would you cite the version you got today?"

### Slide 10: The demo (~3 minutes)

- **Visual**: Three columns, three outputs side by side
- **What you do**: Run the same prompt three times live (or pre-record). Show divergence.
- **What to highlight**: [NEED:] which divergences land hardest. Candidates: number that changes (e.g., sample size 245 vs 247 vs "approximately 250"); claim that contradicts itself across runs; nuance that disappears in one run but not others.
- **Optional**: Run it with temperature=0 to show even "deterministic" mode can differ across model versions or token-by-token sampling artifacts.
- **Speaker note**: "There is no 'the AI answer.' There is a distribution. You're picking one sample without knowing it."

### Slide 11: Debrief (~90 seconds)

- **Visual**: A single quote-style slide
- **The lesson**: "The AI said so" is not a citation. It is a coin flip you didn't know you were taking.
- **The grad-student angle**: When you cite a source, you are vouching for something a future reader can verify. AI outputs are not verifiable in this sense, by design.
- **The Harari connection**: Ch. 8 (Networks). Networks scale information faster than they verify it.
- **Closer**: "If the answer changes when you ask twice, it is not an answer. It is a sample."

---

## Section 5: Demo 3, defend this chain (slides 12 to 14, ~6 minutes)

### Slide 12: Setup (~60 seconds)

- **Visual**: A single claim on screen, in big type
- **Title**: Defend this chain
- **The setup**: A single specific claim, like "$525,000 in NSF graduate student support went to Idaho researchers studying ancient forest networks in 2024."
- **The ask**: "Where did this number come from? How would you verify it? How many steps does it take to trace it back?"
- **Speaker note**: "This one is the hardest because the AI didn't make any one mistake. It made a chain of small choices."

### Slide 13: The demo (~3 minutes)

- **Visual**: A horizontal chain of custody, six or seven nodes
- **The chain**: Source PDF -> OCR -> structured JSON -> aggregation script -> CSV -> dashboard -> published claim
- **What you do**: Walk the audience through each link. At each one, point out where AI participated and what you'd have to vouch for to defend it.
- **[NEED:]** which evidence to show. Options:
    - A. Use the AI4RA evaluation harness to show actual replicate runs (heaviest, most credible)
    - B. Use the data lakehouse to show the same number arrived at via two different pipelines (medallion architecture demo)
    - C. A simpler hand-walked diagram (lowest tech risk, fastest to build)
- **The pivot**: "Notice that the AI is in the chain at multiple points. Each time, it's a link you have to vouch for personally."

### Slide 14: Debrief (~90 seconds)

- **Visual**: The chain again, this time with each link annotated as "you vouched for this"
- **The lesson**: Provenance is a chain, not a fact. Every link is a defense you must be able to mount.
- **The trap**: AI does not give you provenance. It hides it. The output looks finished, which is exactly when you stop checking.
- **The Harari connection**: Ch. 10 (the Future). Information systems that hide their seams produce confident readers who cannot defend what they read.
- **Closer**: "If you cannot point to where every number came from, you do not have a claim. You have a vibe."

---

## Section 6: Closing (slide 15, ~2 minutes)

### Slide 15: Takeaway and handoff (~2 minutes)

- **Visual**: Thesis again, plus the three-zone decision framework
- **Headline (return)**: Provenance is the new literacy.
- **The framework** (from the Layman reading): three zones. Automate where the chain is short and verifiable. Augment where you stay in the loop. Leave alone where you cannot defend the output.
- **The grad-student commitment**: "Build the verification habit now, before AI use becomes a reflex you no longer notice."
- **Handoff to discussion**: "One question to start: what is one claim you have made this semester that you could not defend if I asked you to right now?"
- **[NEED:]** any specific other discussion seed you want.

---

## Open questions for Barrie

Decided:
- Slide 3 hook = Vandalizer + NSF 26-508 RFP, cost-sharing FLIP
- Slide 6 Demo 1 = Vandalizer link + DEB award notice download, Barrie drives live
- Slide 8 Demo 2 conceptual = port the Module 1 token-builder interactive
- Slide 9 = Data Crawler Carl link card
- Slide 10 = back to Vandalizer for live reproducibility check
- Slide 13 Demo 3 = AI4RA Prompt Library + Mindrouter, two-card slide

Still need:
1. **Vandalizer URL**: confirm `https://vandalizer.nkn.uidaho.edu/` (your message) vs `https://vandalizer.uidaho.edu` (the existing Module 1 slide). Two different instances, or one?
2. **Mindrouter URL**: confirm `https://mindrouter.uidaho.edu` with no path, and that it is publicly reachable for the audience.
3. **AI4RA Prompt Library URL**: confirm `https://github.com/AI4RA/prompt-library`.
4. **Slide 10 Vandalizer prompt**: which specific prompt or setup will you re-run to show non-determinism live? Same setup as Demo 1, or a different one?
5. **Slide 13 demo content**: which specific prompt and run do you plan to walk through in Prompt Library + Mindrouter? So I can name them on the debrief.
6. **Slide 13 mental note**: do you want the prompt-library and mindrouter cards side-by-side on one slide, or one per slide (would push us to 16 slides total, slightly over time budget)?

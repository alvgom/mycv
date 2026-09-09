# Roche — Senior Computational & Applied AI Scientist (2026)

Living notes for this application. Updated continuously. Nothing here is
compiled into the CV.

## Job at a glance

- **Role:** Senior Computational & Applied AI – Scientist
- **Team:** Imaging Data Insights (within Computational Medicine, Computational
  Sciences Centre of Excellence / CoE). Team split across Basel, Penzberg, South
  San Francisco.
- **Location:** Basel
- **Reports to:** Group Leader – Imaging Data Insights Europe
- **Hiring manager:** Stefan Frässle. **Recruiter:** Haley Belfield.
- **Grade:** SE6 (target). **Job family:** Research. **Type:** Full time, regular.
- **Req ID:** 202608-121873. Posted 08/31/2026.
- **Nature:** Internal **Talent Marketplace** opportunity (Alvaro is already at
  Roche, `alvaro.gomariz@roche.com`).
- **Role character:** Individual contributor senior scientist — "mentor junior
  scientists," "influence without formal authority." Not a people-management
  line role.

## Overall verdict

**Strong fit (~8/10).** Core requirements met, several exceeded. Once the GenAI/
agentic and multimodal/clinical material below is surfaced, the two apparent
gaps largely close. Remaining genuine gap: classic radiology modalities
(CT/PET/DXA) and neuroimaging toolchains — not central to Alvaro's history.

## Requirement → evidence mapping

Meets or exceeds:
- PhD (Computer Vision, ETH) + ~5.5 yrs pharma R&D at Roche. **Exceeds** the "3+ yrs".
- Deep biomedical image analysis / AI/ML — whole career.
- Computational workflows for quantitative imaging — MLOps, ETL, gigapixel data
  engineering, automatic QC of annotations, Nextflow, SLURM/LSF.
- Translate imaging → decision-driving insights — AI covariate to improve
  probability of success in IBD trials; build-vs-buy benchmarking guiding
  corporate decisions. (This is the JD's exact language.)
- Multidisciplinary teams / influence without authority — matrix teams of 5–10;
  aligning biostatistics, clinical science, early development; co-leading a
  25–35-person data science network.
- Trusted, business-oriented partnerships — sourced/closed Scribe contract,
  Virgo evaluation agreement; academic + gastroenterologist collaborations.
- Model validation / uncertainty quantification / QA / experimental design —
  signature strength (Bayesian regression, uncertainty-aware detection;
  evaluation "beyond accuracy," robustness + subgroup analyses).
- Software engineering best practices — Git, CI/CD, Docker, AWS, SLURM & LSF.
- Foundation models — company-wide digital-pathology FM initiative, DINOv2
  adaptation, adopted internal package, 3 lead-author papers. **Differentiator.**
- Python + PyTorch/TensorFlow + OpenCV/ITK/SciPy.

Partial / needs surfacing (material exists — see "Source facts" below):
- Generative AI / Agentic AI — real experience exists but is **absent from the
  CV**. See Source facts §1.
- Clinical imaging modalities (MRI, ultrasound, ophthalmic, micro-CT) — present
  in the CV but under-emphasised; publications back all of them. See §2.
- Multimodal integration (imaging + clinical) — strong IBD work not yet
  captured. See §3.
- Imaging platforms (3D Slicer, Fiji, Napari) — has experience, not listed. See §4.

Genuine gaps (no evidence; do not fabricate):
- CT / PET / DXA modalities.
- Neuroimaging toolchains (FreeSurfer / FSL / SPM).
- Omics (genomics/transcriptomics/etc.) — adjacent only (H&E → genetic-screening
  signal). See §5 for RWD.
- MONAI / scikit-image not listed (adjacent to existing skills).
- R is "basic" only.

---

## Source facts provided by Alvaro (for later inclusion; not yet in CV)

### §1 Generative & Agentic AI  — real experience, currently invisible

What "GenAI / Agentic AI" means in these roles (working definition):
- **Generative models** — LLMs and multimodal foundation models; also
  image-generative methods (diffusion, GANs) for synthesis/augmentation.
- **Agentic AI** — an LLM that *plans and acts*: calls tools/APIs, retrieves
  data, executes multi-step workflows autonomously. Common vocabulary: tool use
  / function calling, ReAct, RAG (retrieval-augmented generation), vector DBs,
  **MCP (Model Context Protocol)**, orchestration frameworks (LangChain/
  LangGraph, LlamaIndex, AutoGen, CrewAI).
- **AI coding agents** — using agentic tools to accelerate software delivery.
  Industry-known tools to name (claim only what you actually use): Claude Code,
  Cursor, GitHub Copilot, Windsurf, Aider. **[VERIFY: which ones Alvaro uses]**

Alvaro's actual experience (CONFIRMED; his own words, to be rephrased for CV):
- **Generative models:** strong grasp of the *foundations*; **no hands-on model
  training/building**. Familiar with *applications* — building software that
  calls **LLMs via API**, and **LangChain**. (Claim application/integration
  familiarity, not model development.)
- **Agentic AI:** hands-on via **LangChain** in the hackathon project (below).
- **AI coding agents:** **very extensive** use of **Claude Code, Cursor, and
  GitHub Copilot** — part of his **latest (current) role**. This is the
  everyday-credibility anchor.
- **Built an MCP server** to interact with a complex relational database in
  **AWS Athena**. Previously the team depended on an external SQL engineer;
  the MCP lets anyone query the data directly and even learn SQL. **Directly
  tied to the IBD AI project** (that project's data lives in Athena). Strong
  concrete example of agentic infrastructure that unblocked a whole team.
- **Hackathon — "Supplier Intelligence"** (Roche × Microsoft Azure AI
  Hackathon, Nov 2024; team of 4: Prajit Kadavil, Mathieu Cayssol, Alvaro
  Gomariz, Anil Yuce). Accurate details from the project deck
  (`Supplier Intelligence.pdf`):
  - Automates supplier due-diligence for a Global Category Manager (Biologics
    & Chemicals): builds a matrix of suppliers with **ISO certifications
    (9001, 13485, 14001)** and **sustainability rankings (EcoVadis, MSCI ESG,
    CDP, Sustainalytics)**, returning **structured JSON output with source
    URLs**.
  - **Stack:** Google search to locate company sites / certification PDFs +
    custom LLM pipelines (**ScrapeGraphAI**) + **GPT-4** to standardize
    extracted content; **Streamlit** UI **deployed on Azure**; code on GitLab.
    Learnings noted: multiple websites beat one; RAG didn't help much.
  - **Concrete value:** replaces a manual search that currently takes **~1 hour
    per supplier**; scalable via parallel backend (no supplier-count limit).
  - **Tooling note:** deck emphasizes ScrapeGraphAI/GPT-4; Alvaro earlier said
    LangChain. **[CONFIRM which to name in the CV]** — skills.tex currently
    lists LangChain.
  - **DECISION: include as a side bullet under the current Roche position**
    (framed as a side project / hackathon), not a headline.

Takeaway: the GenAI "gap" is really a *surfacing* problem, not a real gap.
Reframe as "Generative & Agentic AI: LLM agents (API), LangChain, MCP, RAG;
AI-assisted development with Claude Code / Cursor / Copilot."
Honesty guardrail: application/integration + agentic tooling, **not** training
generative models from scratch.

### §2 Clinical imaging modalities — present but under-emphasised
- **MRI** — PhD-era; **did NOT result in a paper.** It was part of the
  **missing-modalities / attention-mechanism** PhD work. **DECISION: add MRI to
  the CV** in that context (attention + missing modalities), not as a separate
  publication.
- **Ultrasound** — "Siamese Networks with Location Prior for Landmark Tracking
  in Liver Ultrasound Sequences," ISBI 2019 (lead author).
- **Ophthalmic (OCT)** — Roche Data Scientist / postdoc era; multiple pubs incl.
  MICCAI 2022 (lead), several ARVO abstracts, and **Medical Image Analysis 2025
  (lead author)** — a recent top-tier ophthalmology imaging paper.
- **micro-CT** — PhD-era.
- Interacted with **clinicians** on all of these.
- Note: the doctoral-researcher CV bullet already lists "MRI, ultrasound,
  micro-CT, and different microscopy types," and the postdoc bullet mentions
  ophthalmic segmentation — so modalities are *there* but easy to miss.
- **DECISION: highlight the modality breadth primarily in the COVER LETTER**
  (Alvaro's preference), while keeping/adding MRI in the CV per above. Don't
  claim CT/PET/DXA.

### §3 Multimodal (imaging + clinical) IBD prognostic modelling — KEY PROJECT
- Core of the IBD work: built **prognostic models that beat the clinical
  baseline** (a hard baseline to beat), combining **endoscopy imaging + clinical
  data** — Alvaro led this multimodal integration.
- **Application:** assessed the model's prognostic value to support its
  inclusion as a **covariate adjustment** in the **statistical analysis plan
  (SAP) of a Phase 3 trial (AMETRINE)**.
- **Result (CONFIRMED, use with care):** the model boosted **effective sample
  size by ~3.4%** on the target dataset vs. **~0.5%** from the clinical baseline.
  Ultimately **not enough evidence for inclusion** in the SAP.
  - **DECISION (Alvaro's lean):** the exact numbers are "a bit meaningless
    without the right context" → likely **omit raw numbers on the CV**; describe
    the work qualitatively ("prognostic multimodal model evaluated for
    covariate-adjustment in a Ph3 trial SAP, outperforming the clinical
    baseline"). Numbers can be kept in reserve for interview.
- This is prime evidence for the JD's "patient stratification, biomarker
  development, endpoint strategies, portfolio decisions" and
  "integrate imaging with clinical/digital/omics/RWD" language. Also shows
  direct collaboration with **biostatistics + clinical development**.

### §4 Imaging platforms to add to Skills
- **3D Slicer, Fiji, Napari** — Alvaro has hands-on experience. Add to the
  "Frameworks & tools" (or a dedicated imaging line) in `skills.tex`.
  (Fiji/ImageJ + ITK already implied; make explicit.)

### §5 Omics / RWD — clarification
- **Omics** = molecular profiling data (genomics, transcriptomics, proteomics,
  etc.). Alvaro has **no direct omics** work; closest is lung-cancer H&E →
  signal "comparable to routine genetic screening" (imaging as proxy — adjacent,
  not omics itself).
- **RWD (real-world data)** = data from routine clinical practice / outside
  controlled trials (EHR, registries, claims, routine imaging).
- Alvaro has **BOTH trial data and RWD** experience in IBD (CONFIRMED):
  - **Trial data:** participated in **curating/harmonising large historical
    trials**, adapting older coding to modern trial standards — a substantial
    **data-harmonisation effort done jointly with biostatistics**.
  - **RWD:** ingested a **real-world dataset from the Paris IBD center** and,
    with his team, curated it for integration into Roche's current databases.
- **DECISION: capture both in the current Roche position** — trial-data
  harmonisation (with biostats) and RWD ingestion/curation (Paris IBD center).
  Strong hits on "multimodal data integration," "RWD," and cross-functional
  partnership with biostatistics.

### §6 Leadership scope & style + sharper facts (from principal-scientist letter, 2026-09)
Source: an internal cover letter Alvaro used applying for Principal AI/ML Data
Scientist in his own group. Learnings to reuse (all Alvaro's own words/claims):
- **One-line unifier:** "technical expert in multimodal ML, with experience
  across ophthalmology, oncology, and IBD." Ties the whole career together;
  candidate line for CV quote and/or cover letter.
- **What "multimodal" means for him:** methods for **imaging and unstructured
  clinical data** (use this precision instead of bare "multimodal").
- **Leadership style (for principal-level signalling):** leads through
  **technical authority + cross-functional alignment + capability building**,
  not line management — maps onto the JD's "influence without formal authority"
  and "mentor." Scope already spans strategy/roadmap, clinical-trial impact,
  methodology, data/annotation, external partnerships, and community =
  principal-level breadth.
- **Sharper facts to reconcile with the CV:**
  - Contract engineers: letter says **4** (CV currently "2–4"). **[CONFIRM]**
  - **Virgo:** "evaluation agreement for use of their foundation model in our
    main use case" (CV currently says "image-analysis evaluation and a potential
    multi-sponsor consortium"). **[CONFIRM which is current/accurate]**
  - **Scribe:** contract **plus ongoing assessment for other projects**.
  - "5 renowned academic experts" = **KOLs**; gastroenterologists = GI doctors.
  - Foundation-model development + **patent application** already reflected.
- **DECISION pending:** whether to reintroduce a light leadership/style note in
  the CoE letter (Alvaro earlier cut leadership as "too much"; but it supports
  the principal-level aim). Keep CV leadership bullets as the main vehicle.

---

## Strategy decisions

### Level / grade
- Posting is SE6 = **same level Alvaro holds now**.
- Alvaro's plan: **request Principal Scientist level** (believes it's realistic).
- Guidance: **demonstrate** principal-level scope in the materials (strategy,
  cross-functional leadership, external partnerships, mentoring, org-level
  impact) but **negotiate the actual grade in conversation** with the recruiter
  (Haley Belfield) / hiring manager (Stefan Frässle) — early screening or
  interview — rather than stating "I want a higher grade" in the cover letter.
  Since it's an internal move, raising it with the recruiter up front is natural.
  **[DECISION pending Alvaro's preference: cover letter vs. interview.]**

### Quote / positioning
- Switch the active `\quote` in `cv.tex` to the **research-oriented variant**
  (foundation models, multi-modality, uncertainty estimation, rigorous
  statistical evaluation) — better JD match than the leadership-forward one.
  Alvaro agreed.
- Keep leadership impact visible in the experience bullets (supports the
  principal-level ask) without the quote leading on "team lead."

### Framing / ophthalmology
- Do **not** frame Alvaro as a current ophthalmology specialist — recent work
  isn't there; would feel inauthentic.
- But it's legitimate to note a **recent top-tier ophthalmology imaging
  publication (Medical Image Analysis 2025)** produced via background work
  during the last position — evidence of clinical-imaging-biomarker breadth.
- Lead the story with **rigorous evaluation + multimodal + foundation models +
  clinical decision impact (IBD)**; use ophthalmology/ultrasound/MRI as
  breadth evidence. The **cover letter** is the place to connect these dots.

### Cover-letter narrative arc (Alvaro's idea, 2026-09)
Three-act "insider returning to early research" story:
1. **Early research** — Alvaro's Roche **postdoc (Mar 2021–Jul 2022) was in
   pRED Informatics**, working on ophthalmic OCT. That organization is related
   to (has since been reorganized/transformed toward) today's **Computational
   Sciences CoE** — "not exactly the same, but I know the group well."
   **[CONFIRM lineage wording; don't overstate "predecessor" if not literally
   true — safe framing: "what was then pRED Informatics" + "I know this world
   from the inside".]**
2. **Product development** — moved to the applied side; learned what it takes to
   advance ML into **external-facing software** and into **evidence robust
   enough for late-stage clinical trials**. Supporting CV facts: AMETRINE-1/2
   Ph3 covariate work; Scribe/Virgo partnerships; MLOps; digital-pathology
   software package; OCT analysis software (Momaku, ROSA).
3. **Return to early research** — bring that delivery/clinical rigor back
   upstream. Candidate "why/where" angles: (a) leverage — where computational
   science most shapes the portfolio, before programs reach the clinic;
   (b) bridge — pair early-research creativity with product-grade delivery
   discipline; (c) de-risk — reusable, rigorously evaluated imaging/multimodal
   AI that de-risks decisions early; (d) evidence — turn complex imaging into
   decision-ready evidence that shapes program design/prioritization.
   **[DECISION pending: which angle(s).]**

---

## Executed changes (2026-09-08)

Baseline before edits: **5 pages**. After edits: **5 pages** (no growth). CV and
cover letter both compile cleanly with XeLaTeX. One pre-existing 15pt overfull in
the experience table alignment (title/date columns) — not caused by these edits;
left untouched per CLAUDE.md typography rule.

**Findings that changed the earlier list:**
- The research-oriented `\quote` was **already active** (not the leadership one).
  So no swap — replaced it with a fresh role-tailored quote instead (below).
- **MRI/ultrasound/micro-CT already listed** in the doctoral "imaging domains"
  bullet — no new MRI bullet needed; breadth surfaced in the cover letter.
- User **removed the duplicate Data-scientist entry** themselves.

CV:
- [x] `cv.tex`: replaced active `\quote` with role-tailored text (dropped
      "foundation models"; GenAI framed as *applied*, not core). Old research +
      leadership quotes preserved as commented VARIANTs.
- [x] `skills.tex`: added **Generative & Agentic AI** line; added dedicated
      **Imaging tools** line (3D Slicer, Fiji, Napari, ITK, OpenCV; ITK/OpenCV
      moved out of Frameworks).
- [x] `experience.tex` (Senior DS): rewrote to 7 bullets — colonoscopy objective
      (prognostic AI covariate + reusable assets); multimodal Ph3 covariate
      (qualitative, no numbers); annotation campaign + scoring/detection at
      inter-rater agreement; RWD (Paris) + trial harmonisation + MCP/agentic
      (merged); tightened Scribe/Virgo; softened DP adoption ("two teams");
      DS network. + **OPTIONAL hackathon-iso** bullet [ON] (LangChain agent).
- [x] `experience.tex` (Postdoc): 3 clumsy bullets → 2 (OCT methods; prototyped/
      informed features, 3 devices + RWD, informed later FM work).
- [x] `experience.tex` (Data scientist Aug 2022): reworded bullet 5.
- [x] `experience.tex` (doctoral): "missing modalities" → "learning with missing
      modalities".
- [x] `publications.tex`: typo "Ibañez v" → "Ibañez V".

Cover letter:
- [x] Created `cover_letters/letter_RocheCSCoE.tex` (1 page). Generic opening;
      connects imaging biomarkers + modality breadth (OCT/US/MRI/micro-CT) +
      rigorous eval/uncertainty + multimodal IBD prognostic work + MCP/agentic +
      partnerships; cites MedIA 2025 as breadth; demonstrates principal-level
      scope without stating a grade ask.
      (See "Finalization pass (2026-09-09)" below for the final letter state —
      address, date, tone, and content all resolved.)

## Resolved (was: open questions)
1. **AI coding tools:** Claude Code, Cursor, GitHub Copilot (extensive, current
   role). GenAI = application/integration + LangChain, not model training.
2. **Hackathon agent:** include as a side bullet under current Roche role
   (framed as company hackathon).
3. **IBD metric:** AMETRINE Ph3, covariate-adjustment in SAP; +3.4% effective
   sample size vs +0.5% baseline; not adopted. Keep qualitative on CV; numbers
   for interview.
4. **IBD data:** BOTH — trial-data harmonisation (with biostats) AND RWD (Paris
   IBD center). Capture both.
5. **MRI:** no paper; part of PhD missing-modalities/attention work — add to CV.
6. **Level ask:** demonstrate principal scope in materials; negotiate grade in
   conversation (not in the letter).

## Finalization pass (2026-09-09)

Iterated live with Alvaro. Final state of all three documents:

**Page counts (all compile clean, XeLaTeX):** `cv.pdf` 5 pp · `scientific_contributions.pdf` 3 pp · `cover_letters/letter_RocheCSCoE.pdf` 1 pp. (CV/supplement grew a page from the added abstracts; core CV still ~2 pp, rest is publications.)

**Cover letter — finalized (`letter_RocheCSCoE.tex`):**
- Address set to **Imfeldstrasse 103, CH-8037 Zürich**; date **9th September 2026**; generic opening ("Dear Hiring Team").
- Rewritten for a natural, non-corporate tone; **imaging-scientist identity** made explicit ("the common thread has been extracting quantitative information from images and connecting it to biological and clinical questions").
- Opening: role sits in early research (where he started, "now evolved into Imaging Data Insights" — **lineage kept as-written per Alvaro**) + applies product-development experience.
- Lessons framed as personal conviction (multimodal; plan so evidence "grows with the molecule"; regulatory/productization vs value); GenAI reframed to senior "newer AI tooling, including foundation models and agentic approaches… without compromising [reproducibility]".
- One concise leadership line (technical direction + cross-functional alignment + capability building); closes on the "imaging science + multimodal AI + product-dev + cross-functional leadership" combination.
- Nature/Science/MedIA citations removed from the letter (kept in CV); no em-dashes.

**CV — additional edits this pass:**
- Quote: role-tailored, modest, no "foundation models"/superlatives (final wording in `cv.tex`).
- `experience.tex` Senior DS: added **reusable assets** clause (bullet 1); **mentoring** line ("seven interns across my Roche roles"); dissemination bullet says **"seven conference abstracts as first or last author"** (= the IBD-specific count; **kept bare per Alvaro**, though the full conference list totals 10 incl. 3 digital-pathology); bullet 6 reworded "Earlier in this role (through March 2024)"; hackathon = "Side project: Built an LLM agent (ScrapeGraphAI, LangChain, RAG)…".
- `skills.tex`: **Generative & Agentic AI** line (RAG removed — scoped to the hackathon bullet instead); dedicated **Imaging tools** line.
- `publications.tex`: added **UEG Week 2025 ×2** (UEG Journal Vol 13, Issue S8; no per-abstract DOI — section DOIs .70039/.70035 are index/collection, not usable), **DDW 2026 ×1** (last author), **UEG Week 2026 ×2 (accepted)** (last author); standardized **Gutierrez-Becker** hyphenation; fixed "Ibañez V".

**Open decisions — kept as-is per Alvaro (2026-09-09):**
- CV bullet 2 keeps **"outperforms the clinical baseline"** (not softened, unlike the letter).
- Abstract count stays bare **"seven"** (not qualified "on this program", not softened to "multiple").

## Still open
- **ARVO abstract reformatting** — Alvaro flagged one ARVO/IOVS entry (articleid 2783182) needs correcting, but the page is Cloudflare-blocked; **waiting on pasted citation details** (title/authors/volume/issue/DOI) and which of the 3 ARVO entries it is.
- Per-abstract DOIs for the two **UEG 2025** entries, if they ever become available (currently none exist — section-level only).

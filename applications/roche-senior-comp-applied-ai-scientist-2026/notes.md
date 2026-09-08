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
- **Hackathon (company gig):** built a **LangChain agent for supplier
  ISO-certification verification** — gathers supplier info from the internet,
  verifies whether certification criteria are met, and returns links to the
  supporting sources (autonomous retrieval + tool use + verification +
  citations). **DECISION: include as a side bullet under the current Roche
  position** (framed as a company hackathon), not a headline.

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

---

## Planned changes (to execute later, after review)

CV:
- [ ] `cv.tex`: activate research-oriented `\quote` variant.
- [ ] `skills.tex`: add **Generative & Agentic AI** line (LLM APIs, LangChain,
      MCP, RAG; AI-assisted dev with Claude Code / Cursor / Copilot);
      add **3D Slicer, Fiji, Napari** to imaging tools.
- [ ] `experience.tex` (current Roche entry): surface
      (a) **MCP/Athena** agentic infrastructure (democratised data access, tied
          to IBD project),
      (b) **multimodal clinical+imaging IBD prognostic model** evaluated for
          Ph3 (AMETRINE) covariate adjustment in the SAP, beating clinical
          baseline (qualitative; numbers held for interview),
      (c) **RWD (Paris IBD center) ingestion/curation** + **historical-trial
          data harmonisation with biostatistics**,
      (d) **side bullet: LangChain hackathon agent** (supplier ISO-cert
          verification).
- [ ] `experience.tex` (doctoral entry): add **MRI** in the missing-modalities /
      attention-mechanism context (no paper — describe as project work).
- [ ] Reuse/adjust existing VARIANT blocks where possible; keep leadership scope
      visible (supports the principal-level ask).

Cover letter (new, e.g. `cover_letters/letter_RocheCSCoE.tex`):
- [ ] Connect: clinical imaging biomarkers + **modality breadth (OCT/US/MRI/
      micro-CT)** + rigorous eval/uncertainty + multimodal (clinical+imaging) +
      foundation/agentic AI + cross-functional partnerships (biostats, clinical).
- [ ] Note the recent **Medical Image Analysis 2025** ophthalmology paper as
      breadth evidence (not as current focus).
- [ ] **Demonstrate** principal-level scope; do **not** state the grade ask in
      writing — raise it with recruiter/HM in conversation.

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

## Still open
- (none blocking) — ready to draft edits when Alvaro says go.

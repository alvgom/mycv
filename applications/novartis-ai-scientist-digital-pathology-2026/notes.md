# Novartis — AI Scientist, Image Analysis & Digital Pathology (2026)

Living notes for this application. Updated continuously. Nothing here is
compiled into the CV.

## Job at a glance

- **Role:** AI Scientist – Image Analysis & Digital Pathology
- **Team:** Oncology Data Science, AI & Innovation Team, Biomedical Research
- **Location:** Basel or Cambridge (onsite; relocation offered)
- **Req ID:** REQ-10084320. Posted 2026-08-24.
- **Level:** individual-contributor scientist. PhD (ML/CS/Applied Math/Comp Bio)
  or MSc + 4 yrs industry.
- **Salary (CH):** 102,200 – 189,800 CHF.
- **Character:** hands-on AI/ML for digital pathology in oncology drug discovery;
  publications and conference presentations expected.

## Job requirements (verbatim gist)

- AI/DL to extract insights from digital pathology imaging: **H&E, IHC, mIF,
  spatial transcriptomics**.
- **Foundation models** (pre-trained, self-supervised, multi-purpose,
  multi-modal); generative AI for drug discovery.
- **Imaging biomarker development**; collaborate with **pathologists** and
  translational teams to interpret image-derived biomarkers.
- Evaluation, validation, benchmarking of image-analysis algorithms.
- **Tissue segmentation, cell phenotyping, feature extraction, spatial
  analysis**.
- Publications / conference presentations.
- **PyTorch**; segmentation/classification/detection/representation learning.
- Bonus: **generative AI, DP foundation models, geometric deep learning,
  multi-modal learning**.

## Overall verdict

**Strong fit (~8/10).** Mostly a re-emphasis job, not a rewrite. The base CV was
tuned for the Roche Imaging Data Insights / CoE role (broad imaging + clinical
decision + IBD-led); this role is narrower: digital pathology, oncology,
foundation models, cell/spatial analysis.

## Requirement → evidence (verified)

Strong / direct:
- **Cell detection, phenotyping, feature extraction, spatial analysis** —
  the PhD core. Verified via abstracts (Europe PMC):
  - Nat Commun 2018: *"spatial statistical methods to examine cell distributions
    and physical associations"* over defined stromal **cell types**.
  - Sci Adv 2022: uncertainty-aware **cell detection** + probabilistic spatial
    analysis.
- **DP foundation models** — company-wide FM initiative: DINOv2, 35M+ **H&E**
  WSIs, distributed pre-training, adopted internal package, 3 lead-author papers.
  (H&E only — user confirmed the product focus was H&E.)
- **H&E / oncology** — lung-cancer patient stratification (MIL, GNN, SSL,
  survival).
- **Pathologist collaboration** — worked closely with pathologists guiding the
  clinical setting, image interpretation, and algorithm interpretability; a
  pathologist was the **clinical lead** of the lung-cancer project.
- **Evaluation / benchmarking** — build-vs-buy benchmarking; evaluation beyond
  accuracy; uncertainty quantification.
- **Geometric DL / multimodal** — pyramidal GCN (multiscale topology); multimodal
  imaging + clinical.
- **PyTorch, PhD in CV, publications** — met.

Honest bridges (NOT direct claims):
- **mIF (multiplex immunofluorescence)** — the PhD used multiplexed
  **immunofluorescence** microscopy (confocal, light-sheet) with heterogeneous
  antibody marker panels. Verified: NMI 2021 abstract — *"staining with a variety
  of carefully-selected markers visualized as color channels"*, method for
  *"heterogeneous datasets with combinations of markers"*. This is a genuine
  match to **mIF**, framed as multiplexed IF microscopy.
- **Spatial transcriptomics** — no transcriptomics/omics; bridge via spatial
  statistics/analysis only. Do NOT claim.

Genuine gaps (do not fabricate):
- **IHC (chromogenic brightfield)** — not done. PhD work is immunofluorescence,
  not chromogenic IHC. Bridge only via antibody-staining familiarity; do NOT
  write "IHC".
- **Spatial transcriptomics / omics** — none.
- **Generative AI** — applied only (LLM/agentic via MCP, LangChain; FM
  *adaptation*). No training of generative image models (diffusion/GANs) from
  scratch. Keep honesty guardrail.

## Decisions (from Alvaro, 2026)

1. **Re-emphasis:** promote DP but stay chronologically honest — DP is not
   current, so it gets its own **past** titled entry, not moved to the top of the
   current role.
2. **Titles:** comfortable replacing generic HR titles ("Senior Data Scientist"/
   "Data Scientist") with **functional** titles that match the actual work and
   timeline. Combine content from active + commented variants.
3. **Cover letter:** initially deferred; **now written** (`cover_letters/letter_Novartis.tex`, 1 p) in the CS-CoE tone.
4. **Gaps:** honest bridges (mIF via multiplexed IF; spatial via spatial stats);
   do not claim IHC/spatial transcriptomics.
5. **H&E only** for the DP foundation-model product work.
6. **Dates:** sequential / clean split —
   **Technical Lead — AI Video Colonoscopy: May 2024 – Present**;
   **Technical Lead — Digital Pathology & Computational Oncology: Aug 2022 – Apr 2024**.

## Planned CV structure

Roche, Switzerland (Mar 2021 – Present). Titles use scientist grade + functional
descriptor to show progression (Postdoc → AI/ML Scientist → Senior AI/ML
Scientist), state the scientist identity (echoes the Novartis "AI Scientist"
title), and avoid two identical "Technical Lead" entries reading as flat/a quick
postdoc→lead jump. Faithful rendering of the real HR titles Data Scientist /
Senior Data Scientist.
- **Senior AI/ML Scientist & Technical Lead - AI Video Colonoscopy** · May 2024 –
  Present (transferable rigor: multimodal Ph3 covariate model, rigorous/subgroup
  evaluation, annotation campaign, RWD harmonization, MCP/agentic, DS network +
  mentoring; IBD-specific detail trimmed).
- **AI/ML Scientist - Digital Pathology & Computational Oncology** · Aug 2022 –
  Apr 2024 (merges lung-cancer H&E + foundation-model variant: DINOv2, 35M+ H&E,
  distributed pre-training, adopted package, 3 papers, benchmarking; MIL/GNN/SSL/
  survival; pathologist collaboration incl. clinical lead).
- **Postdoctoral Researcher - Ophthalmic Imaging (OCT)** · Mar 2021 – Jul 2022.

Education (PhD): reword bullets to surface **multiplexed immunofluorescence
microscopy, cell detection/phenotyping, spatial analysis**.

Skills: lead ML line with digital pathology, foundation models, SSL, MIL,
GNNs/geometric DL, cell detection & spatial analysis, multi-modality.

Quote: DP + foundation models + spatial/oncology variant.

Publications: keep reverse-chronological convention (do NOT reorder by relevance
— would break the dating convention; DP papers already visible in conferences).

## Cover letter (`cover_letters/letter_Novartis.tex`)
- Tone/structure mirror `letter_RocheCSCoE.tex` (personal, first person, no
  em-dashes), but external: drops the Roche "returning to my roots" arc.
- Arc: (1) identity = quantitative imaging + biology/clinical questions, aimed at
  DP for oncology drug discovery; (2) DP core (FM on tens of millions of H&E WSIs,
  DINOv2/SSL, lung-cancer stratification, pathologist clinical lead, benchmarking);
  (3) cell detection/phenotyping/spatial analysis of multiplexed IF + 3D microscopy
  (NMI/Sci Adv/Nat Commun) as the mIF/spatial-biology bridge; (4) delivery
  discipline + FM/agentic tooling without compromising standards; (5) publications
  + light leadership, close on AI & Innovation / Oncology Data Science.
- Honesty kept: "multiplexed immunofluorescence" (not IHC); "multiplexed imaging
  and spatial biology" (no spatial-transcriptomics claim); agentic tooling framed
  as applied.
- **[FLAG] Email:** letter + CV currently use the **Roche** address. For an
  external Novartis application, consider switching both to the personal gmail
  (commented alternative already in the letter preamble).
- **[FLAG] Dateline** currently "Basel" (mirrors CS CoE); address is Zürich.

## Open / for interview
- IHC (chromogenic) — none; be ready to distinguish IF vs IHC if asked.
- Spatial transcriptomics — none; lead with spatial statistics transferability.
- Generative image models — applied FM adaptation, not from-scratch training.

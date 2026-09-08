# CV Project

This repository contains my professional CV written in LaTeX.

## Primary goal

Help me maintain, improve, and tailor the CV while preserving factual
accuracy and the existing visual quality.

## Critical factual constraints

- Never invent facts.
- Never invent employers, job titles, dates, publications, awards,
  responsibilities, technologies, results, or metrics.
- Do not add quantitative claims unless they already exist in the repository
  or I explicitly provide them.
- If a requested change would require information that is not available,
  tell me what information is missing instead of guessing.
- Rewording and reorganizing existing factual information is allowed.

## Editing principles

- Prefer concise, precise, technical language.
- Remove filler and generic corporate language.
- Prefer concrete accomplishments and technical contributions.
- Avoid exaggeration.
- Preserve technically meaningful terminology.
- Maintain consistency of tense, punctuation, capitalization, and style.
- Do not change dates or proper nouns without explicit justification.
- Do not modify visual styling unless I ask for it.

## CV length

- There is no fixed page limit. Two pages is a loose preference for the core
  CV, but supplementary information may legitimately extend it.
- After substantial edits, compile the CV and report the resulting page count
  so I can decide whether it is acceptable.
- Prefer improving wording or removing low-value content before reducing
  font size, margins, or whitespace.
- Do not silently alter typography to make content fit.

## Project structure

- `cv.tex` — primary CV; assembles content from `cv-sections/*.tex` via
  `\input`.
- `scientific_contributions.tex` — standalone supplement ("Additional
  Information"), reuses `cv-sections/publications.tex`.
- `cover_letters/*.tex` — standalone, per-employer cover letters using the
  same class.
- `ag-cv.cls` — the active document class (a customized fork of Awesome-CV).
  Note it still self-identifies internally as `awesome-cv`, which produces a
  harmless class-name warning at build time.
- `awesome-cv.cls` — the upstream original, kept for reference only. Not used
  by `cv.tex`. Do not edit it to change CV output.
- `fonts/`, `portrait.jpeg`, `fontawesome.sty` — assets.

## Content toggles

The top of `cv.tex` sets flags that switch content and formatting across
sections. Respect the selected values when editing:

- `\cvtype{long|short}`
- `\awardsmoney{yes|no}`
- `\showsupervisors{yes|no}`
- `\authornames{long|short}`
- `\publicationstype{long|short}`

## LaTeX

- Preserve the existing LaTeX architecture unless there is a good reason
  to change it.
- Prefer semantic edits over formatting hacks.
- Do not introduce unnecessary packages.
- Do not replace working macros simply because another implementation is
  possible.
- Key custom macros/environments (defined in `ag-cv.cls`): `cventries` /
  `\cventry` / `\cventryag`, `cvitems`, `cvsubentries` / `\cvsubentry`,
  `cvpublications` / `\cvpublication` / `\cvpreprint` / `\cvtalk`,
  `cvskills` / `\cvskill`, `cvhonors` / `\cvhonor`. Reuse these rather than
  hand-rolling layout.
- Preserve comments that contain useful authoring information (see the note
  on commented-out variant content below).

## Commented-out variant content

Section files intentionally contain large amounts of commented-out content.
These are alternate phrasings and variants I switch between when tailoring
the CV for different applications. They are NOT dead code.

- Do not delete or "clean up" commented-out content unless I explicitly ask.
- When editing, do not assume the uncommented version is the only relevant
  one; ask if it is unclear which variant is current.

### Marker convention

Commented-out variants are labelled with greppable marker comments so each
block is self-describing. List every marker with:

    grep -rn "VARIANT\|OPTIONAL\|ALT-ITEM\|NOTES" cv-sections/

Four tokens (all plain LaTeX comments — they never affect output):

- `% VARIANT <slug> — <description>  [ACTIVE|INACTIVE]`
  One alternative of an entry. Exactly one variant in a group is `[ACTIVE]`
  (uncommented); the rest are `[INACTIVE]` (commented). A group may be
  introduced by a `% VARIANT GROUP: <name>` header explaining the choice.
- `% OPTIONAL <slug> — <description>  [ON|OFF]`
  A standalone block that can be toggled on/off independently.
- `% ALT-ITEM — <description>`
  Alternate `\item` bullet(s) for the surrounding (active) entry.
- `% NOTES <slug> — <what this is about>` … `% END NOTES <slug>`
  A free-form, unpolished brain-dump attached to a specific entry (see
  "Tailoring notes" below).

When adding or editing variants, keep the marker and its `[STATE]` accurate.
When switching which variant is active, update the `[STATE]` fields so exactly
one variant per group remains `[ACTIVE]`.

### Tailoring notes (`NOTES` blocks)

A `NOTES` block is raw source material I attach to an entry — quick, unpolished
thoughts, extra facts, context, or hints about what to emphasise for certain
applications. Format (every line a LaTeX comment, so it never renders):

    % NOTES roche-lead — raw material for the current Roche role
    % led the colonoscopy thing end to end, ~10 people
    % for research-heavy roles stress the foundation-model / DINOv2 work
    % for leadership roles stress cross-functional + stakeholder alignment
    % patent filed 2024 (check exact number before using)
    % END NOTES <slug>

How to use these blocks when I ask you to write or tailor a section — either
from explicit instructions or to match a specific job/position:

- Treat `NOTES` as a **pool of source facts and guidance**, not as text to
  insert. Never paste note text verbatim; rephrase into the CV's concise,
  technical style.
- Select only what is **relevant** to the request or target role; ignore the
  rest. Different applications will draw on different lines from the same block.
- The normal factual constraints still apply. Notes count as information I
  have provided, so you may use facts stated there — but do not extrapolate
  beyond them, and if a note is vague, flags uncertainty ("check…"), or would
  need a number I have not given, ask rather than invent.
- Notes are working scratch space: never delete or rewrite them unless I ask,
  and do not "promote" a note into a visible bullet without my go-ahead.

## Compilation

This project **must** be compiled with XeLaTeX (it uses `fontspec`,
`unicode-math`, and custom OTF/TTF fonts loaded from `fonts/`). Do not use
pdfLaTeX; it will fail.

After making substantive changes, compile the CV.

Primary build command:

    latexmk -xelatex cv.tex

The supplement compiles the same way:

    latexmk -xelatex scientific_contributions.tex

Note on environment: the CV is normally authored on Overleaf. A local build
requires a full TeX Live (not BasicTeX); the class depends on `enumitem`,
`tcolorbox`, `sourcesanspro`, and `xifthen`, which BasicTeX does not ship.

If compilation fails:

1. Read the LaTeX error.
2. Determine whether the failure was caused by your edits.
3. Fix the root cause.
4. Compile again.
5. Do not consider the task complete until the document compiles successfully.

Also check for:

- undefined references
- missing files
- significant overfull boxes
- unexpected page-count changes

## Git

- Inspect `git diff` before finishing a substantial change.
- Do not commit or push unless I explicitly ask you to.
- Do not rewrite Git history unless I explicitly request it.
- Do not delete untracked files without asking.
- Keep changes focused on the task I requested.

## Working style

For substantial CV changes:

1. Inspect the relevant existing content.
2. Explain briefly what you propose to change.
3. Make the changes.
4. Compile the CV.
5. Inspect the resulting diff.
6. Summarize what changed and flag any unresolved issues.

For small wording changes, you may edit directly without producing an
unnecessary plan.
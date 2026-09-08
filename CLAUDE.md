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

- The target CV length is 2 pages.
- After substantial edits, compile the CV and check that the page count
  remains within the target.
- Prefer improving wording or removing low-value content before reducing
  font size, margins, or whitespace.
- Do not silently alter typography to make content fit.

## LaTeX

- Preserve the existing LaTeX architecture unless there is a good reason
  to change it.
- Prefer semantic edits over formatting hacks.
- Do not introduce unnecessary packages.
- Do not replace working macros simply because another implementation is
  possible.
- Preserve comments that contain useful authoring information.

## Compilation

After making substantive changes, compile the CV.

Primary build command:

    latexmk -pdf cv.tex

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
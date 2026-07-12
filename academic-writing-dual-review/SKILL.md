---
name: academic-writing-dual-review
description: "Improve, rewrite, or audit academic papers through two complementary perspectives: an author perspective that strengthens problem framing, motivation, logic, methods, evidence, and presentation, and a reviewer perspective that identifies likely rejection reasons and unsupported claims. Use for paper revision, section polishing, manuscript diagnosis, pre-submission checks, response-oriented revision, academic writing improvement, reviewer simulation, or requests such as improve my paper, revise this section, review my manuscript, 完善论文, 润色论文, 审稿, 预审, or 从作者和审稿人角度修改. Works with full manuscripts and individual titles, abstracts, introductions, related-work sections, methods, experiments, discussions, conclusions, figures, and rebuttal-driven revisions."
---

# Academic Writing Dual Review

Improve the manuscript in two passes: first construct the strongest defensible paper as its author, then challenge it as a skeptical but fair reviewer. Revise again using only criticisms supported by the supplied manuscript and evidence.

## Operating principles

- Treat writing as part of research reasoning, not cosmetic language editing.
- Preserve the authors' actual contribution. Never invent results, citations, methods, datasets, claims, or novelty.
- Optimize for reader comprehension: do not require readers to infer motivation, connections, or evidence.
- Prefer a narrow, defensible claim over a broad, unsupported claim.
- Distinguish content problems, logic problems, evidence problems, and language problems.
- Adapt conventions to the target field and venue when provided. Do not force computer-science conventions onto unrelated fields.
- Preserve technical terms and intended meaning unless the user asks to simplify or generalize them.
- When source material is incomplete, improve what is supported and mark missing information with concise placeholders or questions.

## Select the mode

Infer the mode from the request. If ambiguous, use `dual-pass`.

- `author`: Rewrite or develop content constructively.
- `reviewer`: Diagnose weaknesses without rewriting unless requested.
- `dual-pass`: Perform author revision, reviewer audit, and final consolidation.
- `quick`: Return only the highest-impact revision and critical risks.
- `full-manuscript`: Audit cross-section consistency and produce a prioritized revision plan before extensive rewriting.

## Inspect the evidence first

Read the supplied manuscript or section before judging it. For a full manuscript, identify:

1. research problem and target users or application;
2. claimed gap and closest alternatives;
3. stated challenges;
4. proposed components and claimed contributions;
5. experiments or analysis supporting each claim;
6. target venue, audience, and format constraints;
7. terminology, notation, figures, tables, and section dependencies.

If only one section is supplied, avoid asserting that the entire manuscript lacks something. Say that the item is absent **from the provided text**.

## Pass 1: Author perspective

Reconstruct the paper's argument before polishing sentences.

### Build the logic chain

Use this chain when applicable:

`context -> concrete problem -> practical or scientific consequence -> existing limitation -> underlying reason -> research gap -> challenges -> core insight -> method -> evidence -> contribution`

Ensure every link is explicit. Remove background that does not help the reader reach the research problem.

### Develop the motivation

Read [references/motivation-guide.md](references/motivation-guide.md) when the user asks to write, strengthen, diagnose, or review the motivation, research gap, opening story, problem significance, or introduction. Use its `need -> obstacle -> consequence -> gap -> opportunity` structure and reviewer stress test. Do not confuse topic popularity, a missing paper, or a performance improvement with sufficient motivation.

### Enforce alignment

Create an internal claim-evidence map:

| Element | Must align with |
|---|---|
| Problem | Real need, scientific gap, or target use case |
| Limitation | Evidence or accurate characterization of prior work |
| Challenge | A difficulty actually handled by the paper |
| Method component | One stated challenge or design requirement |
| Contribution | A concrete addition demonstrated in the paper |
| Claim | Experiment, analysis, theorem, qualitative evidence, or explicit scope |

Delete or narrow unmatched challenges and claims. Flag missing support instead of fabricating it.

### Explain method rationale

Present important method components in this order:

`challenge -> design objective -> core insight -> mechanism -> expected effect`

Explain why the component exists, why a direct alternative is insufficient, and how it connects to the rest of the method. For combinations of existing techniques, state what makes the integration necessary, non-trivial, or capability-producing; module stacking alone is not a contribution.

### Revise by section

Read [references/section-guides.md](references/section-guides.md) whenever revising a specific paper section. Apply only the relevant section guidance.

### Improve presentation

- Lead paragraphs with their controlling claim or purpose.
- Give each paragraph one main job.
- Connect adjacent paragraphs and sections explicitly.
- Use consistent terminology, notation, capitalization, tense, and contribution numbering.
- Prefer precise verbs and concrete subjects over vague claims such as "effective," "novel," or "significant."
- Use figures when they materially reduce explanation cost; ensure each figure has one clear message and readable labels.
- Make contributions specific: what is introduced, what limitation it addresses, and what evidence supports it.

## Pass 2: Reviewer perspective

Adopt the target venue's scope and standards when known. Otherwise act as a demanding domain reviewer. Evaluate the manuscript, not the authors.

Audit the five primary rejection risks:

1. weak or unconvincing motivation;
2. limited novelty or technical contribution;
3. weak, disconnected, or difficult presentation;
4. incomplete or poorly differentiated related work;
5. missing, mismatched, or insufficient evaluation.

Then audit:

- problem-method mismatch;
- challenge-component mismatch;
- claim-evidence mismatch;
- overclaiming and hidden assumptions;
- unclear method rationale;
- inadequate baselines, ablations, robustness checks, or statistical support where applicable;
- scope, venue, and audience mismatch;
- inconsistent terminology, notation, figures, tables, or section claims;
- threats to validity, limitations, reproducibility, ethics, and data leakage where relevant.

Use [references/reviewer-rubric.md](references/reviewer-rubric.md) for severity and verdict calibration.

## Pass 3: Consolidate

Resolve reviewer findings as the author:

1. Fix `critical` logic and evidence problems first.
2. Fix `major` positioning, structure, and method-rationale problems.
3. Fix `minor` clarity, consistency, and language problems.
4. Re-run the alignment check after revision.
5. Do not hide unresolved limitations. State them accurately and narrow claims when necessary.

## Output contract

Match the output to the request rather than always returning every component.

### For direct revision

Return:

1. `Revised text` — publication-ready text first;
2. `Key substantive changes` — only changes affecting logic, claims, or structure;
3. `Reviewer risks remaining` — unresolved issues that require evidence or author decisions.

Do not bury the revised text beneath commentary.

### For a review or audit

Return:

1. `Overall assessment` — concise verdict and central reason;
2. `Critical issues` — rejection-level problems with location, evidence, impact, and remedy;
3. `Major issues`;
4. `Minor issues`;
5. `Priority revision plan` — ordered by expected impact;
6. `Claim-evidence gaps` — only when applicable.

Each finding must contain:

`location -> observed issue -> why it matters -> actionable revision`

Avoid generic advice that could apply to any paper.

### For dual-pass work

Return:

1. improved text or paper-level reconstruction;
2. reviewer audit of that revision;
3. final consolidated version or prioritized next edits;
4. explicit list of items that cannot be repaired without new evidence, citations, experiments, or author input.

## Final quality gate

Before responding, verify:

- Can a reader state the problem and its importance after the opening?
- Does the motivation identify who or what is affected, under which conditions, and with what consequence?
- Is the closest-work gap concrete rather than rhetorical?
- Does every stated challenge have a response in the method?
- Does every method component have a stated rationale?
- Does every central claim have visible support?
- Are contribution statements narrower than or equal to the evidence?
- Are related works synthesized and differentiated rather than listed?
- Are terminology, notation, figures, and section claims consistent?
- Is the requested revised artifact delivered before explanatory commentary?

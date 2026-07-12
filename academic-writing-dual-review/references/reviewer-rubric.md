# Reviewer Rubric

## Severity

### Critical

Likely rejection-level problem that threatens validity, contribution, or comprehensibility. Examples:

- the problem is unclear or unmotivated;
- central novelty collapses against the closest work;
- the method does not address the stated problem;
- key claims have no supporting evidence;
- evaluation design cannot answer the research question;
- serious leakage, invalid comparison, or unsupported causal claim.

### Major

Material weakness that could change reviewer confidence or score but is plausibly repairable without replacing the whole study. Examples:

- incomplete rationale for major components;
- missing strong baseline or important ablation;
- unclear gap relative to a category of prior work;
- overbroad claims relative to datasets or settings;
- substantial cross-section inconsistency;
- missing limitations or robustness analysis.

### Minor

Localized clarity, consistency, presentation, or language issue that does not alter the core conclusion.

## Evaluation dimensions

Score only when requested, using 1–5 with evidence.

| Dimension | 1 | 3 | 5 |
|---|---|---|---|
| Motivation | unclear or irrelevant | plausible but incomplete | concrete, consequential, and well supported |
| Novelty | indistinguishable or trivial | incremental but identifiable | clearly differentiated and consequential |
| Technical soundness | invalid or unsupported | mostly sound with gaps | rigorous and fully traceable |
| Presentation | disconnected or opaque | understandable with effort | coherent, precise, and reader-oriented |
| Related work | missing or list-like | adequate but weakly differentiated | comprehensive, synthesized, and fair |
| Evaluation | mismatched or insufficient | supports some claims | directly and convincingly tests all main claims |
| Reproducibility | essential details absent | partial detail | sufficient detail and artifacts where applicable |

## Verdict calibration

- `Strong reject`: fatal validity or contribution problem with no credible repair in the current work.
- `Reject`: one or more critical issues or several compounding major issues.
- `Borderline`: meaningful contribution but reviewer confidence is limited by repairable gaps.
- `Accept`: contribution is clear, sound, supported, and well presented, with only minor issues.
- `Strong accept`: unusually important, rigorous, and convincing work.

Do not produce a verdict when the supplied material is too partial. Instead state the review boundary.

## Finding format

Use this compact structure:

```text
[Severity] Short issue title
Location: section, paragraph, claim, figure, or quoted phrase
Evidence: what the manuscript actually states or omits
Impact: how this affects validity, novelty, or reader confidence
Revision: a concrete change the authors can make
```

Prefer three well-supported findings over ten generic observations.

# Section-Specific Writing Guides

Read only the section relevant to the task.

## Title

- Name the central problem, method or insight, and context when useful.
- Avoid unsupported superlatives and vague phrases such as "a novel framework."
- Keep terminology consistent with the abstract and problem definition.

## Abstract

Use a compact sequence:

1. problem and importance;
2. specific limitation or gap;
3. proposed approach and core insight;
4. main evidence or results;
5. bounded implication.

Do not introduce unexplained acronyms, citations, broad background, or claims absent from the paper.

## Introduction

For detailed motivation construction and diagnosis, read [motivation-guide.md](motivation-guide.md).

Move rapidly from context to the specific problem. A useful structure is:

1. concrete task, users, or scientific importance;
2. state of the art and remaining limitation;
3. underlying reason the limitation persists;
4. precise problem and key challenges;
5. core insight and method overview;
6. specific, evidence-backed contributions.

Avoid multiple paragraphs of generic field history. State only challenges addressed later. Ensure contribution bullets are not merely a table of contents.

## Related work

- Group studies by approach, assumption, problem setting, or capability.
- Summarize the shared idea and limitation of each group.
- Compare each group with the proposed work on the dimensions that matter.
- Identify the closest work explicitly and distinguish it fairly.
- Do not use missing citations as the sole novelty argument.
- Do not claim "no prior work" unless the search justifies it; prefer bounded wording.

## Problem formulation and preliminaries

- Define the task before presenting the solution.
- State inputs, outputs, assumptions, constraints, and objective.
- Use a notation table when notation is dense.
- Use one symbol per concept and one concept per symbol.
- Explain why assumptions are realistic or delimit their scope.

## Method

Open with an overview that maps challenges to components. For each component, write:

`motivation -> objective -> insight -> mechanism -> interaction -> complexity or behavior`

Separate conceptual novelty from implementation detail. Explain non-obvious design choices and avoid architecture narration without rationale.

## Experiments or empirical analysis

Organize evaluation around research questions or claims, not merely datasets:

- effectiveness or primary outcome;
- comparison with closest and strongest baselines;
- component contribution through ablation;
- sensitivity, robustness, generalization, or subgroup behavior;
- efficiency and resource cost when relevant;
- qualitative analysis, failure cases, or error analysis;
- statistical uncertainty or significance where appropriate.

For each result, state observation, interpretation, and scope. Do not claim causality from correlational evidence or general superiority from narrow benchmarks.

## Discussion and limitations

- Explain what the results mean beyond repeating them.
- Distinguish observed evidence from interpretation.
- State boundary conditions, failure cases, and threats to validity.
- Explain what remains unresolved without undermining supported contributions.

## Conclusion

Restate the problem, core insight, and supported result without introducing new claims. Keep future work specific and connected to acknowledged limitations.

## Figures and tables

- Give each visual one principal message.
- Make labels readable at final publication size.
- Use consistent names, colors, scales, and ordering.
- Write captions that allow partial understanding without searching the body.
- Refer to every figure and table in the text and explain the takeaway.
- Avoid decorative complexity and raw screenshots when a clear schematic would communicate better.

## Rebuttal-driven revision

- Translate each reviewer comment into an underlying concern.
- Address the concern directly with a revision, evidence, clarification, or justified scope boundary.
- State exactly what changed and where.
- Do not dismiss a comment merely because the requested change seems unnecessary; explain the evidence-based resolution.

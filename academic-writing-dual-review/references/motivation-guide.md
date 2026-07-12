# Motivation Writing Guide

Use this guide to construct or review the motivation in an abstract, introduction, problem statement, method component, or research proposal.

## Source method

Base this workflow on the motivation-writing method in Chan and Wu, *Mastering the Academic Writing Mindset: A Guide to Crafting Computer Science Papers* (2026), especially Sections 5.1-5.4, 5.10-5.12, and 6.3. Preserve its central method: write as a reader, continuously ask concrete questions, tell a connected story, clearly present the value of the work, define the problem before the solution, and motivate every major method choice.

## Core principle

Motivation must establish **necessity**, not merely introduce a topic. Follow the book's reader-oriented question sequence. A convincing motivation lets the reader answer:

- What is the studied concept or task, explained intuitively?
- What are its concrete applications?
- Who are the users or affected stakeholders?
- How do those users employ it in practice?
- Why is this task or capability necessary when alternatives exist?
- What is the specific problem or challenge?
- How serious is it, preferably with evidence or quantitative values?
- For an established topic, why is another solution needed?
- For a new topic, why should this problem be studied for the first time?
- Why is the proposed direction a plausible response?

Do not treat these statements as sufficient motivation:

- "X has attracted increasing attention."
- "X is widely used in many applications."
- "Few studies have examined X."
- "Existing methods are not perfect."
- "Our method improves accuracy."

They provide background, an absence claim, or a result, but do not establish why the research is needed.

## Apply the book's question-driven workflow

Before drafting prose, answer the following questions in plain language. Do not write around an unanswered question.

1. `What is it?` Explain the task or concept intuitively and make the text self-contained. Add a motivating figure or example when words alone impose high comprehension cost.
2. `Who uses it?` Identify actual users, domain experts, systems, institutions, or scientific communities.
3. `How is it used?` Describe how the task supports a real workflow or scientific objective; do not merely list application names.
4. `Why this approach or task?` Explain why substitutes do not eliminate the need. If alternative tools exist, state the distinctive value of the studied task.
5. `What exactly goes wrong?` Name the bottleneck, failure condition, violated assumption, or trade-off.
6. `How serious is the problem?` Provide a quantitative example, complexity analysis, observed failure, diagnostic result, or credible consequence when available.
7. `Why another solution?` For an old topic, explain what current solutions still cannot achieve and whether the proposed objective is more accurate, efficient, reliable, scalable, fair, safe, or otherwise meaningfully better.
8. `Why study it first?` For a new topic, provide stronger evidence of practical or scientific need; novelty by absence is insufficient.
9. `What challenges must be solved?` State only the challenges addressed by the proposed method and later evaluation.
10. `Why this method?` Explain the intellectual path: design rationale, considered alternatives, why they are insufficient, and the core insight behind the chosen design.

Use the answers to draw an internal connection map before writing:

`concept -> users -> use process -> necessity -> concrete problem -> evidence of severity -> unresolved limitation -> research objective -> challenges -> core insight -> method`

If any transition is abrupt, add the missing reasoning rather than a generic transition phrase.

## Build the motivation chain

Translate the book's questions into the following five-part prose chain. Compress or expand it according to section length.

### 1. Need

Identify the concrete scientific or practical capability that matters.

Specify where possible:

- stakeholder, user, system, population, or scientific community;
- task or decision they need to perform;
- operating context or boundary condition;
- desired property such as accuracy, reliability, efficiency, fairness, safety, interpretability, or scalability.

Prefer:

> In long-horizon dialogue agents, the system must retain action-critical information while removing redundant history to operate within a fixed context budget.

Avoid:

> Large language model agents have become increasingly popular.

When introducing applications, explain how the task is used in them. A list such as "applications include healthcare, finance, and education" is not yet motivation.

### 2. Obstacle

Explain what prevents the need from being satisfied. Identify the **mechanism of failure**, not only a low metric.

Ask:

- What assumption breaks in the target setting?
- What resource, information, or supervision is unavailable?
- What trade-off cannot be handled?
- Under what condition do existing methods fail?
- Why does simply scaling or tuning the existing approach not solve it?

Weak:

> Existing methods achieve limited performance.

Stronger:

> Existing compression methods prioritize semantic redundancy, but do not distinguish redundant content from infrequent information that determines later actions; consequently, they may remove evidence that appears locally unimportant but becomes critical several steps later.

Follow the book's emphasis on magnitude: replace ungrounded statements such as "the operation is slow" with a representative runtime, operation count, complexity, failure rate, resource cost, or concrete counterexample whenever the evidence exists.

### 3. Consequence

State why the obstacle matters. Connect the technical limitation to a measurable scientific, practical, or decision-level cost.

Possible consequences include:

- incorrect decisions or degraded outcomes;
- unsafe or unfair behavior;
- excessive computation, latency, energy, or annotation cost;
- inability to deploy at the required scale;
- invalid scientific conclusions;
- failure to generalize to the target population or setting.

Avoid dramatic consequences that the manuscript does not substantiate.

### 4. Gap

Define exactly what capability, understanding, or evidence is missing. A gap is not simply "nobody has combined A and B."

Use one or more defensible gap types:

- `capability gap`: current methods cannot provide a required behavior;
- `assumption gap`: methods rely on an assumption violated in the target setting;
- `setting gap`: an important operating condition remains unsupported;
- `knowledge gap`: the mechanism or relationship is not adequately understood;
- `evidence gap`: a consequential claim lacks evaluation in relevant populations or conditions;
- `measurement gap`: existing metrics or benchmarks do not capture the target risk or capability;
- `integration gap`: existing components cannot be combined directly because of a concrete incompatibility.

Bound absence claims carefully. Prefer:

> Existing studies largely optimize average compression quality, leaving the risk of deleting action-critical information insufficiently controlled.

Avoid unless verified:

> No previous work has studied this problem.

### 5. Opportunity

Introduce the core insight or research direction that makes progress plausible. Do not jump directly from the gap to a list of modules.

Explain:

- what new observation changes the problem;
- what principle guides the solution;
- why that principle addresses the identified failure mechanism;
- what capability becomes possible.

Example:

> This suggests treating compression as a risk-control problem: instead of retaining content solely by estimated relevance, the system should explicitly bound the probability of discarding information whose future action value is uncertain.

The opportunity should lead naturally to the method, but it need not reveal all implementation details.

Present the opportunity positively and accurately. Following the book's "salesman" analogy, make the paper's real advantage visible instead of foregrounding every weakness; never exaggerate, conceal invalidity, or fabricate results. Bound limitations elsewhere and keep motivational claims proportional to evidence.

## Recommended paragraph architecture

Adapt the number of paragraphs to the venue and manuscript.

### Paragraph 1: Concrete need

Explain the task intuitively, establish the users, show how they use it, and state its distinctive practical or scientific value. Use a motivating example or figure when helpful. Use broad context only when it directly supports the need.

### Paragraph 2: Existing progress and precise limitation

Acknowledge what current methods or alternatives achieve, then identify the condition under which they fail and explain why. Quantify the severity when possible.

### Paragraph 3: Consequence and unresolved gap

Show what the limitation prevents or risks. State the missing capability or understanding precisely.

### Paragraph 4: Core insight and research objective

Present the conceptual opportunity, formulate the research goal, and transition to the proposed approach.

For a short abstract, compress the four paragraphs into two to four sentences without dropping the obstacle or consequence.

Maintain explicit connection between paragraphs. Do not describe applications in one paragraph and suddenly announce an efficiency method in the next; insert the missing chain showing the computational bottleneck, its magnitude, and why it prevents the stated use.

## Old problem versus new problem

### For an established problem

Answer:

- Why is another method necessary?
- Which unresolved setting, failure mode, or trade-off remains?
- Why can the closest methods not be extended trivially?
- Is the gain meaningful for the target use case, not only statistically detectable?

Do not motivate an established problem only by seeking a higher benchmark score.

### For a new problem or setting

Answer:

- Who encounters the problem?
- Why has it become important now?
- What observable evidence suggests that it exists?
- Why do adjacent formulations fail to capture it?
- What makes the problem tractable and worth formalizing?

"No one has studied it" increases the burden of motivation rather than satisfying it.

## Method-level motivation

Motivate each major component separately:

`local challenge -> failed direct approach -> design requirement -> component insight -> expected effect`

Example pattern:

> Directly applying X would cause Y because Z. We therefore require a mechanism that preserves A while controlling B. Based on the observation that C, we introduce D, which performs E.

Do not justify a component retrospectively only because an ablation shows that it improves performance.

Make the design thought process visible, as required by the book:

- Why was the method designed this way?
- Which stated challenge does it address?
- Which alternatives were considered?
- Why are those alternatives unsuitable?
- What core insight guided the design?
- Why should the method generalize beyond favorable tuning or one dataset?

## Evidence for motivation

Use the strongest available support:

1. real use case, observed phenomenon, or domain requirement;
2. prior empirical or theoretical evidence;
3. diagnostic analysis showing the failure mode;
4. motivating example or counterexample;
5. small preliminary study;
6. carefully bounded reasoning when direct evidence is unavailable.

Do not fabricate statistics or citations. If the manuscript lacks evidence for a central motivational claim, flag it as a required author input or study.

## Reviewer stress test

Audit the motivation with these questions:

1. Is the opening specific enough to identify the affected task and setting?
2. Is importance demonstrated, or merely asserted with words such as "critical" and "important"?
3. Does the limitation describe why existing approaches fail?
4. Is the consequence credible and proportional to available evidence?
5. Is the gap a missing capability or understanding rather than only a missing combination?
6. Is the closest work treated fairly?
7. Does the proposed insight directly address the stated failure mechanism?
8. Would the paper still matter if the reported metric improvement were small?
9. Are all motivating challenges actually addressed and evaluated later?
10. Does the target venue's audience care about this problem?
11. Can a non-specialist reviewer understand the task without reading cited papers first?
12. Are applications explained as workflows rather than listed as names?
13. Is the claimed severity supported quantitatively when quantitative evidence is available?
14. Is there an uninterrupted connection from application to problem and from problem to method?
15. Does the text clearly highlight the work's genuine advantage without exaggeration?

Classify failures:

- `critical`: the reader cannot determine why the problem needs solving, or the method does not address the motivating problem;
- `major`: importance is plausible but the obstacle, consequence, or gap is weakly supported;
- `minor`: the logic is sound but wording, ordering, or specificity can improve.

## Motivation revision output

When the user specifically asks to improve motivation, return:

1. `Motivation diagnosis`: identify the broken or missing links;
2. `Reconstructed motivation chain`: need, obstacle, consequence, gap, opportunity;
3. `Revised text`: provide publication-ready prose;
4. `Evidence still needed`: list only claims requiring citations, diagnostics, data, or author confirmation;
5. `Reviewer stress test`: report remaining rejection risks concisely.

When sufficient source material exists, place `Revised text` first, following the main skill's direct-revision output contract.

## Reusable sentence functions

Use these as logical functions, not rigid templates:

- Need: `In [setting], [stakeholder/system] must [capability] to [consequence or objective].`
- Progress: `Existing approaches have improved [capability] by [main strategy].`
- Obstacle: `However, they typically assume [assumption], which breaks when [condition].`
- Mechanism: `Under this condition, [failure mechanism], causing [technical effect].`
- Consequence: `As a result, [practical/scientific consequence].`
- Gap: `What remains missing is [precise capability, understanding, or evidence].`
- Opportunity: `This observation suggests [core insight or reframing].`
- Objective: `Accordingly, this work investigates/develops [bounded objective].`

Avoid using every sentence function mechanically. Produce a coherent argument appropriate to the field and venue.

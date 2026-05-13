# NASA ROSES Lessons Learned — Recurring Pitfalls and Strengths from Prior Submissions

> **Purpose.** This file distills patterns observed across multiple NASA ROSES proposals and the reviewer evaluations that followed (programs spanning Earth Surface & Interior, WATER, Weather, HMA, SERVIR, A.08 Water Resources, A.09 Earth AI Foundation Models). It is intended to be consulted **before drafting** any NASA proposal and **during proposal review**. Pitfalls listed here have appeared in *more than one* panel summary or are clearly recurring across the proposal portfolio.
>
> All examples are anonymized: no investigator names, no institutional identifiers, no budget figures, no end-user organization names. Reviewer quotes are paraphrased or kept generic enough that they cannot be traced to a specific proposal.

---

## How to Use This File

1. **Before drafting:** Work through the [Pre-Submission Pitfall Checklist](#pre-submission-pitfall-checklist). Treat each item as a "must-pass" gate before submission.
2. **During section drafting:** Consult the [Section-by-Section Annotated Guidance](#section-by-section-annotated-guidance) — each section flags what reviewers have historically criticized in proposals from this portfolio.
3. **At reviewer-style review:** Use the [Pre-Submission Self-Review Prompts](#pre-submission-self-review-prompts) as a Socratic checklist. Most prompts mirror exact reviewer questions that have appeared in prior panel summaries.
4. **For positive reinforcement:** The [Recurring Strengths to Preserve](#recurring-strengths-to-preserve) section catalogs what *has worked* — keep doing these.

This file complements but does **not** replace `nasa_guidelines.md`. That file covers the *what* and *how* of NASA proposals; this file covers the *what to watch out for*.

---

## Pre-Submission Pitfall Checklist

A proposal is not ready to submit until each of these is honestly answered "Yes."

### Scope and Feasibility
- [ ] Is the number of distinct tasks **≤ 5** for a 2-year project, **≤ 7** for a 3-year project? (Historically, proposals with 7–8 tasks in 2 years are flagged "highly ambitious / feasibility concerns.")
- [ ] Does each task have a **specific, time-boxed deliverable** rather than an open-ended activity?
- [ ] Has the scope been pressure-tested: "Could a reviewer reasonably argue this is too much for the timeline and budget?" If yes, cut.
- [ ] Are integration / harmonization / scaling claims **bounded** by the case study, or have they been overextended to "national-scale" / "transferable to other regions" without supporting evidence?

### ARL Advancement
- [ ] Is the proposed ARL jump **≤ 2 levels per project year**? (ARL 4 → 7 in two years has been flagged "optimistic.")
- [ ] Is the **starting ARL evidenced** by published validation, prior partnership documentation, or a demonstrated prototype — not merely asserted?
- [ ] For each ARL increment, is the bridging activity (e.g., what specifically moves from "prototype in lab" to "prototype in relevant environment") **named and resourced**?
- [ ] Does the ARL claim distinguish between "demonstrated in simulated operational environment" and "demonstrated in partner's actual decision-making"? Reviewers scrutinize this gap.

### Preliminary Results
- [ ] Does each major technical claim have a **figure or quantitative result** from prior work (F1 scores, runtimes, error metrics, validation plots)?
- [ ] Is preliminary work described at **sufficient methodological detail** to evaluate? Reviewer pattern: "preliminary results are not described in sufficient detail to evaluate model performance" is one of the most common major weaknesses.
- [ ] When citing prior application to a different region or dataset, is **the actual demonstration shown** in the proposal — not just claimed? (Historical pitfall: "the proposal mentions the model has been applied to [region] … however, no demonstration is provided.")
- [ ] Are figures legible at print size? Captions self-contained?

### End-User Engagement
- [ ] Is the end user a **direct decision-maker**, or only a data intermediary? Reviewer pattern: "the pathway to decisional end-users is indirect and intermediary-based" has been flagged as a relevance weakness.
- [ ] If the team-embedded partner is an intermediary, is there **at least one direct end user** also listed (as Co-I, funded consultant, or signatory of a substantive commitment letter)?
- [ ] Is the end user's **specific decision** described — not "water managers will use this" but "the [specific role] will use this output to decide whether to [specific action] within [specific time window]"?
- [ ] Is engagement evidence (years of prior collaboration, signed MOU, IRB-approved interviews, prior workshops) **dated and concrete**, not aspirational?
- [ ] Does the proposal describe **end users' direct involvement in evaluation and validation**, not just initial requirements? Reviewer pattern: "while [the intermediary] provides a credible partner, direct involvement of end users in evaluation and decision-making is not clearly defined."

### Performance Metrics
- [ ] Is every quantitative target (resolution, latency, accuracy, lead time, efficiency multiplier) **explicitly justified** against the baseline? Numbers like "1000× speedup," "10 m resolution," "sub-hour latency," "85% accuracy" must each have a baseline-relative rationale.
- [ ] For each target, is the **threshold of impact** stated — i.e., what level of improvement is required for the end user to actually change behavior? Panel feedback explicitly recommends: "clearly define metrics and suggest the threshold of impact they need to reach to 'make a difference' for the end user's decision."
- [ ] Are metrics **internally consistent**: a "sub-hour latency" claim must align with the data-ingest and inference pipeline budgets described elsewhere.

### Uncertainty and Methodology
- [ ] If a surrogate / emulator / data-driven model is trained against a physics-based reference, has **the physics model's own uncertainty** been quantified and propagated? Reviewer pattern: "it should have been clearly described how the uncertainties involved in the physical model (and its impact on the emulator) are going to be accounted for."
- [ ] Are alternative approaches **acknowledged and dismissed with rationale** rather than ignored? (Historical pitfall: a panel asked why an empirical model was not considered; the proposal had not discussed this.)
- [ ] Is each methodological choice (e.g., LoRA fine-tuning, infinite-slope formulation, mixture-of-experts) **justified relative to alternatives**, not presented as obvious?
- [ ] Are validation datasets **independent** of training data? (Reviewers explicitly check this for ML/foundation-model proposals.)

### Solicitation Alignment
- [ ] Has the solicitation text been **quoted and mapped** to specific project tasks? Historical pitfall: a proposal claimed novelty in assimilating a specific data type the solicitation requested — but that data type was "never addressed in the project plan." This was scored as a relevance weakness.
- [ ] Does every solicitation priority topic / objective have a corresponding task or subsection?
- [ ] For DAPR programs, is **all identifying information removed** from the S/T/M section (institutional names, lab facility names, self-citations in first person, PI initials in figure captions)?

### Transition and Sustainability
- [ ] Does the transition plan identify a **specific post-project host** (an institution, infrastructure, or industry partner) — not "we will explore" or "future funding could support"?
- [ ] Does the transition include **knowledge transfer**, not just code? (Docker images, video training libraries, co-developed user manuals are concrete; "documentation" alone is vague.)
- [ ] Is the transition plan resilient to **end-user staff turnover**?
- [ ] Are post-project operational costs addressed? Who pays for compute, hosting, maintenance?

### Internal Coherence
- [ ] Does the **budget reconcile with the work plan**? Reviewer pattern: "the budget is also difficult to reconcile with the work plan." Each task should have visible personnel-month commitments matching its scope.
- [ ] Do **task durations in the Gantt chart match the personnel effort table**?
- [ ] Are forecast windows (e.g., 1-day, 3-day, 7-day outlooks) **aligned with the actual dynamics** of the hazard being forecast? Reviewer pattern: "the selected forecasting windows are not clearly aligned with shorter-timescale flash flood dynamics."

---

## Top-10 Recurring Reviewer Critiques

Each entry below is grounded in at least one panel summary; most appear across multiple proposals. The wording approximates the standard reviewer phrasing.

### 1. "Highly ambitious in scope … raises feasibility concerns"
**Pattern.** Proposals attempt to deliver multiple complex components (data harmonization, forecasting, independent evaluation, alerting, scenario planning, transition, scaling) within a short timeframe.

**Why reviewers flag it.** A reviewer reads the task list and asks: "Could three FTE-years actually deliver all of this, with stakeholder co-development and ARL advancement?" The answer is usually no.

**Mitigation.**
- Drop secondary deliverables; promote one to the headline.
- Re-cast "national-scale" or "horizontal scalability" demonstrations as **one bounded transferability pilot** rather than open-ended scaling claims.
- Move ambitious features into the **Transition Plan** ("after the project, the platform can scale to …") rather than committing to deliver them within the award period.

### 2. "Preliminary results lack sufficient detail"
**Pattern.** A figure shows that the proposed method "works" but the proposal does not specify: training data, validation split, performance vs. baseline, what was held out, why this particular dataset, what failed, what was learned.

**Why reviewers flag it.** Reviewers cannot evaluate feasibility without numbers and methodology behind the figure.

**Mitigation.**
- Every preliminary-result figure caption must contain: (a) data source, (b) baseline comparison, (c) metric and value, (d) what this demonstrates for the proposed work.
- Add a brief "what was learned and what remains" paragraph for each preliminary result.
- If preliminary work was done by the team but not yet published, cite a preprint or repository link.

### 3. "ARL progression appears optimistic"
**Pattern.** A proposal claims advancement from ARL 3–4 to ARL 6–7 in two years, with the end-state requiring "use in partner's decision-making."

**Why reviewers flag it.** ARL 6 → ARL 7 requires the system to be running in the partner's decision workflow — not a one-time demonstration. Two-year jumps of 3+ ARL levels are rarely credible.

**Mitigation.**
- Target ARL advancement of **one ARL per project year** unless the starting level is heavily documented.
- For each ARL level claimed, identify **the specific evidence** that will be generated by which task (e.g., "ARL 5 evidence: validated against historical events in Year 1 Q3 via Task 4 retrospective evaluation").
- Distinguish "simulated operational environment" (ARL 6) from "active partner decision-making use" (ARL 7) and resource them separately.

### 4. "Direct end-user involvement in evaluation is unclear"
**Pattern.** Proposals describe partnerships with data intermediaries (regional data centers, geospatial hubs) but the actual decision-makers (emergency managers, planners, agency operations staff) appear only as "users of the dashboard."

**Why reviewers flag it.** NASA ES2A explicitly requires user-centered design with the decisional end-user. An intermediary-only team raises a relevance weakness.

**Mitigation.**
- Embed **at least one direct end-user** on the team as a funded Co-I or consultant.
- Describe evaluation activities (tabletop exercises, scenario reviews, scored decision drills) where end users — not intermediaries — provide feedback.
- Letters of support from the intermediary alone are insufficient; include a letter from the end-user organization stating their intent to use the outputs.

### 5. "Performance metrics not consistently well defined or justified"
**Pattern.** A proposal promises "10 m resolution," "sub-hour latency," "85% accuracy," "1000× speedup" — but the justification for *why these specific thresholds* is missing.

**Why reviewers flag it.** Reviewers see numbers as decoration unless paired with: (a) baseline, (b) end-user threshold of acceptability, (c) measurement method, (d) what changes if the target is not reached.

**Mitigation.**
- Create a **Metrics Table** with columns: Metric | Baseline | Target | Why this threshold | Measurement method.
- For every speedup or efficiency claim, identify the baseline implementation, hardware, and dataset of comparison.
- State the **decision-relevance** of each metric: "30 min latency is the threshold below which evacuation orders can be issued before flood onset."

### 6. "Uncertainty in the [physics-based reference model] is not addressed in the emulator"
**Pattern.** A data-driven model is trained against a physics-based reference (CREST-iMAP, hydrodynamic model, etc.) and treated as ground truth. The emulator's accuracy is reported relative to the reference — but the reference's own error is not propagated.

**Why reviewers flag it.** The fused product can never be more accurate than the training target. Reviewers reading "0.9 accuracy relative to physics-based simulations" expect a discussion of the absolute accuracy.

**Mitigation.**
- Quantify the reference model's validation error against observations.
- Describe how reference uncertainty propagates through training (e.g., loss weighting, ensemble training, residual learning).
- Include an **external** validation against independent observations (gauge data, satellite EO maps not used for training) in addition to the in-house benchmark.

### 7. "Methodology lacks technical specificity"
**Pattern.** Sections describing the technical approach use accurate vocabulary (LoRA, Hierarchical ViT, FSDP, Swin-shifts, super-resolution, bias correction) but do not specify: input/output dimensions, target loss, optimizer, training data scale, hyperparameter selection, validation split.

**Why reviewers flag it.** Buzzword-dense methodology reads as "the team knows the tools" but not "the team has decided exactly what they will do."

**Mitigation.**
- For each technical choice, answer: input/output dimensions, dataset size and split, loss function, hyperparameter selection method, validation metric.
- Replace "we will employ [advanced technique]" with "we will employ [technique] configured as [specific configuration] based on [preliminary result or prior work]."
- A method that could not be reproduced from the proposal is not specific enough.

### 8. "Solicitation language is invoked but specific priorities are not addressed"
**Pattern.** A proposal opens with the right buzzwords (ES2A, decision-making, EO integration, Key Result 2.2) but the task plan addresses only a subset of solicitation priorities — or claims novelty in an area the project does not actually pursue.

**Why reviewers flag it.** Reviewers cross-check solicitation priorities against the project description. A claimed novelty unaddressed in the work plan is grounds for a **major relevance weakness**.

**Mitigation.**
- Build a **Solicitation-Mapping Table** as an internal QA tool: every priority topic listed in the call → which task addresses it → which deliverable evidences it.
- For each claimed novelty in the abstract/summary, confirm that the technical approach contains a corresponding subsection.
- Remove novelty claims the project does not deliver.

### 9. "The model choice / approach is not justified relative to alternatives"
**Pattern.** A specific model family is used because the team developed it, without discussion of why this model fits the use case better than alternatives (e.g., why physics-based when empirical would also work; why this foundation model over another; why infinite-slope over more complex slope-failure models).

**Why reviewers flag it.** Reviewers ask: "Why this model? Was an alternative considered? What is the cost of being wrong?"

**Mitigation.**
- Add a brief **Method Selection Rationale** paragraph for each major modeling choice: alternatives considered, why this one, what evidence supports the choice.
- When using an in-house model family across multiple proposals, re-justify it each time relative to the specific use case — do not assume reviewers know the model's pedigree.
- If the in-house model has been validated in a related but different domain, present that validation; if not, acknowledge the gap and propose a calibration / validation task.

### 10. "Generalization claims are overextended"
**Pattern.** A proposal demonstrates a method in one case study (one watershed, one region, one set of climate zones) and then claims the approach will generalize to the entire CONUS, or to other regions, or to other hazards.

**Why reviewers flag it.** A reviewer who reads "this approach can scale to the entire nation" expects evidence; absent evidence, this reads as overselling.

**Mitigation.**
- Bound generalization claims to **what the project will actually demonstrate** (one additional region as a transferability pilot, with explicit acknowledgment of limitations).
- Distinguish **demonstrated scalability** (Year 2 transferability pilot) from **architectural scalability** (the design supports transfer, even if not demonstrated within the award).
- Avoid phrases like "can be applied nationwide" unless the project will demonstrate national application.

---

## Section-by-Section Annotated Guidance

### Decision-Making Activity (DMA)

**What has worked.** Newer proposals lead with a clear paragraph naming the end-user organization, their institutional mandate, and the specific decisions they make. A **Metrics Table** with rows like *Lead Time*, *Spatial Resolution of Risk*, *Time to Situational Awareness* and columns *Baseline → Target → Method of Assessment* has been an effective device. Decision-making sections that read like operational briefings (concrete decisions, time windows, authority to act) score better than those that frame the end user generically.

**What to watch for.**
- **End-user identity check.** The end user named in the DMA must be the same entity referenced in the engagement plan, letters of support, transition plan, and task leads. Inconsistency across sections is visible to reviewers.
- **Decision specificity.** A reviewer should be able to summarize the end user's decision in one sentence after reading the DMA. If the decision could be replaced with "use this for planning" or "improve situational awareness," it is too generic.
- **Authority to act.** State explicitly that the tool **informs but does not replace** decisional authority. This anticipates reviewer concerns about automation displacing human judgment.

**Pitfall.** Listing decision activities at increasing level of generality ("for the city, for the region, for the nation") signals scope creep. Pick one primary end user with one primary decision context.

### Anticipated Results and Improvements

**What has worked.** A baseline-vs-target paragraph with quantitative improvement deltas, followed by an ARL advancement narrative tied to specific tasks.

**What to watch for.**
- **Target justification.** Each numerical target needs a justification beyond "this is what the technology can do." The justification should reference end-user needs (e.g., "30-minute latency is required because evacuation orders must be issued before water reaches critical roads").
- **Improvement vs. baseline.** If the comparison product is FEMA flood maps, the National Water Model, an empirical regression, or a published benchmark, name it explicitly and describe its specific limitations.

**Pitfall.** Phrasing like "significant improvement" or "dramatically reduces" without numbers will be flagged. Replace with deltas.

### Background, Motivation, and Significance

**What has worked.** Region-specific recent events (named flood years, drought years, casualty figures) ground the motivation. Trend data with a regression line is a powerful figure.

**What to watch for.**
- **Avoid the global-to-local funnel for too long.** Reviewers tire of two paragraphs on global climate change before the proposal reaches the actual problem.
- **Citations should be recent.** Reviewers notice when most citations are >5 years old, especially in a field that changed recently (e.g., foundation models, NISAR availability).

### Preliminary Results

**This is the single most-criticized section across the portfolio.** Reviewers consistently report that preliminary results are described at a high level without methodological detail.

**Minimum content per preliminary result figure.**
1. Data source (named dataset, time period, spatial extent).
2. Method summary (1–2 sentences, sufficient for reproduction at a high level).
3. Baseline comparison (named, with metric).
4. Result with units and uncertainty.
5. Interpretation (what this evidences for the proposed work, and what remains).

**Pitfalls.**
- Showing only the team's method without a baseline.
- Claiming the method "has been applied in [region]" without showing the result.
- Reusing the same figure across multiple proposals without updating the caption to the specific use case.

### Technical Approach / Methodology

**What has worked.** Clear data-flow diagrams (raw inputs → preprocessing → model → outputs → decision products), task-numbered subsections, and named NASA EO assets with rationale for inclusion.

**What to watch for.**
- **Buzzword density vs. specificity.** A paragraph that contains LoRA, Swin-shifts, FSDP, Hierarchical ViT, multi-scale patch embeddings, super-resolution decoders, and inter-sensor cross-calibration without specifying configurations will read as showmanship.
- **Each technique needs a decision rationale.** "Why LoRA and not full fine-tuning?" "Why Swin-shifts and not vanilla attention?" — answer these in one sentence each.
- **End-to-end timing budget.** If the proposal claims sub-hour latency, walk through the data-ingest → preprocessing → inference → post-processing → publication pipeline and state where the minutes go.

**Pitfall.** Treating the in-house model family (CREST family, EF5, iCRESLIDE) as the obvious choice without re-justifying it for each new use case. Reviewers outside the immediate community do not share this assumption.

### ARL Assessment

**What has worked.** Explicit "Starting ARL: X. Ending ARL: Y." statements, with each level supported by named evidence (publications, partnerships, validations).

**What to watch for.**
- **ARL inflation.** Be conservative. ARL 6 means "demonstrated in simulated operational environment with end-user testing" — not "we expect to demo it once." ARL 7 means active use in decision workflows — not "we expect they will use it."
- **Evidence per level.** For each level claimed, name the evidence artifact (validation report, scored exercise, signed acceptance) and the task that generates it.

**Pitfall.** Claiming the project ends at ARL 7 or 8 in a 2-year project with no prior operational deployment. Reviewers see this as optimistic.

### Project Risks and Mitigation

**What has worked.** A structured risk table with Likelihood / Impact / Mitigation columns.

**What to watch for.**
- **Quality, not quantity.** Listing 8 risks with shallow mitigations is weaker than listing 4 risks with credible mitigations.
- **Mitigations should be funded.** If "end-user turnover" is a risk and the mitigation is "documentation," that documentation should appear as a Year 2 deliverable with effort allocated.

**Pitfall.** Risks acknowledged but mitigation strategies generic ("we will monitor and adjust"). Reviewers flag this as "weak risk mitigation."

### Transition and Sustainability Plan

**What has worked.** Naming a specific post-project host (operational partner, intermediary infrastructure, industry partner) with a Letter of Commitment confirming sustained hosting. Video training libraries and Docker-containerized deployments are concrete.

**What to watch for.**
- **Operational cost ownership.** Reviewers expect a statement that post-project compute, hosting, and maintenance costs are absorbed by an identified party. Vague "open-source release" is insufficient.
- **End-user self-sufficiency.** The transition plan should describe how the end user will *operate* the tool without the original team.

**Pitfall.** A transition plan that ends with "future grant proposals will sustain the work" is read as failure to plan for sustainability.

### Earth Science to Action (ES2A) Alignment

**What has worked.** Explicit mapping to ES2A pyramid level and naming of specific Key Results (KR 1.2, 1.3, 2.1, 2.2, 2.3) with a sentence connecting each KR to a project activity.

**What to watch for.** ES2A sections that read as a literature citation rather than a project-specific alignment. The reviewer should be able to draw a line from KR 2.2 to a specific deliverable.

### Project Management, Schedule, and Personnel

**What has worked.** A Gantt chart with task durations matching personnel effort.

**What to watch for.**
- **Budget-schedule consistency.** Reviewer pattern: "the budget is difficult to reconcile with the work plan." Personnel effort in the budget should sum to plausible task delivery.
- **Single PI doing everything.** If the PI leads 5 of 7 tasks and only 9 calendar months are allocated, reviewers do the math.
- **Co-I role specificity.** Each Co-I should have a named role tied to specific tasks, not just a domain label.

---

## Recurring Strengths to Preserve

These elements have been positively cited or quietly succeeded across multiple proposals — keep them.

1. **Clear Decision-Making Activity sections** with named end users, mandates, and specific decision contexts. Newer proposals do this well; preserve the template.
2. **Quantitative Metrics Tables** with baseline → target → assessment method columns.
3. **Structured engagement frameworks** (CBPR phases, quarterly engagement cycles, IRB protocols for community-engaged research) — particularly effective when years of prior engagement are documented.
4. **ARL-task alignment** in the work plan — each task tagged with the ARL it targets.
5. **NASA EO breadth** — proposals leveraging GPM, SMAP, GRACE, Landsat, MODIS, Sentinel, SWOT, NISAR consistently score well on relevance to NASA assets.
6. **Comparison against operational baselines** (FEMA flood maps, National Water Model, Google Flood Hub, USGS gauges) — reviewers appreciate seeing the proposed system positioned against real systems, not just academic baselines.
7. **Interdisciplinary team composition** (Earth science + computer science + social science + civil engineering + end-user representation) — this aligns with ES2A interdisciplinary expectations.
8. **Open Science commitments** beyond minimum compliance (Hugging Face for model weights, Zenodo for data archive, Docker containerization, public sandbox environments).
9. **Iterative co-development language** — workshops, scenario-based evaluations, versioned refinement logs.
10. **Risk tables with mitigation strategies** — even when individual mitigations are critiqued, the structured presentation is appreciated.

---

## Anti-Patterns Specific to This Portfolio's Proposal Style

Observations across the portfolio — anonymous, general patterns to watch.

### The "Toolset / Platform / Framework" Pattern
Many proposals frame the deliverable as a multi-component integrated system (toolset, platform, framework, digital twin, intelligent platform). This framing is appealing but routinely triggers feasibility concerns: reviewers count the components, multiply by the duration, and conclude the scope is too large.

**Mitigation.** When using "platform" framing, ensure the **headline component** (one model, one tool) is unambiguous and the other components are either lightweight or already exist.

### The "In-House Model Family" Pattern
Proposals frequently rely on a related family of models developed by the team (a distributed hydrological model and its coupled flood-inundation and landslide variants, an ensemble framework, etc.). This is a strength when validated, but a reviewer may not share the assumption that the model family is the right choice for *this* use case.

**Mitigation.** Re-justify the model family per proposal, citing the most directly relevant validation. If the validation is in a different region or hazard, acknowledge this and propose a calibration / validation task explicitly.

### The "Many Tasks, Two Years" Pattern
Several proposals propose 7–8 tasks within a 2-year project. Reviewers do not budget reading time per task; they read the count and react to scope.

**Mitigation.** Consolidate. A task that produces a single intermediate deliverable should be a *subsection* of a larger task. Aim for 4–5 tasks for 2-year projects, 5–7 for 3-year projects.

### The "Generic End-User Description" Pattern
Some proposals describe end users at the level of "emergency managers and city planners" without naming a specific organization or describing their actual decisions. Newer proposals have moved toward specificity (named tribal nation department, named regional data center, named state agency); older proposals were more generic.

**Mitigation.** Always name the organization, their statutory or operational mandate, and the specific decisions they make.

### The "Intermediary as End User" Pattern
Several proposals embed a data intermediary (a regional data center, a geospatial hub) on the team and treat them as the end-user representative. Reviewers consistently flag this as indirect: the intermediary may host the tool but does not make the decisions.

**Mitigation.** Embed both an intermediary (for operational hosting) **and** at least one direct decision-maker (for evaluation and adoption).

### The "Solicitation Quoted, Not Mapped" Pattern
Proposals open with the right solicitation phrases but the technical sections do not systematically address each priority topic.

**Mitigation.** Build an internal table mapping every solicitation priority → which task / subsection addresses it. If any priority lacks a task, decide: address it or remove the claim that the proposal addresses it.

### The "Buzzword Density without Specificity" Pattern
Particularly visible in AI/ML proposals (foundation models, transformers, LoRA, FSDP, attention mechanisms, super-resolution, downscaling). Vocabulary signals familiarity; configurations signal commitment.

**Mitigation.** Each technical term should be paired with a specific configuration choice and a one-sentence justification.

### The "Missing Direct Validation Demonstration" Pattern
Historical pitfall (carries forward): claiming prior application to a region or dataset without showing the result in the proposal.

**Mitigation.** If a prior application is mentioned, show one figure of the result. If no figure is available, cite a publication that contains it.

---

## Pre-Submission Self-Review Prompts

Run through these questions before submission. Each maps to a real reviewer question that has appeared in panel summaries from this portfolio.

### Feasibility
1. If a reviewer counted the tasks and divided by the duration, would they conclude the scope is feasible? If not, what gets cut?
2. For each component (data harmonization, modeling, evaluation, transition, scaling), is there a clear single-sentence deliverable?
3. Is the most ambitious claim (national-scale, foundational, transformative) backed by a specific demonstration within the award period?

### Preliminary Evidence
4. Pick the most important preliminary figure. Could a reviewer reproduce its description from the text? Does it have a baseline, a metric, a value, and an interpretation?
5. Have any claims about prior application to a region / hazard / domain been backed by a figure or citation?
6. Are the preliminary results recent enough that they reflect the state-of-the-art at submission time?

### End-User Specificity
7. Name the end user in one sentence. Name the decision in one sentence. State what changes about that decision after the project. Could a non-expert summarize all three in one paragraph?
8. Is the end user a decision-maker, or only a data intermediary? If only an intermediary, who decides?
9. What is the end user's role in evaluation — not just initial requirements, but in scoring outputs?

### Metrics Justification
10. For each numerical target (resolution, latency, accuracy, lead time, speedup), what is the baseline, why this threshold, and how is it measured?
11. At what threshold does the metric "make a difference" for the end user's decision? Is that threshold stated?
12. Are the metrics internally consistent — does a sub-hour latency claim survive a walk through the data-ingest pipeline?

### ARL Discipline
13. What evidence supports the starting ARL? Cite it.
14. For each ARL increment, name the bridging activity, its resource allocation, and the artifact that evidences advancement.
15. Could a reviewer reasonably argue the ARL claim is optimistic? If yes, drop the end-state by one level.

### Uncertainty and Methodology
16. If a surrogate model is trained against a physics-based reference, where is the reference's own error discussed?
17. For each major modeling choice, has an alternative been considered? Why was this one selected?
18. Is the validation data independent of training data?

### Solicitation Alignment
19. Build the Solicitation-Mapping Table mentally: every priority → which task? Any unmapped priorities? Any claimed novelties without corresponding tasks?
20. (DAPR programs) Does the S/T/M section read as anonymous? Self-citations in third person, institutional names removed, lab facility names generic?

### Internal Coherence
21. Does the budget reconcile with the work plan? Pick a task and confirm the personnel-months allocated match what its scope requires.
22. Are forecast windows, spatial resolutions, and temporal cadences consistent with the hazard dynamics being addressed?
23. Are the same end users, decisions, and metrics referenced consistently across DMA, Anticipated Results, Tasks, Transition Plan, and ES2A sections?

### Reviewer Empathy
24. Read the proposal as if you have read 14 others today and have 30 minutes for this one. What do you remember? What is the one-sentence summary?
25. What would you, as a reviewer, write as the *Major Weakness*? Has that weakness been addressed in the text?

---

## Cross-References

- **For NASA-specific structural guidance**: `nasa_guidelines.md`
- **For specific aims / objective writing**: `specific_aims_guide.md`
- **For broader impacts / societal value**: `broader_impacts.md`
- **For budget preparation**: see relevant section of `nasa_guidelines.md`

---

*This file is a living distillation. When a new proposal is reviewed and the panel summary reveals a recurring pitfall not yet listed, add it to the Top-10 list (or rotate out a now-mitigated item). When a new strength is positively cited, add it to the Strengths section.*

# NSF Lessons Learned — Reviewer Mental Models, Recurring Critiques, and Red Flags

> **Purpose.** This document distills patterns observed across National Science Foundation (NSF) proposals and panel evaluations (spanning GEO, CISE/OAC, ENG, RISE, and cross-cutting interdisciplinary programs like CAIG, HDR, and AI Institutes). It captures **what NSF reviewers and panels actually look for**, what triggers immediate skepticism (red flags), and how to bulletproof proposals before submission.
>
> Consult this guide **before drafting** any NSF proposal, **during section writing**, and **during red-team/internal review**.

---

## Executive Summary: What NSF Reviewers Look For vs. What Triggers Red Flags

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                           NSF REVIEWER MENTAL MODEL                         │
├──────────────────────────────────────┬──────────────────────────────────────┤
│      WHAT WINS REVIEWER ENTHUSIASM   │        WHAT TRIGGERS RED FLAGS       │
├──────────────────────────────────────┼──────────────────────────────────────┤
│ • Concrete, falsifiable hypotheses   │ • Grand philosophical claims with    │
│ • Clear mechanistic/scientific       │   loose algorithmic mapping          │
│   discovery pathway (not just tools) │ • Testing nature through a single    │
│ • Rigorous baseline comparisons      │   narrow conceptual model            │
│   (ML vs classical, single vs multi) │ • "Why not classical DL/optimizer?"  │
│ • Physics-grounded AI architectures  │   left completely unanswered         │
│   with anti-reward-hacking guards    │ • Uncalibrated / arbitrary bins      │
│ • Feasible scope with proportional   │ • "Democratizing high-stakes AI" to  │
│   co-PI effort & compute arithmetic  │   non-experts without safety bounds  │
│ • 100% letter-to-narrative match     │ • Claiming tribal/community ties     │
│ • Clean supplementary docs (no       │   without signed letters of support  │
│   "ghost personnel" or boilerplate)  │ • Template artifacts (e.g. postdoc   │
│ • Exemplary DMSP (open models, code, │   mentoring when no postdoc budgeted)│
│   interaction logs, CF/NetCDF/JSONL) │ • Under-budgeted collaborative PIs   │
└──────────────────────────────────────┴──────────────────────────────────────┘
```

---

## The 10 Critical NSF Red Flags & Fatal Flaws

### 1. The "Grand Philosophical Framing vs. Method Reality" Disconnect
* **The Fatal Mistake**: Framing a pragmatic machine learning pipeline (e.g., comparing LoRA fine-tuning vs. few-shot system prompting) as solving a fundamental century-old philosophical dilemma (e.g., "Reductionism vs. Holism" or "Revealing Universal Scaling Laws").
* **What Reviewers Think**: Reviewers are domain scientists and computational experts. When they see grandiose philosophical claims ("LLMs as philosophical agents discovering new governing laws"), they immediately check if the method can actually produce mathematical proofs or physical derivations. If the actual pipeline is simply prompt engineering and parameter calibration, reviewers score this as a major weakness: *"The mapping between the philosophical divide and the two LLMs is looser than claimed; this reflects LLM prompting priors rather than genuine epistemological orientations."*
* **How to Fix**:
  - Keep the framing tightly coupled to what your method can empirically measure.
  - Frame the work as *evaluating computational representations*, *inductive biases*, or *agentic workflows* rather than claiming the AI will directly "discover universal physical laws," unless you have an explicit, end-to-end symbolic/analytical discovery pipeline.
  - Distinguish between **AI benchmarking** (measuring performance across scales) and **scientific discovery** (deriving new mechanistic insights).

### 2. The Single-Model Conflation Trap
* **The Fatal Mistake**: Hypothesizing about fundamental physical behavior (e.g., scale-dependent predictability across 1 to >1000 km² catchments) while running only a single domain simulator (e.g., CREST, WRF-Hydro, or ParFlow).
* **What Reviewers Think**: *"Tying the AI agent strictly to one model means any performance degradation at larger or smaller scales could simply reflect that specific model's structural limitations or parameter sensitivity, rather than any fundamental scaling law."*
* **How to Fix**:
  - Explicitly acknowledge the structural limitations of the chosen model.
  - Propose a multi-model benchmark or ablation (e.g., testing across a bucket model, a distributed conceptual model, and a fully distributed hydrodynamic model).
  - Explicitly decouple **model structural error** from **scale-dependent physical behavior**.

### 3. The "Why Not Classical ML or Traditional Optimization?" Justification Void
* **What Reviewers Ask**:
  1. *"Deep learning architectures (LSTMs, Graph Neural Nets, Neural ODEs) already bypass scaling bottlenecks by training at the target scale. Why use an LLM for parameterization?"*
  2. *"Traditional global optimization algorithms (SCE-UA, MCMC, CMA-ES, PEST) already calibrate conceptual models efficiently. What is the value proposition of LLMs debating parameters?"*
* **The Fatal Mistake**: Assuming that using modern LLMs or Agentic AI is self-evidently justified without defending against classical deep learning or established numerical optimization baselines.
* **How to Fix**:
  - Provide an explicit **Why LLMs / Agents?** justification matrix.
  - Highlight distinct capabilities that classical numerical optimizers cannot perform:
    - Ingesting unstructured multimodal data (text manuals, soil survey PDFs, spatial maps, agency reports, hydrograph shapes).
    - Generating interpretable reasoning chains, diagnostic explanations, and hypothesis auditing.
    - Zero-shot / few-shot transfer to ungauged basins via domain knowledge synthesis.
    - Autonomous self-debugging and code generation.
  - Include classical optimizers (SCE-UA, MCMC, Bayesian Optimization) and classical DL (LSTMs) as explicit **control baselines** in your evaluation tables.

### 4. AI Vulnerability Blindspots: Reward Hacking & Equifinality
* **The Fatal Mistake**: Proposing Reinforcement Learning with Simulation Feedback (RLSF) or physics-in-the-loop training without discussing how to prevent the model from gaming the objective function.
* **What Reviewers Think**: In environmental and physical modeling, **Equifinality** (many different parameter sets yielding the same hydrograph fit for the wrong physical reasons) is a classic problem. If an LLM is rewarded purely on Nash-Sutcliffe Efficiency (NSE) or Kling-Gupta Efficiency (KGE), it will rapidly discover unphysical parameter combinations that maximize the score.
* **How to Fix**:
  - Explicitly address **Reward Hacking** and **Equifinality**.
  - Detail multi-objective and physics-constrained reward functions:
    - Mass/energy balance penalty terms ($\text{Penalty}_{\text{mass}} = |\sum P - \sum ET - \sum Q - \Delta S|$).
    - Parameter plausibility regularizers based on soil/geomorphological priors.
    - Multi-variable validation (evaluating not just streamflow, but also evapotranspiration, soil moisture, and peak timing).
    - Out-of-sample stress testing on extreme historical events.

### 5. Arbitrary Thresholds and Ignoring Confounding Landscape Variables
* **The Fatal Mistake**: Defining stratification bins purely by a single metric (e.g., catchment area: 1–10, 10–100, 100–1000, >1000 km²) without physical justification or consideration of confounding factors.
* **What Reviewers Think**: *"Why assume the transitional scale is 100–1000 km²? Catchment characteristics (geology, steep terrain, urbanization, regulation) matter more than area alone. In an urban basin <100 km², spatial heterogeneity can be far higher than in a 5000 km² flat prairie basin."*
* **How to Fix**:
  - Provide literature-grounded citations for any classification boundaries.
  - Incorporate multi-dimensional stratification: basin size cross-tabulated with aridity index (Budyko), topographic relief, land use (urban vs. pristine), and degree of human regulation (dams/reservoirs).

### 6. The "Democratizing High-Stakes AI" Trap (Unsafe Non-Expert Deployment)
* **The Fatal Mistake**: Arguing that your agentic framework allows non-experts (e.g., municipal staff, citizen scientists, community volunteers) to generate flood risk assessments or policy reports with simple natural language prompts, without detailing safety guardrails.
* **What Reviewers Think**: *"The potential for bias and hallucination is dangerous given the proposal for non-experts to generate risk reports. Regions without funding or data will have worse models, and deploying unvalidated natural-language simulation to non-experts without a certified engineer/expert in the loop is a severe public safety risk."*
* **How to Fix**:
  - Frame non-expert tools as **Exploratory Educational & Decision-Screening Aids**, NOT autonomous decision-making or official risk-certification engines.
  - Mandate **Human-in-the-Loop (HITL)** validation workflows: outputs must include prominent uncertainty bounds, calibration logs, and explicit disclaimers requiring professional hydrologist review.
  - Detail quantitative bias mitigation for data-scarce basins (e.g., transfer learning from hydro-climatically similar donor basins, synthetic data augmentation, zero-shot uncertainty intervals).

### 7. The Missing Letter Trap (Claiming Partnerships Without Letters)
* **The Fatal Mistake**: Mentioning specific community organizations, tribal nations, city departments, or industrial partners in the narrative, but failing to include signed Letters of Collaboration in the Supplementary Documents.
* **What Reviewers Think**: Reviewers cross-check the narrative against the Supplementary Documents page by page. If you write: *"We will work with the Otoe-Missouria Tribal Nation and train mentees on CARE principles for Indigenous data governance"*, but there is no letter from that Tribal Nation, reviewers flag this as a critical omission: *"While tribal engagement was noted, no letter from a tribal nation was provided."*
* **How to Fix**:
  - Every external organization named in the Project Description MUST have a corresponding PAPPG-compliant Letter of Collaboration.
  - If a partnership is exploratory and lacks a formal letter, frame it generically (e.g., *"We will engage regional water management stakeholders following established protocols..."*) rather than naming a specific entity as a committed partner.

### 8. Ghost Personnel & Copy-Paste Boilerplate in Supplementary Documents
* **The Fatal Mistake**: Leaving leftover text from earlier proposal templates in the Mentoring Plan, Facilities, or Budget Justification (e.g., describing mentoring for a "Postdoctoral Scholar" when the budget only requests Graduate Research Assistants).
* **What Reviewers Think**: *"There is a mention of a postdoc having the opportunity to teach in the Mentoring Plan. Not sure if this is a typo, or an artifact from a previous version of the proposal."* This signals carelessness and undermines reviewer confidence in the team's project management.
* **How to Fix**:
  - Run a strict cross-document reconciliation: Every role named in the Mentoring Plan (Postdoc, Grad Student, Undergrad) MUST match the budget tables exactly.
  - Use the new NSF PAPPG rules: Mentoring Plans are now required for **both Postdocs and Graduate Students**. Ensure the plan explicitly names the exact personnel categories budgeted.

### 9. Scope vs. Team Effort & Compute Arithmetic Mismatch
* **The Fatal Mistake**: Proposing a massive, multi-tiered project (e.g., curating 1.2M domain texts + pre-training/fine-tuning a 20B LLM + distributed RLSF simulation on HPC + multi-agent debate council + global 1,000-basin benchmarking + CloudBank web serving) while allocating minimal effort (e.g., 0.5 summer months for PIs, $79k total over 3 years for a collaborative institution).
* **What Reviewers Think**:
  1. *"The scope is overly ambitious for the team size, duration, and effort allocation."*
  2. *"The role of the collaborative PI does not match the modest resource allocation."*
  3. *"The computational cost of training a 20B parameter model with RLSF is not analyzed. Are the requested ACCESS credits and institutional GPUs actually sufficient?"*
* **How to Fix**:
  - **Compute Feasibility Proof**: Provide explicit arithmetic for GPU training and inference:
    $$\text{Compute Needed} = N_{\text{tokens}} \times 6 \times N_{\text{params}} \times \text{epochs} \approx X\text{ GPU-hours on NVIDIA A100/H100}$$
    Show that the requested ACCESS credits or institutional GPU nodes cover this requirement with a $1.5\times$ margin.
  - **Effort-to-Task Balance**: Ensure every collaborative PI has substantial, defensible person-months (typically $\ge 1.0$ month/year) for leading major tasks.

### 10. Superficial Multi-Agent Framing vs. SOTA AI Literature
* **The Fatal Mistake**: Claiming that a "Multi-Agent Debate / Council" is fundamentally novel, without citing current literature on LLM reasoning bounds or comparing against single-agent baselines.
* **What Reviewers Think**: Reviewers knowledgeable in AI will cite recent literature (e.g., *Wang et al., 2024: "Rethinking the Bounds of LLM Reasoning: Are Multi-Agent Discussions the Key?"*) showing that multi-agent debates often underperform or simply match single-agent prompting with self-consistency or chain-of-thought, while incurring $N\times$ token overhead.
* **How to Fix**:
  - Acknowledge existing multi-agent scientific frameworks (e.g., INDRA, ChemCrow, ChatEval).
  - Explicitly include a **Single-Agent vs. Multi-Agent Ablation Study** in your experimental tasks.
  - Justify the debate mechanism in terms of complementary domain roles (e.g., physical boundary enforcement vs. systemic contextual adaptation), not just generic "multi-agent intelligence."

---

## NSF Reviewer Psychology & Panel Dynamics

Understanding how NSF panels evaluate proposals is essential to structuring your narrative:

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                           THE NSF PANEL DYNAMICS                            │
├─────────────────────────────────────────────────────────────────────────────┤
│ 1. THE 3-REVIEWER SYSTEM:                                                   │
│    • Primary Reviewer: Deep read, summarizes project, leads discussion.     │
│    • Secondary Reviewer: Checks methodology, feasibility, data, budget.     │
│    • Tertiary / Scribe: Often an out-of-discipline panelist who evaluates   │
│      clarity, Broader Impacts, and overall significance.                    │
│                                                                             │
│ 2. THE 15-MINUTE PANEL DISCUSSION:                                          │
│    • Proposals are discussed for only 10–15 minutes during the panel.       │
│    • Any clear fatal flaw (unfeasible compute, missing letters, overclaim)   │
│      allows the panel to quickly move the proposal to "Medium / Low Priority"│
│    • Proposals in the "Fundable" tier have ZERO unaddressed fatal flaws and  │
│      provide easy soundbites for the Primary Reviewer to defend.            │
│                                                                             │
│ 3. THE SKEPTICISM ESCALATOR:                                                │
│    • Buzzwords ("revolutionize", "philosophical AI") raise reviewer defense.│
│    • Concrete equations, preliminary data, and falsifiable hypotheses lower │
│      defenses and build trust.                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## Section-by-Section Annotated Guidance & Critique Prevention

### 1. Project Summary (1 Page)
* **Mandatory Structure**: Must contain three distinct labeled headers: `Overview`, `Intellectual Merit`, `Broader Impacts`.
* **Reviewer Checklist**:
  - [ ] Does the **Overview** state the core scientific problem, the methodology, and the key innovation in plain, accessible language?
  - [ ] Does the **Intellectual Merit** summarize specific, falsifiable scientific hypotheses and the exact knowledge advancement?
  - [ ] Does the **Broader Impacts** outline concrete societal benefits, educational integration, and target stakeholders (with metrics)?
  - [ ] Are any buzzwords pruned in favor of precise technical mechanisms?

### 2. Background and Motivation (1–2.5 Pages)
* **Goal**: Establish the grand scientific challenge and prove why existing approaches (both classical domain science and current AI) fail.
* **What Reviewers Look For**:
  - Citation of community consensus documents (e.g., NRC Decadal Surveys, "23 Unsolved Problems in Hydrology", IPCC AR6).
  - Clear articulation of the **epistemic bottleneck** (e.g., why laboratory physical equations fail to aggregate to macro scales).
  - Concrete preliminary results from the PIs demonstrating that they have already built the initial proof-of-concept (e.g., preliminary code, pilot benchmark scores, published preprints).

### 3. Science Hypotheses and Objectives (1–1.5 Pages)
* **Goal**: State 2–4 clear, falsifiable hypotheses that drive the research tasks.
* **Format**:
  $$\text{Hypothesis } H_n: \text{ [Clear assertion with directionality and underlying physical mechanism]}$$
* **Reviewer Trap**: Hypotheses that are merely task descriptions (e.g., *"We hypothesize that building HydroGPT will be useful"*).
* **Fix**: Ensure each hypothesis asserts a specific causal relationship that can be proven false (e.g., *"We hypothesize that the predictive skill of microphysics-constrained LLMs decays with catchment area ($>1000\text{ km}^2$) at a faster rate than unconstrained foundation models due to unresolved spatial heterogeneity"*).

### 4. Detailed Research Tasks and Methodology (7–9 Pages)
* **Goal**: Provide step-by-step technical execution plans for each task.
* **Required Sub-Elements for Every Task**:
  1. **Objective & Rationale**: What is being done and why.
  2. **Data & Methods**: Specific algorithms, datasets (with spatial/temporal coverage), loss functions, and software frameworks.
  3. **Baselines & Controls**: Classical domain baselines (e.g., traditional calibration algorithms, standard numerical models, classical deep learning).
  4. **Expected Milestones & Deliverables**: Exact datasets, model weights, open-source repositories, or papers.
  5. **Potential Pitfalls & Alternative Strategies**: (CRITICAL!) Explicitly describe what the team will do if the primary method encounters failure modes (e.g., reward hacking, training instability, data scarcity).

### 5. AI Cyberinfrastructure, Compute Feasibility, & Data Management
* **Reviewer Checklist**:
  - [ ] Is there an explicit table of compute requirements (GPU models, node counts, storage TB, memory requirements)?
  - [ ] Are national cyberinfrastructure allocations (NSF ACCESS, NCAR, NAIRR, CloudBank) explicitly named with active project IDs or detailed credit calculation breakdowns?
  - [ ] Is the software stack portable (Docker/Singularity, Hugging Face, PyTorch, Ray)?

### 6. Broader Impacts (1.5–2 Pages)
* **Reviewer Checklist**:
  - [ ] Are the educational activities concrete and integrated into existing courses?
  - [ ] Is there a dedicated workforce development plan spanning all participating institutions (including undergraduate engagement at regional/PUI/MSI institutions)?
  - [ ] Is community engagement supported by explicit letters of collaboration?
  - [ ] Are ethical AI considerations (mitigating bias in data-scarce regions, preventing hallucination, human-in-the-loop validation) rigorously addressed?

### 7. Results from Prior NSF Support (Up to 5 Pages)
* **Mandatory Format for Every Named PI/co-PI with NSF awards in past 5 years**:
  - NSF Award Number, Title, Amount, Period of Support.
  - **Intellectual Merit**: Summary of findings, major advances.
  - **Broader Impacts**: Educational and societal outcomes.
  - **Publications & Products**: Specific citations resulting from the award.
  - **Data and Research Products**: Location and accessibility of archived data.
  - If a PI has no prior NSF support, explicitly state: *"PI [Name] has had no prior NSF support in the past five years."*

---

## Pre-Submission Self-Audit Checklist: The NSF "Must-Pass" Gate

Before submitting an NSF proposal, every item on this checklist must be verified:

### Conceptual & Methodological Integrity
- [ ] **Falsifiable Hypotheses**: Are all hypotheses explicitly numbered, directional, and falsifiable with proposed experiments?
- [ ] **Scientific vs. AI Boundary**: Does the proposal explain how AI outputs translate into *new physical/scientific knowledge*, not just an ML benchmark?
- [ ] **Classical Baseline Inclusion**: Are standard domain models and classical optimization/ML algorithms included as control baselines?
- [ ] **Multi-Model / Multi-Domain Validation**: Is the scientific finding isolated from the idiosyncrasies of a single software simulator?
- [ ] **AI Failure Modes Addressed**: Are reward hacking, hallucination, equifinality, and out-of-distribution generalization explicitly analyzed with mitigation plans?
- [ ] **Multi-Agent Value Justified**: Is the multi-agent/council design justified against single-agent prompting and existing scientific agent frameworks?

### Team, Resources, and Budget Alignment
- [ ] **Effort Reconciled with Scope**: Does every PI and co-PI have adequate funded person-months to lead their assigned tasks?
- [ ] **Subaward / Collaborative Equity**: Are collaborative institutions adequately resourced for the deliverables they own?
- [ ] **Compute Feasibility Arithmetic**: Is the GPU/compute requirement explicitly calculated and proven feasible with named allocations?
- [ ] **Zero Ghost Personnel**: Does the Mentoring Plan only discuss personnel categories (Grad Students, Postdocs, Undergrads) that are actually funded in the budget?

### Compliance, Letters, and Supplementary Documents
- [ ] **Letter-to-Narrative 1-to-1 Match**: Does every external stakeholder, community partner, or tribal nation mentioned in the text have a signed Letter of Collaboration in the exact NSF PAPPG template format?
- [ ] **No Unallowable Letter Endorsements**: Are all letters strictly compliant with PAPPG (no unsolicited letters of endorsement; standard 1-sentence collaboration format unless solicitation specifies otherwise)?
- [ ] **Exemplary DMSP**: Does the Data Management Plan specify community metadata conventions (CF/NetCDF, JSONL, Model Cards, ISO 19115) and long-term repositories (HydroShare, Zenodo, Hugging Face)?
- [ ] **SciENcv Biosketches**: Are all senior personnel biosketches and Current & Pending Support generated through SciENcv in the active PAPPG version?

---

## Recurring Strengths to Preserve (What Reviewers Praised)

When designing competitive NSF proposals, keep and amplify these highly successful patterns:

1. **Simulation-in-the-Loop AI Formulations (e.g., RLSF)**: Replacing subjective human feedback with deterministic, physical simulation metrics (NSE, KGE, conservation laws) is universally recognized by reviewers as a high-impact, publishable AI contribution.
2. **Community "Gold-Standard" Knowledge Corpora**: Curating open-access, AI-ready domain corpora (peer-reviewed papers, agency reports, simulation traces) with PyTorch dataloaders and Hugging Face release fills a recognized bottleneck in science.
3. **Grounding in Consensus Grand Challenges**: Anchoring objectives directly to community consensus questions (e.g., "23 Unsolved Problems in Hydrology", Earth System Decadal Survey) gives immediate legitimacy to the research motivation.
4. **Transparent Agent Interaction Archival**: Preserving multi-agent debate logs and reasoning traces as open datasets in the DMSP provides a novel contribution to the science of AI reasoning.
5. **Concrete Preliminary Metrics**: Demonstrating working end-to-end agents with published preprints and quantitative case-study benchmarks establishes high PI credibility.

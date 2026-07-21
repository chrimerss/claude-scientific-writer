# NASA ROSES Proposal Guidelines

## Overview

NASA's Research Opportunities in Space and Earth Sciences (ROSES) is the primary vehicle for soliciting research proposals in Earth science, heliophysics, planetary science, and astrophysics. ROSES is released annually as an omnibus solicitation (NRA) containing dozens of individual program elements, each with distinct objectives, page limits, and review criteria. This guide focuses on Earth science applied research programs—particularly **A.08 (Water Resources)** and **A.09 (Earth AI Foundation Models)**—distilled from analysis of successful proposals.

**Key Distinction**: Unlike NSF or NIH, NASA Earth science applied research proposals are **decision-support-oriented**. They must demonstrate a clear pathway from Earth observation (EO) data to operational decision-making by identified end users. This "Earth Science to Action" (ES2A) philosophy pervades every section.

Before drafting the proposal, always remember to check out the program call for proposal document to cover every aspect of the required elements. Otherwise, it is an unsuccessful proposal. For example, the RFP for NISAR A.3 is at https://nspires.nasaprs.com/external/viewrepositorydocument/cmdocumentid=1083026/solicitationId=%7B0073A14E-AFC3-13BD-0128-56AFE0030B08%7D/viewSolicitationDocument=1/A.3%20NISAR_DART_Amend48-v2.pdf.

> **Companion file**: `nasa_lessons_learned.md` in this directory distills recurring pitfalls and reviewer critique patterns from prior submissions in this portfolio. Consult it **before drafting** any NASA proposal and **during proposal review**. It contains a pre-submission checklist, the top-10 recurring reviewer critiques, section-by-section annotated guidance, and Socratic self-review prompts derived from actual panel summaries.

> **Companion file**: `nasa_earth_action_guidebook.md` distills the official NASA Earth Science Applications Guidebook (June 2026, 84 pp.) into proposal-relevant guidance. Covers the five-task user engagement framework, three building blocks, co-development methods (HCD, SDM), impact definition (Use → Action → Benefit), EA-specific budget categories, team composition, transition & sustainability planning, implementation challenge taxonomy, and ARL pathway details. Consult it **during proposal development** for user-engagement language, impact framing, and co-development planning.

---

## High-Level Strategic Insights

The principles below cut across NASA program elements and reflect repeated lessons from competitive (funded and unfunded) NASA submissions in this portfolio. Internalize these before writing.

### 1. Scope is the most common cause of weakness ratings
Across review cycles spanning more than a decade, the single most consistent panel critique is "highly ambitious in scope … raises feasibility concerns." A NASA reviewer reads the task list, multiplies by the project duration, and asks whether the team can plausibly deliver. **Default to fewer, deeper tasks** (4–5 for 2-year projects, 5–7 for 3-year projects). Resist the impulse to bundle data harmonization, modeling, evaluation, alerting, scenario planning, and scaling into a single award.

### 2. Solicitation alignment is binary
Reviewers extract solicitation priority topics and check whether each is addressed by a specific task. A proposal that **claims novelty in an area the project does not actually pursue** earns a major relevance weakness — historically the difference between a "Good" and a "Very Good" score. Before submission, build an internal Solicitation-Mapping Table: every priority → which task → which deliverable. Remove novelty claims the project will not deliver.

### 3. Preliminary results decide credibility
The most common major weakness across the portfolio is "preliminary results are not described in sufficient detail." Reviewers cannot evaluate feasibility from a figure alone. Every preliminary-result figure needs (1) data source, (2) method summary, (3) baseline, (4) metric and value, (5) interpretation. When citing prior application to a region or dataset, **show the actual result** — do not just state that the model "has been applied." Unevidenced application claims have been flagged as minor weaknesses for over a decade.

### 4. End users must be decision-makers, not intermediaries
NASA's ES2A framework demands user-centered design with the **decisional end-user**. Embedding only a data intermediary (a regional data center, a geospatial hub) on the team is consistently flagged as an indirect pathway. Embed *both*: an intermediary for hosting and at least one direct end user (emergency manager, planner, agency operations lead) for evaluation and adoption. Letters of support from the intermediary do not substitute for the end user's commitment.

### 5. Every quantitative target needs a baseline and an impact threshold
A claim of "10 m resolution," "1000× speedup," "85% accuracy," or "sub-hour latency" must answer three reviewer questions: (a) compared to what baseline; (b) why this specific threshold; (c) at what level does the improvement actually change end-user behavior. Panel notes have explicitly recommended: *"When proposing metrics of merit, clearly define them and suggest the threshold of impact they need to reach to 'make a difference' for the end user's decision."* Build a Metrics Table early in the proposal: Metric | Baseline | Target | Why this threshold | Measurement method.

### 6. ARL claims must be conservative and evidenced
ARL advancement of more than one level per project year is rarely credible. ARL 6 means "demonstrated in simulated operational environment with end-user testing"; ARL 7 requires active use in partner decision workflows. Claims of ARL 4→7 in two years are routinely flagged optimistic. **For each ARL level**, name the specific evidence (validation report, scored exercise, signed acceptance) and the task that generates it. If preliminary partnerships and validations do not document the starting ARL, the entire trajectory is suspect.

### 7. Uncertainty must propagate through every coupled model
When a surrogate, emulator, or data-driven model is trained against a physics-based reference, reviewers expect explicit treatment of how the **reference model's own uncertainty** affects the trained system. "0.9 accuracy relative to physics-based simulation" does not address absolute accuracy. Quantify the reference's validation error against observations, describe propagation through training, and include an independent observation-based validation in addition to the in-house benchmark.

### 8. Methodological specificity beats vocabulary density
AI/ML, foundation-model, and data-fusion proposals routinely accumulate impressive vocabulary (LoRA, FSDP, Hierarchical ViT, super-resolution, Swin-shifts, cross-calibration) without specifying configurations. A reviewer reading buzzword-dense methodology infers the team knows the tools but has not made commitments. **Each technical choice needs**: input/output dimensions, dataset size and split, loss function, validation metric, and a one-sentence justification relative to alternatives. A method that could not be reproduced from the proposal is not specific enough.

### 9. Transition plans must name a host and absorb operational costs
"Future grant proposals will sustain the work" reads as failure to plan. Transition plans should identify a specific post-project host (intermediary infrastructure, operational partner, industry partner), describe knowledge transfer (Docker containers, video training libraries, co-developed user manuals, not just code), and address who pays for post-project compute, hosting, and maintenance. The transition must be resilient to end-user staff turnover.

### 10. Internal coherence is visible to reviewers
Budget that does not reconcile with the work plan; Gantt chart task durations that do not match personnel effort; forecast windows misaligned with hazard dynamics; metrics inconsistent across the DMA, methods, and anticipated results — all of these are flagged as minor weaknesses or "issues that reduce confidence." Before submission, cross-walk: DMA end user ↔ task leads ↔ letters of support ↔ transition plan; performance metrics ↔ methodology ↔ anticipated results; task durations ↔ personnel months ↔ Gantt chart.

### 11. Justify in-house model families per submission
Teams with a developed model family tend to reuse it across proposals, often without re-justifying the choice for each new use case. Reviewers outside the immediate community do not share the assumption that the model family is the obvious choice. Re-justify it each time, naming the most directly relevant prior validation. If validation is in a different region or hazard, acknowledge the gap and propose a calibration / validation task explicitly.

### 12. Generalization claims must be bounded
A demonstration in one region or one hazard cannot support a claim of "national-scale" or "transferable to other hazards" applicability. Bound generalization claims to what the project will actually demonstrate (one additional region as a transferability pilot, with explicit acknowledgment of limitations). Distinguish demonstrated scalability (within the award) from architectural scalability (the design supports transfer).

### 13. DAPR compliance is unforgiving
For Dual Anonymous Peer Review programs, identifying information in the S/T/M section is grounds for return. Common DAPR slips: institutional names embedded in figure captions, lab facility names, self-citations in first person ("our previous work"), PI initials in screenshots. Run a final DAPR pass: replace institution names with generic descriptors, render self-citations in third person ("the proposing team has previously …"), strip identifying metadata from figures.

### 14. Reviewer attention is finite
A panel reviewer may read 12–15 proposals per cycle. Structural devices that reward skimming — clear section headings, summary tables, one-sentence task descriptions, a Metrics Table, a Solicitation-Mapping Table — measurably help. The one-sentence summary of the proposal should be unambiguous after a 30-second skim of the DMA and Anticipated Results sections.

### 15. Internal coherence is checked at every seam
Reviewers cross-walk: **research questions ↔ tasks ↔ budget lines ↔ team expertise**. A research question with no answering task, an answering task with no funded effort, or funded effort without the named expertise to execute it — each is a visible inconsistency. The most reliable internal-coherence audit is a single internal table: RQ | Task | Personnel (named) | Budget line | Deliverable. Walk the table before submission; every cell should be filled. Two specific failure modes to watch: (a) the **risk-mitigation section that argues against a condition that motivates one of the project's own deliverables** (e.g., a surrogate model is proposed to handle computational demands, and the risk section then argues computational demands are unlikely to be a problem), and (b) **multi-component proposals where readiness detail is uneven** — uniformly described for some components but glossed over for others. Reviewers infer the gloss-over components are less mature than the headline ARL suggests. PI funded time, line-item specificity, and budgeted workshops / stakeholder activities are also routinely checked seams.

### 16. Domain-standard alternatives must be acknowledged, not ignored
For every NASA EO product chosen (IMERG, SMAP, MODIS, MERRA-2, GPM, etc.), domain reviewers know the non-NASA operational alternatives in the same niche (MRMS, Stage IV, AORC, HRRR, NLDAS, OpenStreetMap, local LiDAR). Defaulting to the NASA product without acknowledging these alternatives reads as either unfamiliarity with the field or unwillingness to use the best tool for the job. **NASA reviewers want NASA assets justified, not assumed.** A brief comparison paragraph (candidate products, native resolution / latency, strengths, limitations for this use case, why the chosen product wins, or why a fusion is proposed) closes this gap. The same logic applies inside ML methodology: when proposing a generative or super-resolution downscaling architecture, the known failure mode of **extreme-event underestimation** must be explicitly addressed (tail-aware loss, tail-explicit validation, conditional sampling). For non-traditional data sources (crowdsourced, citizen science, social media), the collection pipeline, accuracy validation, and prior-use evidence must be described. Acknowledging known failure modes and known alternatives is the cheapest way to demonstrate methodological maturity.

### 17. User engagement must be deep, documented, and iterative — not transactional
NASA's official Earth Action Guidebook (2026) codifies what reviewers already penalize: user engagement that begins and ends with a letter of support is insufficient. Proposals must demonstrate a **five-task engagement sequence**: (1) Know the Territory — research the user's landscape, mandates, and existing data use; (2) Reach Out and Listen — use experiential questions ("What keeps you up at night?", "What decision would you like to be more certain about?") rather than "What do you need?"; (3) Frame the Challenge Together — structured needs assessment (stakeholder mapping, journey mapping, key informant interviews); (4) Co-design a Solution — active, systematic iteration on products, data, roles, sustainability, and training; (5) Formalize the Proposal — user engagement plan, transition plan, and joint definitions of success. Proposals where user engagement reads as a single meeting or an exchange of emails will be flagged. The **Three Building Blocks** are: relationships (built before the solicitation, not during), listening (close understanding of workflows, obstacles, and data limitations), and fitting science to the user's problem (not promoting a dataset or model). The two-sentence test: can you articulate (1) why now, (2) why this approach, and (3) who will use it? See `nasa_earth_action_guidebook.md` §2–3 for full framework.

### 18. Impact must be defined as Use → Action → Benefit, not just outputs
NASA Earth Action defines impact in three tiers: **Use** (extent of application use by users/public), **Action** (real-world activities and changes in users' decisions), and **Benefit** (positive results for users, their partners, or their environment). A proposal that only promises outputs (datasets, tools, maps) without articulating outcomes (changed decisions) and impact (societal benefit) will score below competitive proposals. NASA distinguishes outputs (what the project delivers), outcomes (changes in user activities and decisions), and impact (higher-level social, economic, or environmental change). For each tool output, write a **Decision-to-Action sentence**: "When the output indicates X, the end user is authorized to take action Y within time window Z." Develop a **theory of change** mapping program activities → outcomes → impact, and co-develop performance metrics *with* users (right-sized, started early, aligned with users' existing metrics and funders' M&E frameworks). See `nasa_earth_action_guidebook.md` §5 for the full impact framework.

---

## NASA ROSES Program Structure

### Common Earth Science Applied Research Programs

| Program Element | Focus | Typical Duration | ARL Requirement |
|---|---|---|---|
| A.08 Water Resources | EO integration for water management decisions | 2–3 years | ARL 5→8 (Type 2) |
| A.09 Earth AI Foundation Models | Prithvi and NASA FM applications | 2 years | ARL 3→5 |
| A.37 SERVIR Applied Sciences | Geospatial services for developing nations | 3 years | Varies |
| A.46 Earth Surface & Interior | Geodesy, solid Earth applications | 3 years | Varies |
| A.49 New Investigator Program | Early career Earth scientists | 3 years | N/A |

### Application Readiness Levels (ARL)

The ARL framework is **central** to NASA applied research proposals. It mirrors Technology Readiness Levels but is adapted for decision-support applications. Proposals must clearly state starting and ending ARL and demonstrate a credible advancement plan.

| ARL | Description | Key Evidence |
|---|---|---|
| ARL 1 | Basic research applicable to decision-making | Literature review, conceptual link |
| ARL 2 | Application concept formulated | Feasibility analysis, end-user identification |
| ARL 3 | Proof of application concept | Preliminary results, documented end-user needs |
| ARL 4 | Application prototype in lab environment | Working prototype, internal verification |
| ARL 5 | Application demonstrated in relevant environment | Validated with realistic scenarios, user feedback |
| ARL 6 | Application prototype in simulated operational environment | Tested by end users, systematic evaluation |
| ARL 7 | Application prototype in partner's decision-making | Active use in decision workflows |
| ARL 8 | Application completed and qualified | End-user approval, sustained operational use |
| ARL 9 | Application proven through sustained use | Long-term operational deployment |

**Critical Tip**: Reviewers scrutinize ARL claims. Provide specific evidence for your starting ARL (published validations, documented partnerships, letters of support) and a clear, stepwise plan to reach the target ARL.

---

## Required Proposal Sections

NASA ROSES Earth science proposals follow a structured format. The exact section names may vary by program element, but the following components are universal:

### 1. Science/Technical/Management (S/T/M) Section

This is the core of the proposal (typically 15 pages for A.08, varies by program). It must include:

#### 1.1 Decision-Making Activity (DMA)
**This section is critical and unique to NASA applied research programs.** It must clearly identify:

- **Who is the end user?** Name the specific organization and their mandate. Not "water managers" generically—identify the exact agency, department, and person if possible.
- **What decisions do they make?** Describe the specific operational decisions (allocation, emergency response, planning).
- **What is the current baseline?** Document how decisions are currently made, what data they use, and what gaps exist.
- **How will NASA EO improve this?** Articulate the specific improvement pathway from EO data to better decisions.

**Best Practice Pattern** (from successful proposals):
```
1. Name the end user and their institutional mandate
2. Describe 2-4 specific decision-making activities with operational context
3. Document current baseline practice and its limitations
4. Explain the opportunity: how EO fills the gap
5. Define measurable evaluation metrics for improvement
```

**Example Structure** (from A.08 Water Resources):
- Primary end user: [Organization name], responsible for [specific mandate]
- Decision context: [drought allocation / flood response / infrastructure planning]
- Current practice: Relies on [local gauges, static maps, expert judgment]
- Limitation: [spatial gaps, temporal delays, no basin-scale context]
- Proposed improvement: [EO-informed dashboard providing X hours lead time, Y% improvement]

**Example Structure** (from A.09 Foundation Models):
- Primary end user: [Organization], responsible for [emergency management]
- Decision metrics: Actionable Lead Time, Spatial Precision, Assessment Efficiency
- Baseline capabilities vs. targeted improvements (use a table)
- Clear link between FM capabilities and decision-support needs

**Writing Tips**:
- Use concrete, quantitative improvement targets (e.g., "30–40% improvement in lead time")
- Describe the end user's authority and autonomy to act on the information
- Emphasize that your tool informs but doesn't automate decisions
- Include funded Co-I roles or formal MOUs for end users

#### 1.2 Anticipated Results and Improvements
Describe specific, measurable outcomes:

- **Quantitative metrics**: Lead time improvement, spatial resolution improvement, accuracy targets
- **Operational improvements**: Earlier decisions, greater consistency, reduced uncertainty
- **ARL advancement**: Clear statement of starting and ending ARL with evidence pathway
- **Tangible benefits**: What changes in operational practice
- **Evaluation plan**: How improvements will be measured against baseline

**Best Practice**: Create a table mapping expected outcomes → decision-making improvements → performance measures.

#### 1.3 Project Elements / Description of Project

**Background and Motivation**:
- Frame the problem in terms of societal significance and decision-making urgency
- Use specific, recent events or statistics to establish need (e.g., floods, droughts)
- Connect to regional or national priorities

**Research Questions / Decision Challenges**:
- Frame as applied research questions linking EO to decision support
- Be explicit about what gap this project fills
- Distinguish from pure science questions—emphasize operational relevance

**Current Resources for Decision Making**:
- Document what tools, data, and processes end users currently employ
- Identify specific gaps that NASA EO can address
- This establishes the baseline against which improvement is measured

**Technical Approach**:
- Describe methodology in sufficient detail for feasibility assessment
- Include clear data flow: EO inputs → processing → indicators → decision products
- Emphasize NASA EO assets used (GPM, SMAP, GRACE, Landsat, Sentinel, SWOT, etc.)
- For AI/ML approaches: describe training data, model architecture, validation strategy
- Include preliminary results and figures demonstrating proof-of-concept

**Alignment with NASA Program**:
- Quote specific language from the solicitation
- Map your project to stated priority topics
- Reference the ES2A strategy and relevant Key Results
- Connect to NASA mission phrases like "integrate EO into decision-making"

#### 1.4 Project Risks and Mitigation Strategies
NASA reviewers explicitly evaluate risk. Structure as:

| Risk | Likelihood | Impact | Mitigation |
|---|---|---|---|
| EO product uncertainty | Medium | Medium | Multi-source validation, mission team outreach |
| Dashboard adoption barriers | Low | High | Iterative co-design, training, documentation |
| End-user turnover | Medium | Medium | Institutional MOU, reusable documentation |
| Computational constraints | Low | Medium | Surrogate models, modular architecture |

**Common Risk Categories**:
1. **Data/EO product risks**: Quality, latency, availability
2. **Technical risks**: Model accuracy, computational scalability
3. **Adoption risks**: End-user engagement, organizational change
4. **Scalability risks**: Transferability to new regions, generalization

### 2. Transition Plan
**This section is critical for NASA applied proposals.** It demonstrates how the research will transition from a research product to sustained operational use.

**Required Elements**:
- **Institutional ownership**: Who takes over after the project?
- **Training and capacity building**: How will end users become self-sufficient?
- **Documentation and user guides**: Co-developed with end users
- **Hosting and maintenance**: Where will the system live post-project?
- **Sustainability strategy**: How will it continue without NASA funding?
- **Barriers and mitigation**: Staff turnover, budget constraints, technology evolution

**Best Practice Pattern**:
```
1. Technology handoff: Containerized deployment, open-source code
2. Training: Workshops, video libraries, hands-on exercises with historical events
3. Documentation: Co-developed user manuals, operational guides
4. Hosting: End-user infrastructure or partner platforms
5. Sustainability: Aligned with existing workflows, low maintenance cost
6. Long-term tracking: Documented use pathways, not formal reporting
```

**Strong Examples**:
- "Docker-containerized codebase for reproducible deployment"
- "Video-based Training Library for self-onboarding independent of original stakeholders"
- "Graceful degradation: caches last-valid state if connectivity fails"
- "End users bear post-award operational costs, confirmed via Letters of Support"

### 3. Project Management and Schedule

**Required Elements**:
- Year-by-year task breakdown aligned with ARL milestones
- Gantt chart or timeline table showing task overlap and dependencies
- Clear PI and Co-I responsibilities for each task
- Decision points and go/no-go criteria
- Required program activities (annual meetings, reporting)
- Publication targets

**Best Practice**: Use a table format:

| Task | Year 1 Q1-Q2 | Year 1 Q3-Q4 | Year 2 Q1-Q2 | Year 2 Q3-Q4 | Lead |
|---|---|---|---|---|---|
| Task 1: Needs Assessment | ████ | | | | PI, Co-I 3 |
| Task 2: Model Development | | ████ | ████ | | Co-I 1 |
| Task 3: Validation | | | ████ | ████ | Co-I 2 |
| Publication | | × | | × | PI |

### 4. Earth Science to Action (ES2A) Section

This section demonstrates alignment with NASA's strategic framework. Reference:

- **ES2A Pyramid Levels**: Foundational Knowledge → Applied Research → Solutions & Societal Value → Public Understanding
- **Key Results**: 
  - KR 1.2: Cutting-edge technology
  - KR 1.3: Integrated and trusted Earth system data
  - KR 2.1: Models capturing Earth system intricacies
  - KR 2.2: Co-designed solutions and tools to support users
  - KR 2.3: Trusted information
- **Scaling Strategy**: Both vertical (efficiency gains) and horizontal (new regions/users/domains)
- **Interdisciplinary Team**: Spanning Earth science, computer science, social science

**Writing Tips**:
- Map your project to a specific ES2A pyramid level
- Reference specific Key Results by number
- Describe both vertical and horizontal scaling pathways
- Explain the interdisciplinary nature of the team

### 5. Open Science and Data Management Plan (OSDMP)

**Required Sections**:
1. **Data Management**:
   - Expected data types, formats, volumes, and standards
   - Data archiving and accessibility (NASA-approved repositories: Zenodo, Figshare, NASA Earthdata)
   - Schedule for public availability
   - Licensing (Creative Commons Attribution 4.0)
   - Persistent identifiers (DOIs)
   - Data exempt from sharing (with justification)

2. **Software Management**:
   - Expected software development
   - Repository hosting (GitHub + Zenodo for long-term preservation)
   - Licensing (MIT, GPL v3, or Apache 2.0)
   - Model weights (Hugging Face for ML models)
   - Documentation and reproducibility

3. **Publication Sharing**:
   - Open access commitment
   - Preprint servers (arXiv, ESSOAr)
   - NASA public access policy compliance

4. **Other Open Science Activities**:
   - Reproducibility documentation (Jupyter notebooks, README files)
   - FAIR principles adherence

5. **Roles and Responsibilities**:
   - PI as primary data steward
   - Institutional oversight for data management

### 6. Table of Personnel and Work Effort

Standard table format showing:
- Each team member's role
- Months committed per year (NASA-funded vs. total vs. other funded projects)
- Summed across project duration

### 7. Budget and Budget Narrative

**Budget Items Typically Include**:
- **Personnel**: PI, Co-Is, postdocs, graduate students, technical staff
- **Travel**: NASA program meetings, conferences (AGU, EGU), end-user site visits, workshops
- **Subawards**: Collaborating institutions
- **Computing**: HPC, cloud, GPU, storage
- **Publications**: Open-access fees ($2,000–$3,050 per article)
- **Workshops**: Venue, meals, incentives, materials for end-user engagement
- **Data Management**: Mandatory institutional data curation costs
- **Equipment**: External hard drives, sensors (if applicable)
- **Consultant Costs**: End-user representatives at hourly rates

**Travel Budget Tips**:
- Base estimates on GSA per diem rates for specific destinations
- Include conference registration as separate line item
- Budget for NASA-required program meetings (location TBD → use Washington DC rates)
- Include end-user site visits in border/remote areas

**Best Practices**:
- Use current GSA rates for lodging and M&IE per diem
- Include inflation factors (3% for personnel, 2.3% for other costs per year)
- Budget open-access publication costs ($2,500–3,050 per article)
- Include workshop costs with detailed justification (meals, incentives, materials)
- End-user partners: funded Co-I or hourly consultant rate ($100/hr typical)

### 8. Letters of Support/Commitment

**Essential for NASA Proposals**:
- End-user commitment letters confirming participation, data provision, and adoption intent
- Collaborator letters specifying roles and commitments
- Institutional letters confirming resources and support
- Mission science team letters (for EO product access/guidance)

**Strong Letters Include**:
- Specific commitment of time/resources
- Statement of need for the proposed capability
- Confirmation of intent to use outcomes beyond project period
- Description of how outputs integrate with existing workflows

---

## Dual Anonymous Peer Review (DAPR)

Many NASA programs now use DAPR. Key requirements:

- **Remove all identifying information** from the S/T/M section
- Reference your own work in the third person
- Do not include institutional names in the technical narrative
- Anonymize figures, team descriptions, and facilities
- Use generic terms like "the PI" or "the project team"
- Biographical sketches and budget narratives are NOT anonymized

**Common DAPR Mistakes**:
- Self-citation that reveals identity ("our previous work [PI et al., 2024]")
- Institutional references ("the University of XYZ's supercomputer")
- Unique facility names that identify the institution
- Including PIs name in figure captions

---

## Writing Style and Strategy

### NASA-Specific Language Patterns

Successful NASA proposals consistently use specific language patterns:

**Decision-Support Framing**:
- "The decision-making activity addressed by this project is..."
- "End users retain full authority to implement actions informed by project outputs"
- "Effectiveness is evaluated by comparing baseline practices with documented decision scenarios"
- "The tool informs but does not automate or replace operational authority"

**EO Integration Language**:
- "This project leverages NASA Earth observations to..."
- "EO-informed indicators that support basin-scale decision-making"
- "Translating spatially continuous EO signals into interpretable indicators"
- "NASA EO provides basin-scale information at spatial and temporal resolutions relevant to..."

**ARL Advancement Language**:
- "The project advances from ARL X to ARL Y through..."
- "Validation at ARL X has been demonstrated through retrospective event analyses"
- "Progression to ARL Y is achieved through integration into end-user operational environments"
- "End-user approval for ARL 8 is achieved within the project award period through..."

**Co-Development Language**:
- "Co-developed with end users through iterative engagement"
- "User-centered design and decision interpretability"
- "Structured interviews, workflow mapping, and tabletop exercises"
- "Feedback informs refinement of indicator presentation, aggregation scales, and update frequency"

### Effective Persuasion Techniques

1. **Lead with the Decision Context**: Open the proposal with the end user's problem, not the science.
2. **Quantify Everything**: Replace vague claims with specific numbers (lead time, accuracy, improvement percentages).
3. **Use Tables for Clarity**: Decision metrics, ARL progression, risk mitigation, timeline—tables are highly effective.
4. **Show Preliminary Partnerships**: Document prior engagement (years of collaboration, MOUs, IRB-approved interviews).
5. **Establish Credibility Early**: Reference team's prior NASA-funded work and validated tools.
6. **Figures Are Critical**: Include workflow diagrams, study area maps, preliminary results, conceptual frameworks.
7. **Address "So What?"**: Every technical capability must link back to a decision-making improvement.

### Section-by-Section Page Allocation

For a 15-page S/T/M section (A.08 Water Resources):

| Section | Pages | Notes |
|---|---|---|
| Decision-Making Activity | 1.5–2 | Sets the operational context |
| Anticipated Results | 1–1.5 | Quantitative targets, ARL advancement |
| Background/Motivation | 1.5–2 | Problem significance, study area |
| Research Questions | 0.5–1 | Applied, decision-focused |
| Current Resources | 0.5–1 | Baseline documentation |
| ARL Assessment | 0.5 | Starting and ending ARL with evidence |
| NASA Program Alignment | 0.5 | Quote solicitation language |
| Technical Approach | 4–5 | Methods, data, preliminary results |
| Risks and Mitigation | 0.5–1 | Structured risk table |
| Transition Plan | 1–1.5 | Post-project sustainability |
| Project Management | 0.5–1 | Schedule, roles, timeline table |
| ES2A | 0.5–1 | Strategic alignment |

---

## Program-Specific Guidance

### A.08 Water Resources Program

**Focus**: Integration of NASA EO into water management decision-making

**Priority Topics** (check annual solicitation for current priorities):
- Water System Risk Assessment and Adaptive Management
- Drought Resilience and Water Scarcity Management
- Integrated Water Infrastructure for Stormwater and Floodwater Management

**Proposal Types**:
- **Type 1**: Starting at ARL 1–3, advancing to ARL 5–6
- **Type 2**: Starting at ARL 5, advancing to ARL 7–8

**Key Requirements**:
- Clear end-user identification with funded participation
- Documented baseline decision-making practices
- Measurable improvement metrics
- Transition plan for sustained use post-project
- ES2A alignment

**Writing Tips**:
- Emphasize operational relevance over scientific novelty
- Describe specific decision workflows, not just data products
- Show how NASA EO data is translated into actionable indicators
- Document prior end-user engagement extensively
- Include Letters of Support from end-user organizations

### A.09 Earth AI Foundation Models

**Focus**: User-centered applications leveraging NASA's Prithvi Foundation Models (Prithvi-EO, Prithvi-WxC)

**Key Requirements**:
- Must use NASA Prithvi foundation models
- Must demonstrate efficiency gains (reduced compute, reduced labeled data)
- Must demonstrate scalability (vertical: efficiency; horizontal: transferability)
- Must involve end-user co-development
- Must advance ARL (typically ARL 3→5)

**Unique Considerations**:
- **Quantify FM efficiency**: Report GPU hours saved, labeled data reduction (%), inference speedup (×)
- **Demonstrate transferability**: Show the FM approach can generalize to new regions without retraining
- **Benchmark against baselines**: Compare with non-FM approaches (e.g., UNet, physics-based models)
- **Prithvi-specific language**: "Prithvi-EO as environmental representation learning," "Prithvi-WxC as atmospheric context conditioning"

**Writing Tips**:
- Frame Prithvi as enabling capabilities otherwise infeasible (data-poor regions, real-time needs)
- Quantify anticipated efficiency gains with specific numbers
- Describe fine-tuning strategy (LoRA, decoder head replacement)
- Include F1 scores and validation metrics from preliminary work
- Show the FM addresses specific solicitation emphasis on efficiency and scalability

---

## Engagement and Co-Development Strategies

### Community-Based Participatory Research (CBPR)

Used effectively in proposals involving tribal nations and underserved communities:

**Phase Structure**:
1. Partnership formation and trust building
2. Needs assessment and problem definition
3. Solution co-design and indicator review
4. Prototype development and testing
5. Collaborative evaluation
6. Capacity building and transition

**Key Elements**:
- **Sustained engagement**: Document years of prior interaction (not just pre-proposal meetings)
- **Institutional agreements**: MOUs signed with tribal councils or agency leadership
- **IRB protocols**: For interviews and surveys
- **Cultural sensitivity**: Data sovereignty, privacy preferences, consent processes
- **Training**: Embedded throughout, not just end-of-project handoff

### Stakeholder Engagement Framework

For government and institutional end users:

**Engagement Timeline**:
- **Phase 1** (Year 1): Structured interviews, workflow mapping, needs validation
- **Phase 2** (Year 1–2): Indicator review, dashboard co-design, prototype testing
- **Phase 3** (Year 2–3): Collaborative evaluation, tabletop exercises, training

**Engagement Methods**:
- Structured interviews with operational staff
- Workflow mapping to document baseline practices
- Tabletop exercises using retrospective events
- Scenario-based evaluations with operational narratives
- Workshops (quarterly meetings + annual in-person workshops)
- Feedback loops with versioned refinement logs

**Documentation**:
- Meeting summaries and decision logs
- Evaluation records linking feedback to system updates
- Training materials co-developed with end users
- User manuals and operational guides

---

## Figures and Visual Communication

### Required/Expected Figures

1. **Study Area Map**: Showing geographic context, end-user jurisdiction, key features
2. **Project Workflow/Architecture Diagram**: Data flow from EO inputs through processing to decision outputs
3. **Project Structure Diagram**: Components, working groups, and ARL progression
4. **Preliminary Results**: Demonstrating proof-of-concept and feasibility
5. **Engagement Framework**: Showing stakeholder interaction model
6. **Project Timeline**: Gantt chart or table with ARL milestones
7. **Conceptual Framework**: Showing the science-to-action pathway

### Figure Best Practices for NASA Proposals
- Include figure captions that are informative and self-contained
- Reference figures in text ("as shown in Figure X")
- Use consistent styling and color schemes
- Show real data (maps, model outputs, validation results)
- Include screenshots of dashboard/platform prototypes if available
- Number figures sequentially and reference them in order

---

## Reference Formatting

NASA ROSES does not mandate a specific citation style. Common practices:
- Numbered references in brackets [1], [2–3]
- Author-year in parentheses (Smith et al., 2024)
- Full reference list at the end of the S/T/M section
- Include DOIs for all published works
- Preprints acceptable (cite as arXiv with DOI)
- Include NASA technical reports and mission documentation

---

## Checklist: Before Submission

### Compliance
- [ ] Page limits respected (S/T/M, OSDMP, budget narrative)
- [ ] Formatting requirements met (font, margins, spacing)
- [ ] DAPR compliance (if applicable—no identifying information)
- [ ] All required sections included
- [ ] Budget and budget narrative complete for all institutions
- [ ] Table of Personnel and Work Effort included
- [ ] Letters of Support from end users and collaborators
- [ ] Current and Pending Support for all senior personnel
- [ ] Biographical Sketches for all key personnel

### Content Quality
- [ ] Decision-making activity clearly identified and described
- [ ] End user named with specific mandate and decision authority
- [ ] ARL starting and ending levels documented with evidence
- [ ] Measurable improvement metrics defined
- [ ] NASA EO assets clearly specified and justified
- [ ] Preliminary results demonstrating feasibility included
- [ ] Risks identified with structured mitigation strategies
- [ ] Transition plan addresses sustainability post-project
- [ ] ES2A alignment explicitly stated with Key Results
- [ ] Engagement timeline with methods described
- [ ] OSDMP complete with FAIR-compliant plans
- [ ] Budget aligns with proposed activities and timeline

### Strategic
- [ ] Program element priorities explicitly addressed
- [ ] Solicitation language quoted and mapped to project
- [ ] End-user letters confirm need, commitment, and adoption intent
- [ ] Team composition matches required expertise
- [ ] Prior NASA-funded work and partnerships referenced
- [ ] Inter-agency and inter-institutional coordination described
- [ ] Scalability argument made (both vertical and horizontal)

---

## Common Rejection Reasons

1. **Weak end-user engagement**: No documented partnership, vague stakeholder descriptions
2. **Unclear ARL progression**: No evidence for starting ARL or unrealistic advancement plan
3. **Missing decision context**: Science-focused without operational decision-making connection
4. **Insufficient preliminary results**: Claims of readiness without supporting evidence
5. **Vague transition plan**: No clear pathway to sustained use beyond project period
6. **Misalignment with program priorities**: Project doesn't match solicitation focus areas
7. **Overly ambitious scope**: Too much proposed for budget and timeline
8. **Weak risk mitigation**: Risks acknowledged but not adequately addressed
9. **Generic improvement claims**: No quantitative targets or measurable metrics
10. **DAPR violations**: Identifying information in anonymized sections

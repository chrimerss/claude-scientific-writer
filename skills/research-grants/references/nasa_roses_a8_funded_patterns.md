# NASA ROSES A.8 Water Resources Applications — Patterns from Funded Proposals

## Purpose and Scope

This reference distills recurring structural, rhetorical, and content patterns observed across the cohort of proposals that **advanced past the Science Mission Directorate (SMD) screening stage** for NASA ROSES-2025 A.8 Water Resources Applications (NNH25ZDA001N-WATER). Of 66 submitted final proposals in that cycle, roughly 14 abstracts passed initial SMD assessment and proceeded to programmatic, financial, and compliance review at the NASA Shared Services Center.

The synthesis is intended as a working blueprint when drafting NASA ROSES applied-science proposals — particularly A.8, but the same patterns transfer to A.9 (Foundation Models), A.36 (Earth Action), A.37 (Decision Support through Earth Science Research), and related applied program elements that share the Application Readiness Level (ARL) framework and Earth Science to Action (ES2A) strategy.

**How to use this file**:
- Consult **before drafting** an abstract or Decision-Making Activity (DMA) section.
- Cross-check **during a section-level rewrite** against the section-by-section patterns table.
- Run the **pre-submission checklist** at the end as a final gate before institutional review.
- Use the **failure-mode patterns** at the end to diagnose weak drafts.

For complementary guidance, also load:
- `nasa_guidelines.md` — structural rules, page-limit policy, DAPR, OSDMP requirements.
- `nasa_lessons_learned.md` — pitfalls and reviewer critique patterns from prior cycles.

---

## Part 1 — Twelve Recurring Traits in Funded A.8 Abstracts

The following patterns appear in **at least 10 of the 14** funded abstracts. Treat anything missing from your draft that appears here as a likely scoring weakness.

### Trait 1 — Named operational end-user with co-investigator (Co-I) status

Every funded abstract names at least one specific federal, state, tribal, or municipal agency as the operational end user. The strongest abstracts list **multiple end users across governance levels** (e.g., a Regional Forecast Center plus two state water management districts, or a state Department of Natural Resources plus a binational treaty commission).

**Pattern**:
- End users are funded or unfunded **Co-Is**, not just letter-of-support signatories.
- The end-user agency is the **decision-making authority** for the activity being supported (water-rights curtailment, reservoir release, drought declaration, treaty allocation, dam safety inspection).
- A specific named decision-making activity (DMA) is stated, often with its statutory or regulatory basis (e.g., "1944 U.S.–Mexico Water Treaty mandate," "Drought is declared when water supplies are below 75% of average").

**What to avoid**: Vague end users ("water managers," "stakeholders," "the broader community") with no governance authority over the decision being supported.

### Trait 2 — Explicit ARL start → ARL end trajectory

Every funded abstract states the **starting ARL with evidence** and the **ending ARL targeted by project completion**. Typical trajectories observed:

| Project Type | Typical Start ARL | Typical End ARL |
|---|---|---|
| Type 1 (lower-readiness, longer transition) | ARL 2 | ARL 5 |
| Type 1 (mid-stage prototype) | ARL 4 | ARL 7 |
| Type 2 (operationally focused) | ARL 5 | ARL 8 or 9 |

The funded abstracts consistently include phrases like:
- "starts at ARL 5, with an operational prototype already demonstrated for the region, and progresses through testing, validation, and institutional integration to ARL 8–9."
- "By project end, we will deliver a fully-sustainable suite of tools at ARL 9, run in both analysis and ensemble forecast mode."
- "advances from Application Readiness Level (ARL) 5 to 8, with operational adoption by [end user] at completion."

**What to avoid**: Stating an ARL with no evidence (no prior demonstration cited), or claiming ARL 8–9 from a starting point of ARL 3.

### Trait 3 — Co-development / co-design language

The verbs **"co-develop," "co-design," "co-production,"** and the noun phrase **"co-developed with end users"** appear in nearly every funded abstract. They are not buzzwords — they signal a specific reviewer-expected workflow:

- **Year 1**: Joint needs assessment with end users; agreement on product specifications.
- **Year 2**: Prototype evaluation with end users in the loop; iterative refinement.
- **Year 3**: Operational handoff; training; institutional integration; sustained use after project end.

**Recurring construction patterns** (paraphrased and anonymized):
- "We will co-develop and implement a set of decision-support tools that will mitigate…"
- "This crucial feedback will guide product refinement, training materials, and determine end-user adoption."
- "Regular meetings, workshops and user support will foster broad adoption, bridging treaty authority with community-level implementation."

### Trait 4 — Specific NASA Earth Observation (EO) assets named and matched to function

Funded abstracts almost never say "we will use NASA satellite data." Instead, they enumerate **specific missions with the specific variable each provides**, and frequently bundle assets across the hydrologic cycle. Most-cited assets across the 14 abstracts:

| Asset | Typical variable | Frequency |
|---|---|---|
| SMAP | Soil moisture | High |
| GRACE / GRACE-FO | Terrestrial water storage anomalies | Medium-High |
| SWOT | Surface water elevation / extent | High |
| GPM / IMERG | Precipitation | High |
| ECOSTRESS | Evapotranspiration / surface temperature | Medium |
| Landsat 8/9 (OLI) | Surface reflectance, irrigation mapping | High |
| MODIS (Terra/Aqua) | Snow cover, ET, long record extension | Medium-High |
| VIIRS (Suomi, NOAA20, NOAA21) | Snow cover, daily multi-overpass | Medium |
| Sentinel-1 (via NASA OPERA RTC) | Wet snow, SAR-derived water extent | Medium |
| NISAR | High-resolution soil moisture, SAR | Medium-High |
| OCI / PACE | Snow, vegetation indices | Low-Medium |
| EMIT | Hyperspectral validation | Low |
| MERRA-2 / GEOS-S2S-3 | Reanalysis / forecast | Medium |
| OpenET (NASA-supported partner) | Field-scale ET | Medium |
| NLDAS-3, LIS, SPoRT-LIS | Land surface model assimilation | High |

**Pattern**: A funded abstract typically names **4–8 distinct NASA assets**, paired with the specific decision improvement each enables. The strongest abstracts also note **mission-readiness alignment** (e.g., "NISAR — newest radar mission that will provide soil moisture at 100-meter resolution every 6–12 days") — demonstrating that the proposal leverages NASA's current investment portfolio.

### Trait 5 — Explicit ES2A strategy alignment with named Key Results

The Earth Science to Action (ES2A) strategy is referenced directly in nearly every funded abstract. The most precise abstracts cite **specific ES2A Objectives and Key Results** (e.g., "Key Results 1.3, 2.2, and 2.3" or "Objective 2: Deliver Trusted Information to Drive Earth Resilience Activities").

**Pattern**: Generic alignment ("supports NASA's mission") is not enough. Successful abstracts map their work to a named Objective and at least one Key Result, and connect each Key Result to a concrete project activity.

### Trait 6 — Co-located AI/ML and physics-based modeling

Roughly 11 of 14 funded abstracts integrate machine learning or AI with traditional physics-based hydrology. Common patterns:

- **Physics-informed ML / hybrid physics-AI**: ML model trained on physics-based simulations or constrained by physical laws (mass balance, water rights, environmental flow).
- **AI weather/climate models adopted as forcings**: GraphCast, Pangu-Weather, SFNO, Fuxi-S2S used as inputs to hydrologic models.
- **Deep learning for forecasting and downscaling**: LSTM, deep-learning super-resolution, ensemble learning for irrigation/snow/streamflow.
- **Trustworthy AI framing**: Bootstrap ensembles, spatial cross-validation, interpretability, uncertainty quantification.

Several abstracts also tie their AI work to the **White House AI Action Plan** or note "AI-Enabled Science" explicitly — a strong cue that program managers are receptive to AI framing in 2025–2026.

**What to avoid**: ML as a black box with no validation, no uncertainty estimate, and no physical constraint or interpretability mechanism.

### Trait 7 — Quantified problem framing in the opening paragraph

The first paragraph almost always anchors the problem with **concrete numbers**: population served, irrigated acreage, hydropower generated, dollars at risk, dams regulated, or flood frequency. Representative paraphrased openings:

- "[Region]'s [N] regulated reservoirs represent a critical opportunity for advancing water resilience, much like the >90,000 dams in the United States."
- "The Colorado River is a lifeline for over 40 million people. Water management in the [Basin] is increasingly constrained by drought, declining reservoir storage, and rising demand."
- "Groundwater from the Ogallala Aquifer supports millions of acres of irrigated crops in this region, yet decades of over-pumping combined with hotter, drier conditions are threatening long-term agricultural sustainability."

**Pattern**: Numbers establish that the decision being supported has high stakes. They prime the reviewer to weight ES2A and Broader Value scores favorably.

### Trait 8 — Three-phase project structure (Year 1 → Year 2 → Year 3)

The funded abstracts that include a timeline almost universally follow a three-phase structure:

- **Year 1** — Needs Assessment / Prototype: Joint user needs assessment, baseline benchmarking, initial algorithm development.
- **Year 2** — Scaling / Validation: Historical reprocessing or expanded regional coverage, validation against in situ data, iterative end-user evaluation.
- **Year 3** — Operational Deployment / Transition: Integration into end-user operational workflows, training, documentation, sustained operational support.

This maps cleanly to the ARL framework: needs assessment activities advance ARL 2 → 4; scaling and validation advance ARL 4 → 6; operational integration advances ARL 6 → 8/9.

### Trait 9 — Specific region + transferable framework dual-framing

Each funded abstract is rooted in a specific geographic region (Hampton Roads, the arid Southwest, Texas river basins, the Upper Mississippi 9-foot channel, the Upper Colorado, Hawaiian reservoirs, the Rio Grande, Washington State, California's Central Valley, the western U.S. AR corridor). At the same time, each frames the work as a **transferable model** for similar regions:

- "Hampton Roads will serve as a regional testbed for protecting communities, ports, military bases, and NASA facilities, while creating a transferable framework for other flood-prone U.S. coastal regions."
- "demonstrating a framework transferable to the 90,000 dams across the United States."
- "provides a scalable model for other transboundary basins worldwide."

**Pattern**: The specific region is what makes the partnership credible; the transferable framework is what justifies NASA-scale investment.

### Trait 10 — Multi-benefit / compound-hazard framing

Roughly half of the funded abstracts frame their work as addressing **multiple hazards or benefits simultaneously**:

- Compound flooding (rainfall + tides + surge + subsidence).
- Floods AND droughts (Managed Aquifer Recharge during high-flow events).
- Dam safety AND drought resilience AND wildfire protection AND irrigation.
- Drought monitoring AND low-flow / streamflow risk.

This framing helps the proposal address multiple solicitation priority topics and signals operational versatility.

### Trait 11 — Transition / sustainability plan in the abstract itself

Every funded abstract includes at least one sentence explicitly describing **post-project sustainability**. The transition plan is not deferred to a later section — it appears in the abstract. Recurring constructions:

- "Sustainability will be achieved through integration into existing State Climate Office and SE DEWS operational workflows in formats directly usable for drought assessment, monitoring, and communication."
- "the [tool] will be fully embedded in [agency]'s treaty allocation workflow and adopted by [bank] for evaluating water project investments, ensuring sustainability beyond the project lifetime."
- "with sustained operational support once tested and accepted within respective agencies."

### Trait 12 — Open Science deliverables (code, data, dashboards)

Funded abstracts increasingly specify **open-source deliverables** that are directly usable by water agencies:

- Python packages installable via `pip`.
- Cloud-based dashboards and web visualization tools.
- Open-access portals and data repositories.
- Documented APIs and ensemble products.
- Reusable training datasets and analysis-ready grids.

This pattern aligns with NASA's Open-Source Science Initiative (OSSI) and the OSDMP requirement.

---

## Part 2 — Section-by-Section Pattern Map

Use this table when drafting or auditing a NASA applied-science abstract or full S/T/M section.

| Section | Must-have element | Common pattern in funded abstracts |
|---|---|---|
| Opening / Problem framing | Quantified stakes, named region, decision-maker named | "[N] million people / [N] acres / >$[N]B in decisions" + named agency |
| Decision-Making Activity (DMA) | Specific decision, statutory or operational basis | Named agency, named statute or operational mandate, gap in current decision tools |
| Significance / Gap | Current decision tools' specific limitation | "fragmented," "self-reported," "outdated consumptive use estimates," "point-based measurements" |
| Approach overview | NASA assets named with function | 4–8 NASA missions/products listed with the variable each contributes |
| Innovation | What is new (algorithm, integration, scale, AI/physics fusion) | "first operational fusion of…," "physics-informed ML," "downscaled via deep-learning super-resolution" |
| ARL trajectory | Start ARL with evidence, end ARL with plan | Explicit start → end (e.g., "ARL 5 to 8") with milestones per year |
| Co-development plan | Named end user(s), workshops, dashboards, training | "co-develop," "co-design," workshops in Year 2/3, dashboards in formats agencies use |
| Validation | In-situ comparison, multiple independent sources | Flux towers, soil moisture probes, gauge records, meter databases, ASO, pumping data |
| Risk / uncertainty | Quantitative uncertainty, alternatives, contingency | Bootstrap ensembles, spatial cross-validation, "if X fails, we fall back to Y" |
| Transition plan | Operational handoff, sustainability, ongoing use | "embedded in [agency] workflow," "sustained operational support," "institutional integration" |
| ES2A alignment | Objective + Key Result mapped to activities | Direct quote of Key Result number, tied to specific Year-N activity |
| Broader value | Transferable framework, scale-out potential | "scalable to [other regions]," "framework transferable to [larger universe]" |

---

## Part 3 — Language and Framing Patterns

### Verbs that recur in funded openings
- "co-develop," "co-design," "co-produce"
- "translate" (NASA EO into decision-ready information)
- "transition" (from ARL X to Y)
- "operationalize," "integrate," "embed"
- "benchmark," "validate," "evaluate"
- "advance" (an ARL or a capability)

### Phrases that signal applied-program fit
- "Earth Science to Action" / "ES2A Key Result [N.N]"
- "decision-support tool / system / framework / platform / dashboard"
- "actionable / decision-ready / operationally relevant"
- "co-developed with end users"
- "transition plan" / "sustained operational use" / "beyond the project lifetime"
- "Application Readiness Level (ARL) X to Y"
- "NASA Earth Observations (EO)"

### Phrases to avoid (signal Research-program fit, not Applied)
- "fundamental understanding of…" (without a paired decision)
- "novel method for…" (without a paired end user)
- "first study of…" (without a paired decision)
- "stakeholders" used as a substitute for a named end user
- "potential users" or "future end users" (Applied programs require committed, named end users)

### Structural openings that work
- **The Resource-at-Stake opening**: Lead with the resource (river, aquifer, reservoir system, basin) and quantify its scale, then state the management decision under stress.
- **The Hazard-Volatility opening**: Lead with the hazard regime (flood, drought, compound, AR clustering) and quantify economic or human cost, then state the decision-support gap.
- **The Critical-Infrastructure opening**: Lead with the asset class (dams, navigation locks, levees, military installations) and quantify the inventory, then state the safety or operations decision.

### Structural closings that work
- **The Transferable-Testbed closing**: Specific region serves as testbed; the framework generalizes to a much larger population.
- **The Embedded-in-Workflow closing**: At project end, the tool is part of the named agency's standard operating procedure.
- **The ES2A-Realization closing**: The work explicitly realizes ES2A by turning NASA assets into trusted, sustained decisions.

---

## Part 4 — NASA EO Asset Selection Matrix

Match the variable your DMA needs to the NASA mission most reviewers expect you to name.

| If you need… | Strongest asset(s) | Often paired with |
|---|---|---|
| Soil moisture (surface) | SMAP, NISAR | NLDAS-3, SPoRT-LIS |
| Soil moisture (high-resolution, 6–12 day revisit) | NISAR | SMAP for cross-calibration |
| Terrestrial water storage / groundwater anomaly | GRACE, GRACE-FO | In situ wells |
| Surface water elevation | SWOT | USGS / OPERA gauges |
| Precipitation | GPM, IMERG | In situ gauges, MRMS |
| Evapotranspiration | ECOSTRESS, OpenET | Flux towers |
| Snow cover / snow water equivalent | MODIS, VIIRS, Landsat (high-res), Sentinel-1 (OPERA RTC) | ASO, SNOTEL, in situ |
| Wet snow / snowmelt onset | Sentinel-1 (OPERA RTC), VIIRS | NISAR, in situ |
| Irrigated area / land use | Landsat 8/9, Sentinel-2 | OpenET, in situ irrigation status |
| Land surface temperature | ECOSTRESS | MODIS for record extension |
| Hyperspectral validation | EMIT | PACE / OCI |
| Reanalysis / forcing | MERRA-2 | NLDAS-3 |
| Subseasonal forecasts | GEOS-S2S-3 | IFS, NMME, AI weather models |
| Vegetation / aerosols | PACE, OCI | MODIS |

**Pairing rule**: NASA assets should appear in **input-validation-product** triplets. For example: "We will train a deep-learning forecast model with SMAP and NISAR (inputs), validate against in situ soil moisture probes and flux towers (validation), and deliver a basin-level low-flow forecast at 3 km resolution (product)."

---

## Part 5 — Type 1 vs Type 2 Decision Tree

A.8 distinguishes Type 1 (research-leaning, lower starting ARL) from Type 2 (operations-leaning, higher starting ARL). The funded cohort suggests:

**Choose Type 1 if**:
- Starting ARL is 2–4 (analytical proof-of-concept demonstrated, but no relevant-environment demonstration yet).
- End-user partnership is committed but new.
- Algorithm or product is novel and needs benchmarking before deployment.
- Three-year path to ARL 5 is realistic.

**Choose Type 2 if**:
- Starting ARL is 5–6 (relevant-environment prototype already demonstrated).
- End-user partnership has multi-year history (prior NASA, agency, or co-authored publications).
- Goal is operational adoption (ARL 8–9) within the project period.
- Sustained institutional support is documented (cost-share, formal partnership letters).

**Common mistakes**:
- Submitting Type 2 with no prior NASA-funded heritage demonstrating ARL 5+.
- Submitting Type 1 when a prior project already advanced the work to ARL 5 (reviewers will see the lower ARL claim as inconsistent with the cited heritage).

---

## Part 6 — Pre-Submission Checklist (A.8 / Applied NASA ROSES)

Run this checklist before institutional review. Each unchecked item is a likely scoring deduction.

**Decision-Making Activity (DMA)**
- [ ] At least one named federal/state/tribal/municipal agency identified as primary end user.
- [ ] End user holds a Co-I role (funded or unfunded) — not just letter-of-support.
- [ ] Statutory or operational mandate for the decision is named.
- [ ] Current decision-tool limitation is specific and documented (not generic).

**ARL Trajectory**
- [ ] Starting ARL stated **with evidence** (prior demonstration, published validation, prior NASA award).
- [ ] Ending ARL stated **with plan** (which milestones advance which ARL step).
- [ ] Type 1 vs Type 2 classification matches the ARL trajectory.

**NASA EO Assets**
- [ ] At least 4 specific NASA missions or products named.
- [ ] Each asset is paired with the variable it contributes.
- [ ] Input-validation-product triplet is explicit.
- [ ] At least one current or forthcoming NASA mission (e.g., NISAR, SWOT, PACE) is leveraged where relevant.

**ES2A Alignment**
- [ ] Named ES2A Objective is cited.
- [ ] At least one named Key Result (e.g., "Key Result 2.2") is mapped to a specific project activity.

**Co-Development**
- [ ] The verb "co-develop" or equivalent appears.
- [ ] Workshops, training, or iterative feedback loops are described.
- [ ] Dashboard, portal, or other operational delivery format is specified.

**AI / ML (if used)**
- [ ] AI/ML approach is described, not just named.
- [ ] Physical constraint or interpretability mechanism is included.
- [ ] Uncertainty quantification approach is specified.
- [ ] Validation against in situ or operational reference is planned.

**Transition Plan**
- [ ] Post-project sustainability mechanism named.
- [ ] Institutional integration pathway described (workflow, software repository, cloud handoff).
- [ ] Training and documentation are included in scope.

**Transferability**
- [ ] Specific region is named.
- [ ] Larger universe of regions/users to which the work transfers is named.
- [ ] Mechanism of transfer (open-source release, replicable framework) is stated.

**Open Science**
- [ ] OSDMP requirement addressed.
- [ ] Code, data, and documentation release plan stated.
- [ ] License and repository identified.

**Problem Framing**
- [ ] Opening paragraph contains at least one quantitative stake (population, acreage, dollars, infrastructure inventory).
- [ ] Compound or multi-benefit framing applied where relevant.
- [ ] Solicitation priority topic explicitly named.

---

## Part 7 — Failure-Mode Patterns to Diagnose Weak Drafts

If your draft lacks competitive features, the issue is usually one of the following:

1. **Missing operational decision**: The draft describes a scientific question or product but never says **what decision** the product will inform, **who** makes that decision, or **how** the decision changes once the product is delivered. Fix: identify a named decision, named decision-maker, and the delta in the decision under the new product.

2. **Generic end user**: The draft references "water managers" or "stakeholders" but no specific agency, person, or governance body. Fix: name the agency, name the role (PI, Co-I), name the decision they hold authority over.

3. **ARL stated without evidence**: The draft claims "we will advance from ARL 5 to 8" but does not cite the prior demonstration, publication, or NASA-funded heritage that justifies the ARL 5 start. Fix: cite the evidence inline.

4. **NASA assets as wallpaper**: The draft lists NASA missions in a paragraph but does not pair each with a function or validation source. Fix: rewrite as input-validation-product triplets.

5. **AI as a black box**: The draft says "we will use machine learning" with no architecture, no training data, no validation, no uncertainty. Fix: name the architecture (LSTM, U-Net, transformer, physics-informed neural network), the training data, the validation set, and the uncertainty estimate.

6. **No transition plan in the abstract**: The draft defers sustainability to a later section. Fix: include at least one sentence in the abstract describing operational handoff.

7. **No region or only a region**: Either the draft is so generic it could apply anywhere (no operational credibility) or so regional it has no scale-out value (no NASA-scale investment justification). Fix: name a specific region AND name the transferable framework.

8. **ES2A alignment is generic**: The draft says "supports NASA's mission" or "aligns with Earth Science to Action" without citing a specific Objective or Key Result. Fix: cite the specific Key Result number and map it to a project activity.

9. **Type 1 / Type 2 mismatch**: The draft is labeled Type 2 but the trajectory and prior heritage match Type 1, or vice versa. Fix: re-read the solicitation's Type definitions and reclassify if needed before submission.

10. **No quantified stakes**: The opening paragraph asserts importance without numbers. Fix: anchor the opening in a number (population, dollars, acres, dams, megawatts, miles of channel).

---

## Part 8 — Worked Anonymous Template for a Strong A.8 Abstract

Use this as a structural scaffold. Fill the bracketed elements with your project specifics.

> **[Resource at stake or Hazard regime — 1 sentence with a quantified stake]**. [Specific operational decision] is currently constrained by [specific limitation of current decision tools — point data, fragmented sources, outdated estimates, sparse in situ measurements]. [Current end-user-level consequence — slower decisions, less accurate allocations, missed early warnings, increased risk to people/assets].
>
> We propose to co-develop a [Type 1 / Type 2] decision-support [tool / system / framework / dashboard] with [Named End User 1, Named End User 2, Named End User 3] to [specific decision improvement]. The proposed system integrates [NASA Asset 1] for [variable], [NASA Asset 2] for [variable], [NASA Asset 3] for [variable], and [NASA Asset 4] for [variable], with [physics-based model / hybrid physics-AI framework / deep learning architecture] and validation against [in situ source 1, in situ source 2, operational reference].
>
> The project begins at Application Readiness Level (ARL) [N], demonstrated by [prior heritage — prior NASA project, prior publication, prior operational use], and will advance to ARL [M] through three phases: **Year 1** — [needs assessment and prototype]; **Year 2** — [scaling, historical reprocessing, validation]; **Year 3** — [operational deployment, training, institutional integration with end-user workflow]. [Trustworthy AI / uncertainty quantification mechanism] will be applied throughout.
>
> Sustainability will be achieved through [specific handoff: agency cloud deployment, integration into agency reporting workflow, embedding in operational forecast platform]. Open-source deliverables include [Python package, web dashboard, public data portal]. The work directly addresses ES2A Objective [N] and Key Result [N.N] by [specific mechanism], and addresses the solicitation priority topic "[verbatim priority topic name]." [Specific region] serves as a testbed for a framework transferable to [larger universe of regions/users].

---

## Part 9 — How This File Was Built

This reference was synthesized by reading every abstract in the publicly released list of NASA ROSES A.8 Water Resources Applications proposals (NNH25ZDA001N-WATER) that passed SMD-screening review and proceeded to programmatic/financial/compliance review. Of 66 final proposals submitted to the call, the cohort analyzed here represents the subset that advanced past initial science merit review.

Patterns were extracted by tagging each abstract for: ARL trajectory, end-user identification, NASA EO asset enumeration, ES2A alignment, co-development language, AI/ML integration, geographic framing, multi-hazard framing, transition plan, and open-science deliverables. Patterns appearing in ≥10 of the 14 abstracts were promoted to "Trait" status (Part 1). Patterns appearing in 6–9 abstracts were treated as section-level conventions (Part 2). Lower-frequency but high-signal patterns were retained as language conventions (Part 3) or asset-selection guidance (Part 4).

No proposer names or institutional affiliations are reproduced here. All language patterns shown are paraphrased and anonymized.

---

**Companion files**:
- `nasa_guidelines.md` — structural rules, page limits, DAPR, OSDMP requirements.
- `nasa_lessons_learned.md` — section-by-section reviewer critique patterns and Socratic self-review prompts.
- `specific_aims_guide.md` — for NIH-style aims when adapting for non-NASA programs.
- `broader_impacts.md` — NSF Broader Impacts framing (note: NASA Applied programs equivalent is Decision-Making Relevance + Broader Value).

# Section Moves

Sentence-by-sentence templates, each anchored to verbatim text from the six source papers.
Quoted blocks are the author's own published prose.

---

## Abstract

Five moves, in this order. Total 150–200 words.

1. **Importance**, stated flatly, usually with a superlative or a share of the population.
2. **However / Although: the gap**, one sentence.
3. **Here we / We assessed: what was done**, naming models and resolution.
4. **Results as numbers**, global first, then the worst region, then the trend.
5. **Call to action or implication.**

> Flash floods are largely driven by high rainfall rates in convective storms that are
> projected to increase in frequency and intensity in a warmer climate in the future.
> **However,** quantifying the changes in future flood flashiness is challenging due to the
> lack of high-resolution climate simulations. **Here we use** outputs from a continental
> convective-permitting numerical weather model at 4-km and hourly resolution and force a
> numerical hydrologic model at a continental scale to depict such change. **As results
> indicate,** US floods are becoming 7.9% flashier by the end of the century assuming a
> high-emissions scenario. The Southwest (+10.5%) has the greatest increase in flashiness
> among historical flash flood hot spots, and the central US (+8.6%) is emerging as a new
> flash flood hot spot. Additionally, future flash flood-prone frontiers are advancing
> northwards. **This study calls on** implementing climate-resilient mitigation measures for
> emerging flash flood hot spots.

Same five moves, different domain:

> Rice serves as a staple food for over half of the world's population. **Although** the
> reduction of rice yields by droughts is well known, when flooding fully submerges rice
> plants for over 1 week, crops cannot survive. **Considering rice growth stages, using** a
> flood dynamics model and difference-in-differences, **we assessed** the causal impact of
> rice crop submergence on yield losses from 1980 to 2015. **Globally,** these floods reduce
> annual rice yield by 4.3%, with China's East Coast experiencing 14% losses. Since 2000,
> yield losses have increased due to more frequent extreme floods, a trend anticipated to
> continue. **Our findings highlight the need for** flood-resistant rice cultivars …

When the paper is a review, move 3 becomes the corpus description and move 4 becomes the
enumerated set of directions:

> Through an analysis of publications from 1970 to 2023, this review provides a foundational
> understanding of state-of-the-science flood model developments. … The most ambitious
> research directions are those that involve coupling flood models with models in diverse
> fields and involve: (1) atmospheric sciences …, (2) epidemiology …, (3) economics …

**Abstract checklist:** at least three numerals · exactly one `However`/`Although` pivot ·
zero dashes · final sentence names an action or a user.

---

## Plain-language summary (AGU / EGU style)

Shorter sentences than the abstract. Mean ~18 words. No acronyms after first definition.
Uses `how often` and `how long` in place of frequency and duration.

> Flash floods are among the most devastating natural hazard types that can cause severe
> property damage and loss of life. However, it's challenging to measure and quantify the
> severity. This study proposes a new way of quantifying flash flood intensity using a newly
> developed Flashiness-Intensity-Duration-Frequency (F-IDF) curve. It links flash flood
> severity with how often they happen and how long they last. We mapped F-IDF values across
> the United States and found that certain areas are more prone to flash floods than others.
> … This new quantification tool can help experts better identify and respond to flash flood
> risks.

---

## Introduction

Five paragraphs is the standard shape.

### P1. The hazard, sized

Sentence 1 is a superlative. Sentence 2 is money and lives with a date range. Sentence 3
narrows to the subset this paper addresses. Optionally close on the framing question.

> Floods in the United States are the most devastating water-related natural hazards.
> According to the National Weather Service storm reports, floods have cost more than 159
> billion US dollars and 2000 fatalities from 1996 to 2020, let alone immeasurable damage to
> ecosystems. Among all types of floods, flash floods are one of the most devastating
> subsets, accounting for nearly half of those economic losses. The central question for the
> hydrologic science community, practitioners, and more urgently the weather service agencies
> becomes: How do future floods evolve under a changing climate?

Variants of the opening sentence, all of which work:

- `Floods are one of the most devastating and deadliest natural hazards across the globe.`
- `Flooding stands as one of the world's most devastating natural hazards, accounting for
  lost lives, economic damage, and ecosystem degradation.`
- `Weather radars have deepened our understanding of precipitation microphysics, improved
  quantitative precipitation estimates, and severe weather forecasts and warnings.`

### P2. Mechanism and why existing tools fall short

State the physical control, then the theoretical expectation, then why the standard tool
cannot see it. `In contrast,` introduces the better tool.

> Although the Clausius-Clapeyron equation infers a theoretical 7% increase in atmospheric
> water holding capacity per degree Celsius warming, extreme precipitation might be
> increasing even more due to changes in storm structure, storm dynamics, and large-scale
> weather patterns. Global Climate Models (GCMs), which are mainly designed for simulating
> large-scale climate variables, poorly represent mesoscale weather systems because of their
> coarse resolutions (>10 km) and insufficient parameterization schemes. … **In contrast,**
> convection-permitting models that operate at kilometer-scale grid spacing start to resolve
> convective processes …

### P3. Taxonomy of prior approaches

Announce that you are classifying, then classify. `We generalize them into A and B
approaches.` Give each a sentence of definition, an example, a strength, and a limitation.
Close each with a short verdict sentence.

> We generalize them into event-dependent and event-independent approaches. An event-dependent
> approach directly calculates flash flood risks based on archived flash flood events or a
> flashiness index. … Since it is event-dependent, this approach presumably delivers accurate
> and precise results. **Alternatively,** an event-independent approach seeks a statistical
> model that relates climate variables and basin physiography to flash flood risks. In doing
> so, this approach bypasses the requirement for observations, which is particularly useful in
> ungauged basins or rural regions. **Its validity, however, requires particular attention.**

### P4. Enumerated gap

The signature move. Announce the count, then `First / Second / Third`.

> Despite these well-studied impacts, large-scale assessments of flood-related rice crop loss
> remain underexplored, especially compared to drought impacts. **We hypothesize three reasons
> for this research gap. First,** floods are typically restricted to rice fields, driven by
> topographic variations, making correlations between local flood occurrences and national
> yield data less apparent. **Second,** rice, as a semi-aquatic crop, exhibits some flood
> resilience and tolerance of submergence for 3 to 4 days—a tolerance it lacks under drought
> conditions. **Third,** no clear criteria exist to define a "rice-killing" flood, limiting
> consistency across studies.

### P5. The closing move: goal, then objectives, then implication

**This is the most reliable structural habit in the author's introductions. Every paper does
it.** The final paragraph runs three moves, always in this order, and the introduction is not
finished until all three are on the page.

```
[G] Overarching goal.   One sentence. What this study is for, stated at the highest level.
                        Optionally preceded by the setup: the model, domain, period, resolution.
[O] Objectives.         The goal decomposed into 2–4 concrete, verb-led tasks.
                        Lettered (a)(b)(c) with semicolons, or First/Second/Third, or a
                        compact "we X … and Y …" pair.
[I] Implication.        One sentence naming who uses the result and for what decision.
                        This is the last sentence of the introduction.
```

Set the goal up with `Here, we define …`, `In this study, …`, `Taking advantage of …, we
quantify …`, or `Given …, we propose …`. Name the model, the domain, the period, and the
resolution before or inside the goal sentence.

#### Fully lettered objectives (GRL)

> **[G]** Hence, we introduce the Flashiness-Intensity-Duration-Frequency (F-IDF) curve for the
> first time. … **[O] The aim of this article is threefold:** (a) introducing the methods of
> calculating a F-IDF curve; (b) mapping F-IDF values for all US stream gages; and (c)
> investigating geographical and hydrometeorological factors associated with F-IDF values.
> **[I]** The newly introduced F-IDF curve can be applied to observed or simulated hydrographs,
> meaning that it can be integrated into any flood forecast system.

#### Compact paired objectives (Science Advances)

> **[G] In doing so, we quantify** the effects of rice-killing floods on rice yields in major
> rice-growing regions **[O] and identify** vulnerable regions whose rice productions are
> susceptible to floods. **[I] The results of this study can inform** stakeholders and
> decision-makers' plans to mitigate flood losses and adapt agriculture to climate extremes.

#### Goal split across two sentences (Communications Earth & Environment)

> **[G] Taking advantage of the benefits of convection-permitting models, we quantify** the
> impacts of climate change on future flood flashiness changes over the conterminous US
> (CONUS), **[O] which conveys information such as flood hazards, exposure, vulnerability, and
> impacts in the future.** … **[G′] This study hopes to provide quantitative assessments on**
> changes in future flood-producing storms and flood flashiness, including geographical shifts
> in flash flood hotspots. **[I] It can be served as a basis for** adapting nationwide flash
> flood planning strategies **and calls on** implementing climate-resilient mitigation measures
> for emerging flash flood hotspots.

#### Goal and implication in one sentence (BAMS)

> **[G] The goal of this study is to examine** the systematic differences of radar reflectivity
> between the NOAA WSR-88D network and the NASA–JAXA DPR **[I] and to draw attention to**
> radar-application users in recognizing their differences.

#### Review articles: objectives become the section roadmap

For reviews the objectives move is realized as an ordered walk through the sections, but the
goal and implication sentences still bracket it.

> **[G]** As the CREST model was announced in 2011, we review the development of CREST and its
> applications to water-related issues over the past decade in the following sections. … **[O]**
> In the following sections, we follow the chronological order and focus on the model core,
> which is the main package to reveal the relative changes to the source. **At last,** we
> summarize the limitations and provide outlooks for the CREST model family in terms of new
> components to be considered for development.

> **[O]** The remainder of section 1 provides context … Section 2 briefly provides flood-type
> terminology … Section 3 discusses the recent advances in flood inundation models. … **[I]**
> Section 6 identifies three frontier topic areas for which research progress would be
> difficult but represents ambitious steps forward in flood-inundation modeling.

#### Sentence stems for each move

**Goal.** `The goal of this study is to …` · `This study hopes to provide …` ·
`In doing so, we quantify …` · `Taking advantage of …, we quantify …` ·
`Hence, we introduce … for the first time.` · `Given …, we propose a new method using …` ·
`we review the development of … in the following sections`

**Objectives.** `The aim of this article is threefold: (a) …; (b) …; and (c) ….` ·
`we quantify … and identify …` · `First, … Second, … Third, …` ·
`In the following sections, we … At last, we …`

**Implication.** `The results of this study can inform stakeholders and decision-makers' plans
to …` · `It can be served as a basis for adapting …` · `and calls on implementing …` ·
`meaning that it can be integrated into any …` · `and to draw attention to … users in
recognizing …` · `in the hope of stimulating new research endeavors`

#### Common failure modes

- Stopping after the objectives. An introduction that ends on `(c) investigating …` is
  unfinished. The implication sentence is mandatory.
- Merging goal and objectives into one long sentence. Keep the goal at a higher level than
  the objectives it decomposes into. If they read at the same altitude, the goal is too narrow.
- Listing more than four objectives. Three is the norm; four is the ceiling.
- Writing the implication as a restatement of the results. It names a **user** and a
  **decision**, not a finding.
- Objectives that are not verb-led. Use gerunds (`introducing`, `mapping`, `investigating`) or
  first-person verbs (`we quantify`, `we identify`), consistently within one list.

---

## Results

Lead each paragraph with the finding, not the method. Attach magnitude to place immediately.
Escalate: global → national → regional worst case.

> Globally, these devastating floods reduce annual rice yield by an average of 4.3% (Fig. 3).
> In major rice-producing countries of China and India, yield losses are even more pronounced,
> at 5.3 and 6.4%, respectively, corresponding to production losses of 10 million and 5 million
> tonnes or 5 and 4% of national production. In specific regions, such as the China East Coast,
> yield losses can reach up to 14% (Fig. 3A).

Report statistics inline with interpretation attached in the same sentence:

> The analysis reveals a significant negative correlation (r = −0.5, P < 0.05), indicating
> that reductions in rice yield are strongly associated with increased economic losses.

---

## Discussion

### D1. Agreement with the literature

> This study conveys some similar conclusions found in other studies. For instance, decreasing
> trends in the duration of extreme rainfall and floods has been widely reported using either
> historical observations or climate simulations. … **However,** disagreements in streamflow
> responses to these precipitation changes are found across studies.

### D2. Why our results differ, enumerated

Never defensive. Attribute the difference to specific design choices, in order.

> Our results differ from some other simulations regarding flood magnitudes because **firstly**
> we use the high-end emissions scenario, RCP8.5, that dramatically warms and invigorates the
> atmosphere. **Second,** unlike both dynamic and thermodynamic evolution of weather patterns
> in GCMs, our PGW scheme only permits investigation of the less uncertain component of
> thermodynamic changes to the atmosphere. **Third,** the hourly and 4-km resolution model
> simulations resolve convective-scale weather phenomena that are only parameterized in GCMs.

### D3. The exception paragraph

Where results run counter to expectation, say so plainly and offer one physical explanation.

> Although our results demonstrate that rice-killing floods overwhelmingly reduce rice yields
> across most global river basins where rice is grown, there are notable exceptions where
> floods appear to enhance rice yields. … **A plausible explanation for this phenomenon is**
> the high evaporative demand in these regions.

### D4. Sensitivity and robustness

State what was varied, over what range, and what happened. Report the null result honestly.

> To rigorously assess the robustness of our causal findings, we conducted additional
> sensitivity analyses by reestimating the DiD model under varying thresholds for flood depth
> and duration. … Results show that yield loss increases as the flood depth approaches the crop
> height … but levels off at a minimum once the crop is fully submerged.

---

## Limitations

Concede in the first sentence, then enumerate. Close by reframing the limitation as a bound,
not a defect.

> **This work by no means intends to deliver an exhaustive depiction of future floods.** The
> PGW approach is based on a high-end emissions scenario, which may or may not be realized in
> the future. Furthermore, anthropogenic impacts such as Land Use Land Cover type changes and
> river regulations are not considered in the modeling settings. … **Therefore, our results
> could serve as a basis or benchmark if not the worst-case scenario.**

Alternative opener with explicit enumeration:

> There are some uncertainties in our quantification of yield loss that warrant further
> exploration. **First,** … **Second,** we cannot account for postflood replantation. …
> **Last,** our study focuses solely on physiological damage to rice crops …

---

## Conclusions

Restate what the paper introduced in one sentence. Give the scale of what was done. Then the
numbered findings. Then one forward-looking sentence naming the next study.

> This article introduces the F-IDF curve to quantify the intensity, duration, and frequency of
> flash floods adopting a similar concept of the R-IDF curve. The F-IDF curves are quantified
> for 3,722 US stream gages. … The conclusions are drawn as follows:
>
> 1. F-IDF curves are capable of revealing the spatial variability of flashy basins across the
>    US and the following places are identified as flash-flood-prone regions: …
> 2. The flash flood events in the US are predominately triggered by extreme rainfall. …
>
> Similar to flood studies, predicting flashiness values in ungauged basins is a grand challenge
> that warrants scientific exploration. **We plan to integrate F-IDF curves into flash flood
> forecast models over the US and beyond in a future work.**

---

## Review-article outlook sections

Numbered directions, each with a bolded imperative headline, then a paragraph of justification.

> **Direction 1. Focus on understudied flood types and compound flooding impacts:** Despite
> significant advances in flood modeling for major types such as fluvial, pluvial, and coastal
> flooding, several flood types and complex interactions remain understudied. …
>
> **Direction 2. Development of AI flood models that incorporate physics and provides
> out-of-sample validation:** The emergence of surrogate models using AI is well underway …

The section may open with a question addressed to the reader. This is the one rhetorical
question the voice permits outside the introduction:

> What does this review suggest as promising directions for future flood modeling research?

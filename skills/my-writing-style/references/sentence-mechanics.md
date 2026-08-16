# Sentence Mechanics

Operational rules for reproducing the measured rhythm. Read `SKILL.md` §1 and §3 first.

---

## 1. Length control

The corpus distribution to reproduce (397 sentences):

```
 ≤10 words   5.6%   ▍
11–20 words  36.9%  ██████████████
21–30 words  38.4%  ███████████████
31–40 words  14.9%  ██████
 >40 words    4.3%  ▍
```

Two consequences:

- **Roughly two sentences in five are short (≤20 words).** A paragraph of five sentences
  should contain at least two of them. Drafts that read "off" are usually drafts where every
  sentence landed in the 25–35 band.
- **Variation carries the rhythm, not length.** Follow a 30-word evidence sentence with a
  12-word consequence sentence. The author does this constantly:

  > Systematic differences in reflectivity are found, with ground radar reflectivity on
  > average 2.4 dB smaller than that of the DPR. *(21 w)*
  > … Further investigation into understanding and alleviating the systematic bias between
  > the two platforms is needed. *(17 w)*

### Splitting procedure

When a sentence exceeds 35 words:

1. Find the highest-level connective (`and`, `but`, `while`, `which`, `because`, `so that`).
2. Cut there.
3. Promote the connective to a sentence-initial adverbial: `However,` `Therefore,`
   `In contrast,` `As such,` `Additionally,`.
4. If the second half now lacks a subject, repeat the noun rather than using a pronoun.

Do **not** split by inserting a semicolon. See §3.

---

## 2. Clause budget

| Pattern | Allowed |
|---|---|
| Main clause only | Always — aim for ~1 in 3 sentences |
| Leading subordinate + main | Yes, ~1 in 5 sentences (`Although …, we …`) |
| Main + one trailing relative | Yes, sparingly |
| Leading subordinate + main + trailing relative | **No** |
| Two stacked `which` clauses | **No** |
| Main + `, which …, which …` | **No** |

Measured subordinator use, per sentence: `that` 0.21, `as` 0.20, `which` 0.06, everything
else below 0.03. So: `that` and `as` are natural; `which` is a special occasion; `whereas`,
`whilst`, `insofar as` are foreign to this voice.

### Preferred simplification moves

| Complex | Simple |
|---|---|
| `X, which is defined as Y, was applied` | `X is defined as Y. We applied it to …` |
| `Because A, B, and therefore C` | `A. Therefore, B and C.` |
| `It is worth noting that X` | `Notably, X.` or just `X.` |
| `There are several studies that show X` | `Several studies show X.` |
| `In order to quantify` | `To quantify` |
| `Due to the fact that` | `Because` |

---

## 3. Punctuation

**Em/en dash.** Budget: ≤ 1 per 500 words, ≤ 2 per section, ≤ 1 per paragraph. Only the
paired appositive form. See `SKILL.md` §1.

Worked rewrites:

> ✗ `The PGW approach is based on a high-end emissions scenario — RCP8.5 — which may or may
> not be realized.`
> ✓ `The PGW approach is based on a high-end emissions scenario, RCP8.5. This scenario may or
> may not be realized.`

> ✗ `Three factors drive the discrepancy — calibration, attenuation, and scattering volume.`
> ✓ `Three factors drive the discrepancy: calibration, attenuation, and scattering volume.`

> ✓ *(keep — paired appositive defining a newly named term)*
> `We introduce the Flashiness-Intensity-Duration-Frequency (F-IDF) curve—a three-dimensional
> description of a flash flood event—for the first time.`

**Semicolon.** Only inside a lettered enumeration:

> `It is found that (a) the return periods of flash flood events are highly associated with
> the return periods of rainfall events; (b) climatological precipitation amounts exhibit the
> most positive correlation with flashiness; and (c) correlation of flashiness with basin
> attributes decreases with increasing return periods.`

Never `Clause one; clause two.` Use a period.

**Parentheses.** Frequent and welcome — about 12 per 1,000 words. They carry:

- acronym definitions on first use: `Coupled Routing and Excess STorage (CREST)`
- signed magnitudes attached to regions: `the Southwest (+10.5%)`, `the central US (+8.6%)`
- statistics: `(r = −0.5, P < 0.05)`, `(fig. S5A)`
- resolution and unit qualifiers: `(roughly 25 km at the Equator)`

**Colon.** Use for the threefold aim, for lists, and to open an enumerated direction.
This is the correct replacement for most tempting dashes.

**Comma.** One or two per sentence. About a third of sentences carry none. Three or more is
a rewrite signal.

---

## 4. Voice and agency

Default to `we` for anything the authors chose to do:

> `We aggregate our results to 17 homogeneous climate regions …`
> `We generalize them into event-dependent and event-independent approaches.`
> `We collected those papers through the keyword search and applied manual inspection …`

Use passive only where the agent is genuinely irrelevant or is the data itself:

> `Systematic differences in reflectivity are found …`
> `The F-IDF curves are quantified for 3,722 US stream gages.`

Avoid `It is worth noting that`, `It should be emphasized that`, `It can be seen that`.
The author's own equivalents are shorter: `It is noteworthy that`, `Notably`, `To be noted`.
Prefer deleting them entirely.

---

## 5. Numbers

- Give a percentage whenever a change is claimed. `7.9% flashier`, `4.3%`, `14% losses`,
  `2.4 dB`, `reduced by an average of 70%`.
- Attach numbers to named places, not to abstractions.
- Give the date range with the number: `from 1996 to 2020`, `during 2000–2019`,
  `from 1980 to 2015`.
- Spell resolution explicitly: `4-km and hourly`, `0.25° (roughly 25 km at the Equator)`,
  `1 km and 10 min`.
- Round in the abstract, keep precision in results.

---

## 6. Rhythm template for a body paragraph

```
[1] Flat topic claim.                             12–18 w, no comma
[2] Mechanism or prior support.                   22–30 w, one subordinate clause
[3] The number.                                   18–26 w, parenthetical magnitude
[4] However / In contrast, the qualification.     18–28 w
[5] Consequence, naming who acts.                 12–20 w
```

Worked example built to the template (median 21 w, no dash, no semicolon):

> Groundwater flooding remains one of the most underrepresented flood types in inundation
> modeling research. It is driven jointly by land subsidence and sea-level rise, processes that
> operate on decadal time scales and are rarely resolved in event-based simulations. Fewer than
> 5% of the 336 reviewed studies address it directly, compared with the 61% that treat fluvial
> flooding (Fig. 4). However, its importance is growing as coastal aquifers respond to continued
> extraction and to rising sea levels along subsiding deltas. Coupled subsidence-hydrology
> models would give coastal planners a defensible basis for long-term zoning decisions.

Note the shape: sentence 1 carries no comma, sentence 2 carries the only subordinate clause,
sentence 3 carries the number and the figure reference, sentence 4 pivots, sentence 5 names
the user. No sentence exceeds 30 words.

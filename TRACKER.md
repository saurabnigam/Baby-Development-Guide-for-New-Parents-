# Work Tracker

> Status of the red-team review and content build.
> Findings are defined in [RED-TEAM-REVIEW.md](RED-TEAM-REVIEW.md); this file tracks what's been done about them.

**Last updated:** 2026-08-06

---

## Status key

| | Meaning |
|---|---------|
| ✅ | Done |
| 🔄 | Partially done — detail in the note |
| ⬜ | Not started |
| ➖ | Won't do — reason given |

---

## Progress at a glance

| Phase | Scope | Done | Total | |
|-------|-------|------|-------|---|
| **0** | Red team audit | 50 | 50 | ✅ |
| **1** | P0 safety fixes | 12 | 12 | ✅ |
| **2** | P1 factual corrections | 18 | 18 | ✅ |
| **3** | New teaching modules (the D-series) | 10 | 10 | ✅ |
| **4** | P2 structural fixes | 6 | 10 | 🔄 |
| **5** | Examples added to existing age modules | 5 | 12 | 🔄 |
| **6** | Citations across modules 05–20 | 5 | 16 | 🔄 |
| **7** | Depth parity across age modules | 3 | 11 | 🔄 |
| **8** | **Chapter-by-chapter rewrite pass** | 5 | 20 | 🔄 |
| | **Total** | **114** | **149** | **77%** |

---

## Phase 0 — Red team audit ✅

| | Item | Output |
|---|------|--------|
| ✅ | Read all 27 files (~6,650 lines) | — |
| ✅ | 12 P0 safety findings | [RED-TEAM-REVIEW.md §A](RED-TEAM-REVIEW.md#a-safety-gaps--p0) |
| ✅ | 18 P1 factual findings | [§B](RED-TEAM-REVIEW.md#b-factual-and-evidence-problems--p1) |
| ✅ | 10 P2 structural findings | [§C](RED-TEAM-REVIEW.md#c-structural-and-credibility-problems--p2) |
| ✅ | 10 coverage-gap findings | [§D](RED-TEAM-REVIEW.md#d-what-the-guide-never-actually-teaches--p1) |

---

## Phase 1 — P0 safety fixes ✅

| | ID | Finding | Fix | File |
|---|----|---------|-----|------|
| ✅ | A1 | No safe sleep in 0–3 mo module | Added full "Read This First: Safe Sleep" section, ABCs + room-sharing + sofa risk + swaddle stop | [03](03-newborn-0-3-months/README.md) |
| ✅ | A2 | No safe sleep in the *sleep* module | Added "Safe Sleep for Infants — Non-Negotiable First" + product warnings + a non-judgemental bed-sharing section | [16](16-sleep-and-development/README.md) |
| ✅ | A3 | Nothing on never shaking a baby | Added "When the Crying Won't Stop" — put the baby down, walk away, tell every caregiver | [03](03-newborn-0-3-months/README.md) |
| ✅ | A4 | No water safety anywhere | Full section: layers of protection, where children drown by age, water competence, teaching progression 0–18, open water, rip currents | [23 §3](23-life-skills-critical-moments/README.md#part-3-water--swimming) |
| ✅ | A5 | Choking hazards listed, response missing | Added CPR/choking-class prompts in 03, 05, 23, and the parent checklist | 03, 05, 23 |
| ✅ | A6 | No car seat guidance | Added to "Other Safety Essentials" and Module 23 | [03](03-newborn-0-3-months/README.md), [23](23-life-skills-critical-moments/README.md) |
| ✅ | A7 | Suicidality named with no crisis pathway | Full section: ask directly, means restriction, what not to say, international crisis numbers | [14](14-age-12-18/README.md#if-you-are-worried-about-suicide-or-self-harm) |
| ✅ | A8 | No poison / button-battery warning | Added to 06, 23, DISCLAIMER, and both trackers | 06, 23, DISCLAIMER |
| ✅ | A9 | No body safety / consent content | Full section: anatomical names, private-parts rule, secrets vs surprises, safe adults, no-forced-affection | [23 §7](23-life-skills-critical-moments/README.md#part-7-body-safety--consent) |
| ✅ | A10 | Egg yolk as first food; sesame missing | Corrected to whole egg; full top-9 allergen list with a how-to and reaction signs | [05](05-infant-6-9-months/README.md) |
| ✅ | A11 | No oral health content | Added to the life-skills timeline: gums from 6 mo, adult brushes/checks to 7–8, dental visit by age 1 | [23](23-life-skills-critical-moments/README.md) |
| ✅ | A12 | Mobile recommended without safety caveat | Added: remove by ~5 months, nothing in the crib, cord length | [03](03-newborn-0-3-months/README.md) |

---

## Phase 2 — P1 factual corrections ✅

| | ID | Was | Now | File |
|---|----|-----|-----|------|
| ✅ | B1 | "90% of brain development before age 5" | Corrected to brain *volume*; explicit "not a closing door" | [README](README.md), [01](01-brain-science-fundamentals/README.md) |
| ✅ | B2 | "EQ predicts success better than IQ (Goleman; Mayer & Salovey)" | Claim removed with an explanation of why, incl. the citation error | [00](00-prerequisites/README.md), [21](21-building-eq/README.md) |
| ✅ | B3 | Whole-brain synapse counts as Huttenlocher | Reframed as regional density extrapolations; precision caveat added | [01](01-brain-science-fundamentals/README.md) |
| ✅ | B4 | "Peak synaptic density ~2 years" | Corrected — peaks vary by region; diagram relabelled | [01](01-brain-science-fundamentals/README.md), [README](README.md) |
| ✅ | B5 | "50% reduction in verbal interactions (Radesky 2014)" | Fabricated figure removed; claim restated to match the actual study | [01](01-brain-science-fundamentals/README.md) |
| ✅ | B6 | Hart & Risley cited unqualified | Replication failure noted; Weisleder & Fernald and turn-taking carry the claim | [01](01-brain-science-fundamentals/README.md), [22](22-building-iq/README.md) |
| ✅ | B7 | Transgenerational epigenetics overclaimed | Explicit "not established in humans" callout | [01](01-brain-science-fundamentals/README.md) |
| ✅ | B8 | "The Golden Ratio: 70/30 Rule" | Replaced with "Mostly Follow, Sometimes Stretch"; invented numbers removed | [02](02-milestones-overview/README.md) |
| ✅ | B9 | Attachment % as fact, disorganized at 5% | Corrected to ~15%, sourced, with a cultural-variation caveat | [02](02-milestones-overview/README.md) |
| ✅ | B10 | Two-word phrases by 24 mo as referral trigger | Moved to 30 mo per CDC 2022, with an explanation of why | [02](02-milestones-overview/README.md) |
| ✅ | B11 | Crawling listed as a milestone | Reframed as one of several normal patterns; CDC removal noted | [02](02-milestones-overview/README.md) |
| ✅ | B12 | Garbled breastfed-iron guidance | Corrected to 1 mg/kg/day from 4 months; screening vs supplementation separated | [03](03-newborn-0-3-months/README.md) |
| ✅ | B13 | "Research by pediatrician Donald Winnicott" | Corrected to a clinical concept, with what the research does support | [00](00-prerequisites/README.md) |
| ✅ | B14 | Well-child schedule missing newborn visit | Added 3–5 day visit and annual-from-3; noted country variation | [00](00-prerequisites/README.md) |
| ✅ | B15a | Calcium 270 mg at 9–12 mo | Corrected to ~260 mg AI | [06](06-infant-9-12-months/README.md) |
| ✅ | B15b | Calcium/iron/protein straddling age 3–4 | Split into age-3 and age-4 values | [10](10-age-3-4/README.md) |
| ✅ | B15c | Calcium 1,300 mg attributed to "AAP/WHO" | Attributed correctly to IOM/NASEM; WHO difference noted | [13](13-age-7-12/README.md) |
| ✅ | B15d | Protein 46/52 g across all of 12–18 | Split: 34 g for 9–13, 46/52 g from 14 | [14](14-age-12-18/README.md) |
| ✅ | B16 | "Avoid walkers" vs "push walker recommended" | Explicit callout distinguishing push walkers from sit-in walkers | [06](06-infant-9-12-months/README.md) |
| ✅ | B17 | Juice limit given only at age 4–5 | Added the tighter 1–3 year limit to modules 08, 09, 10 | 08, 09, 10 |

*B18 ("10 or more exposures" unsourced) folded into Phase 6.*

---

## Phase 3 — New teaching modules ✅

| | ID | Gap | Delivered |
|---|----|-----|-----------|
| ✅ | D1 | No method for teaching a skill | [The Teaching Loop](23-life-skills-critical-moments/README.md#part-1-the-teaching-loop) — model, break down, together, watch, fade. Forward and backward chaining |
| ✅ | D2 | Empathy named 11× taught 0× | [Four-step empathy skill](21-building-eq/README.md#part-2-empathy--the-four-step-skill) + real progression table 0–18 + scripts + "my child laughed when someone got hurt" |
| ✅ | D3 | Patience absent | [Three sub-skills](21-building-eq/README.md#part-3-patience--three-skills-not-one), waiting ladder, 10-second rule, boredom protocol — with the marshmallow-test replication caveat |
| ✅ | D4 | No coherent behaviour model | [Module 24](24-behaviour-and-discipline/README.md) — behaviour equation, three-part response, limits, consequences, playbook, and an explicit corporal-punishment position |
| ✅ | D5 | Food *behaviour* untaught | [Part 7](24-behaviour-and-discipline/README.md#part-7-food--mealtime-behaviour) — why "one bite" backfires, behaviour by age, guests, restaurants, teaching fullness, picky vs ARFID |
| ✅ | D6 | Swimming and all critical-moment skills absent | [Module 23](23-life-skills-critical-moments/README.md) — water, roads, cycling, kitchen, body safety, money, self-care, chores, emergencies, digital |
| ✅ | D7 | IQ treated as something that happens | [Module 22](22-building-iq/README.md) — turns, dialogic reading, attention, curiosity, EF, problem-solving, number sense, and what doesn't work |
| ✅ | — | No tracker for any of it | [EQ & IQ Skills Tracker](parent-toolkit/eq-iq-skills-tracker.md) + [Life Skills Tracker](parent-toolkit/life-skills-tracker.md) |
| ✅ | — | New modules unreachable | Added to README (Part 6 + "How do I…" index), PRD, toolkit README, lesson objectives |
| ✅ | — | Cross-links from age modules | Added from 06, 08, 09, 12 into the new modules |

### Still open from the D-series

| | ID | Gap | Plan |
|---|----|-----|------|
| ⬜ | D8 | Family systems — siblings, co-parenting, grandparents who parent differently, only children, twins, blended families | New Module 25 |
| ⬜ | D9 | Children who develop differently — prematurity beyond Module 04, neurodivergence, disability, what happens *after* an evaluation | New Module 26. Currently every red-flag section ends at "talk to your paediatrician" and drops the parent there |
| ⬜ | D10 | Regional adaptation — which guidance is US-specific vs universal | Partly addressed in [DISCLAIMER](DISCLAIMER.md); needs per-module flags |

---

## Phase 4 — P2 structural fixes 🔄

| | ID | Finding | Status |
|---|----|---------|--------|
| ✅ | C1 | No repo-level disclaimer | [DISCLAIMER.md](DISCLAIMER.md) created, linked from README |
| ✅ | C3 | Editorial changelog leaking into Module 04 | "What Changed in This Verified Version" → "The Short Version" |
| ✅ | C5 | Brand names against the PRD's own scope | LEGO, Duplo, Uno, Candy Land, Snakes and Ladders, Sequence Junior all genericised in 09, 10, 11, 12, 13 |
| ✅ | C6a | Module 12 missing "Parent Behaviors That Matter Most" | Added |
| ✅ | C6b | Module 12 missing sleep and screen guidance | Added "Sleep, Screens & Movement at School Age" |
| ✅ | C6c | Module 02 milestone tables missing Motor/Language for 5–7, 7–12, 12–18 | All three completed |
| ✅ | C7 | Markdown rendering breaks | Fixed in 08 (×2) and 09 (×2) |
| ✅ | C8 | Toolkit checklists stopped at age 5 | Added 5–12 and 12–18 daily checklists, plus two safety checklists |
| 🔄 | C9 | "70% weight on 0–5" not true | PRD now states the actual figure and flags it as unmet. Fixing it properly needs Phase 7 |
| ⬜ | C10 | Cross-cutting modules don't link back to age modules | 15–19 still have no inbound links to specific stages |
| ⬜ | C2 | Module 04 is 19% of the repo | Phase 7 |
| ⬜ | C4 | PRD's citation metric unmet in 24 of 27 files | Phase 6 |

---

## Phase 8 — Chapter-by-chapter rewrite pass 🔄

One chapter at a time. Each pass does four things: **plain language** (target
grade 6–8), **accuracy check**, **worked examples**, and **references verified
against the source this session** — never recalled.

### Rule for this phase

> **No citation goes in that hasn't been opened and checked in this session.**
> Two bad references were caught this way and discarded: a PMID that pointed at
> a paper on peritoneal dialysis, and another that pointed at neonatal glucose
> monitors. Both would have looked entirely plausible in a reference list.

### Progress

| Ch | Status | Grade before → after | Reading ease | Refs verified | Key correction |
|----|--------|---------------------|--------------|---------------|----------------|
| 00 Start Here | ✅ | 13.0 → **6.6** | 37.7 → 70.4 | 5 | Real WHO milestone windows; IDEA Part C fee rules |
| 01 Brain Science | ✅ | 13.5 → **6.5** | 33.1 → 67.0 | 12 | Removed brain-volume figures not present in the cited paper |
| 02 Milestones | ✅ | 14.0 → **7.6** | 40.6 → 62.3 | 6 | Attachment percentages corrected again (Deneault 2023) |
| 03 Newborn | ✅ | 10.1 → **6.4** | 53.9 → 70.9 | 10 | Safe-sleep risk multipliers; AHT/crying peak alignment |
| 05 6–9 months | ✅ | 13.6 → **7.0** | 36.2 → 68.1 | 6 | LEAP trial numbers; gagging vs choking |
| 06 9–12 months | ⬜ | 12.6 | 41.2 | | |
| 07 12–18 months | ⬜ | 13.4 | 36.3 | | |
| 08 18–24 months | ⬜ | 13.1 | 38.7 | | |
| 09 2–3 years | ⬜ | 13.4 | 35.0 | | |
| 10 3–4 years | ⬜ | 14.6 | 30.0 | | |
| 11 4–5 years | ⬜ | 14.7 | 28.8 | | |
| 12 5–7 years | ⬜ | 15.5 | 31.6 | | |
| 13 7–12 years | ⬜ | 16.1 | 19.0 | | |
| 14 12–18 years | ⬜ | 12.6 | 37.8 | | |
| 15 Nutrition | ⬜ | 16.4 | 24.4 | | |
| 16 Sleep | ⬜ | 12.3 | 43.3 | | |
| 17 Play | ⬜ | 18.0 | 20.8 | | |
| 18 Screens | ⬜ | 17.4 | 27.3 | | |
| 19 Challenges | ⬜ | 19.1 | 17.6 | | |
| 20 Resources | ⬜ | 11.9 | 40.2 | | |
| 04 3–6 months | ➖ | 7.9 | 61.1 | 20 | Already at the bar. Two items flagged below |
| 21–24 Teaching | ➖ | 7.4–8.7 | 59.9–65.8 | — | Written to this standard |

**Health-literacy target is grade 6–8** (CDC/NIH guidance for material aimed at
the public). Every completed chapter is inside it.

### Open items found mid-pass

- **Vitamin D threshold mismatch.** Ch03 now says formula-fed babies need no
  supplement above ~27 oz/day, verified against AAP. Module 04 says 32 oz.
  Reconcile when Ch04 is reviewed.
- **Module 04 is the only module with an Indian-food section and an
  evidence-strength table.** Decide whether to generalise these or replicate
  them across the age modules.
- **AAP's iron-at-4-months recommendation has formal internal dissent** from its
  own Section on Breastfeeding. Ch03 says so plainly. Keep that framing in
  Ch15.

---

## Phase 5 — Examples in existing age modules 🔄

The new modules 21–24 are example-dense by design. The existing age modules mostly are not — Module 04 is the exception and shows what the standard should be (scripted dialogue, worked examples, "say this" blocks).

| | Module | What it needs |
|---|--------|---------------|
| ✅ | 03 Newborn | Worked example: reading a full overstimulation cycle from cue to recovery |
| ✅ | 05 6–9 mo | Scripted first-solids session. Worked example of social referencing |
| ⬜ | 06 9–12 mo | Scripted separation goodbye. Worked example of following a point |
| ⬜ | 07 12–18 mo | Scripted "I do it" standoff. Worked example of a helper job going wrong |
| ⬜ | 08 18–24 mo | Full scripted tantrum, start to repair |
| ⬜ | 09 2–3 yr | Scripted sharing conflict. Scripted toilet-learning refusal |
| ⬜ | 10 3–4 yr | Scripted peer conflict with both perspectives narrated |
| ⬜ | 11 4–5 yr | Scripted losing-a-game meltdown. Scripted friendship exclusion conversation |
| ⬜ | 12 5–7 yr | Scripted after-school decompression. Scripted "I'm bad at reading" |
| ⬜ | 13 7–12 yr | Scripted social-problem-solving conversation. Scripted low-confidence moment |
| ⬜ | 14 12–18 yr | Scripted collaborative problem-solving. Scripted "I don't want to talk about it" |
| ⬜ | 15–19 | One worked example each |

---

## Phase 6 — Citations ⬜

Currently: Module 04 has 20 inline links; modules 00–02 have author-year with no links; **modules 05–20 have no citations at all.**

| | Module | Action |
|---|--------|--------|
| ⬜ | 00, 01, 02 | Convert author-year to linked citations |
| ⬜ | 03, 05–20 | Replace unattributed "Research Notes" assertions with named, linked sources — or delete the claim |
| ⬜ | All | Add a "Last reviewed" date line |
| ⬜ | B18 | Source or hedge the "10+ exposures" figure in Module 07 |
| ⬜ | All | Verify every external link resolves |

---

## Phase 7 — Depth parity ⬜

Module 04 is 1,270 lines. The median age module is ~250. All are advertised as "3 hrs."

| | Module | Lines now | Target |
|---|--------|-----------|--------|
| ⬜ | 03 Newborn | 327 | ~500 |
| ➖ | 04 3–6 mo | 1,268 | Leave. This is the reference standard |
| ⬜ | 05 6–9 mo | 272 | ~500 |
| ⬜ | 06 9–12 mo | 258 | ~500 |
| ⬜ | 07 12–18 mo | 247 | ~500 |
| ⬜ | 08 18–24 mo | 271 | ~500 |
| ⬜ | 09 2–3 yr | 258 | ~450 |
| ⬜ | 10 3–4 yr | 256 | ~450 |
| ⬜ | 11 4–5 yr | 241 | ~450 |
| ⬜ | 12 5–7 yr | 234 | ~400 |
| ⬜ | 13 7–12 yr | 196 | ~400 |
| ⬜ | 14 12–18 yr | 245 | ~400 |

Alternatively: trim Module 04 to match. Depth parity matters more than absolute depth — a parent of a 7-month-old should not get a fifth of what a parent of a 4-month-old gets.

---

## Files touched this round

**Created (8)**

| File | Lines | What |
|------|-------|------|
| [RED-TEAM-REVIEW.md](RED-TEAM-REVIEW.md) | 293 | The full audit — 50 findings |
| [TRACKER.md](TRACKER.md) | this file | Status of everything |
| [DISCLAIMER.md](DISCLAIMER.md) | 64 | Medical scope, emergencies, regional differences |
| [21-building-eq/](21-building-eq/README.md) | 595 | Regulation, empathy, patience, repair |
| [22-building-iq/](22-building-iq/README.md) | 432 | Language, attention, curiosity, EF, number sense |
| [23-life-skills-critical-moments/](23-life-skills-critical-moments/README.md) | 591 | Teaching loop + swimming, roads, kitchen, body safety, money, emergencies |
| [24-behaviour-and-discipline/](24-behaviour-and-discipline/README.md) | 501 | Behaviour model, playbook, food behaviour |
| [parent-toolkit/eq-iq-skills-tracker.md](parent-toolkit/eq-iq-skills-tracker.md) | 188 | Quarterly EQ/IQ review |
| [parent-toolkit/life-skills-tracker.md](parent-toolkit/life-skills-tracker.md) | 226 | Skill-by-skill, four columns |

Repo grew from **6,648** lines to **10,179** — a 53% increase, with the four teaching modules accounting for 2,119 of it.

**Modified (16)**

`README.md` · `prd.md` · `00-prerequisites` · `01-brain-science-fundamentals` · `02-milestones-overview` · `03-newborn-0-3-months` · `04-infant-3-6-months` · `05-infant-6-9-months` · `06-infant-9-12-months` · `08-toddler-18-24-months` · `09-age-2-3` · `10-age-3-4` · `11-age-4-5` · `12-age-5-7` · `13-age-7-12` · `14-age-12-18` · `16-sleep-and-development` · `parent-toolkit/README.md` · `parent-toolkit/lesson-objectives.md` · `parent-toolkit/parent-checklists.md`

---

## Recommended next order

1. **Phase 6 (citations)** — the credibility gap is the biggest remaining risk. A guide that says "research shows" 40 times without a single link is asking to be disbelieved, and the PRD promises otherwise.
2. **Phase 5 (examples)** — highest reader value per hour of work, and directly what was asked for in this round.
3. **D8 and D9 (Modules 25, 26)** — the two remaining coverage gaps. D9 in particular: right now every red-flag list ends at "talk to your paediatrician" and abandons the parent at the moment they most need the next step.
4. **Phase 7 (depth parity)** — largest effort, and it should follow the citation and example work rather than precede it, or it just multiplies the unsourced text.
5. **C10** — cheap. Add inbound links from modules 15–19 to the age modules.

---

## Notes for whoever picks this up

- **Don't delete a rejected red-team finding.** Mark it ➖ with the reason. A finding someone considered and dismissed is more useful to the next reviewer than a missing row.
- **Module 04 is the quality bar.** When writing or expanding any age module, open it first: scripted dialogue, worked examples, "say this" blocks, real inline links, an evidence-strength table.
- **Safety content is not negotiable down for length.** If a module gets trimmed, the safety sections stay.
- **Where the evidence is weak, say so.** The B-series corrections deliberately kept the caveats visible rather than quietly deleting the claims. That honesty is a feature of this guide now, and it should survive future edits.

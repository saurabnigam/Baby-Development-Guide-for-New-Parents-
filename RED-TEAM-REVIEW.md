# Red Team Review

> An adversarial audit of the Baby IQ & EQ Development Guide.
> Reviewed: all 27 content files (~6,650 lines) at commit `5a63cf2`.
> Method: read every file, then attack it from four angles — **could this hurt a child?**, **is this actually true?**, **is this internally consistent?**, **what is missing that a parent would reasonably expect?**

**Headline:** the guide's voice, tone, and non-judgmental stance are genuinely good, and the responsive-caregiving core is sound. The problems are (1) a set of real **safety omissions** in a document that parents will treat as authoritative, (2) a handful of **overclaimed statistics** — including the guide's own central IQ/EQ thesis, (3) severe **depth inequality** between modules, and (4) the guide talks *about* EQ, IQ, and life skills constantly but never actually **teaches** them.

Findings are numbered so the [TRACKER](TRACKER.md) can reference them.

---

## Severity key

| Level | Meaning |
|-------|---------|
| **P0** | Could contribute to physical harm, or is a safety topic a parent would expect and not find |
| **P1** | Factually wrong, unsupported, or a major gap against the guide's own stated goals |
| **P2** | Inconsistency, structural defect, or credibility problem |

---

## A. Safety gaps — P0

### A1. Module 03 (0–3 months) has no safe-sleep guidance at all

The highest-SIDS-risk window in a child's life is 1–4 months. [Module 03](03-newborn-0-3-months/README.md) covers day-night confusion, crying, overstimulation, tummy time, and feeding — and never once says *back to sleep, firm flat surface, nothing in the crib, room-share don't bed-share*. [Module 04](04-infant-3-6-months/README.md) has an excellent "Safe Sleep Rules" block. Module 03 needs it more.

### A2. Module 16 — the *dedicated sleep module* — has no safe-sleep content either

[Module 16](16-sleep-and-development/README.md) discusses newborn sleep fragmentation, night waking, bedtime routines, and snoring red flags. A parent who searches this guide for "sleep" and lands here gets **zero** SIDS risk-reduction information. This is the single most surprising omission in the repo.

### A3. Nothing on abusive head trauma / "never shake a baby"

Module 03 correctly notes that crying peaks around 6–8 weeks. That peak coincides with the peak incidence of shaken baby syndrome. The guide tells parents what to check and when to call the pediatrician, but never gives the one instruction that matters most at 3am: *it is always safe to put the baby down in a safe space and walk away for five minutes; it is never safe to shake them.*

### A4. No water safety or drowning prevention anywhere

Drowning is the leading cause of death for children aged 1–4 in the US and among the top causes worldwide. The guide has 27 files and does not mention bathtubs, buckets, pools, or supervision. This is also the exact topic requested in this round of work — see [Module 23](23-life-skills-critical-moments/README.md).

### A5. Choking hazards are listed; choking *response* is not

Modules 04, 05, 06 all list choking hazards and the toilet-paper-roll test. No module tells a parent to learn infant back blows / chest thrusts / CPR, or where to take a class. Listing the hazard without the response is half a safety message.

### A6. No car seat or travel safety

Not mentioned in any module. Module 04 correctly says to move a sleeping baby out of a car seat — which is the only place car seats appear at all.

### A7. Module 14 raises suicidality with no crisis pathway

[Module 14](14-age-12-18/README.md) lists "self-harm, suicidal thinking" under red flags and stops there. A guide that names this risk owes the reader: how to ask directly, that asking does not plant the idea, means-restriction (locking up medications and firearms), and an actual number to call. Added in the revision.

### A8. No poisoning, medication, or button-battery guidance

Module 04's small-objects list includes "buttons" and "coins" but never button/coin-cell batteries, which cause caustic oesophageal burns within hours and are a genuine emergency. No mention of poison control, detergent pods, or medication storage.

### A9. No body safety, consent, or abuse-prevention content

The guide teaches empathy, emotion words, and social scripts, but never the standard early-childhood body-safety curriculum: correct anatomical names, "your body belongs to you," secrets vs surprises, safe adults, and that most abuse comes from someone known. This is both a safety gap and an EQ gap.

### A10. First-food and allergen inconsistencies

- [Module 05](05-infant-6-9-months/README.md) lists **"egg yolk"** as a priority first food. Current guidance is whole egg, well-cooked — yolk-only both under-delivers iron and delays the allergen exposure that the same module recommends.
- Module 04's allergen list includes **sesame**; Module 05's does not. Sesame has been a top-9 labelled allergen in the US since 2023.
- Module 05 says allergens should be introduced "around the time solids begin" but gives no *how* (small amount, at home, earlier in the day, one at a time, keep it in the diet regularly). Module 04 does. Module 05 is the module a 6-month-old's parent actually reads.

### A11. No oral health content anywhere

No first dental visit by age one, no wiping gums, no fluoride toothpaste smear, no bottle-in-bed caries, no juice-and-teeth link — despite six modules covering feeding in detail.

### A12. Mobile recommended without its safety caveat

Module 03's toy table recommends a "gentle musical mobile" with no note to remove it once the baby can push up on hands and knees (~5 months), which is the standard strangulation/entanglement caveat.

---

## B. Factual and evidence problems — P1

### B1. "90% of brain development happens before age 5" — README, first bold line

This is the guide's opening claim and it is misleading. The underlying fact is that **brain volume** reaches roughly 90% of adult size by age 5. "Development" is not volume: myelination, synaptic refinement, and prefrontal maturation continue into the mid-20s — which **this guide itself states** in Module 01's myelination timeline. The headline contradicts the content, and it is exactly the kind of claim that makes anxious parents feel they have already missed the window.

### B2. "EQ is a stronger predictor of life success than IQ" — Module 00

> *"Research shows EQ is a **stronger predictor of life success** than IQ (Goleman, 1995; Mayer & Salovey, 1997)."*

This is the single most consequential error in the guide, because it is the framing claim for the whole product.

- It is Goleman's **trade-book popularization**, not a finding of Mayer & Salovey, who explicitly distanced their ability model from that claim.
- Meta-analytic evidence does not support it. Cognitive ability remains the strongest single predictor of academic and job performance; emotional intelligence shows modest **incremental** validity over cognitive ability and personality.
- Citing Mayer & Salovey for a claim they did not make is a citation error, not just an overstatement.

The honest version — which is also the more useful one for parents — is that IQ and EQ predict *different* outcomes, that EQ predicts relationship quality and mental health better than IQ does, and that they are not in competition. The guide's own "The Critical Insight" paragraph immediately below already says this well; the ranking sentence should simply go.

### B3. Whole-brain synapse counts attributed to Huttenlocher — Module 01

The table gives "Synapses at birth ~50 trillion / at age 2 ~1,000 trillion (2× adult levels)" sourced to Huttenlocher 2002. Huttenlocher measured **synaptic density in specific cortical regions** from post-mortem tissue. Whole-brain quadrillion figures are extrapolations that are widely flagged as unreliable. Present them as illustrative orders of magnitude or drop the precision.

### B4. "Peak synaptic density: ~2 years" — README diagram and Module 01

Synaptic density peaks at very different times in different regions: roughly 4–12 months in primary visual cortex, and several years later in prefrontal cortex. A single number for "the brain" is wrong, and it undercuts the guide's own (correct) message that executive function has a long runway.

### B5. "Caregiver phone distraction → 50% reduction in verbal interactions (Radesky et al., 2014)"

Radesky's 2014 study was a naturalistic observation of caregivers and children in fast-food restaurants. It described absorption patterns and child bids for attention. It did not report a 50% reduction in verbal interactions. The number appears to be invented or imported from elsewhere. The underlying point (parental device absorption reduces responsiveness) is real and well-supported — it just needs a real citation and no fake percentage.

### B6. Hart & Risley cited without the replication problem — Module 01

The 5-Minute Action Plan cites Hart & Risley (1995) alongside Weisleder & Fernald (2013). The "30 million word gap" has failed to replicate (Sperry, Sperry & Miller, 2019), rested on 42 families, and has been extensively criticised for deficit framing of low-income and non-white families. For a guide whose principles include "non-judgmental" and "culturally inclusive," this citation is a liability. Weisleder & Fernald — which measured *child-directed* speech and found effects within a low-SES Spanish-speaking sample — carries the claim better on its own.

### B7. Transgenerational epigenetic inheritance overclaimed — Module 01

> *"These epigenetic changes can potentially be passed to future generations."*

Transgenerational epigenetic inheritance is established in some animal models and **not** established in humans. The hedge "potentially" does not do enough work in a document parents read as settled science.

### B8. "The Golden Ratio: 70/30 Rule" — Module 02

Presented with a heading that implies established science and a number that implies measurement. No such ratio exists in the developmental literature. The *idea* — mostly follow the child, sometimes stretch them — is sound and is a fair reading of Vygotsky. The invented numerals and the "Golden Ratio" branding are not.

### B9. Attachment distribution percentages presented as fact — Module 02

Secure 65% / anxious-resistant 10% / avoidant 20% / disorganized 5% is given with no source and no caveat. In normative Western samples disorganized attachment runs closer to 15%, and substantially higher in high-risk samples (van IJzendoorn et al., 1999). Distributions also vary meaningfully by culture, which matters for a guide claiming cultural inclusivity.

### B10. "No two-word phrases by 24 months" as a referral trigger — Module 02

CDC's revised (2022) milestone checklists place two-word phrases at **30 months**, deliberately, to reduce false alarms. As written this will send a large number of typically developing 24-month-olds' parents into avoidable panic — in a guide whose stated aim is to reduce exactly that.

### B11. "Begins crawling" listed as a 6–9 month milestone — Module 02

CDC removed crawling from its checklists in 2022 because a meaningful share of typically developing children never crawl. Keep it as a common pattern; don't list it as a milestone.

### B12. Iron guidance for breastfed infants is garbled — Module 03

> *"breastfed infants may need supplemental iron screening by 4 months"*

This conflates two different things. AAP recommends **oral iron supplementation of 1 mg/kg/day** for exclusively and partially breastfed infants starting at 4 months, continuing until iron-rich complementary foods are established; universal **anemia screening** is at 12 months. Module 04 handles this correctly ("ask at the 4-month checkup"). Module 03 should match.

### B13. "Winnicott's research" — Module 00

Donald Winnicott's "good enough mother" was a clinical and psychoanalytic concept developed from practice, not a research finding. He was a paediatrician *and* psychoanalyst. Small, but it is a factual claim about the provenance of an idea the guide leans on.

### B14. Well-child visit schedule incomplete — Module 00

Lists 1, 2, 4, 6, 9, 12, 15, 18, 24, 30 months then annually. Omits the **3–5 day newborn visit**, which is the visit most tied to feeding problems, jaundice, and weight loss in the first week.

### B15. Nutrient values straddle age boundaries — Modules 06, 10, 12, 13, 14

| Module | Value given | Problem |
|--------|-------------|---------|
| 06 (9–12 mo) | Calcium 270 mg/day | Current DRI Adequate Intake for 7–12 months is **260 mg** |
| 10 (age 3–4) | Calcium 1,000 mg/day | RDA is **700 mg** at age 3, 1,000 mg from age 4 — the row covers both |
| 10 (age 3–4) | Iron 10 mg "from age 4" | Never states the age-3 value (**7 mg**) in a table headed "Age 3 to 4" |
| 13 (age 7–12) | Calcium 1,300 mg "(AAP/WHO)" | 1,300 mg is the US IOM/NASEM RDA for 9–18. **WHO recommends lower intakes.** Attribution is wrong |
| 14 (age 12–18) | Protein 46 g (girls) / 52 g (boys) | These are the **14–18** RDAs. The 9–13 RDA is 34 g. The row covers 12–18 |

Each individually is small. Together they signal that the nutrient tables were assembled without a single source-of-truth reference — which is why the same nutrient gets different numbers in different modules.

### B16. Walker advice contradicts itself across modules

[Module 04](04-infant-3-6-months/README.md) says flatly: *"Avoid walkers. They do not teach walking and can be dangerous."* [Module 06](06-infant-9-12-months/README.md) recommends a *"push-along walker or wagon"* and [Module 07](07-toddler-12-18-months/README.md) a *"push wagon or walking trolley."*

These are different products — sit-in baby walkers (banned in Canada, ~2,000 US ER visits/year) versus push toys the child stands behind. But the guide never says so, so a parent reading both modules gets a flat contradiction on a safety item.

### B17. Juice limit given only where it matters least — Module 11

Module 11 (age 4–5) gives "4 to 6 oz per day maximum," which is right for that age. The tighter limit — **4 oz/day for ages 1–3, and none under 12 months** — never appears in Modules 06–09, which are the modules where juice overconsumption, appetite suppression, and dental caries actually start.

### B18. "10 or more exposures" stated as fact — Module 07

Widely repeated, and the underlying research (Wardle, Cooke and colleagues) does support repeated taste exposure — but the specific number varies by food and study, and the guide gives it unsourced and unhedged.

---

## C. Structural and credibility problems — P2

### C1. No repo-level medical disclaimer, licence, or review dates

Only Module 04 carries a medical-safety note. There is no root-level disclaimer, no LICENSE, no CONTRIBUTING, and no "last reviewed" date on any file. For health content this is the baseline expectation, and its absence undercuts the guide's evidence-based positioning.

### C2. Module 04 is 19% of the entire repo

| Module | Lines |
|--------|-------|
| 04 (3–6 months) | **1,270** |
| Next largest (01) | 292 |
| Median age module | ~250 |

The README promises "3 hrs" for each age module. A parent of a 4-month-old gets a genuinely excellent, deeply worked, fully sourced module. A parent of a 7-month-old, a 3-year-old, or a 10-year-old gets roughly a fifth of that. This is the largest quality problem in the guide after the safety gaps, and it is invisible from the README.

### C3. Editorial scaffolding leaked into parent-facing content — Module 04

The section **"What Changed in This Verified Version"** is an internal changelog addressed to whoever edited the file, not to a parent. It also implies, by contrast, that the other 20 modules are *un*verified — which, per C4, is more or less true, but should not be disclosed by accident.

### C4. The PRD's own success metric is unmet in 24 of 27 files

> *PRD success metric: "Every major claim links to peer-reviewed research."*

- Module 04: 20 inline links to CDC/AAP/WHO and named journal articles. Excellent.
- Modules 00, 01, 02: author-year citations, no links.
- Modules 05–20: a "Research Notes" section of unattributed assertions — *"Research on attachment consistently shows…"*, *"Studies on infant motor exploration show…"* — with no citation of any kind.

### C5. Brand names throughout, against the PRD's own scope

> *PRD, Out of Scope: "Specific brand product recommendations."*

Modules 09, 10, 11, 12, 13 name LEGO, LEGO Duplo, LEGO Technic, Duplo, Uno, Uno Junior, Candy Land, Snakes and Ladders, and Sequence Junior. Beyond the scope violation, this dates the content and excludes families where those products aren't sold or affordable.

### C6. Module structure degrades in the later modules

"Parent Behaviors That Matter Most" appears in every module from 03 through 11, then vanishes from 12, 13, and 14. Module 02's milestone tables carry Motor and Language rows for every band up to 4–5, then drop both for 5–7, 7–12, and 12–18. Module 12 — the school-start module — has no sleep and no screen guidance, the two things that most disrupt a new schoolchild.

### C7. Markdown rendering breaks

Missing blank lines before headings and after paragraphs at [08-toddler-18-24-months/README.md:174](08-toddler-18-24-months/README.md), [:189](08-toddler-18-24-months/README.md), [09-age-2-3/README.md:167](09-age-2-3/README.md), and [:182](09-age-2-3/README.md). These render as run-together text.

### C8. Toolkit coverage stops at age 5

[parent-checklists.md](parent-toolkit/parent-checklists.md) has daily checklists for 0–12m, 3–6m, 1–2y, 2–5y. Nothing for 5–7, 7–12, or 12–18, though the course covers to 18 and [lesson-objectives.md](parent-toolkit/lesson-objectives.md) does include those modules.

### C9. The "70% weight on 0–5 years" claim doesn't hold

PRD comprehensiveness metric claims 70% weight on ages 0–5. By line count the 0–5 modules are roughly 55% of the repo, and Module 04 alone accounts for a third of that.

### C10. Cross-cutting modules don't link back to age modules

Modules 15–19 are written to apply "at every stage" but contain no links into the age modules where the specifics live, so a parent reading the nutrition module has no path back to their child's stage.

---

## D. What the guide never actually teaches — P1

This section is the brief for the new content. The pattern is consistent: the guide **names** these capacities as milestones and then moves on, without ever telling a parent how to build them.

### D1. No method for teaching a skill

The single most reusable thing a parent can learn is a repeatable teaching loop — model, break down, scaffold, hand over, fade. The guide has 100+ activities and no method behind them. **→ [Module 23](23-life-skills-critical-moments/README.md), "The Teaching Loop"**

### D2. Empathy is named 11 times and taught zero times

It appears as a milestone in Modules 02, 07, 08, 09, 10, 11 and as a benefit of pretend play. There is no developmental progression (contagious crying → concern → comfort attempts → perspective-taking → moral emotion), no scripts, no answer to "my child watched another child cry and did nothing." **→ [Module 21](21-building-eq/README.md)**

### D3. Patience and delayed gratification: absent

Mentioned once, as a 5–7 milestone ("can delay gratification"), as if it arrives on schedule. No waiting practice, no frustration ladder, no boredom tolerance, no interrupting rules. Any treatment also needs the replication caveat: Watts, Duncan & Quan (2018) found the marshmallow test's predictive power largely attenuated after controlling for family background. **→ [Module 21](21-building-eq/README.md)**

### D4. Behaviour teaching has no coherent model

Tantrums, hitting, biting, limits, and choices appear as scattered troubleshooting entries across seven modules. There is no unifying model (connect before correct; teach the replacement behaviour; natural vs logical consequences; what to do *after*), no discussion of what actually happens in the child's brain during a limit, and — notably — **no statement on corporal punishment**, despite the AAP's 2018 policy statement being one of the clearest evidence positions in all of paediatrics. **→ [Module 24](24-behaviour-and-discipline/README.md)**

### D5. Food *behaviour* is untaught, though food *nutrition* is well covered

Six modules cover what and when to feed. None cover: how to teach a child to sit at a table, why "one bite" rules backfire, how to handle eating at other people's homes, restaurant behaviour, food as reward, or teaching a child to notice their own fullness. **→ [Module 24](24-behaviour-and-discipline/README.md), "Food Behaviour"**

### D6. Swimming and every other critical-moment skill: absent

Nothing on water competence, road and traffic safety, cycling, kitchen and knife and fire, money, body safety and consent, first aid, sleeping alone, hygiene and self-care, chores, or digital independence — the concrete "how do I teach my kid to do X" questions parents actually ask. **→ [Module 23](23-life-skills-critical-moments/README.md)**

### D7. IQ is treated as something that happens, not something you build

Cognitive milestones are listed everywhere; the *habits* that build thinking — curiosity, question quality, attention span, working memory, problem-solving stamina, metacognition, reading, number sense — have no home. **→ [Module 22](22-building-iq/README.md)**

### D8. Family systems barely exist

Siblings get one troubleshooting entry in Module 19. Nothing on co-parenting alignment, grandparents and caregivers who parent differently, only children, twins, or blended families — despite "acknowledge diverse family structures" being PRD principle 4.

### D9. No content for children who develop differently

Prematurity and corrected age appear only in Module 04. Nothing on neurodivergence, disability, or what to do *after* an evaluation — the guide's red-flag sections all end at "talk to your pediatrician" and drop the parent there.

### D10. Regional and cultural adaptation is inconsistent

Module 04 is written with Indian food examples (khichdi, ragi, dal, paneer, amla) and Indian-context nutrition advice. No other module does this, and no module says which guidance is US-specific (Early Intervention/IDEA, 988, AAP schedules) versus universal.

---

## Summary

| Category | P0 | P1 | P2 | Total |
|----------|----|----|----|-------|
| A. Safety gaps | 12 | — | — | 12 |
| B. Factual / evidence | — | 18 | — | 18 |
| C. Structural | — | — | 10 | 10 |
| D. Coverage gaps | — | 10 | — | 10 |
| **Total** | **12** | **28** | **10** | **50** |

**Fix order:** every P0 first (they are cheap — most are a paragraph), then B1/B2 (the two headline claims the whole guide rests on), then the D-series new modules, then the B-series numeric corrections, then C.

Status of each finding is tracked in [TRACKER.md](TRACKER.md).

---

*This review is a working document. If you disagree with a finding, note the reason in the tracker rather than deleting the row — a rejected finding with a reason is more useful to the next reviewer than a missing one.*

# Cochrane Risk of Bias 2 (RoB 2) Tool

## Overview

The Risk of Bias 2 (RoB 2) tool is the recommended tool for assessing risk of bias in randomized controlled trials (RCTs) included in Cochrane systematic reviews. It provides a structured framework for evaluating bias across five domains, using signaling questions to guide domain-level judgments.

**Key References:**
- Sterne JAC, Savovic J, Page MJ, et al. RoB 2: a revised tool for assessing risk of bias in randomised trials. BMJ. 2019;366:l4898.
- Higgins JPT, Savovic J, Page MJ, Elbers RG, Sterne JAC. Chapter 8: Assessing risk of bias in a randomized trial. In: Cochrane Handbook for Systematic Reviews of Interventions version 6.4. Cochrane, 2023.

---

## General Principles

### Scope of Assessment

- RoB 2 assesses risk of bias for a **specific result** (outcome, time point, and analysis) within a study
- The same study may have different risk of bias judgments for different outcomes
- Assess the **effect of assignment to intervention** (intention-to-treat) or the **effect of adhering to intervention** (per-protocol), as appropriate to the review question

### Assessment Approach

- Each domain has a set of **signaling questions** with response options
- Signaling questions lead to a **domain-level judgment**
- Domain-level judgments combine into an **overall risk of bias judgment**
- Every judgment requires a **supporting rationale** with specific evidence from the study

### Response Options for Signaling Questions

| Response | Meaning |
|----------|---------|
| Yes (Y) | Indicates low risk of bias for that aspect |
| Probably Yes (PY) | Likely low risk of bias, but some uncertainty |
| No (N) | Indicates a concern about bias for that aspect |
| Probably No (PN) | Likely a concern about bias, but some uncertainty |
| No Information (NI) | Insufficient information to make a judgment |

### Domain-Level Judgment Options

| Judgment | Symbol | Meaning |
|----------|--------|---------|
| Low risk of bias | Green (+) | The domain is judged to be at low risk of bias |
| Some concerns | Yellow (?) | There is some concern about bias, but not sufficient to be judged high risk |
| High risk of bias | Red (-) | The domain is judged to be at high risk of bias |

---

## Domain 1: Bias Arising from the Randomization Process

### Purpose

Assesses whether the allocation sequence was adequately generated and concealed, and whether there were baseline imbalances that suggest problems with randomization.

### Signaling Questions

| # | Question | Response Options |
|---|----------|-----------------|
| 1.1 | Was the allocation sequence random? | Y / PY / PN / N / NI |
| 1.2 | Was the allocation sequence concealed until participants were enrolled and assigned to interventions? | Y / PY / PN / N / NI |
| 1.3 | Did baseline differences between intervention groups suggest a problem with the randomization process? | Y / PY / PN / N / NI |

### Judgment Algorithm

```
If 1.1 = Y/PY AND 1.2 = Y/PY AND 1.3 = N/PN:
  --> Low risk of bias

If 1.1 = Y/PY AND 1.2 = Y/PY AND 1.3 = NI:
  --> Some concerns (baseline differences cannot be assessed)

If 1.1 = NI AND 1.2 = NI:
  --> Some concerns (insufficient information about randomization)

If 1.1 = N/PN OR 1.2 = N/PN:
  --> High risk of bias (inadequate randomization)

If 1.3 = Y/PY (and imbalances are not compatible with chance):
  --> High risk of bias (baseline imbalances suggest problem)
```

### Detailed Guidance

- **Adequate sequence generation methods:** Computer-generated random numbers, random number tables, coin tossing, dice rolling, drawing lots, shuffled sealed envelopes
- **Inadequate methods:** Alternation, date of birth, hospital number, date of admission, clinician judgment
- **Adequate concealment:** Central randomization (telephone, web-based), sequentially numbered opaque sealed envelopes (SNOSE), pharmacy-controlled
- **Inadequate concealment:** Open allocation schedule, unsealed envelopes, alternation

---

## Domain 2: Bias Due to Deviations from Intended Interventions

### Purpose

Assesses whether there were deviations from the intended interventions that arose because of the experimental context (i.e., that would not have occurred outside of the trial).

**Note:** This domain has two variants:
- **Effect of assignment to intervention** (intention-to-treat effect)
- **Effect of adhering to intervention** (per-protocol effect)

### Signaling Questions -- Effect of Assignment to Intervention

| # | Question | Response Options |
|---|----------|-----------------|
| 2.1 | Were participants aware of their assigned intervention during the trial? | Y / PY / PN / N / NI |
| 2.2 | Were carers and people delivering the interventions aware of participants' assigned intervention during the trial? | Y / PY / PN / N / NI |
| 2.3 | If Y/PY/NI to 2.1 or 2.2: Were there deviations from the intended intervention that arose because of the experimental context? | Y / PY / PN / N / NI / NA |
| 2.4 | If Y/PY to 2.3: Were these deviations likely to have affected the outcome? | Y / PY / PN / N / NI / NA |
| 2.5 | If Y/PY to 2.4: Were these deviations from intended intervention balanced between groups? | Y / PY / PN / N / NI / NA |
| 2.6 | Was an appropriate analysis used to estimate the effect of assignment to intervention? | Y / PY / PN / N / NI |
| 2.7 | If N/PN/NI to 2.6: Was there potential for a substantial impact (on the result) of the failure to analyse participants in the group to which they were randomized? | Y / PY / PN / N / NI / NA |

### Signaling Questions -- Effect of Adhering to Intervention

| # | Question | Response Options |
|---|----------|-----------------|
| 2.1 | Were participants aware of their assigned intervention during the trial? | Y / PY / PN / N / NI |
| 2.2 | Were carers and people delivering the interventions aware of participants' assigned intervention during the trial? | Y / PY / PN / N / NI |
| 2.3 | If Y/PY/NI to 2.1 or 2.2: Were important co-interventions balanced across intervention groups? | Y / PY / PN / N / NI / NA |
| 2.4 | Could failures in implementing the intervention have affected the outcome? | Y / PY / PN / N / NI |
| 2.5 | Did study participants adhere to the assigned intervention regimen? | Y / PY / PN / N / NI |
| 2.6 | If N/PN/NI to 2.3 or 2.5: Was an appropriate analysis used to estimate the effect of adhering to the intervention? | Y / PY / PN / N / NI / NA |

### Judgment Algorithm (Effect of Assignment)

```
If participants/carers blinded (2.1 & 2.2 = N/PN) AND 2.6 = Y/PY:
  --> Low risk of bias

If deviations unlikely to affect outcome (2.4 = N/PN) AND 2.6 = Y/PY:
  --> Low risk of bias

If deviations balanced (2.5 = Y/PY) AND 2.6 = Y/PY:
  --> Low risk of bias

If unblinded AND deviations arose AND affected outcome AND unbalanced:
  --> High risk of bias

If inappropriate analysis (2.6 = N/PN) AND substantial impact (2.7 = Y/PY):
  --> High risk of bias

Otherwise:
  --> Some concerns
```

---

## Domain 3: Bias Due to Missing Outcome Data

### Purpose

Assesses whether outcome data were available for all, or nearly all, participants randomized.

### Signaling Questions

| # | Question | Response Options |
|---|----------|-----------------|
| 3.1 | Were data for this outcome available for all, or nearly all, participants randomized? | Y / PY / PN / N / NI |
| 3.2 | If N/PN/NI to 3.1: Is there evidence that the result was not biased by missing outcome data? | Y / PY / PN / N / NI / NA |
| 3.3 | If N/PN to 3.2: Could missingness in the outcome depend on its true value? | Y / PY / PN / N / NI / NA |
| 3.4 | If Y/PY/NI to 3.3: Is it likely that missingness in the outcome depended on its true value? | Y / PY / PN / N / NI / NA |

### Judgment Algorithm

```
If 3.1 = Y/PY (data available for nearly all participants):
  --> Low risk of bias
  "Nearly all" typically means < 5% missing, or up to 10-20% if reasons
  are clearly documented and unrelated to outcome

If 3.2 = Y/PY (evidence from sensitivity analyses or other evidence
  that result is robust to missingness):
  --> Low risk of bias

If 3.3 = N/PN (missingness does not depend on true value):
  --> Low risk of bias
  Examples: administrative censoring, planned interim analysis

If 3.3 = Y/PY/NI AND 3.4 = Y/PY:
  --> High risk of bias

If 3.3 = Y/PY/NI AND 3.4 = PN/NI:
  --> Some concerns
```

### Additional Guidance

- Consider whether missingness differs between groups
- Consider reasons for missingness (dropout, loss to follow-up, withdrawal)
- Sensitivity analyses for missing data include: worst-case/best-case analysis, multiple imputation, pattern-mixture models
- "Nearly all" data: generally < 5% missing is acceptable; 5-20% requires judgment based on reasons and balance

---

## Domain 4: Bias in Measurement of the Outcome

### Purpose

Assesses whether the outcome was measured appropriately and whether measurement or ascertainment could have differed between groups.

### Signaling Questions

| # | Question | Response Options |
|---|----------|-----------------|
| 4.1 | Was the method of measuring the outcome inappropriate? | Y / PY / PN / N / NI |
| 4.2 | Could measurement or ascertainment of the outcome have differed between intervention groups? | Y / PY / PN / N / NI |
| 4.3 | If N/PN/NI to 4.1 AND N/PN to 4.2: Were outcome assessors aware of the intervention received by study participants? | Y / PY / PN / N / NI |
| 4.4 | If Y/PY/NI to 4.3: Could assessment of the outcome have been influenced by knowledge of intervention received? | Y / PY / PN / N / NI / NA |
| 4.5 | If Y/PY/NI to 4.4: Is it likely that assessment of the outcome was influenced by knowledge of intervention received? | Y / PY / PN / N / NI / NA |

### Judgment Algorithm

```
If 4.1 = N/PN AND 4.2 = N/PN:
  --> Low risk of bias (appropriate method, no differential measurement)

If 4.3 = N/PN (assessors blinded):
  --> Low risk of bias

If 4.4 = N/PN (outcome not susceptible to influence by knowledge):
  --> Low risk of bias
  Examples: all-cause mortality, laboratory values with automated reading

If 4.5 = Y/PY:
  --> High risk of bias

If 4.5 = PN/NI:
  --> Some concerns

If 4.1 = Y/PY:
  --> High risk of bias (inappropriate measurement method)
```

### Outcome Susceptibility to Bias

| Outcome Type | Susceptibility | Notes |
|-------------|---------------|-------|
| All-cause mortality | Very low | Objective, difficult to influence |
| Lab values (automated) | Low | Objective measurement |
| Clinician-assessed outcomes | Moderate to High | Depends on blinding |
| Patient-reported outcomes | High | Strongly influenced by expectations |
| Composite outcomes | Variable | Depends on subjective components |

---

## Domain 5: Bias in Selection of the Reported Result

### Purpose

Assesses whether the reported result is likely to have been selected from among multiple measurements, analyses, or subsets of data.

### Signaling Questions

| # | Question | Response Options |
|---|----------|-----------------|
| 5.1 | Were the data that produced this result analysed in accordance with a pre-specified analysis plan that was finalized before unblinded outcome data were available for analysis? | Y / PY / PN / N / NI |
| 5.2 | Is the numerical result being assessed likely to have been selected, on the basis of the results, from multiple eligible outcome measurements (e.g. scales, definitions, time points) within the outcome domain? | Y / PY / PN / N / NI |
| 5.3 | Is the numerical result being assessed likely to have been selected, on the basis of the results, from multiple eligible analyses of the data? | Y / PY / PN / N / NI |

### Judgment Algorithm

```
If 5.1 = Y/PY AND 5.2 = N/PN AND 5.3 = N/PN:
  --> Low risk of bias (pre-specified analysis, no evidence of selection)

If 5.1 = NI AND 5.2 = PN AND 5.3 = PN:
  --> Some concerns (no protocol available, but no evidence of selection)

If 5.2 = Y/PY OR 5.3 = Y/PY:
  --> High risk of bias (evidence of selective reporting)

If 5.1 = N/PN AND 5.2 = PN AND 5.3 = PN:
  --> Some concerns (analysis not pre-specified)
```

### Indicators of Selective Reporting

- Discrepancies between protocol/registry and published report (different primary outcome, different analysis method, different time point)
- Outcome mentioned in methods but not reported in results
- Unusual choice of outcome measure or analysis (e.g., change from baseline instead of final values, or vice versa)
- Evidence of data-driven analysis choices (e.g., "we chose to use X because it produced a significant result")
- Composite outcome created post-hoc

---

## Overall Risk of Bias Judgment

### Algorithm

The overall judgment is derived from the five domain-level judgments:

| Scenario | Overall Judgment |
|----------|-----------------|
| All domains are Low risk of bias | **Low risk of bias** |
| Some concerns in at least one domain, but no High risk in any domain | **Some concerns** |
| High risk of bias in at least one domain | **High risk of bias** |
| Some concerns in multiple domains (and together they substantially lower confidence in the result) | **High risk of bias** |

### Decision Rules

```
All domains = Low
  --> Overall: Low risk of bias

At least one domain = Some concerns, no domain = High
  --> Overall: Some concerns
  UNLESS multiple "some concerns" judgments together substantially
  lower confidence --> then Overall: High risk of bias

Any domain = High
  --> Overall: High risk of bias
```

### Important Considerations

- The overall judgment is **not an average** across domains -- a single high-risk domain renders the overall judgment high risk
- Multiple "some concerns" can collectively warrant an overall "high risk" judgment
- The overall judgment should be accompanied by a direction of bias when possible (favors intervention, favors comparator, towards null, away from null, unpredictable)

---

## Presenting RoB 2 Results

### Traffic Light Table

Present domain-level and overall judgments for each study-outcome combination:

```
Study      | D1  | D2  | D3  | D4  | D5  | Overall
-----------|-----|-----|-----|-----|-----|--------
Study A    |  +  |  +  |  +  |  ?  |  +  |   ?
Study B    |  +  |  -  |  +  |  +  |  +  |   -
Study C    |  +  |  +  |  +  |  +  |  ?  |   ?
Study D    |  ?  |  +  |  -  |  +  |  +  |   -

Legend: + = Low risk    ? = Some concerns    - = High risk
```

### Summary Bar Chart

Show the proportion of studies at each risk of bias level, per domain:

```
Domain                  | Low    | Some concerns | High
------------------------|--------|---------------|------
D1: Randomization       | |||||| | |||           |
D2: Deviations          | ||||   | ||||          | ||
D3: Missing data        | |||||  | |||           | ||
D4: Measurement         | |||    | |||||         | ||
D5: Reported result     | ||||   | ||||          | ||
Overall                 | ||     | |||||         | |||
```

### Tools for Visualization

- **robvis:** R package for creating risk of bias visualizations (traffic light plots and weighted bar charts)
- **Cochrane Review Manager (RevMan):** Built-in risk of bias summary and graph tools
- **Excel/Spreadsheet:** Manual creation with conditional formatting

---

## Variants of RoB 2

| Variant | Purpose | Key Differences |
|---------|---------|-----------------|
| RoB 2 for individually randomized parallel-group trials | Standard version | As described above |
| RoB 2 for cluster-randomized trials | Cluster-RCTs | Additional signaling questions about identification/recruitment bias and loss of clusters |
| RoB 2 for crossover trials | Crossover designs | Additional considerations for period effects and carryover |

---

## Common Pitfalls

| Pitfall | Guidance |
|---------|----------|
| Assessing study-level bias instead of result-level bias | RoB 2 is designed for specific results; different outcomes may have different risk of bias |
| Conflating "no information" with "low risk" | Lack of reporting is NOT evidence of low risk; judge as "some concerns" or seek additional information |
| Using RoB 2 for non-randomized studies | Use ROBINS-I for non-randomized studies of interventions |
| Not providing supporting rationale | Every judgment MUST be accompanied by a specific justification referencing the study |
| Assessing overall risk as an average | A single high-risk domain = overall high risk |

---

## Additional Resources

- RoB 2 tool and guidance: https://www.riskofbias.info/welcome/rob-2-0-tool
- RoB 2 Excel template: Available from riskofbias.info
- robvis R package: https://github.com/mcguinlu/robvis
- Cochrane Handbook Chapter 8: https://training.cochrane.org/handbook/current/chapter-08

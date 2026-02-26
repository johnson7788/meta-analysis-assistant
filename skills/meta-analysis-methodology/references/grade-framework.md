# GRADE Evidence Certainty Framework

## Overview

The Grading of Recommendations, Assessment, Development and Evaluations (GRADE) framework is the most widely adopted approach for rating the certainty (quality) of a body of evidence and for grading the strength of recommendations in healthcare. It provides a systematic, transparent, and structured method for moving from evidence to decisions.

**Key References:**
- Guyatt GH, Oxman AD, Vist GE, et al. GRADE: an emerging consensus on rating quality of evidence and strength of recommendations. BMJ. 2008;336(7650):924-926.
- Schunemann HJ, Brozek J, Guyatt G, Oxman AD (editors). GRADE Handbook. Available from https://gdt.gradepro.org/app/handbook/handbook.html

---

## Four Levels of Evidence Certainty

| Level | Symbol | Definition | Interpretation |
|-------|--------|------------|----------------|
| **High** | ++++  | We are very confident that the true effect lies close to that of the estimate of the effect. | Further research is very unlikely to change our confidence in the estimate of effect. |
| **Moderate** | +++O | We are moderately confident in the effect estimate: the true effect is likely to be close to the estimate of the effect, but there is a possibility that it is substantially different. | Further research is likely to have an important impact on our confidence in the estimate of effect and may change the estimate. |
| **Low** | ++OO | Our confidence in the effect estimate is limited: the true effect may be substantially different from the estimate of the effect. | Further research is very likely to have an important impact on our confidence in the estimate of effect and is likely to change the estimate. |
| **Very Low** | +OOO | We have very little confidence in the effect estimate: the true effect is likely to be substantially different from the estimate of effect. | Any estimate of effect is very uncertain. |

---

## Starting Points

The starting certainty level depends on the study design:

| Study Design | Starting Level | Rationale |
|-------------|---------------|-----------|
| Randomized controlled trials (RCTs) | **High** | Randomization controls for confounding and minimizes bias |
| Observational studies (cohort, case-control, cross-sectional) | **Low** | Higher risk of confounding and other biases |

From the starting point, the certainty can be **downgraded** (up to 3 levels) or **upgraded** (up to 3 levels, for observational studies only) based on specific factors.

---

## Five Downgrade Factors

### 1. Risk of Bias (Study Limitations)

Risk of bias refers to systematic errors in the design, conduct, or analysis of included studies that may affect the results.

**Criteria for Downgrading:**

| Severity | Action | Typical Situations |
|----------|--------|-------------------|
| No serious limitations | No downgrade | Most studies at low risk of bias |
| Serious limitations | Downgrade 1 level | Several studies with some concerns; one or more studies at high risk of bias that substantially contribute to the pooled estimate |
| Very serious limitations | Downgrade 2 levels | Most studies at high risk of bias for the outcome |

**Key Domains to Consider:**
- Randomization process (sequence generation, allocation concealment)
- Deviations from intended interventions (blinding, co-interventions)
- Missing outcome data (attrition, ITT analysis)
- Measurement of the outcome (blinding of assessors, objective vs. subjective)
- Selection of the reported result (pre-specification, multiple analyses)

**Decision Factors:**
- Proportion of information from studies at high risk of bias
- Likely direction and magnitude of bias
- Whether sensitivity analysis excluding high-risk studies changes the result

---

### 2. Inconsistency

Inconsistency refers to unexplained heterogeneity in the results across included studies.

**Criteria for Downgrading:**

| Severity | Action | Typical Situations |
|----------|--------|-------------------|
| No serious inconsistency | No downgrade | I2 < 40%; overlapping confidence intervals; consistent direction of effect |
| Serious inconsistency | Downgrade 1 level | I2 = 40-75%; some variation in magnitude; point estimates vary substantially |
| Very serious inconsistency | Downgrade 2 levels | I2 > 75%; conflicting directions of effect; no plausible explanation |

**Factors to Assess:**
- **Magnitude of heterogeneity:** I2 statistic, tau2, prediction interval
- **Direction of effects:** Do all studies point in the same direction?
- **Overlap of confidence intervals:** Do individual study CIs overlap with the pooled estimate?
- **Explained heterogeneity:** Can subgroup analyses or meta-regression explain the variability?

**Important Notes:**
- Do NOT rely solely on I2 -- consider the clinical importance of the observed variation
- If heterogeneity is fully explained by a plausible subgroup analysis, do not downgrade (but consider rating separately for subgroups)
- The prediction interval provides a more informative assessment than I2 alone

---

### 3. Indirectness

Indirectness occurs when the available evidence does not directly address the review question.

**Types of Indirectness:**

| Type | Description | Example |
|------|-------------|---------|
| **Population** | Studied population differs from the target population | Studies in adults applied to pediatric patients |
| **Intervention** | Studied intervention differs from the intervention of interest | Different dose, formulation, or delivery method |
| **Comparator** | Studied comparator differs from the comparator of interest | Active comparator when placebo was of interest |
| **Outcome** | Studied outcome is a surrogate for the outcome of interest | Blood pressure reduction instead of cardiovascular events |
| **Indirect comparison** | No head-to-head comparison; reliance on indirect evidence | Comparing A vs. B through A vs. C and B vs. C |

**Criteria for Downgrading:**

| Severity | Action | Typical Situations |
|----------|--------|-------------------|
| No serious indirectness | No downgrade | Evidence directly addresses the review question |
| Serious indirectness | Downgrade 1 level | One important dimension of indirectness |
| Very serious indirectness | Downgrade 2 levels | Multiple dimensions of indirectness; surrogate outcome with uncertain correlation |

---

### 4. Imprecision

Imprecision refers to the degree of uncertainty around the effect estimate due to random error.

**Criteria for Downgrading:**

| Severity | Action | Typical Situations |
|----------|--------|-------------------|
| No serious imprecision | No downgrade | Confidence interval is narrow; clear clinical decision possible |
| Serious imprecision | Downgrade 1 level | Confidence interval crosses one clinical decision threshold |
| Very serious imprecision | Downgrade 2 levels | Confidence interval crosses both clinical decision thresholds (includes both benefit and harm) |

**Methods for Assessing Imprecision:**

**Approach 1: Clinical Decision Thresholds**
1. Define the minimally important difference (MID) or clinical decision threshold
2. Evaluate whether the confidence interval crosses the threshold
3. If CI crosses the null AND the MID, evidence is imprecise

**Approach 2: Optimal Information Size (OIS)**
1. Calculate the sample size required for an adequately powered individual trial
2. If the total sample size across studies is less than the OIS, consider downgrading
3. Even if the OIS is met, still assess the confidence interval

**Rules of Thumb:**
- For dichotomous outcomes: total events < 300 often indicates imprecision
- For continuous outcomes: total sample < 400 often indicates imprecision
- These are rough guides; always consider the confidence interval width relative to clinical thresholds

---

### 5. Publication Bias

Publication bias occurs when the available studies are a non-representative sample of all studies conducted, typically because studies with non-significant or unfavorable results are less likely to be published.

**Criteria for Downgrading:**

| Severity | Action | Typical Situations |
|----------|--------|-------------------|
| Undetected | No downgrade | Comprehensive search; no evidence of bias |
| Strongly suspected | Downgrade 1 level | Funnel plot asymmetry; significant Egger's test; missing trial register results; predominantly industry-funded studies |
| Very strongly suspected | Downgrade 2 levels (rare) | Very strong evidence of widespread non-publication |

**Evidence Suggesting Publication Bias:**
- Asymmetric funnel plot (visual assessment)
- Significant statistical tests (Egger's, Begg's, Peters')
- Comparison of published results with trial register entries
- Predominantly positive results in a field where null findings are expected
- Predominantly small studies with large effects
- Industry funding with selective outcome reporting

**Important Notes:**
- Funnel plot tests require at least 10 studies to have adequate power
- Funnel plot asymmetry may reflect causes other than publication bias (small-study effects, heterogeneity)
- Absence of evidence for publication bias is not evidence of absence

---

## Three Upgrade Factors (for Observational Studies)

Observational studies start at "Low" certainty. The following factors may warrant upgrading:

### 1. Large Magnitude of Effect

| Magnitude | Action | Criteria |
|-----------|--------|----------|
| Large effect | Upgrade 1 level | RR > 2.0 or RR < 0.5 based on consistent evidence from at least 2 studies with no plausible confounders |
| Very large effect | Upgrade 2 levels | RR > 5.0 or RR < 0.2 based on direct evidence with no major threats to validity |

**Conditions for Upgrading:**
- The effect size is sufficiently large that confounding alone is unlikely to explain it
- The association is consistent across studies
- No important methodological limitations that could produce such a large effect
- The effect is biologically plausible

---

### 2. Dose-Response Gradient

| Evidence | Action | Criteria |
|----------|--------|----------|
| Dose-response present | Upgrade 1 level | A clear gradient between dose/exposure level and outcome across studies or within studies |

**Conditions for Upgrading:**
- A consistent dose-response gradient is observed
- The gradient is biologically plausible
- The relationship is monotonic (increasing dose leads to increasing/decreasing effect)
- Confounding is unlikely to produce the observed gradient

---

### 3. Residual Confounding Would Reduce the Effect

| Evidence | Action | Criteria |
|----------|--------|----------|
| Residual confounding strengthens confidence | Upgrade 1 level | All plausible residual confounders would reduce the observed effect or increase it if no effect was observed |

**Explanation:**
- If all plausible biases would work against the observed effect (i.e., bias would reduce the apparent effect), then the true effect is likely at least as large as observed
- This situation increases confidence in the finding
- Example: If sicker patients receive the treatment and still have better outcomes, uncontrolled confounding by severity would bias toward the null

---

## GRADE Evidence Profile / Summary of Findings Table

### Standard SoF Table Format

```
+--------------+--------+-----------+------+-------+-------+-------+-------+----------+
| Outcome      | No. of | Study     | Risk | Incon | Indir | Impr  | Pub   | Overall  |
| (timeframe)  | studies| design    | of   | sist  | ect   | ecis  | bias  | certainty|
|              |        |           | bias | ency  | ness  | ion   |       |          |
+--------------+--------+-----------+------+-------+-------+-------+-------+----------+
| Outcome 1    | k      | RCT/Obs   | -1   | 0     | 0     | -1    | 0     | Moderate |
| Outcome 2    | k      | RCT/Obs   | 0    | -1    | 0     | 0     | 0     | Moderate |
| Outcome 3    | k      | Obs       | 0    | 0     | -1    | 0     | 0     | Very Low |
+--------------+--------+-----------+------+-------+-------+-------+-------+----------+

0 = no downgrade; -1 = serious (downgrade 1); -2 = very serious (downgrade 2)
```

### Interactive SoF Table (Recommended Format)

| Column | Content |
|--------|---------|
| Outcomes | Outcome name, measurement, follow-up period |
| Number of participants (studies) | Total N (k studies) |
| Relative effect (95% CI) | RR, OR, or HR with CI |
| Anticipated absolute effects: Risk with comparator | Baseline risk per 1000 |
| Anticipated absolute effects: Risk difference with intervention | Absolute difference per 1000 (95% CI) |
| Certainty of evidence | High / Moderate / Low / Very Low |
| What happens (plain language) | Narrative statement of the result |

### Footnotes

Each rating decision should have a corresponding footnote explaining:
- **Why** the evidence was downgraded or upgraded
- **By how much** (1 or 2 levels)
- **Specific details** supporting the judgment

---

## Step-by-Step GRADE Assessment Process

### Step 1: Define the Question
- Use PICO to frame the question
- Identify the most important outcomes (up to 7)

### Step 2: Rate the Starting Certainty
- RCTs start at High
- Observational studies start at Low

### Step 3: Consider Downgrading
For each outcome, assess each of the 5 downgrade domains:
1. Is there serious or very serious risk of bias?
2. Is there serious or very serious inconsistency?
3. Is there serious or very serious indirectness?
4. Is there serious or very serious imprecision?
5. Is there strongly suspected publication bias?

### Step 4: Consider Upgrading (Observational Studies Only)
1. Is there a large or very large magnitude of effect?
2. Is there a dose-response gradient?
3. Would residual confounding reduce the demonstrated effect?

### Step 5: Assign Final Certainty Rating
- Start from the initial level
- Apply downgrades (subtract)
- Apply upgrades if applicable (add)
- Final rating cannot go below Very Low or above High

### Step 6: Construct the Evidence Profile / SoF Table
- Document all judgments and rationale
- Present both relative and absolute effects
- Include plain-language summary statements

---

## Common Mistakes in GRADE Assessment

| Mistake | Correction |
|---------|------------|
| Double-counting risk of bias and inconsistency | Each domain should capture different aspects; do not downgrade for the same issue twice |
| Not defining clinical decision thresholds for imprecision | Pre-specify MIDs before assessing imprecision |
| Using I2 as the sole measure of inconsistency | Consider direction of effects, prediction intervals, and clinical diversity |
| Failing to consider publication bias | Assess for every outcome, even if unable to use statistical tests |
| Downgrading for all domains equally | Some domains may be more important than others for a given outcome |
| Upgrading observational studies without justification | Upgrading is only appropriate when specific criteria are clearly met |
| Confusing certainty of evidence with strength of recommendation | Certainty is about evidence; recommendations also consider values, costs, and feasibility |

---

## GRADE in Practice: Software Tools

| Tool | Purpose | URL |
|------|---------|-----|
| GRADEpro GDT | Create evidence profiles and SoF tables | https://gradepro.org/ |
| MAGIC (MAGICapp) | Guidelines and evidence summaries | https://magicevidence.org/ |
| RevMan | Cochrane review production including GRADE | https://revman.cochrane.org/ |

---

## Additional Resources

- GRADE Working Group: https://www.gradeworkinggroup.org/
- GRADE series in the Journal of Clinical Epidemiology (2011-2013): comprehensive guidance on each domain
- GRADE Handbook: https://gdt.gradepro.org/app/handbook/handbook.html
- BMJ GRADE series: https://www.bmj.com/content/bmj-grade-series

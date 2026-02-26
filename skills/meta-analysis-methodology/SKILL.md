---
name: meta-analysis-methodology
description: |
  This skill should be used when the user discusses meta-analysis methodology, PRISMA guidelines,
  risk of bias assessment, heterogeneity interpretation, effect size selection, evidence grading,
  or any systematic review methodological question. Provides authoritative reference knowledge
  for meta-analysis best practices.
version: 1.0.0
---

# Meta-Analysis Methodology Knowledge Base

This skill provides authoritative reference knowledge for conducting rigorous meta-analyses and
systematic reviews. It covers effect measure selection, statistical model choice, heterogeneity
assessment, reporting standards, risk of bias evaluation, and evidence grading. Use this skill
to ensure methodological decisions align with current best practices and established guidelines.

## When This Skill Applies

- Choosing effect measures (OR vs RR vs MD vs SMD)
- Fixed-effect vs random-effects models
- Interpreting heterogeneity (I², tau², Q)
- PRISMA 2020 reporting requirements
- Risk of bias tools (RoB 2, NOS, QUADAS-2)
- GRADE framework for certainty of evidence
- Special situations (zero events, few studies, missing data)

## Quick Decision Guides

### Effect Measure Selection

| Data Type | Recommended Measure | When to Use |
|---|---|---|
| Binary outcomes | RR (Risk Ratio) | Default for binary data; intuitive interpretation; preferred when baseline risk varies |
| Binary outcomes (case-control) | OR (Odds Ratio) | Case-control studies; rare outcomes where OR approximates RR; logistic regression outputs |
| Continuous (same scale) | MD (Mean Difference) | All studies use the same measurement instrument and units |
| Continuous (different scales) | SMD (Standardized Mean Difference) | Studies use different instruments measuring the same construct (e.g., different depression scales) |
| Time-to-event | HR (Hazard Ratio) | Survival data with censoring; accounts for varying follow-up durations |
| Correlation | Fisher's z | Transform r to Fisher's z for analysis; back-transform for reporting |

**Key considerations:**

- RR is generally preferred over OR for randomized trials because it is more interpretable.
- OR overestimates the effect when the outcome is common (>10%).
- SMD (Hedges' g) includes a small-sample correction and is preferred over Cohen's d.
- Always report effect measures with 95% confidence intervals.

### Model Selection

| Scenario | Recommended Model | Rationale |
|---|---|---|
| Studies are clinically and methodologically similar | Fixed-effect (Mantel-Haenszel) | Assumes one true effect size; weights by inverse variance |
| Studies differ in populations, interventions, or settings | Random-effects (REML + Knapp-Hartung) | Accounts for between-study variance (tau²); wider, more conservative CIs |
| Few studies (k < 5) | Fixed-effect with caution | Random-effects tau² estimate is imprecise with few studies; interpret with caution |
| Very rare events (<1% incidence) | Peto method | Best performance for rare events; avoids zero-cell corrections |
| Rare events with balanced groups | Mantel-Haenszel (no correction) | Performs well without continuity corrections when groups are balanced |

**Key considerations:**

- The Knapp-Hartung adjustment is recommended over the standard DerSimonian-Laird method for random-effects models because it provides more accurate confidence intervals, especially when the number of studies is small.
- REML (Restricted Maximum Likelihood) is the preferred estimator for tau² in most situations.
- A fixed-effect model does not assume homogeneity; it estimates the weighted average effect but does not generalize beyond the included studies.
- When k < 5, consider presenting individual study results alongside any pooled estimate.

### Heterogeneity Interpretation

| I² Range | Interpretation | Recommended Action |
|---|---|---|
| 0-40% | Might not be important | Report I² and Q-test p-value; proceed with pooled estimate |
| 30-60% | Moderate heterogeneity | Explore sources with subgroup analysis or meta-regression; check for clinical diversity |
| 50-90% | Substantial heterogeneity | Investigate causes before pooling; present subgroup results; consider whether pooling is appropriate |
| 75-100% | Considerable heterogeneity | Strong justification needed to pool; focus on exploring sources of heterogeneity; narrative synthesis may be more appropriate |

**Key considerations:**

- I² describes the percentage of variability due to heterogeneity rather than sampling error, but it does not indicate the magnitude of the between-study variance.
- Always report tau² (absolute between-study variance) alongside I² for a complete picture.
- The Q-test (Cochran's Q) has low power when few studies are included; a non-significant Q does not confirm homogeneity.
- Prediction intervals show the range within which the true effect of a future study is expected to fall and should be reported alongside confidence intervals in random-effects meta-analyses.
- Overlap in I² ranges is intentional; interpretation depends on the clinical context and the magnitude of effects.

## PRISMA 2020 Reporting Checklist (Key Items)

The PRISMA 2020 statement (Page et al., BMJ 2021) includes 27 checklist items. The most critical items for meta-analysis reporting are:

1. **Title (Item 1):** Identify the report as a systematic review with or without meta-analysis.
2. **Eligibility criteria (Item 6):** Specify inclusion/exclusion criteria with PICO components.
3. **Information sources (Item 7):** List all databases, registers, and other sources searched.
4. **Search strategy (Item 8):** Present full search strategy for at least one database.
5. **Study selection (Item 9):** State the process for selecting studies (screening, eligibility, inclusion).
6. **Synthesis methods (Item 13):** Describe the meta-analytic methods: effect measure, model, software, handling of heterogeneity.
7. **Risk of bias (Item 11-12):** Specify the tool used and how results were incorporated.
8. **Results of syntheses (Item 20):** Present forest plots with CIs, measures of heterogeneity.
9. **Reporting biases (Item 21):** Present assessments of publication bias (funnel plot, Egger's test).
10. **Certainty of evidence (Item 22):** Present GRADE or equivalent assessment for each outcome.

Always include the PRISMA flow diagram showing study identification, screening, eligibility, and inclusion counts.

## Risk of Bias Assessment Tools

### RoB 2 (Revised Cochrane Risk of Bias Tool for Randomized Trials)

Domains assessed:
1. Randomization process
2. Deviations from intended interventions
3. Missing outcome data
4. Measurement of the outcome
5. Selection of the reported result

Each domain is judged as: Low risk / Some concerns / High risk.
Overall judgment follows the worst domain rating.

### Newcastle-Ottawa Scale (NOS) for Observational Studies

Three categories (maximum 9 stars):
- **Selection** (4 stars): Representativeness, selection of non-exposed, ascertainment of exposure, outcome not present at start
- **Comparability** (2 stars): Comparability based on design or analysis (confounding adjustment)
- **Outcome** (3 stars): Assessment of outcome, follow-up length, adequacy of follow-up

Thresholds (commonly used): 7-9 = good quality, 4-6 = fair quality, 0-3 = poor quality.

### QUADAS-2 (Quality Assessment of Diagnostic Accuracy Studies)

Four domains:
1. Patient selection
2. Index test
3. Reference standard
4. Flow and timing

Each domain is assessed for risk of bias; the first three are also assessed for applicability concerns.

## GRADE Framework for Certainty of Evidence

GRADE (Grading of Recommendations, Assessment, Development, and Evaluations) rates the certainty of evidence for each outcome across studies.

### Starting Rating

- Randomized trials start at **High**.
- Observational studies start at **Low**.

### Factors That Lower Certainty (one or two levels each)

| Factor | Common Reasons to Downgrade |
|---|---|
| Risk of bias | Serious limitations in study design or execution |
| Inconsistency | Unexplained heterogeneity (high I², non-overlapping CIs, different directions of effect) |
| Indirectness | Differences in population, intervention, comparator, or outcome from the review question |
| Imprecision | Wide confidence intervals crossing clinically important thresholds; small sample/few events (OIS not met) |
| Publication bias | Asymmetric funnel plot, significant Egger's test, or evidence of missing studies |

### Factors That Raise Certainty (observational studies only)

| Factor | Description |
|---|---|
| Large magnitude of effect | RR > 2 or RR < 0.5 with no plausible confounders (upgrade one level); RR > 5 or RR < 0.2 (upgrade two levels) |
| Dose-response gradient | Clear dose-response relationship increases confidence |
| Residual confounding | All plausible confounders would reduce the observed effect, strengthening confidence |

### Final Certainty Ratings

| Rating | Definition |
|---|---|
| High | Very confident the true effect lies close to the estimate |
| Moderate | Moderately confident; the true effect is likely close but may be substantially different |
| Low | Limited confidence; the true effect may be substantially different from the estimate |
| Very Low | Very little confidence; the true effect is likely substantially different from the estimate |

## Special Situations

### Zero Events

- Do not use a 0.5 continuity correction by default; it can introduce bias.
- Peto odds ratio performs well for rare events with balanced groups and no substantial heterogeneity in effect sizes.
- Mantel-Haenszel method without continuity correction is recommended when at least one arm has events.
- For double-zero studies (no events in either arm), these are typically excluded from the standard meta-analysis but should be reported and discussed.
- Consider beta-binomial models or exact methods for very rare events.

### Few Studies (k < 5)

- Random-effects estimates of tau² are unreliable with fewer than five studies.
- The Knapp-Hartung adjustment is still recommended but confidence intervals may be very wide.
- Present individual study results prominently.
- Be transparent about the limitations of pooling few studies.
- Consider sensitivity analyses to evaluate the robustness of findings.

### Missing Data

- Contact original study authors when feasible.
- Use available-case analysis as the primary approach.
- Conduct sensitivity analyses assuming best-case and worst-case scenarios for missing data.
- Multiple imputation may be appropriate when the missing data mechanism is understood.
- Report the extent and pattern of missing data across studies.

## Reference Materials

The following reference files in the `references/` directory provide detailed guidance on specific topics:

1. **`effect-size-formulas.md`** -- Formulas and derivations for all common effect size measures (OR, RR, RD, MD, SMD, HR, Fisher's z) including variance estimators and transformations.
2. **`heterogeneity-diagnostics.md`** -- Detailed guidance on computing and interpreting I², tau², Q-statistic, H², and prediction intervals, with decision rules for subgroup and sensitivity analyses.
3. **`prisma-2020-checklist.md`** -- Complete PRISMA 2020 27-item checklist with explanations and examples for each item, adapted for meta-analysis reporting.
4. **`risk-of-bias-guides.md`** -- Step-by-step instructions for applying RoB 2, NOS, and QUADAS-2, including signaling questions and worked domain-level judgment examples.
5. **`grade-evidence-tables.md`** -- Templates and worked examples for constructing GRADE Summary of Findings tables, with guidance on rating each domain and documenting judgments.
6. **`publication-bias-methods.md`** -- Methods for assessing and addressing publication bias including funnel plots, Egger's regression, trim-and-fill, selection models (Vevea-Hedges), and p-curve analysis.

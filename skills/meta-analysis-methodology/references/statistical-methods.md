# Statistical Methods Reference for Meta-Analysis

## Overview

This reference provides the key statistical formulas, models, and methods used in meta-analysis. It covers effect size calculation, pooling methods, heterogeneity assessment, and methods for evaluating publication bias and handling special situations.

---

## 1. Effect Size Measures and Formulas

### 1.1 Dichotomous Outcomes

#### Odds Ratio (OR)

The odds ratio compares the odds of an event in the intervention group to the odds in the control group.

```
        a / b       a * d
OR  =  -------  =  -------
        c / d       b * c

Where (2x2 table):
                Event   No Event
Intervention      a        b        n1 = a + b
Control           c        d        n2 = c + d

ln(OR) = ln(a*d) - ln(b*c)

SE(ln(OR)) = sqrt(1/a + 1/b + 1/c + 1/d)

95% CI for ln(OR): ln(OR) +/- 1.96 * SE(ln(OR))
95% CI for OR: exp(ln(OR) +/- 1.96 * SE(ln(OR)))
```

**Properties:**
- Range: 0 to infinity; OR = 1 indicates no effect
- Symmetric on log scale: OR = 2.0 and OR = 0.5 are equidistant from null
- Invariant to which outcome is coded as the "event"
- Overestimates RR when events are common (> 10%)

#### Risk Ratio (Relative Risk, RR)

The risk ratio compares the probability of an event in the intervention group to the probability in the control group.

```
        a / n1       a * (c + d)
RR  =  --------  =  -----------
        c / n2       c * (a + b)

Where:
  n1 = a + b (total in intervention group)
  n2 = c + d (total in control group)

ln(RR) = ln(a/n1) - ln(c/n2)

SE(ln(RR)) = sqrt(1/a - 1/n1 + 1/c - 1/n2)
           = sqrt(b/(a*n1) + d/(c*n2))

95% CI for RR: exp(ln(RR) +/- 1.96 * SE(ln(RR)))
```

**Properties:**
- Range: 0 to infinity; RR = 1 indicates no effect
- More intuitive than OR for clinicians
- Cannot be computed from case-control studies
- Depends on which outcome is selected as the "event"

#### Risk Difference (RD)

The risk difference (absolute risk reduction) is the difference in event rates between groups.

```
RD = a/n1 - c/n2

SE(RD) = sqrt((a*b)/n1^3 + (c*d)/n2^3)

95% CI for RD: RD +/- 1.96 * SE(RD)

Number Needed to Treat (NNT) = 1 / |RD|
```

**Properties:**
- Range: -1 to +1; RD = 0 indicates no effect
- Provides absolute measure of effect (clinically interpretable)
- Depends on baseline risk
- NNT is directly derivable from RD

---

### 1.2 Continuous Outcomes

#### Mean Difference (MD)

The mean difference (also called weighted mean difference) is the difference in means between groups when the same measurement scale is used.

```
MD = X_intervention - X_control

SE(MD) = sqrt(SD1^2/n1 + SD2^2/n2)

95% CI for MD: MD +/- 1.96 * SE(MD)
```

**Properties:**
- Retains the original unit of measurement
- Directly interpretable
- Requires studies to use the same measurement instrument/scale

#### Standardized Mean Difference (SMD)

The standardized mean difference is used when studies measure the same construct on different scales. It expresses the effect in standard deviation units.

**Cohen's d:**
```
d = (X_intervention - X_control) / SD_pooled

SD_pooled = sqrt(((n1-1)*SD1^2 + (n2-1)*SD2^2) / (n1 + n2 - 2))

SE(d) = sqrt(n1+n2)/(n1*n2) + d^2/(2*(n1+n2)))
```

**Hedges' g (bias-corrected):**
```
g = d * J

J = 1 - 3/(4*(n1+n2-2) - 1)    (correction factor)

SE(g) = sqrt((n1+n2)/(n1*n2) + g^2/(2*(n1+n2-2)))
```

**Interpretation of SMD (Cohen's conventions):**

| SMD | Interpretation |
|-----|---------------|
| 0.2 | Small effect |
| 0.5 | Medium effect |
| 0.8 | Large effect |

**Properties:**
- Unitless; allows pooling of different scales
- Hedges' g corrects for small-sample upward bias in Cohen's d
- Interpretation can be less intuitive than MD
- Assumes equal variances across groups (pooled SD)

---

### 1.3 Time-to-Event Outcomes

#### Hazard Ratio (HR)

```
ln(HR) and SE(ln(HR)) are typically extracted from study reports.

If not directly reported, can be estimated from:
- Kaplan-Meier curves (using methods by Parmar, Tierney, or Guyot)
- O-E and V statistics: ln(HR) = (O-E)/V; SE(ln(HR)) = 1/sqrt(V)
- P-values and event counts

95% CI for HR: exp(ln(HR) +/- 1.96 * SE(ln(HR)))
```

---

### 1.4 Correlation

#### Correlation Coefficient (r)

For meta-analysis, Fisher's z-transformation is used:

```
z = 0.5 * ln((1+r)/(1-r))    (Fisher's z transformation)

SE(z) = 1/sqrt(n-3)

95% CI for z: z +/- 1.96 * SE(z)

Back-transform to r: r = (exp(2*z) - 1) / (exp(2*z) + 1)
```

---

## 2. Fixed-Effect Models

Fixed-effect models assume that all studies estimate the same underlying true effect.

### 2.1 Inverse Variance Method (Generic)

The inverse variance method is a general approach applicable to any type of effect measure.

```
Pooled estimate:
  theta_hat = sum(w_i * theta_i) / sum(w_i)

Where:
  theta_i = effect estimate from study i
  w_i = 1 / SE_i^2  (inverse variance weight)
  SE_i = standard error of study i's estimate

SE of pooled estimate:
  SE(theta_hat) = 1 / sqrt(sum(w_i))

95% CI: theta_hat +/- 1.96 * SE(theta_hat)

z-test: z = theta_hat / SE(theta_hat)
P-value: 2 * (1 - Phi(|z|))
```

### 2.2 Mantel-Haenszel Method

The Mantel-Haenszel method is specifically designed for combining 2x2 tables and is more robust than the inverse variance method when data are sparse.

**Mantel-Haenszel Odds Ratio:**
```
OR_MH = sum(a_i * d_i / N_i) / sum(b_i * c_i / N_i)

Where N_i = a_i + b_i + c_i + d_i (total for study i)

SE(ln(OR_MH)):
  Robins, Breslow, and Greenland (1986) formula:

  Let:
    R_i = a_i * d_i / N_i
    S_i = b_i * c_i / N_i
    P_i = (a_i + d_i) / N_i
    Q_i = (b_i + c_i) / N_i

  Var(ln(OR_MH)) =
    sum(P_i*R_i) / (2*(sum(R_i))^2) +
    sum(P_i*S_i + Q_i*R_i) / (2*sum(R_i)*sum(S_i)) +
    sum(Q_i*S_i) / (2*(sum(S_i))^2)
```

**Mantel-Haenszel Risk Ratio:**
```
RR_MH = sum(a_i * n2_i / N_i) / sum(c_i * n1_i / N_i)

SE(ln(RR_MH)):
  Greenland and Robins (1985) formula

  Var(ln(RR_MH)) =
    sum((n1_i*n2_i*(a_i+c_i) - a_i*c_i*N_i) / N_i^2) /
    (sum(a_i*n2_i/N_i) * sum(c_i*n1_i/N_i))
```

**Mantel-Haenszel Risk Difference:**
```
RD_MH = sum(w_i * RD_i) / sum(w_i)

Where:
  w_i = n1_i * n2_i / N_i
  RD_i = a_i/n1_i - c_i/n2_i
```

**Advantages of Mantel-Haenszel:**
- More robust with sparse data (small sample sizes, rare events)
- Does not require continuity corrections for zero cells
- Well-established statistical properties
- Default method in Cochrane reviews for dichotomous outcomes

### 2.3 Peto Method

The Peto method is an approximation for pooling odds ratios, particularly useful for rare events.

```
ln(OR_Peto) = sum(O_i - E_i) / sum(V_i)

Where for each study i:
  O_i = a_i (observed events in intervention group)
  E_i = n1_i * (a_i + c_i) / N_i (expected events under null)
  V_i = n1_i * n2_i * (a_i + c_i) * (b_i + d_i) / (N_i^2 * (N_i - 1))

SE(ln(OR_Peto)) = 1 / sqrt(sum(V_i))

95% CI: exp(ln(OR_Peto) +/- 1.96 / sqrt(sum(V_i)))
```

**Advantages:**
- Handles zero cells without corrections
- Performs well with rare events (event rate < 1%)
- Does not require estimation of the variance for individual studies

**Limitations:**
- Biased when the true OR is far from 1
- Biased when group sizes are very unequal
- Only applicable to odds ratios
- Should not be used when treatment effects are large (OR > 2 or OR < 0.5)

---

## 3. Random-Effects Models

Random-effects models assume that the true effect varies across studies, following a distribution (typically normal) with mean mu and between-study variance tau-squared.

### 3.1 DerSimonian-Laird Method

The most commonly used random-effects method. It uses a method-of-moments estimator for tau-squared.

```
Step 1: Calculate the fixed-effect weights and pooled estimate
  w_i = 1/SE_i^2
  theta_FE = sum(w_i * theta_i) / sum(w_i)

Step 2: Calculate Cochran's Q
  Q = sum(w_i * (theta_i - theta_FE)^2)

Step 3: Estimate tau-squared
  tau^2 = max(0, (Q - (k-1)) / (sum(w_i) - sum(w_i^2)/sum(w_i)))

  Where k = number of studies

Step 4: Calculate random-effects weights
  w_i* = 1 / (SE_i^2 + tau^2)

Step 5: Calculate random-effects pooled estimate
  theta_RE = sum(w_i* * theta_i) / sum(w_i*)

  SE(theta_RE) = 1 / sqrt(sum(w_i*))

  95% CI: theta_RE +/- 1.96 * SE(theta_RE)
```

**Properties:**
- Computationally simple
- Most widely implemented in software
- Tends to underestimate tau-squared with few studies
- CIs may have less than nominal coverage, especially with few studies

### 3.2 Restricted Maximum Likelihood (REML)

REML provides a less biased estimate of tau-squared by iteratively maximizing the restricted log-likelihood.

```
The restricted log-likelihood:
  l_R(tau^2) = -0.5 * [sum(ln(SE_i^2 + tau^2)) +
                ln(sum(1/(SE_i^2 + tau^2))) +
                sum((theta_i - theta_hat)^2 / (SE_i^2 + tau^2))]

Where theta_hat is the weighted mean using weights w_i* = 1/(SE_i^2 + tau^2)

tau^2 is estimated by iterating until convergence:

  tau^2_(new) = tau^2_(old) +
    [sum(w_i*^2 * ((theta_i - theta_hat)^2 - (SE_i^2 + tau^2))) / sum(w_i*^2)] *
    [1 / (sum(w_i*^2) / sum(w_i*) - sum(w_i*^3) / sum(w_i*^2))]
```

**Properties:**
- Less biased estimate of tau-squared than DerSimonian-Laird
- Recommended by many methodologists as the preferred method
- Requires iterative computation
- Confidence intervals may still have suboptimal coverage with few studies

### 3.3 Hartung-Knapp-Sidik-Jonkman (HKSJ) Adjustment

The HKSJ method modifies the confidence interval calculation to use a t-distribution instead of a normal distribution, providing better coverage.

```
Standard random-effects CI (Wald-type):
  theta_RE +/- z_(1-alpha/2) * SE(theta_RE)

HKSJ-adjusted CI:
  theta_RE +/- t_(k-1, 1-alpha/2) * SE_HKSJ(theta_RE)

Where:
  SE_HKSJ^2(theta_RE) = (1/(k-1)) * sum(w_i* * (theta_i - theta_RE)^2) / sum(w_i*)

  k = number of studies
  t_(k-1, 1-alpha/2) = critical value from t-distribution with k-1 degrees of freedom
```

**Properties:**
- Wider, more conservative confidence intervals
- Better nominal coverage, especially with few studies
- Recommended when the number of studies is small (< 10)
- Can produce CIs that exclude the point estimate when heterogeneity is very low (use with Wald-type CI as a fallback)

### 3.4 Other Random-Effects Estimators

| Method | Description |
|--------|-------------|
| Paule-Mandel (PM) | Iterative method; performs well in simulations |
| Empirical Bayes (EB) | Maximum likelihood approach to tau-squared estimation |
| Sidik-Jonkman (SJ) | Non-iterative estimator |
| Hunter-Schmidt | Commonly used in psychology; weights by sample size |
| Maximum Likelihood (ML) | Full ML (tends to underestimate tau-squared) |

---

## 4. Heterogeneity Measures

### 4.1 Cochran's Q Statistic

Tests the null hypothesis that all studies share a common effect size.

```
Q = sum(w_i * (theta_i - theta_FE)^2)

Under H0: Q ~ chi-squared with df = k - 1

P-value: P(chi^2_(k-1) >= Q)
```

**Properties:**
- Low statistical power when few studies are included
- Excessive power when many large studies are included
- Provides a test (yes/no) but not a measure of the degree of heterogeneity
- A non-significant Q does not mean heterogeneity is absent

### 4.2 I-Squared (I2)

Describes the percentage of total variability due to between-study heterogeneity rather than chance.

```
I^2 = max(0, (Q - (k-1)) / Q) * 100%

Or equivalently:
I^2 = max(0, (Q - df) / Q) * 100%

Where df = k - 1

95% CI for I^2 (test-based):
  Use the chi-squared distribution to derive CI for Q, then transform to I^2

Rough interpretation:
  0-40%:   Might not be important
  30-60%:  Moderate heterogeneity
  50-90%:  Substantial heterogeneity
  75-100%: Considerable heterogeneity
```

**Properties:**
- Scale-free (0-100%)
- Does not depend on the number of studies
- Does not indicate the magnitude of heterogeneity on the effect size scale
- Overlapping interpretation ranges are intentional (context matters)
- CI can be very wide with few studies

### 4.3 Tau-Squared (tau2)

The estimated between-study variance.

```
DerSimonian-Laird estimator:
  tau^2 = max(0, (Q - (k-1)) / (sum(w_i) - sum(w_i^2)/sum(w_i)))

Tau (standard deviation):
  tau = sqrt(tau^2)
```

**Properties:**
- On the same scale as the effect measure (squared)
- Interpretable: tau represents the SD of the distribution of true effects
- Directly used in random-effects weights: w_i* = 1/(SE_i^2 + tau^2)
- Can be used to calculate the prediction interval

### 4.4 H-Squared (H2)

```
H^2 = Q / (k - 1)

H = sqrt(H^2)

I^2 = (H^2 - 1) / H^2
```

**Properties:**
- H2 = 1 when there is no heterogeneity
- H2 > 1 indicates heterogeneity
- Mathematically related to I-squared

### 4.5 Prediction Interval

The prediction interval estimates the range within which the true effect of a **new** study would fall with 95% probability.

```
95% Prediction Interval:
  theta_RE +/- t_(k-2, 0.975) * sqrt(tau^2 + SE(theta_RE)^2)

Where:
  t_(k-2, 0.975) = critical value from t-distribution with k-2 df
  tau^2 = between-study variance
  SE(theta_RE) = standard error of pooled estimate
```

**Properties:**
- Always wider than the confidence interval for the pooled effect
- Provides a more complete picture of heterogeneity than I-squared
- Especially informative for clinical decision-making (tells you about the range of possible effects)
- Requires at least 3 studies; most useful with 5+ studies
- Can include clinically important effects in both directions even when the CI is narrow

---

## 5. Subgroup Analysis

### 5.1 Fixed-Effect Test for Subgroup Differences

```
Q_between = Q_total - sum(Q_within_j)

Where:
  Q_total = Cochran's Q for all studies combined
  Q_within_j = Cochran's Q within subgroup j

  Or equivalently:
  Q_between = sum(w_j * (theta_j - theta_overall)^2)

  Where:
    theta_j = pooled effect in subgroup j
    w_j = 1/SE_j^2 (inverse variance weight for subgroup j)
    theta_overall = overall pooled effect

df = number of subgroups - 1

P-value: P(chi^2_df >= Q_between)
```

### 5.2 Random-Effects Test for Subgroup Differences

```
When using a random-effects model within subgroups, the test for
subgroup differences should account for the within-subgroup
random-effects weights:

Q_between = sum(w_j* * (theta_j_RE - theta_overall_RE)^2)

Where w_j* uses the random-effects standard errors
```

### 5.3 Interpretation Guidelines

| Consideration | Guidance |
|--------------|---------|
| Number of comparisons | Adjust for multiple testing or interpret cautiously |
| Pre-specification | Pre-specified subgroups are more credible than post-hoc |
| Biological plausibility | Is the subgroup effect biologically plausible? |
| Within-study vs. between-study | Within-study subgroups are more reliable |
| Consistency | Is the pattern consistent across studies? |
| Size of interaction | Is the difference clinically meaningful? |
| Statistical power | Subgroup tests often have low power |

---

## 6. Meta-Regression

### 6.1 Basic Model

Meta-regression extends the random-effects model by including study-level covariates.

```
theta_i = beta_0 + beta_1 * X_i + zeta_i + epsilon_i

Where:
  theta_i = observed effect in study i
  beta_0 = intercept
  beta_1 = regression coefficient
  X_i = covariate value for study i
  zeta_i ~ N(0, tau^2_residual) (between-study random effect)
  epsilon_i ~ N(0, SE_i^2) (within-study sampling error)
```

### 6.2 Estimation

```
Weighted least squares with random-effects weights:

beta = (X'WX)^(-1) X'W theta

Where:
  W = diag(1/(SE_i^2 + tau^2_residual))
  X = design matrix (including intercept and covariates)
  theta = vector of observed effects

tau^2_residual is estimated iteratively (e.g., REML)
```

### 6.3 R-Squared Analog

```
R^2 = max(0, (tau^2_total - tau^2_residual) / tau^2_total) * 100%

Where:
  tau^2_total = between-study variance from model without covariates
  tau^2_residual = residual between-study variance from meta-regression model
```

### 6.4 Practical Guidelines

- **Minimum studies per covariate:** At least 10 studies per covariate (some recommend 6-10)
- **Ecological fallacy:** Study-level associations may not reflect individual-level associations
- **Multiple testing:** Limit the number of covariates; adjust for multiple comparisons
- **Pre-specification:** Pre-specify covariates and the direction of expected associations
- **Multicollinearity:** Check for correlation between covariates
- **Permutation tests:** Use permutation-based P-values when number of studies is small

---

## 7. Publication Bias Methods

### 7.1 Funnel Plot

A scatter plot of effect size versus precision (typically standard error on the reversed y-axis).

```
Y-axis (inverted): Standard Error (largest at bottom)
  ^
  | small SE     *   *  *  *
  |             *  * * *  *
  |            *  *  *  * *  *
  |          *   *  *  *  *   *
  | large SE  *     *      *   *
  +-----+---------|----------+---->
        0       Effect      X-axis

Symmetric: No evidence of publication bias
Asymmetric (gap in bottom-right): Possible publication bias
```

**Components:**
- X-axis: Effect size (e.g., log OR, log RR, SMD)
- Y-axis: Measure of precision, typically SE (inverted so larger studies are at top)
- Vertical line: Pooled effect estimate
- Diagonal lines: Pseudo 95% confidence limits (pooled effect +/- 1.96*SE)

### 7.2 Egger's Test

A regression-based test for funnel plot asymmetry.

```
Egger's regression:
  theta_i / SE_i = beta_0 + beta_1 * (1/SE_i) + epsilon_i

Or equivalently (weighted regression):
  theta_i = beta_0 * SE_i + beta_1 + epsilon_i

Test: H0: beta_0 = 0 (no asymmetry)
  t = beta_0 / SE(beta_0)
  P-value from t-distribution with k-2 degrees of freedom

Significant P-value (< 0.10 conventionally): evidence of asymmetry
```

**Properties:**
- Recommended for continuous outcomes
- Requires at least 10 studies for adequate power
- Should not be used for odds ratios (use Peters' or Harbord's test instead)
- P < 0.10 is the conventional significance threshold (lower power)

### 7.3 Begg's Test (Rank Correlation)

```
Test statistic: Kendall's tau between the effect size and its variance

tau = (concordant pairs - discordant pairs) / (k*(k-1)/2)

Adjusted for ties:
  z = tau / SE(tau)

SE(tau) = sqrt(2*(2k+5) / (9*k*(k-1)))

P-value from standard normal distribution
```

**Properties:**
- Non-parametric rank-based test
- Lower power than Egger's test
- Less sensitive to outliers
- Requires at least 10 studies

### 7.4 Peters' Test

Alternative to Egger's for dichotomous outcomes (less susceptible to the mathematical relationship between OR and its SE).

```
Peters' regression:
  theta_i = beta_0 + beta_1 * (1/n_total_i) + epsilon_i

Where n_total_i is the total sample size of study i
Weighted by the inverse of the variance of theta_i

Test: H0: beta_1 = 0
```

### 7.5 Trim-and-Fill Method

An iterative procedure that estimates the number of "missing" studies and imputes them to produce an adjusted pooled estimate.

```
Algorithm:
1. Rank studies by their distance from the pooled estimate
2. Trim the most extreme small studies on the side of asymmetry
3. Re-estimate the pooled effect from the remaining studies
4. Iterate until the pooled estimate stabilizes
5. "Fill" in the missing studies (mirror images of the trimmed studies)
6. Re-calculate the pooled effect including the imputed studies

Output:
- Estimated number of missing studies (k0)
- Adjusted pooled effect estimate
- Adjusted confidence interval
```

**Properties:**
- Provides a visual and quantitative adjustment
- Assumption: the asymmetry is caused by publication bias (may not be true)
- Imputed studies are hypothetical; interpret with caution
- Can produce misleading results if asymmetry is caused by heterogeneity rather than bias

### 7.6 Selection Models

```
Copas selection model:
- Models the probability that a study is published as a function of
  its effect size and standard error
- Uses a probit model for the selection process
- Provides adjusted estimates under various assumed selection mechanisms

Vevea and Hedges weight-function model:
- Specifies weight functions for the probability of publication
  as a step function of p-values
- Common cut-points: p < 0.025 (one-tailed significant), p < 0.05, etc.
- Can model different degrees of selection severity
```

### 7.7 PET-PEESE

```
Precision-Effect Test (PET):
  theta_i = beta_0 + beta_1 * SE_i + epsilon_i
  (Weighted by 1/SE_i^2)

  If PET is significant (beta_0 != 0), use:

Precision-Effect Estimate with Standard Error (PEESE):
  theta_i = beta_0 + beta_1 * SE_i^2 + epsilon_i
  (Weighted by 1/SE_i^2)

  beta_0 from PET or PEESE = bias-adjusted effect estimate
```

---

## 8. Special Situations

### 8.1 Zero Events

When one or both arms of a study have zero events, standard formulas fail. Approaches:

**Continuity Correction:**
```
Add a small constant (typically 0.5) to all cells of the 2x2 table:

        Event   No Event
Interv.  a+0.5   b+0.5
Control  c+0.5   d+0.5

Alternative: use treatment-arm continuity correction (proportional to group sizes):
  cc_1 = n2/(n1+n2)  (added to intervention group cells)
  cc_2 = n1/(n1+n2)  (added to control group cells)
```

**Peto Method:**
- Handles single-zero cells naturally without continuity corrections
- Preferred when events are very rare (< 1%)
- Avoid when OR is large or group sizes are very unequal

**Mantel-Haenszel Method:**
- Handles single-zero cells without corrections
- More robust than inverse variance for sparse data

**Double-Zero Studies:**
- Studies with zero events in both arms carry no information about the relative effect
- Typically excluded from meta-analysis (but report their exclusion)
- Including them with continuity corrections can bias results
- Consider beta-binomial models or exact methods for very rare events

**Dedicated Methods for Rare Events:**
- Exact conditional methods
- Bayesian approaches with informative priors
- Generalized linear mixed models (GLMM)
- Beta-binomial model (Stijnen et al.)

### 8.2 Few Studies (k < 5)

When only a few studies are available:

| Issue | Recommendation |
|-------|---------------|
| Heterogeneity estimation | tau^2 estimates are imprecise; consider fixed-effect model if studies are clinically similar |
| Confidence intervals | Use HKSJ adjustment (t-distribution) for random-effects CIs |
| Publication bias tests | Not recommended (< 10 studies); assess qualitatively |
| Subgroup analysis | Not recommended (insufficient power) |
| Meta-regression | Not recommended (need at least 10 studies per covariate) |
| Overall approach | Consider narrative synthesis; present forest plot without pooled estimate if pooling is questionable |

### 8.3 Missing Standard Deviations

When SDs are not reported, they may be estimated from other statistics:

**From Standard Error (SE):**
```
SD = SE * sqrt(n)
```

**From 95% Confidence Interval:**
```
SE = (upper - lower) / (2 * 1.96)
SD = SE * sqrt(n)
```

**From Interquartile Range (IQR):**
```
Wan et al. (2014) method:
  For n > 70:  SD approximately = IQR / 1.35
  For smaller n: SD = (Q3 - Q1) / (2 * Phi^(-1)((0.75*n - 0.125)/(n + 0.25)))
```

**From Range (minimum to maximum):**
```
Hozo et al. (2005) for small samples:
  SD approximately = Range / 4  (for n < 70)
  SD approximately = Range / 6  (for n > 70)

Wan et al. (2014) improved estimator:
  SD = Range / (2 * Phi^(-1)((n - 0.375)/(n + 0.25)))
```

**From Median and IQR (Luo et al., 2018; Wan et al., 2014):**
```
Mean approximately = (Q1 + Median + Q3) / 3  (for symmetric data)

For skewed data, more complex methods are available
(e.g., McGrath et al., 2020; Shi et al., 2020)
```

**From P-value and Sample Size:**
```
t = t-value corresponding to the P-value with df = n1 + n2 - 2

MD = t * sqrt(SD_pooled^2 * (1/n1 + 1/n2))

If only P and n are available:
  SE = MD / t  (or use the z-approximation for large samples)
```

**Borrowing SDs:**
- Use the pooled SD from other studies in the same meta-analysis
- Use SDs from external reference populations
- Use the median SD from included studies
- Document the imputation method and conduct sensitivity analysis

### 8.4 Combining Different Effect Measures

When studies report different effect measures:

**OR to SMD conversion:**
```
SMD = ln(OR) * sqrt(3) / pi

SE(SMD) = SE(ln(OR)) * sqrt(3) / pi
```

**SMD to OR conversion:**
```
ln(OR) = SMD * pi / sqrt(3)

SE(ln(OR)) = SE(SMD) * pi / sqrt(3)
```

**Converting Between RR and OR:**
```
OR = RR * (1 - p_control) / (1 - RR * p_control)

Where p_control = baseline risk in the control group
```

### 8.5 Multi-Arm Studies

When studies have more than two treatment arms:

```
Approaches:
1. Select the most relevant pair of arms (pre-specify criteria)
2. Combine arms (e.g., pool all intervention arms vs. control)
   - For dichotomous data: add events and totals
   - For continuous data: use combined mean and SD formulas:

     N_combined = N1 + N2
     Mean_combined = (N1*M1 + N2*M2) / (N1 + N2)
     SD_combined = sqrt(((N1-1)*SD1^2 + (N2-1)*SD2^2 +
                    N1*N2*(M1-M2)^2/(N1+N2)) / (N1+N2-1))

3. Include all arms but adjust for correlation (advanced: multivariate methods)
4. Split the shared control group (not recommended; loses precision)
```

### 8.6 Crossover Trials

```
For crossover designs, the within-participant comparison is used:

MD = Mean_intervention - Mean_control (within-person)

SE(MD) = SD_diff / sqrt(n)

Where:
  SD_diff = SD of the within-person differences

If SD_diff is not reported:
  SD_diff = sqrt(SD1^2 + SD2^2 - 2*r*SD1*SD2)

  Where r = within-person correlation (often assumed 0.5 if not reported)

When combining crossover and parallel trials:
- Use the within-person effect and SE for crossover trials
- Use the between-group effect and SE for parallel trials
- Combine using standard meta-analysis methods
```

### 8.7 Cluster-Randomized Trials

```
Design effect:
  DE = 1 + (m - 1) * ICC

Where:
  m = average cluster size
  ICC = intraclass correlation coefficient

Effective sample size:
  n_effective = n / DE

For dichotomous outcomes:
  Adjust the number of events and total sample size by the design effect

For continuous outcomes:
  Inflate the SE by sqrt(DE):
  SE_adjusted = SE * sqrt(DE)

If ICC is not reported:
  Use ICC from similar studies or a plausible range
  Conduct sensitivity analysis across a range of ICC values
```

---

## 9. Software Reference

| Software | Type | Key Features |
|----------|------|-------------|
| Python (numpy, scipy, statsmodels, matplotlib, forestplot) | Free (open source) | **本项目首选**；灵活可编程；支持 REML、DL 等估计方法；完整发表偏倚检测；与数据科学生态无缝集成 |
| RevMan (Review Manager) | Free (Cochrane) | Standard for Cochrane reviews; forest plots; risk of bias |
| R (metafor, meta, dmetar) | Free (open source) | Comprehensive; flexible; publication bias tests; meta-regression |
| Stata (metan, metaan, admetan) | Commercial | Flexible; many user-written commands; funnel plots |
| Comprehensive Meta-Analysis (CMA) | Commercial | User-friendly GUI; extensive effect size calculator |
| OpenMeta[Analyst] | Free | GUI-based; standard meta-analysis methods |
| JASP | Free | Bayesian and frequentist meta-analysis; GUI-based |

---

## 10. Quick Formula Reference Card

```
+-------------------+---------------------------------------+---------------------------+
| Measure           | Point Estimate                        | Standard Error            |
+-------------------+---------------------------------------+---------------------------+
| OR (log scale)    | ln(ad/bc)                             | sqrt(1/a+1/b+1/c+1/d)    |
| RR (log scale)    | ln((a/n1)/(c/n2))                     | sqrt(b/(a*n1)+d/(c*n2))   |
| RD                | a/n1 - c/n2                           | sqrt(ab/n1^3 + cd/n2^3)   |
| MD                | X1 - X2                               | sqrt(SD1^2/n1+SD2^2/n2)   |
| SMD (Hedges' g)   | J * (X1-X2)/SD_pooled                 | sqrt(N/(n1*n2)+g^2/(2*N)) |
| Correlation (z)   | 0.5*ln((1+r)/(1-r))                  | 1/sqrt(n-3)               |
+-------------------+---------------------------------------+---------------------------+
| I^2               | max(0, (Q-df)/Q) * 100%              | --                        |
| tau^2 (DL)        | max(0,(Q-df)/(sum(w)-sum(w^2)/sum(w)))| --                        |
| Prediction Int.   | theta +/- t_(k-2)*sqrt(tau^2+SE^2)   | --                        |
+-------------------+---------------------------------------+---------------------------+

Where: N = n1+n2; df = k-1; J = 1-3/(4*df_pooled-1)
```

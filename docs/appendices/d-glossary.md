# Appendix D — Glossary, Mathematical Appendices, Further Reading, Reporting Checklists

## Purpose

A field guide to the words, the three pieces of mathematics the rest of the book leans on, a reading list that is not a cargo cult, and four mini-checklists you can put next to a manuscript. Definitions are operational. If a term here disagrees with a chapter, the chapter’s worked example wins.

Educational only. Checklists are memory aids, not official society policy and not a license to submit.

---

## Glossary

**Action set.** The discrete things you can still do. Treat, test, wait, stop, go. A posterior without an action set is a hobby.

**Adaptive design.** A trial that uses accumulating data to change allocation, sample size, or stopping. The likelihood may remain valid; the usual fixed-\(n\) standard error story does not.

**Anchoring.** Staying too close to the first number seen. The first NIHSS, the first radiologist’s adjective, last year’s base rate.

**Availability.** Judging probability by the ease of recall. The last fatal tPA ICH you saw is not a likelihood.

**Base rate.** \(P(\text{state})\) in the relevant class before the new datum. The number residents skip.

**Base-rate neglect.** Reporting a likelihood (or a stereotype) as a posterior.

**Bayes’ theorem.** \(p(\theta \mid y) \propto p(y \mid \theta)\, p(\theta)\). Odds form: posterior odds \(=\) prior odds \(\times\) LR.

**Bayesian workflow.** The computational cousin of Chapter 19: specify, fit, check, modify, decide. Not a synonym for “we used `brms`.”

**Brier score.** Mean squared error of a probability. A calibration-friendly proper scoring rule.

**Calibration.** Among days you said 0.30, the event happened about 30% of the time. Discrimination can be fine while calibration is not.

**cmdstanr.** R interface to CmdStan. Preferred `brms` backend in this book.

**Commensurate prior.** A hierarchical device for borrowing from historical data that lets the current data down-weight the history when they disagree.

**Complete-case analysis.** Dropping rows with missing covariates. Biased when missingness is informative (Chapter 19, CTA).

**Conjugate prior.** A prior that stays in the same family after the likelihood: Beta with binomial, Normal with Normal known-variance.

**Conversation.** Step 8. The posterior and the threshold in a sentence a non-statistician can use.

**Credible interval.** A posterior interval. This book prefers highest-density intervals (HDIs) on the decision scale.

**CRIT-APP.** The curriculum’s structured critical-appraisal companion: design, selection, intervention, outcome, follow-up, analysis, applicability, abstract honesty. It moves priors. It does not pick Friday’s cutoff.

**Decision threshold.** The posterior probability (or expected utility) at which the action flips. Diagnostic and treatment thresholds are different objects (Chapters 5–6).

**De-identification.** Removing or coarsening identifiers so a derived table can be shared. “We took the names off” is not it (Chapter 20).

**Discrimination.** Whether scores rank events above non-events (AUROC). Not a utility.

**Divergent transition.** A Stan warning that the sampler left the typical set. Do not interpret a fit full of them.

**Effect prior.** A prior on a treatment contrast, distinct from a diagnostic prior on a state.

**Elicitation.** Writing a prior from expert judgment on an observable scale before the new data are shown (Appendix B).

**ESUS.** Embolic stroke of undetermined source. A residue class, not an indication (Chapter 18 Case 3).

**EVPI / EVSI.** Expected value of perfect / sample information. What a clairvoyant, or a study of size \(n\), is worth under your utility.

**Exchangeability.** The modeling claim that group labels carry no leftover information once the hierarchical parameters are known. False for a pediatric site in an adult EVT model.

**Expected utility.** \(\int u(a,\theta)\, p(\theta \mid y)\, d\theta\). The quantity step 7 maximizes.

**File-refit.** `brms` option that reloads an archived fit unless the model or data changed. A pipeline feature, not a convenience (Chapter 20).

**Go/no-go.** A Phase 2 decision rule, preferably on the posterior predictive probability of eventual success, not on \(P(\delta > 0 \mid y_{\text{now}})\).

**HDI.** Highest-density interval. The shortest interval containing a stated posterior probability.

**Hierarchical model.** Parameters that are themselves drawn from a shared distribution. Shrinkage lives here (Chapter 10).

**Highest posterior density.** Synonym of HDI in this book.

**Historical borrowing.** Using previous studies as part of the prior or as a hierarchical group. \(\tau\) *is* the borrowing.

**Informative missingness.** The fact of missingness carries information about the missing value. CTA not done because LVO seemed unlikely.

**Jeffreys prior.** A formal default (Beta(0.5, 0.5) for a binomial). Rarely a clinical prior.

**Likelihood.** \(p(y \mid \theta)\). What the datum would look like under each state or effect. Not a posterior.

**Likelihood ratio.** \(P(\text{datum} \mid \text{state}) / P(\text{datum} \mid \text{not})\). Multiplies prior odds.

**LOO / PSIS-LOO.** Approximate leave-one-out predictive check. Read the Pareto-\(k\) diagnostics.

**Loss function.** \(-u\). The book speaks in utilities; the math does not care.

**LVO.** Large-vessel occlusion. ICA, M1, or proximal M2 unless a chapter says otherwise.

**MCID.** Minimal clinically important difference. A utility in disguise. Should appear in go/no-go priors (Appendix B).

**Measurement error.** The covariate you typed is not the covariate you meant (Chapter 17). Attenuates slopes.

**Mixture prior / mixture posterior.** A discrete weighted combination, used when experts disagree or when a latent mechanism (AF vs not) is unobserved.

**mRS.** Modified Rankin Scale, 0–6. An ordinal outcome; collapsing to 0–2 is a decision, not a law.

**NIHSS.** National Institutes of Health Stroke Scale, 0–42. Bounded, discrete, rater-noisy.

**Partial pooling.** The hierarchical compromise between a separate estimate per group and a single pooled estimate.

**Pauker–Kassirer threshold.** Treat when \(p > H/(B+H)\). The skeleton of Chapters 5–6.

**Posterior.** \(p(\theta \mid y)\). The prior reweighted by the likelihood.

**Posterior predictive.** \(p(\tilde{y} \mid y) = \int p(\tilde{y} \mid \theta)\, p(\theta \mid y)\, d\theta\). The go/no-go object and the PPC object.

**PPC.** Posterior predictive check. Compare replicated data to observed data, in the slice the decision uses.

**Predictive probability of success (PPoS).** Posterior predictive probability that a future analysis will meet a declared rule.

**Prior.** \(p(\theta)\) before the new datum. Must be written, with a source.

**Proper scoring rule.** A penalty that makes honesty about probabilities optimal. Brier is one; AUROC is not.

**\(\widehat{R}\).** Rank-normalized chain-comparison statistic. Teaching bar: \(< 1.01\).

**renv.lock.** Exact R package versions. Necessary, not sufficient (Chapter 20).

**Representativeness.** Judging probability by similarity to a prototype. “Classic LVO” is a prototype.

**Seed.** An integer that makes a sampler’s draws repeatable *within a toolchain*. Decision-reproducibility is the real target.

**Sensitive decision.** An action that flips when the prior or utility moves within a plausible range. Report the flip.

**Shrinkage.** Movement of a group estimate toward the grand mean, stronger when \(n_j\) is small or \(\tau\) is small.

**Skeptical prior.** A prior centered near “no important effect,” used so that a go requires data (Chapter 18 Case 4).

**Spot sign.** CTA contrast within an ICH. A marker for expansion, not a treatment.

**System 1 / System 2.** Fast pattern recognition versus slow explicit updating. This book trains System 2 to audit System 1, not to replace it in the first 30 seconds.

**\(\tau\).** Between-group SD on the parameter scale (often logit). Worksheet 3.

**Teaching number.** An invented, labeled numeric value used so algebra can be shown without fabricating a trial result.

**Test threshold.** The prior below which even a good test is not worth doing.

**Transport.** Moving an estimate from a trial or a hospital into a new population. Hierarchical structure, not hope.

**Treat threshold.** The prior above which you treat without further testing.

**Utility.** A numerical encoding of how much an outcome is worth, including harms. Elicited, not estimated from `brms`.

**Value of information.** The expected utility gained by buying a datum before acting. Clock-aware in stroke.

**Weakly informative prior.** A prior that rules out cartoons but does not pretend to be empty. Relative to the expected likelihood.

**Workflow (this book).** Question, prior, design/data, model, check, estimate, decide, communicate, update, share.

---

## Mathematical appendix

### Beta–binomial

If \(\pi \sim \text{Beta}(\alpha, \beta)\) and \(y \mid \pi \sim \text{Binomial}(n, \pi)\), then

\[
\pi \mid y \;\sim\; \text{Beta}(\alpha + y,\; \beta + n - y).
\]

The prior mean is \(\alpha/(\alpha+\beta)\). The prior sample size is \(\alpha+\beta\). The posterior predictive for a new binary observation is \((\alpha+y)/(\alpha+\beta+n)\). The posterior predictive for \(m\) new trials is Beta-Binomial:

\[
P(\tilde{y} = k \mid y) = \binom{m}{k}
\frac{B(\alpha+y+k,\; \beta+n-y+m-k)}{B(\alpha+y,\; \beta+n-y)}.
\]

Use this for prevalence, response rates, and the next-three-patients conversation (C.16.4).

### Logit and log odds ratios

\[
\text{logit}(\pi) = \log\frac{\pi}{1-\pi}, \qquad
\pi = \frac{e^{\eta}}{1+e^{\eta}}.
\]

A logistic slope \(\beta\) is a change in log-odds. The implied odds ratio is \(e^{\beta}\). To elicit \(\beta\), elicit two risks at a fixed covariate and convert (Appendix B Worksheet 2). Never elicit “a log-OR of 0.4” from a non-methodologist.

A risk ratio and an odds ratio nearly coincide when the baseline risk is small (ESUS at 5%) and diverge when it is not (mRS 0–2 at 30–45%). Match the contrast to the model.

### Highest-density interval

For a unimodal posterior density \(p(\theta \mid y)\), the \(100(1-\alpha)\%\) HDI is the interval \((L, U)\) such that

\[
\int_{L}^{U} p(\theta \mid y)\, d\theta = 1-\alpha
\quad\text{and}\quad
U - L \text{ is minimized}.
\]

Equivalently, \(p(L \mid y) = p(U \mid y)\) and no point outside has higher density than a point inside. For a Normal, the HDI coincides with the equal-tail interval. For a skewed Beta, it does not; report the HDI and the posterior probability of the clinically relevant half-line, e.g. \(P(\delta > 20 \mid y)\).

In R, after a `brms` fit:

```r
# HDI on a named parameter, teaching snippet
library(posterior)
d <- as_draws_df(fit)
qs <- quantile(d$b_nihss, probs = c(0.05, 0.95))   # equal-tail 90%
hdi <- posterior::quantile2(d$b_nihss, probs = c(0.05, 0.95))
# For a true HDI on a skewed draw vector:
tidybayes::median_hdi(d$b_nihss, .width = 0.90)
```

Equal-tail intervals are acceptable when you say they are equal-tail. Do not call an equal-tail interval an HDI.

### The threshold identity

If treating a true state gains \(B > 0\) and treating a false state loses \(H > 0\), expected utility of treating is \(p B - (1-p) H\), of waiting is 0 (up to a constant). Treat when

\[
p \;\geq\; p^{*} = \frac{H}{B+H}.
\]

Every fancy decision analysis in this book is this identity with a more complicated \(B\), \(H\), or \(p\).

---

## Further reading

Grouped so a resident can pick one shelf.

**Decision and bedside probability**

- Sox HC, Higgins MC, Owens DK. *Medical Decision Making*. 2nd ed. Wiley-Blackwell; 2013.
- Pauker SG, Kassirer JP. The threshold approach to clinical decision making. *N Engl J Med*. 1980;302:1109–1117.
- Hunink MGM, Weinstein MC, Wittenberg E, et al. *Decision Making in Health and Medicine*. 2nd ed. Cambridge University Press; 2014.
- Gigerenzer G, Edwards A. Simple tools for understanding risks. *BMJ*. 2003;327:741–744.

**Bayesian data analysis**

- Gelman A, Carlin JB, Stern HS, Dunson DB, Vehtari A, Rubin DB. *Bayesian Data Analysis*. 3rd ed. CRC Press; 2013.
- Gelman A, Vehtari A, Simpson D, et al. Bayesian workflow. *arXiv:2011.01808*. 2020.
- McElreath R. *Statistical Rethinking*. 2nd ed. CRC Press; 2020.
- Spiegelhalter DJ, Abrams KR, Myles JP. *Bayesian Approaches to Clinical Trials and Health-Care Evaluation*. Wiley; 2004.
- O’Hagan A, et al. *Uncertain Judgements*. Wiley; 2006.

**Computation**

- Bürkner P-C. brms: An R package for Bayesian multilevel models using Stan. *J Stat Softw*. 2017;80(1):1–28.
- Stan Development Team. *Stan User’s Guide*. https://mc-stan.org/docs/
- Gabry J, Simpson D, Vehtari A, Betancourt M, Gelman A. Visualization in Bayesian workflow. *J R Stat Soc A*. 2019;182:389–402.
- Vehtari A, Gelman A, Gabry J. Practical Bayesian model evaluation using leave-one-out cross-validation and WAIC. *Stat Comput*. 2017;27:1413–1432.

**Reporting and regulation**

- Bossuyt PM, et al. STARD 2015. *BMJ*. 2015;351:h5527.
- Schulz KF, Altman DG, Moers D, CONSORT Group. CONSORT 2010. *BMJ*. 2010;340:c332. (Use the current CONSORT extension relevant to your design.)
- Collins GS, Reitsma JB, Altman DG, Moons KGM. TRIPOD. *Ann Intern Med*. 2015;162:55–63.
- U.S. Food and Drug Administration. Guidance for the Use of Bayesian Statistics in Medical Device Clinical Trials. 2010.
- Sung L, et al. Guidance for Bayesian analyses in oncology. Various FDA/EMA reflections; start with the 2010 device guidance and the 2020 Bayesian oncology workshop reports.

**Neurology trials whose *designs* this book uses (do not lift tables or figures)**

- NINDS rt-PA Stroke Study Group. *N Engl J Med*. 1995;333:1581–1587.
- Goyal M, et al. HERMES collaboration. *Lancet*. 2016;387:1723–1731.
- Nogueira RG, et al. DAWN. *N Engl J Med*. 2018;378:11–21.
- Albers GW, et al. DEFUSE 3. *N Engl J Med*. 2018;378:708–718.
- Anderson CS, et al. INTERACT2. *N Engl J Med*. 2013;368:2355–2365.
- Qureshi AI, et al. ATACH-2. *N Engl J Med*. 2016;375:1033–1043.
- Hart RG, et al. NAVIGATE ESUS. *N Engl J Med*. 2018;378:2191–2201.
- Diener H-C, et al. RE-SPECT ESUS. *N Engl J Med*. 2019;380:1906–1917.

---

## Mini-checklists

These are *memory* checklists. Official STARD, CONSORT, and TRIPOD items are longer and win when you submit. The Bayesian block is this book’s own, aligned with the FDA device guidance’s spirit and with Chapter 19.

### STARD (diagnostic accuracy, condensed)

| # | Before you submit a diagnostic paper |
|---|---|
| 1 | Clinical role and intended use stated (rule-in, rule-out, where in the pathway). |
| 2 | Eligibility, including the prior-shaping inclusion cuts (NIHSS \(\geq 10\), etc.). |
| 3 | Reference standard defined; time gap between index and reference. |
| 4 | Whether readers of the index test saw the reference, and conversely. |
| 5 | 2×2 (or cutoff-specific) numbers, not only Sn/Sp. |
| 6 | Prevalence in the study sample stated so PPV is not treated as portable. |
| 7 | Indeterminate and missing index tests counted, not dropped. |
| 8 | Interval estimates on Sn, Sp, LRs — and the slice they apply to. |

### CONSORT (trials, condensed)

| # | Before you submit a trial |
|---|---|
| 1 | Design type named (parallel, adaptive, platform); adaptations predeclared. |
| 2 | Eligibility and setting; the population a Chapter 19 user will transport *from*. |
| 3 | Interventions in enough detail to reproduce, including rescue therapy. |
| 4 | Primary outcome, time point, and estimator. |
| 5 | How sample size was chosen, including Bayesian operating characteristics if used. |
| 6 | Randomization unit, allocation concealment, who was blinded to what. |
| 7 | Participant flow (screened, randomized, analyzed). |
| 8 | Outcomes with intervals; harms with the same seriousness as benefits. |
| 9 | The analysis set (ITT, per-protocol) and missing-data method. |

### TRIPOD (prediction models, condensed)

| # | Before you submit a prediction paper |
|---|---|
| 1 | Development, validation, or both — said in the title. |
| 2 | Outcome definition and assessment window. |
| 3 | Candidate predictors, including those *not* in the final model. |
| 4 | Handling of missing predictors (not complete-case by default). |
| 5 | Model specification: family, link, penalization or prior. |
| 6 | Calibration *and* discrimination, in the slices a decision will use. |
| 7 | External validation population named, or an honest “none.” |
| 8 | How to get a prediction from the model (formula, intercept, software). |
| 9 | Decision-curve or expected-utility comparison if a cutoff is recommended. |

### Bayesian reporting (this book)

| # | Before you call an analysis Bayesian |
|---|---|
| 1 | Question stated as a decision, with action set and horizon (step 1). |
| 2 | Prior written, source named, elicitation recorded if expert (step 2, Appendix B). |
| 3 | Prior predictive or at least a read-back of the prior in words. |
| 4 | Likelihood / model specified to the family, link, and grouping factors. |
| 5 | Software, version, backend, seed, \(\widehat{R}\), ESS, divergences. |
| 6 | PPC in the decision slice, not only a global overlay. |
| 7 | Estimates on the decision scale (risks, meters, suite-hours), with HDIs. |
| 8 | Utility or threshold stated; sensitivity of the *action* to prior and utility. |
| 9 | Predictive probability of success if the analysis is a go/no-go. |
| 10 | Shareable bundle: lockfile, derived table or simulated stand-in, archived draws (Chapter 20). |

!!! tip "Clinical Pearl"
    A paper can pass CONSORT and still be the wrong likelihood for your hospital. A paper can pass this Bayesian block and still be a bad decision if the utility is yours rather than the patient’s. Checklists catch omissions. They do not catch the wrong loss function.

---

## How the four appendices fit

| Appendix | Job |
|---|---|
| A | Make the stack run. |
| B | Make the prior a written object. |
| C | Make the exercises answerable without hand-waving. |
| D | Make the words, the three formulas, the reading, and the pre-submission scan shareable. |

Chapters 18–20 are the practice of the same objects: a loop, a sentence, and a file someone else can rebuild.

!!! success "Key Takeaway"
    Fifty-odd words, three formulas, one reading list, four checklists. The Beta update, the logit translation, and the \(H/(B+H)\) threshold are the only mathematics most bedside decisions need; `brms` is how you extend them when the likelihood is no longer conjugate. Report the prior, the slice-wise check, the utility, and the bundle. If a term in the glossary does not change an action or a sentence, you did not need it this week.

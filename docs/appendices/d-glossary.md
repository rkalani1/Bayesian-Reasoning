# Appendix D — Glossary, Mathematical Appendices, Further Reading, Reporting Checklists

## Purpose

A field guide to the words, the four pieces of mathematics the rest of the book leans on, a reading list that is not a cargo cult, and five mini-checklists you can put next to a manuscript. Definitions are operational. If a term here disagrees with a chapter, the chapter’s worked example wins.

Checklists are memory aids, not official society policy and not a license to submit.

---

## Glossary

**Action set.** The discrete things you can still do. Treat, test, wait, stop, go. A posterior without an action set is a hobby.

**Adaptive design.** A trial that uses accumulating data to change allocation, sample size, or stopping. The likelihood may remain valid; the usual fixed-\(n\) standard error story does not.

**Anchoring.** Staying too close to the first number seen. The first NIHSS, the first radiologist’s adjective, last year’s base rate.

**Assurance.** Expected power under a design prior. Not power at a hoped-for \(\delta\).

**ATE / CATE.** Average treatment effect versus conditional (subgroup) average treatment effect. Neither is this patient’s posterior predictive (Chapter 21).

**Availability.** Judging probability by the ease of recall. The last fatal tPA ICH you saw is not a likelihood.

**BAO.** Basilar-artery occlusion. A posterior-circulation LVO; not interchangeable with anterior ICA/M1 in priors or transport (Chapter 4).

**Base rate.** \(P(\text{state})\) in the relevant class before the new datum. The number residents skip.

**Base-rate neglect.** Reporting a likelihood (or a stereotype) as a posterior.

**Bayes factor.** The ratio of marginal likelihoods of two models (or hypotheses), \(BF_{10} = p(y \mid M_1)/p(y \mid M_0)\). It updates prior model odds to posterior model odds. Not a posterior probability, not a p-value, and not a substitute for a ROPE (Chapter 9).

**Bayesian workflow.** The computational cousin of Chapter 19: specify, fit, check, modify, decide. Not a synonym for “we used `brms`.”

**Bayes’ theorem.** \(p(\theta \mid y) \propto p(y \mid \theta)\, p(\theta)\). Odds form: posterior odds \(=\) prior odds \(\times\) LR.

**Brier score.** Mean squared error of a probability. A calibration-friendly proper scoring rule.

**Calibration.** Among days you said 0.30, the event happened about 30% of the time. Discrimination can be fine while calibration is not.

**CIF.** Cumulative incidence function. The probability of having entered a state by time \(t\) in the presence of competing events. Not \(1-\mathrm{KM}\) with the competitor censored (Chapter 12).

**cmdstanr.** R interface to CmdStan. Preferred `brms` backend in this book.

**Collider / confounder / mediator.** Adjustment language. A collider is a common effect; conditioning on it opens a path. A confounder is a common cause. A mediator is on the path from treatment to outcome (Chapter 22).

**Commensurate prior.** A hierarchical device for borrowing from historical data that lets the current data down-weight the history when they disagree.

**Complete-case analysis.** Dropping rows with missing covariates. Biased when missingness is informative (Chapter 24; C.19.3 is a worked CTA example).

**Conjugate prior.** A prior that stays in the same family after the likelihood: Beta with binomial, Normal with Normal known-variance.

**Consistency / positivity.** Causal identification pair. Consistency: the observed outcome under the assigned strategy is the potential outcome of that strategy. Positivity: every covariate pattern you will quote has a nonzero chance of each strategy (Chapters 21–22).

**Conversation.** Step 8. The posterior and the threshold in a sentence a non-statistician can use.

**Credible interval.** A posterior interval. This book uses equal-tailed intervals (ETIs) as the default in tables, and HDIs when the posterior is clearly skewed (Chapter 9).

**CRIT-APP.** The curriculum’s structured critical-appraisal companion: design, selection, intervention, outcome, follow-up, analysis, applicability, abstract honesty. It moves priors. It does not pick Friday’s cutoff.

**DAG.** Directed acyclic graph. Every arrow is an intervention claim; every missing arrow is a claim of no direct effect (Chapter 22).

**Decision curve.** A plot of net benefit against threshold probability \(p_t\) for a model and for the treat-all / treat-none defaults (Chapter 15).

**Decision threshold.** The posterior probability (or expected utility) at which the action flips. Diagnostic and treatment thresholds are different objects (Chapter 14).

**De-identification.** Removing or coarsening identifiers so a derived table can be shared. “We took the names off” is not it (Chapter 20).

**Discrimination.** Whether scores rank events above non-events (AUROC). Not a utility.

**Divergent transition.** A Stan warning that the sampler left the typical set. Do not interpret a fit full of them.

**Effect prior.** A prior on a treatment contrast, distinct from a diagnostic prior on a state.

**Elicitation.** Writing a prior from expert judgment on an observable scale before the new data are shown (Appendix B).

**ELPD.** Expected log predictive density. What LOO and WAIC estimate (Chapter 8).

**Equipoise / RAR.** Community uncertainty that licenses randomization; response-adaptive randomization that tilts allocation as posteriors move (Chapter 26).

**ESUS.** Embolic stroke of undetermined source. A residue class, not an indication (Chapter 18 Case 3).

**EtD.** Evidence-to-Decision table. GRADE’s recommendation machine, not a certainty rating (Chapter 25).

**ETI.** Equal-tailed interval. The central posterior interval with equal probability outside each tail. Default table interval in this book; not an HDI unless the posterior is symmetric.

**EVPI / EVSI.** Expected value of perfect / sample information. What a clairvoyant, or a study of size \(n\), is worth under your utility.

**Exchangeability.** The modeling claim that group labels carry no leftover information once the hierarchical parameters are known. False for a pediatric site in an adult EVT model.

**Expected utility.** \(\int u(a,\theta)\, p(\theta \mid y)\, d\theta\). The quantity step 7 maximizes.

**File-refit.** `brms` option that reloads an archived fit unless the model or data changed. A pipeline feature, not a convenience (Chapter 20).

**g-computation / standardization.** Average \(E(Y \mid A=a, X)\) over a named mix of \(X\). How a fitted outcome model becomes a transported ATE (Chapters 21–22).

**Go/no-go.** A Phase 2 decision rule, preferably on the posterior predictive probability of eventual success, not on \(P(\delta > 0 \mid y_{\text{now}})\).

**GRADE.** A framework for rating certainty of evidence and strength of recommendation. This book treats its domains as Bayesian objects — bias, \(\tau\), transport, threshold, selection — not as a separate qualitative universe (Chapter 25).

**HDI.** Highest-density interval. The shortest interval containing a stated posterior probability.

**Hierarchical model.** Parameters that are themselves drawn from a shared distribution. Shrinkage lives here (Chapter 6).

**Highest posterior density.** Synonym of HDI in this book.

**Historical borrowing.** Using previous studies as part of the prior or as a hierarchical group. \(\tau\) *is* the borrowing.

**HTE.** Heterogeneity of treatment effect. A posterior on a modifier, or a risk-based contrast, not a forest-plot row of unshrunk slices (Chapter 21).

**Immortal time.** A stretch of follow-up an exposed person must survive in order to be counted as exposed. A time-zero defect, not confounding (Chapter 22).

**Informative missingness.** The fact of missingness carries information about the missing value. CTA not done because LVO seemed unlikely.

**IPW / LOCF / selection model.** Inverse-probability weighting, last-observation-carried-forward, and \(p(R \mid Y, X)\). Named alternatives to a joint imputation / pattern-mixture stack (Chapter 24).

**Jeffreys prior.** A formal default (Beta(0.5, 0.5) for a binomial). Rarely a clinical prior.

**Likelihood.** \(p(y \mid \theta)\). What the datum would look like under each state or effect. Not a posterior.

**Likelihood ratio.** \(P(\text{datum} \mid \text{state}) / P(\text{datum} \mid \text{not})\). Multiplies prior odds.

**LOO / PSIS-LOO.** Approximate leave-one-out predictive check. Read the Pareto-\(k\) diagnostics.

**Loss function.** \(-u\). The book speaks in utilities; the math does not care.

**LVO.** Large-vessel occlusion. ICA, M1, or proximal M2 unless a chapter says otherwise. Basilar occlusion is named separately (BAO).

**MAP prior.** Meta-analytic predictive prior for a new control (or a new center). The posterior predictive of the historical model (Chapter 13).

**MAR / MCAR / MNAR.** Missing at random / completely at random / not at random. Statements about \(p(R \mid Y, X)\), not about how hard you tried to call (Chapter 24).

**MCID.** Minimal clinically important difference. A utility in disguise. Should appear in go/no-go priors (Appendix B).

**Measurement error.** The covariate you typed is not the covariate you meant (Chapter 24). Attenuates slopes.

**Mixture prior / mixture posterior.** A discrete weighted combination, used when experts disagree or when a latent mechanism (AF vs not) is unobserved.

**mRS.** Modified Rankin Scale, 0–6. An ordinal outcome; collapsing to 0–2 is a decision, not a law.

**Net benefit.** \(NB = \mathrm{Se}\,\pi - (1-\mathrm{Sp})(1-\pi)\,p_t/(1-p_t)\). Expected utility scaled so one true positive is worth one unit (Chapter 15).

**NIHSS.** National Institutes of Health Stroke Scale, 0–42. Bounded, discrete, rater-noisy.

**Pareto-\(k\).** PSIS-LOO tail diagnostic. Comfortable below 0.5; watch 0.5–0.7; unreliable above 0.7 (Chapter 8).

**Partial pooling.** The hierarchical compromise between a separate estimate per group and a single pooled estimate.

**Pattern-mixture model.** \(p(Y \mid R, X)\, p(R \mid X)\). Needs a named restriction (a shift \(\delta\)) to identify the missing pattern (Chapter 24).

**Pauker–Kassirer threshold.** Treat when \(p > H/(B+H)\). The skeleton of Chapter 14.

**Posterior.** \(p(\theta \mid y)\). The prior reweighted by the likelihood.

**Posterior predictive.** \(p(\tilde{y} \mid y) = \int p(\tilde{y} \mid \theta)\, p(\theta \mid y)\, d\theta\). The go/no-go object and the PPC object.

**Power prior.** Historical likelihood raised to \(a_0 \in [0,1]\). \(a_0 = 1\) is maximal borrowing, not modesty (Chapter 4).

**PPC.** Posterior predictive check. Compare replicated data to observed data, in the slice the decision uses.

**Predictive probability of success (PPoS).** Posterior predictive probability that a future analysis will meet a declared rule.

**Prior.** \(p(\theta)\) before the new datum. Must be written, with a source.

**Proper scoring rule.** A penalty that makes honesty about probabilities optimal. Brier is one; AUROC is not.

**\(\widehat{R}\).** Rank-normalized chain-comparison statistic. Teaching bar: \(< 1.01\).

**renv.lock.** Exact R package versions. Necessary, not sufficient (Chapter 20).

**Representativeness.** Judging probability by similarity to a prototype. “Classic LVO” is a prototype.

**RMST.** Restricted mean survival time, \(\int_0^\tau S(t)\,dt\). Expected days alive out of \(\tau\) (Chapter 12).

**ROPE.** Region of practical equivalence. An interval around a null that you have already called “not a decision-changing effect” (Chapter 9).

**Seed.** An integer that makes a sampler’s draws repeatable *within a toolchain*. Decision-reproducibility is the real target.

**Sensitive decision.** An action that flips when the prior or utility moves within a plausible range. Report the flip.

**Shrinkage.** Movement of a group estimate toward the grand mean, stronger when \(n_j\) is small or \(\tau\) is small.

**Skeptical prior.** A prior centered near “no important effect,” used so that a go requires data (Chapter 18 Case 4).

**Spectrum bias / verification bias.** Wrong sampling frame for Se/Sp; missing reference standard in those who were not referred (Chapter 11).

**Spot sign.** CTA contrast within an ICH. A marker for expansion, not a treatment.

**System 1 / System 2.** Fast pattern recognition versus slow explicit updating. This book trains System 2 to audit System 1, not to replace it in the first 30 seconds.

**Target trial.** The randomized protocol an observational analysis claims to emulate. If you cannot write eligibility, strategies, time zero, follow-up, and the estimand, you do not have one (Chapter 22).

**\(\tau\).** Between-group SD on the parameter scale (often logit). Worksheet 3.

**Teaching number.** An invented, labeled numeric value used so algebra can be shown without fabricating a trial result.

**Test threshold.** The prior below which even a good test is not worth doing. See also \(T_t\) / \(T_{tt}\).

**Transport.** Moving an estimate from a trial or a hospital into a new population. Hierarchical structure, not hope.

**Treat-all / treat-none.** Default strategies on a decision curve. Treat-none has \(NB = 0\). Names flip when the “positive” action is withholding (Chapter 15).

**Treat threshold.** The prior above which you treat without further testing.

**\(T_t\) / \(T_{tt}\).** Testing and test–treatment thresholds. Below \(T_t\), wait; between \(T_t\) and \(T_{tt}\), test; above \(T_{tt}\), treat without the test (Chapter 14).

**Utility.** A numerical encoding of how much an outcome is worth, including harms. Elicited, not estimated from `brms`.

**UW-mRS.** Utility-weighted modified Rankin Scale. A scored version of the ordinal outcome; the weights are a utility, not a likelihood (Chapters 12, 25).

**Value of information.** The expected utility gained by buying a datum before acting. Clock-aware in stroke.

**WAIC.** Widely applicable information criterion. A sibling of PSIS-LOO; prefer PSIS-LOO, whose Pareto-\(k\) tells you when either approximation can be trusted (Chapter 8).

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

Use this for prevalence, response rates, and the next-three-patients conversation (Chapter 5).

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
eti <- posterior::quantile2(d$b_nihss, probs = c(0.05, 0.95))  # equal-tail 90%
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
- Schulz KF, Altman DG, Moher D, CONSORT Group. CONSORT 2010. *BMJ*. 2010;340:c332. (Use the current CONSORT extension relevant to your design.)
- Collins GS, Reitsma JB, Altman DG, Moons KGM. TRIPOD. *Ann Intern Med*. 2015;162:55–63.
- U.S. Food and Drug Administration. Guidance for the Use of Bayesian Statistics in Medical Device Clinical Trials. 2010.
- Sung L, Hayden J, Greenberg ML, Koren G, Feldman BM, Tomlinson GA. Seven items were identified for inclusion when reporting a Bayesian analysis of a clinical study. *J Clin Epidemiol*. 2005;58(3):261–268.
- U.S. Food and Drug Administration. *Guidance for the Use of Bayesian Statistics in Medical Device Clinical Trials*. 2010.

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

These are *memory* checklists. Official STARD, CONSORT, TRIPOD, and GRADE/EtD items are longer and win when you submit. The Bayesian block is this book’s own, aligned with the FDA device guidance’s spirit and with Chapter 19.

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
| 2 | Eligibility and setting; the population a Chapter 21 user will transport *from*. |
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
| 7 | Estimates on the decision scale (risks, meters, suite-hours), with ETIs (HDIs if the posterior is clearly skewed). |
| 8 | Utility or threshold stated; sensitivity of the *action* to prior and utility. |
| 9 | Predictive probability of success if the analysis is a go/no-go. |
| 10 | Shareable bundle: lockfile, derived table or simulated stand-in, archived draws (Chapter 20). |

!!! tip "Clinical Pearl"
    A paper can pass CONSORT and still be the wrong likelihood for your hospital. A paper can pass this Bayesian block and still be a bad decision if the utility is yours rather than the patient’s. Checklists catch omissions. They do not catch the wrong loss function.

### GRADE / Evidence-to-Decision (recommendations, condensed)

GRADE is a certainty-of-evidence system. Evidence-to-Decision (EtD) is the table that turns that certainty into a recommendation. Neither is a Bayesian method. Both are where a posterior, a prediction interval, and a utility are supposed to land, and both are where they usually do not. This mini-checklist is a memory aid for reading or writing a stroke recommendation so that the objects from Chapters 13 and 14 are not laundered into a verb (“we suggest”) with no numbers attached.

| # | EtD domain | The Bayesian question hiding inside |
|---|---|---|
| 1 | Priority of the problem | Is the decision frequent or costly enough to deserve a threshold, or is this a rare corner you should not protocolize? |
| 2 | Desirable effects | What is \(B\), on an outcome the patient would recognize (mRS 0–2, language, independence), with a posterior not a point OR? |
| 3 | Undesirable effects | What is \(H\) (sICH, futile transfer, delayed door), scored with the same seriousness as \(B\)? |
| 4 | Certainty of evidence | Is the interval you are quoting \(\operatorname{CrI}(\mu)\) or a 95% prediction interval? Downgrade for \(\tau\), for spectrum, for a missing small study. |
| 5 | Values | Is \(B/H\) stable across the people who will live with the outcome, or is the editor’s aphasia a different ratio from the banner’s “mild stroke”? |
| 6 | Balance of effects | At the posterior you actually have, which expected-utility line is on top? “Favors intervention” is a crossing, not a vibe. |
| 7 | Resources | Helicopter hours, suite time, lytic cost — enter as a disutility or as a constraint, not as a footnote. |
| 8 | Certainty of resources | Same rule as (4): a point cost with no interval is a guess wearing a spreadsheet. |
| 9 | Cost-effectiveness | A QALY ICER is a policy instrument (Chapter 14). It does not settle the next alteplase. |
| 10 | Equity | Who is systematically below the testing threshold because the likelihood was estimated in someone else’s spectrum? |
| 11 | Acceptability | Will the service act on a posterior of 0.40, or will it wait for a sentence that says “significant”? |
| 12 | Feasibility | Can this hub produce the likelihood the recommendation assumes (perfusion software, DSA, overnight CTA readers)? If not, you are applying \(\mu\) where \(\theta_{\text{new}}\) belongs. |

Certainty ratings — high, moderate, low, very low — are not posterior probabilities. A “moderate” GRADE rating on late-window EVT is a narrative about risk of bias, inconsistency, indirectness, imprecision, and publication bias. You can translate several of those into this book’s objects: inconsistency is \(\tau\) and the prediction interval; imprecision is the width of \(\operatorname{CrI}(\mu)\); publication bias is the selection model in Chapter 13; indirectness is the exchangeability claim (mismatch-selected trials, unselected hub). Risk of bias is not a prior on \(\mu\). It is a reason to distrust the likelihood. Putting a skeptical prior on a biased \(y_i\) and calling the result “GRADE, but Bayesian” is how a committee double-counts the same anxiety.

A recommendation (“we recommend,” “we suggest,” “we suggest against”) is an action. It requires a threshold. EtD often hides the threshold in the balance-of-effects row and then votes. The book’s request is smaller: write \(p^\star = H/(H+B)\), write the posterior or the predictive the recommendation is using, and say whether the recommendation is for the mean of the trial universe or for the next system. A strong recommendation when the prediction interval for \(\theta_{\text{new}}\) still includes a harm-side effect is a recommendation that the next hub will not be able to cash.

Teaching use. If you are appraising a guideline on late-window EVT or on thrombolysis in mild aphasia, score the twelve rows with one sentence each, and mark which rows were answered with a point estimate, which with an interval for \(\mu\), which with a utility, and which with a committee adjective. The empty rows are the ones Chapter 14 told you to refuse to fill with a QALY pulled from a different disease. A panel that completes every GRADE cell and never names \(B\), \(H\), or the prediction interval has produced a recommendation that this book cannot implement at a bedside.

The twelve rows also diagnose a common stroke-guideline failure mode. Rows 2–4 get a pooled odds ratio and a certainty adjective. Rows 5–6 get a vote. Rows 7–12 get a paragraph about cost and training that is not allowed to change the verb. That is how a late-window EVT recommendation written for mismatch-selected trial sites is pasted onto a hub that cannot run the imaging pipeline, and then defended with “the meta-analysis was significant.” Row 4 wanted \(\operatorname{CrI}(\mu)\) *and* the prediction interval. Row 12 wanted \(\theta_{\text{new}}\). Row 6 wanted the expected-utility crossing from Chapter 14. Fill those three and the verb often changes by itself.

!!! tip "Clinical Pearl"
    “We suggest” without a named \(B\), a named \(H\), and a named interval is not a weak recommendation. It is an undeclared threshold. Ask which interval — \(\operatorname{CrI}(\mu)\) or the prediction interval — the panel would allow to flip the verb.

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
    A hundred-odd words, four formulas, one reading list, five checklists. The Beta update, the logit translation, the HDI definition, and the \(H/(B+H)\) threshold are the only mathematics most bedside decisions need; `brms` is how you extend them when the likelihood is no longer conjugate. Report the prior, the slice-wise check, the utility, and the bundle. If a term in the glossary does not change an action or a sentence, you did not need it this week.

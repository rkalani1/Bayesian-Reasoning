# Appendix C — Solutions to Exercises

Solutions are self-contained. Teaching numbers match the curriculum’s invented vignettes; they are not estimates from named trials. Where a chapter file is absent, the exercise is restated in one sentence so the algebra still stands. Hints in the chapters are not repeated here.

---

## Chapter 1 — Why Bayesian Clinical Reasoning

**C.1.1.** A resident says “this examination is classic LVO, so the probability is about 90%.” The mothership base rate for LVO among NIHSS \(\geq 10\) is a teaching 0.35, and the examination’s LR\(^{+}\) is a teaching 2.5. What is the posterior, and which bias did the resident commit?

Odds \(= 0.35/0.65 \times 2.5 = 1.346\). Posterior \(= 1.346/2.346 \approx 0.57\). The resident reported a likelihood as a posterior (base-rate neglect, with a garnish of representativeness). Classic is a likelihood ratio, not a probability.

**C.1.2.** Two last-known-well times are offered: 50 minutes and “this morning.” Availability bias favors the last similar case, which was a wake-up. Write the System-2 move.

Write both clocks as separate priors on onset, assign them weights that come from the informant’s reliability (not from the last case you remember), and carry both through the tPA/EVT window calculation. Do not let the vivid wake-up from Tuesday set the weight.

**C.1.3.** Overconfidence check. You give 70% to “this is seizure-mimic, not stroke.” In the last 20 such pronouncements at 70%, 10 were mimics. Are you calibrated?

No. A 70% bin should hit about 14/20. You are overconfident (or the bin is mislabeled). Recalibrate the verbal “70%” downward toward 0.5 until your hit rate matches.

**C.1.4.** Why is “we should be Bayesian about this” not yet a plan?

Because a mood is not a prior, a likelihood, a loss, or a sentence. The plan names the decision, the number that will be updated, and the threshold that will change the action. Without those, the adverb is decoration.

---

## Chapter 2 — Probability as Degree of Belief

**C.2.1.** A fellow says \(P(\text{tPA ICH}) = 0.06\) “because that is the frequency in NINDS-like cohorts.” The patient is 92 with a large infarct. Is 0.06 a frequency or a belief?

It is a frequency in a reference class that does not include this patient. Used here it is a badly transported belief. A better belief starts at 0.06 and updates for age and infarct size; the number that enters the consent sentence is the belief, labeled as such.

**C.2.2.** You would take 4:1 odds against a PFO being causal in this 68-year-old with AF. What is your \(P(\text{causal PFO})\)?

Odds against 4:1 means \(P = 1/(4+1) = 0.20\). If that feels high when written as a percent, your verbal odds were sloppy. Rewrite.

**C.2.3.** Calibration exercise. Ten predictions at “60%.” Seven hit. Compute the Brier contribution of this bin versus a perfectly calibrated 60% bin with the same \(n\).

Brier for this bin: mean \((0.60 - y_i)^{2} = (3\times 0.60^{2} + 7\times 0.40^{2})/10 = (3\times 0.36 + 7\times 0.16)/10 = 0.208\). Calibrated 60% with 6/10 hits: \((4\times 0.36 + 6\times 0.16)/10 = 0.240\). You were lucky-and-slightly-underconfident; do not over-update a single bin of ten.

**C.2.4.** “The probability the next 6MWD exceeds 40 m is 0.5, but I am very uncertain.” Is that coherent?

Yes, if 0.5 is the predictive probability and “very uncertain” describes the *width of the posterior on the mean*, not the predictive probability itself. A wide posterior can still induce a predictive probability of 0.5. Say which object you mean.

---

## Chapter 3 — Bayes’ Theorem at the Bedside

**C.3.1.** Prior SAH 0.08 after thunderclap. CT LR\(^{-}\) at 2 hours, teaching 0.05. Posterior?

Odds \(= 0.08/0.92 \times 0.05 = 0.00435\). Posterior \(\approx 0.0043\). LP is now a value-of-information question, not a reflex.

**C.3.2.** Same prior, CT at 18 hours, teaching LR\(^{-}\) 0.20. Posterior?

Odds \(= 0.0870 \times 0.20 = 0.0174\). Posterior \(\approx 0.017\). Four times the 2-hour posterior. Time of CT is part of the likelihood.

**C.3.3.** Show Bayes as odds and as probability for prior 0.25, LR 4.

Odds form: \(0.25/0.75 \times 4 = 1.333\), posterior \(0.57\). Probability form: \(P \propto 0.25\times 4 = 1\) versus \((1-0.25)\times 1 = 0.75\), same \(1/1.75 = 0.57\).

**C.3.4.** Three independent teaching LRs: 2.0, 0.5, 3.0, prior 0.20. Posterior?

Product of LRs \(= 3.0\). Odds \(= 0.25 \times 3 = 0.75\). Posterior \(= 0.43\). Independence is the fragile assumption; if the three signs are the same cortical pattern counted thrice, you triple-counted.

---

## Chapter 4 — Likelihood Ratios and Diagnostic Tests

**C.4.1.** Sensitivity 0.88, specificity 0.80. LR\(^{+}\), LR\(^{-}\)?

LR\(^{+}\) \(= 0.88/0.20 = 4.4\). LR\(^{-}\) \(= 0.12/0.80 = 0.15\).

**C.4.2.** A D-dimer in possible CVT: teaching Sn 0.94, Sp 0.40. When is a negative useful?

LR\(^{-}\) \(= 0.06/0.40 = 0.15\). Useful when the prior is already low. At prior 0.10, posterior \(\approx 0.016\). At prior 0.50, posterior \(\approx 0.13\), which will not stop imaging.

**C.4.3.** Why is “CTA is 95% accurate” not a likelihood?

Accuracy is a prevalence-weighted average of Sn and Sp. It is not \(P(\text{data} \mid \text{disease})\) and cannot update a prior. Demand Sn and Sp, or an LR, in the slice you will use.

**C.4.4.** Two cutoffs on the same NIHSS. Cutoff \(\geq 8\): Sn 0.90, Sp 0.45. Cutoff \(\geq 12\): Sn 0.70, Sp 0.78. Which LR\(^{+}\) is larger, and what did you trade?

LR\(^{+}\) at 8 is \(0.90/0.55 = 1.64\). At 12 is \(0.70/0.22 = 3.18\). You traded sensitivity for a more specific rule. Pre-alert at 12 is a different action from pre-alert at 8 (Chapter 19).

---

## Chapter 5 — Diagnostic Thresholds

**C.5.1.** Treat-threshold \(p^{*} = H/(B+H)\). Benefit of treating true disease 10 utiles, harm of treating non-disease 2. \(p^{*}\)?

\(p^{*} = 2/12 = 0.167\). Above that, treat even without more testing if testing is unavailable.

**C.5.2.** A test costs \(C = 0.4\) utiles (delay, contrast). Using Pauker–Kassirer, the test-threshold sits where the expected value of testing equals waiting. With \(B=10\), \(H=2\), Sn \(= 0.9\), Sp \(= 0.9\), give the teaching test-threshold.

The no-test/test threshold is \(p_{\text{test}} = (C + (1-\text{Sp})H) / ((B+H)\text{Sn} - \text{Sp}H + C)\) in the usual derivation; plugging teaching numbers, \(p_{\text{test}} \approx 0.07\). Below 0.07, do not test; between 0.07 and \(p^{*}\) (shifted upward by test cost), test; above the treat threshold, treat. The numerical point of the exercise is the *order*: test threshold \(<\) treat threshold.

**C.5.3.** Prior 0.12, treat threshold 0.25, LR\(^{+}\) 3. Does a positive test cross the treat threshold?

Odds \(= 0.136 \times 3 = 0.409\), posterior \(0.29 > 0.25\). Yes, just. Sensitivity to the 0.25 is required before you commit.

**C.5.4.** Why does a cheaper, faster CTA lower the treat-without-test threshold’s relevance?

Because the alternative to treating is no longer “treat or wait.” It is “test in two minutes.” The relevant comparison becomes test-then-treat versus treat-now, and two minutes of delay rarely justify skipping a test that can drop the posterior from 0.57 to 0.11 (Chapter 18 Case 1).

---

## Chapter 6 — Treatment Thresholds and Expected Utility

**C.6.1.** Annual stroke risk 0.05 on antiplatelet, 0.03 on anticoagulant; extra ICH 0.004. Utilities: stroke \(-1\), ICH \(-1.8\). Net \(\Delta EU\) for anticoagulating?

\(\Delta EU = -1\times(-0.02) + (-1.8)\times(0.004) = 0.020 - 0.0072 = +0.0128\). Anticoagulate under this teaching utility. (Contrast Chapter 18 Case 3, where the ischemic reduction was 0.001, not 0.02.)

**C.6.2.** What ischemic ARR pays for 0.004 extra ICH at ICH weight 1.8?

\(0.004 \times 1.8 = 0.0072\). You need at least 0.72 ischemic events prevented per 100 patient-years.

**C.6.3.** A patient values ICH at \(-3\), not \(-1.8\). Recompute C.6.1.

\(\Delta EU = 0.020 - 3\times 0.004 = 0.020 - 0.012 = +0.008\). Still positive, smaller. Ask the patient; do not import your weight.

**C.6.4.** Why is “NNT = 50” not a decision?

NNT is the reciprocal of ARR. It ignores harm, time horizon, and the patient’s weights. An NNT of 50 with an NNH of 20 for a worse outcome is a refusal, not a recommendation.

---

## Chapter 7 — Prior Elicitation

**C.7.1.** Expert median 0.30, 90% interval 0.15–0.50 on a prevalence. Approximate a Beta.

\(\mu = 0.30\), \(s \approx (0.50-0.15)/3.3 \approx 0.106\). \(\alpha+\beta = \mu(1-\mu)/s^{2} - 1 \approx 0.21/0.0112 - 1 \approx 17.7\). \(\alpha \approx 5.3\), \(\beta \approx 12.4\). Report Beta(5, 12) and read it back.

**C.7.2.** The same expert was shown yesterday’s 8-event-in-20 run. Valid prior?

No. That run is likelihood. Using it as a prior and again as data is double-counting. Elicit from someone who has not seen the new series, or discount the prior explicitly.

**C.7.3.** Two experts: Beta(8, 12) and Beta(3, 3). How do you combine?

A discrete mixture with weights equal to your trust, or carry both through the decision and report whether the action flips. Do not average \(\alpha\)s. The mixture mean is \(w\cdot 0.40 + (1-w)\cdot 0.50\); the mixture variance is larger than either component.

**C.7.4.** Translate “I would be surprised by an odds ratio above 2 or below 0.7” plus median OR 1.1 into a Normal on log-OR.

\(\mu = \log 1.1 \approx 0.095\). 90% interval on OR \(\approx (0.7, 2.0)\) is \((\log 0.7, \log 2) \approx (-0.357, 0.693)\), not symmetric. Use \(\sigma \approx (0.693-(-0.357))/3.3 \approx 0.32\) as a teaching Normal, and note the asymmetry: a log-t or an elicited risk-difference would be more faithful.

---

## Chapter 8 — Conjugate Updating

**C.8.1.** Prior Beta(4, 8), then 7 events in 20. Posterior?

Beta(\(4+7\), \(8+13\)) \(=\) Beta(11, 21). Mean \(11/32 = 0.344\) (prior mean was 0.333). The data were almost exactly the prior mean; the posterior narrowed.

**C.8.2.** How many more events in the next 20 would move the posterior mean above 0.45, starting from Beta(11, 21)?

Let \(s\) be successes in 20. Mean \((11+s)/(52) > 0.45 \Rightarrow 11+s > 23.4 \Rightarrow s \geq 13\). Thirteen or more.

**C.8.3.** Normal-Normal: prior \(\mu \sim \mathcal{N}(0, 10^{2})\), one observation \(y=6\), known \(\sigma=8\). Posterior?

Prior precision \(0.01\), likelihood precision \(1/64 \approx 0.0156\). Posterior precision \(0.0256\), posterior mean \(= (0 + 6\times 0.0156)/0.0256 \approx 3.66\), SD \(\approx 6.25\).

**C.8.4.** Why does a Beta(1, 1) prior plus 0 events in 5 patients not justify “the rate is zero”?

Posterior Beta(1, 6), mean \(1/7 \approx 0.14\), \(P(\pi < 0.05) = F_{\text{Beta}}(0.05; 1, 6) \approx 0.26\). Zero events shrink the mean; they do not pin it at 0.

---

## Chapter 9 — Continuous Outcomes and Effect Sizes

**C.9.1.** Mean NIHSS change \(-4.0\) (SD 6, \(n=40\)) versus \(-1.5\) (SD 6, \(n=38\)). Approximate SE of the contrast and a 95% interval, known-sigma teaching calculation.

Contrast \(= -2.5\). SE \(= 6\sqrt{1/40+1/38} \approx 1.36\). Interval \(-2.5 \pm 1.96\times 1.36 \approx (-5.2, -0.2)\). This is a likelihood interval, not a posterior.

**C.9.2.** Put prior \(\mathcal{N}(0, 3^{2})\) on the contrast and update C.9.1.

Likelihood variance \(1.36^{2} \approx 1.85\). Posterior precision \(1/9 + 1/1.85 \approx 0.652\), mean \(= (0 + -2.5/1.85)/0.652 \approx -2.07\), SD \(\approx 1.24\). The skeptical prior pulled the contrast from \(-2.5\) toward 0 by about 0.4 points.

**C.9.3.** A 6MWD MCID is 40 m. Posterior \(\delta \sim \mathcal{N}(18, 16^{2})\). \(P(\delta > 40)\)?

\(z = (40-18)/16 = 1.375\), \(P \approx 0.085\). More probably helpful than importantly helpful.

**C.9.4.** Why is Cohen’s \(d\) a poor bedside effect size for NIHSS?

Because a one-point NIHSS change has a stable clinical meaning and \(d\) rescales it by a sample SD that mixes case-mix with noise. Report meters, points, or absolute risks.

---

## Chapter 10 — Hierarchical Models

**C.10.1.** Eight hospitals, raw independence rates from 0.28 to 0.61, overall 0.44. Why are the raw extremes the wrong report card?

Small \(n\) hospitals are overdispersed. Partial pooling shrinks them toward 0.44 by a factor that depends on \(\tau\) and on \(n_j\). The 0.28 hospital with \(n=12\) may shrink to \(\sim 0.40\); the 0.61 hospital with \(n=140\) barely moves.

**C.10.2.** Teaching: \(\tau = 0.35\) on the logit, hospital \(n=12\), 4 independents, grand mean logit \(\approx -0.24\). Approximate the shrunk logit.

Likelihood SE on logit \(\approx \sqrt{1/4+1/8} = 0.61\). Weights: prior precision \(1/0.35^{2} = 8.16\), likelihood precision \(1/0.37 \approx 2.68\). Shrunk logit \(\approx (8.16\times-0.24 + 2.68\times\text{logit}(4/12))/(8.16+2.68)\). \(\text{logit}(1/3) \approx -0.69\). Shrunk \(\approx -0.35\), probability \(\approx 0.41\). From 0.33 raw toward 0.44.

**C.10.3.** When should you *not* partially pool a hospital?

When exchangeability is a joke: a pediatric hospital in an adult EVT model, or a center that does not offer EVT at all. Hierarchical models shrink; they do not excuse a broken grouping.

**C.10.4.** A varying slope on NIHSS with \(J=4\) hospitals. What goes wrong?

\(\tau_{\text{slope}}\) is barely identified. The prior on that \(\tau\) *is* the result. Either drop the varying slope, or use a strongly informative Worksheet-3 prior and say so.

---

## Chapter 11 — Computation with brms

**C.11.1.** Write a `brm` call for Bernoulli LVO on NIHSS with the Chapter 19 prior. Specification only.

```r
brm(lvo ~ nihss, family = bernoulli(),
    prior = c(prior(normal(-1.7, 0.8), class = Intercept),
              prior(normal(0.12, 0.06), class = b)),
    seed = 11, chains = 4, iter = 2000)
```

**C.11.2.** \(\widehat{R} = 1.08\) on the intercept, 4000 post-warmup draws. What do you do?

Do not interpret. Increase `adapt_delta`, lengthen warmup, reparameterize, check divergences and pairs plots. \(\widehat{R} < 1.01\) is the teaching bar.

**C.11.3.** Why pass `seed` to `brm()` rather than only `set.seed()`?

Stan’s RNG is not R’s RNG. `brm(..., seed = )` controls the sampler. `set.seed()` controls R-side simulation and posterior-predictive draws you make yourself.

**C.11.4.** `family = gaussian()` on a 0–42 NIHSS outcome. What is the obvious misspecification?

Gaussian is unbounded and homoscedastic. NIHSS is bounded and discrete. Teaching fits sometimes still use it for contrasts; a better first revision is an ordinal model or a truncated distribution. At minimum, PPC will show mass outside 0–42.

---

## Chapter 12 — Model Checking

**C.12.1.** A global `pp_check` looks fine; the NIHSS 6–9 slice is badly miscalibrated. Which check wins?

The slice. Decisions that use a cutoff live in a slice. Global overlay can hide the only error that matters (Chapter 19).

**C.12.2.** Pareto-\(k\) of 0.78 on three observations. Can you trust `loo`?

Not those three. Investigate them (often a rare hospital or an extreme NIHSS). Use moment matching or refit-without, and do not stack models on a `loo` that is still waving.

**C.12.3.** Posterior predictive \(p\)-value for the mean is 0.48, for the minimum is 0.01. Interpretation?

The mean is not a useful discrepancy (it was fitted). The minimum says the model does not produce the left tail you observed — typically a Gaussian on a bounded score.

**C.12.4.** Prior sensitivity: cutoff recommendation flips when the NIHSS slope prior SD goes from 0.06 to 0.30. What do you report?

That the decision is prior-sensitive, plus both recommendations, plus the Worksheet-2 or Appendix B justification for 0.06. Do not pick the flatter prior to look “objective.”

---

## Chapter 13 — Decision Analysis and Value of Information

**C.13.1.** EVPI teaching calculation. Two actions, posterior 0.55 that action A is better by 2 utiles, otherwise B is better by 4. EVPI?

Expected utility of A: \(0.55\times 2 + 0.45\times(-4) = -0.70\). Of B: \(0.55\times(-2)+0.45\times 4 = 0.70\). Choose B, EU \(= 0.70\). With perfect information, EU \(= 0.55\times 2 + 0.45\times 4 = 2.90\). EVPI \(= 2.20\) utiles. If a test costs more than 2.20 on this scale, do not buy it.

**C.13.2.** A CTA that will not change the action has what VOI?

Approximately zero, plus a small negative for delay and contrast. Information unused is not information.

**C.13.3.** Why can EVSI for a 30-day monitor in ESUS be positive even when the current posterior favors antiplatelet?

Because a positive monitor *moves the patient into a different mechanism* (AF), where the action flips (Chapter 18 Case 3). EVSI is about the chance of crossing a threshold, not about the current mean RR.

**C.13.4.** Name a decision whose value of information is dominated by time, not by sample size.

Hyperacute LVO. Another 200 historical rows will not help Bay 3 as much as a two-minute CTA. VOI is clock-aware.

---

## Chapter 14 — Communicating Uncertainty

**C.14.1.** Rewrite “there is a chance of bleeding” for tPA consent using a teaching 6% versus 1%.

“Without this medicine, about 1 in 100 people like you have a serious bleed. With it, about 6 in 100. The medicine is given because it also improves the chance of being independent. I will give you those two numbers again.” No “chance,” no “small risk.”

**C.14.2.** HDI 90% for a risk difference is \((-0.01, 0.11)\). Is “no effect” in the interval a reason to stay silent?

No. The interval is mostly positive. Report the probability of benefit and the probability of harm larger than 2 points, then the decision. “Includes zero” is a frequentist habit in Bayesian clothing.

**C.14.3.** A family asks you to “just tell us if you would do it for your mother.” What is the honest move?

Give your action under *their* weights if they have given you weights; if they have not, give the numbers and one sentence about what most people with similar weights choose. Do not launder their utility into your mother’s.

**C.14.4.** Why is a 50-color posterior density the wrong slide for operations?

Because the decision uses a table of cutoffs × suite-hours × independents (Chapter 19). A density invites coefficient staring. Save it for the supplement.

---

## Chapter 15 — Sequential Decisions and Adaptive Trials

**C.15.1.** Predictive probability of eventual success is 0.18, current \(P(\delta > 0 \mid y) = 0.72\). Go, pause, or stop under Chapter 18’s teaching rule (go if PPoS \(> 0.60\), stop if \(< 0.25\))?

Stop. The current posterior on a one-sided sign is not the go/no-go object. PPoS is.

**C.15.2.** Spending \(\alpha\) at two looks versus a posterior-probability boundary: name one thing they do not share.

A posterior boundary does not require a predeclared \(\alpha\) spend to be coherent as a *belief*. A regulator may still demand a Type I error calculation for the *procedure*. Keep the two languages labeled.

**C.15.3.** After 40 of 200 patients, you peek and change the primary endpoint. What happens to the prior?

It is no longer the prior for the new endpoint. You have used the data twice. Either declare a new parameter and a new prior that does not see these 40 on that endpoint, or admit a data-dependent analysis and drop the confirmatory claim.

**C.15.4.** A response-adaptive randomization has put 80% of patients on arm A. What must the analysis still do?

Model the adaptive mechanism or use a likelihood that is still valid under it (the Bernoulli likelihood is, the usual fixed-n SE story is not). Report allocation as a posterior-predictive check: does the model expect this imbalance?

---

## Chapter 16 — Rare Disease and Small-\(n\)

**C.16.1.** \(n=6\), 2 responses, prior Beta(1, 1). Posterior mean and \(P(\pi > 0.5)\)?

Beta(3, 5), mean 0.375. \(P(\pi > 0.5) = 1 - F_{\text{Beta}}(0.5; 3, 5) \approx 0.23\). Do not write “33% response rate” as if it were known.

**C.16.2.** You want to borrow from a historical adult trial for a pediatric cohort. Name the parameter that *is* the borrowing.

\(\tau\) between adult and pediatric intercepts (or a commensurate-power weight). If \(\tau\) is set near 0 by a default, you have declared the children to be small adults. Worksheet 3.

**C.16.3.** Why is “we are underpowered, so we will be Bayesian” not a design?

A prior does not create information. It *relocates* it. If the prior is honest and wide, the posterior will be wide and the go/no-go will be “pause.” That is the point.

**C.16.4.** Posterior predictive for the next 3 patients, Beta(3, 5). Probability of 0/3 responses?

The posterior predictive is Beta-Binomial. \(P(Y=0) = \dfrac{B(3, 5+3)}{B(3,5)} = \dfrac{B(3,8)}{B(3,5)} = \dfrac{5\cdot6\cdot7}{8\cdot9\cdot10} = 0.292\). Almost 30% of next-three worlds show nothing. Plan the conversation.

---

## Chapter 17 — Imaging, Biomarkers, and Measurement Error

**C.17.1.** NIHSS is measured with teaching inter-rater SD 2 points. True slope of LVO log-odds per true NIHSS is 0.12. What happens to the naive slope?

Attenuation. If true NIHSS SD in the sample is 6, reliability \(= 36/(36+4) = 0.90\), naive slope \(\approx 0.12\times 0.90 = 0.108\). Modest here; worse when reliability is 0.6 (ASPECTS, some biomarkers).

**C.17.2.** A core-volume cutoff of 70 mL from DAWN-like design facts is applied on a scanner that overestimates volume by 15%. Direction of the mistake?

Patients who are truly 61 mL are labeled as 70 mL and excluded (or included, depending on the rule). The applied rule is not the trial rule. Recalibrate the volume, do not import the number.

**C.17.3.** Spot sign LR\(^{+}\) 3.0 was estimated in a research read. Clinical reads have Sn 0.55 rather than 0.70. New LR\(^{+}\) if Sp stays 0.80?

LR\(^{+}\) \(= 0.55/0.20 = 2.75\) if Sp is unchanged; if clinical Sp also falls to 0.70, LR\(^{+}\) \(= 0.55/0.30 = 1.83\). Transport the *readers*, not just the sign.

**C.17.4.** Write a one-line `brms` measurement-error specification for NIHSS.

`brm(lvo ~ me(nihss, nihss_se), family = bernoulli(), prior = ...)`, with `nihss_se` a column (teaching: 2 for all rows, or rater-specific). Then PPC on the observed NIHSS, not only on LVO.

---

## Chapter 18 — Integrated Case Studies

**C.18.1.** Base rate 0.18, examination LR 2.5, same CTA LRs. Treat-without-test?

Prior odds \(= 0.18/0.82 \times 2.5 = 0.549\), prior \(= 0.35\). CTA\(+\): odds \(5.05\), posterior \(0.83\). CTA\(-\): odds \(0.049\), posterior \(0.047\). Treat threshold from Chapter 18, suite free, \(p^{*} \approx 0.17\). Prior 0.35 still exceeds 0.17, so treat-without-CTA remains *defensible if the suite is free*. It is less attractive than at 0.57: a negative CTA now drops you well below threshold (0.047), so CTA is mandatory whenever the suite has opportunity cost, and still wise when it does not. The new treat-without-test decision is “only if delay is costly *and* CTA is unavailable.”

**C.18.2.** Spot-positive \(\log\text{RR} \sim \mathcal{N}(-0.35, 0.25^{2})\). Expansion prior 0.56. Implied ARR?

Point RR \(= e^{-0.35} \approx 0.70\). Expansion under intensive \(\approx 0.56\times 0.70 = 0.39\). ARR \(\approx 0.17\). Using Chapter 18’s 0.25 conversion to good mRS, functional ARR \(\approx 0.043\), against 0.03 renal harm. The ledger can flip: a 140 target becomes reasonable *in the spot-positive stratum* if you believe the modifier. The target *does* change relative to the unmodified case, and you must say the modifier was elicited, not estimated from this patient.

**C.18.3.** Colleague prior \(\log\text{RR}_{\text{isc}} \sim \mathcal{N}(-0.20, 0.15^{2})\). Mixture after negative 30-day monitor (P(AF) \(= 0.05\)); \(\Delta EU\)?

Class-level median RR \(= e^{-0.20} \approx 0.819\). Mixture RR \(= 0.05\times 0.50 + 0.95\times 0.819 = 0.803\). Ischemic risk \(5.0\times 0.803 = 4.015\) per 100, ARR \(= 0.985/100\). \(\Delta EU = 0.00985 - 1.8\times 0.004 = 0.00985 - 0.0072 = +0.00265\). Barely positive. The colleague smuggled *cardioembolic mechanism* into an ESUS residue class: the \(-0.20\) is an AF-trial number wearing an ESUS label.

**C.18.4.** Case 4 posterior was \(\mathcal{N}(14.3, 19.6^{2})\). Next four completers: active \(+60, +60\), placebo \(-10, -10\). Updated posterior? \(P(\delta > 20)\)?

New means: active \(n=10\), sum \(= 8\times 22 + 120 = 296\), mean \(29.6\). Placebo \(n=8\), sum \(= 6\times 4 - 20 = 4\), mean \(0.5\). MLE contrast \(= 29.1\). Variance \(40^{2}(1/10+1/8) = 360\). Combine with skeptical \(\mathcal{N}(10, 30^{2})\): posterior precision \(= 1/900 + 1/360 = 0.003889\), mean \(= (10/900 + 29.1/360)/0.003889 \approx 23.6\), SD \(\approx 16.0\). \(P(\delta > 20) = 1 - \Phi((20-23.6)/16) = \Phi(0.225) \approx 0.59\). Up from roughly 0.38. Not a go under the 0.80 rule.

---

## Chapter 19 — Complete Workflow

**C.19.1.** 90-second SAH version after negative CT at 8 hours. Which steps remain? Sentence?

Steps 1, 2, 6, 7, 8, 9. (3–5 and 10 are the registry.) Question: LP or not. Prior: teaching 0.08 thunderclap. Likelihood: CT at 8 h, LR\(^{-}\) teaching \(\approx 0.10\). Posterior \(\approx 0.009\). Threshold: if you value missed SAH very high, LP still; many will stop. Sentence: “The scan makes a bleed very unlikely, under one in a hundred. A lumbar puncture can push that lower still; I do not think we need it unless you want every last bit of certainty.” Update: if a sentinel-headache story hardens, reopen.

**C.19.2.** Operations will not price suite-hours. Two ways to finish step 7.

(1) Show the expected-utility *surface* over a range of prices and mark the cutoff that is stable across the range they find “plausible.” (2) Constrain: maximize expected independents subject to a hard cap (e.g., 8 wasted hours/month) that they *will* state. “Pick the cutoff you like” is not on the list.

**C.19.3.** 80/420 CTA missing, skipped when LVO seems unlikely. Direction of bias on \(\beta_{\text{NIHSS}}\)?

Missingness is informative and tied to low clinician-suspected LVO, hence to low NIHSS. Complete cases over-represent high NIHSS and confirmed LVO. The NIHSS–LVO slope in complete cases is typically *flattened* at the low end (the very slice a cutoff of 8 needs) and can be *steepened* if remaining low-NIHSS complete cases are the ones clinicians already thought were LVO. Net: biased, direction slice-dependent, unusable for the NIHSS 6–9 calibration. Model the missingness or retrieve the missing CTAs.

**C.19.4.** Prior \(\beta \sim \mathcal{N}(0.12, 0.06^{2})\). \(P(\beta \leq 0)\)? Consistent with “NIHSS is a useful enricher”?

\(z = (0-0.12)/0.06 = -2\), \(P(\beta \leq 0) = \Phi(-2) \approx 0.023\). Yes: the prior already says a non-positive slope is surprising. That *is* the claim that NIHSS enriches. It is informative, and it should be, because a prior that put 50% on a useless NIHSS would contradict the clinical story in step 2.

---

## Chapter 20 — Reproducible Pipelines

**C.20.1.** `.gitignore` and `*.stan` / `.cmdstan/`.

Ignore `.cmdstan/` (or the user-level CmdStan tree; it is a toolchain, not a project artifact). Commit generated `fits/*.stan` only if they are the exact Stan that `brms` sampled *and* you want a Stan user to rebuild without `brms`; otherwise ignore them and commit `make_stancode()` output in the supplement. Always ignore `data/raw/`, `.Rproj.user`, `renv/library/`, `.quarto/`. Commit `renv.lock` and `R/`.

**C.20.2.** Three reasons a private GitHub raw extract is still wrong.

(1) Private is not an access-control story: forks, departing collaborators, screenshots, Actions logs. (2) Git history never forgets; deleting the file later leaves the blob. (3) Institutional contracts and HIPAA/GDPR do not make an exception for “we used a private repo.” Put raw extracts on the approved store; Git gets derived tables.

**C.20.3.** 1.8 GB `brmsfit`. Sharing strategy.

Do not put it on Git. Store it in institutional object storage or Git LFS if allowed. Commit a SHA256 in the sidecar. For strangers: commit posterior *summaries* (`summarise_draws` CSV), a thinned `draws.csv` sufficient to rebuild inline numbers, and a simulated-data script that refits a toy version. The manuscript reads the summaries; the full `.rds` is available on request under a data-use path.

**C.20.4.** A test that catches `nihss` → `NIHSS`.

```r
need <- c("y_ind", "nihss", "age_c", "aspecs", "hospital")
stopifnot(all(need %in% names(d)))
stopifnot(is.numeric(d$nihss), all(d$nihss >= 0 & d$nihss <= 42))
```

Run this at the top of `02-fit-model.R` and `03-checks.R`. A rename then dies before Stan compiles a model on the wrong columns.

---

## How to use these solutions

If your numerical answer disagrees in the second decimal, check whether you used odds or probabilities and whether you treated a teaching LR as independent of a base rate that already contained the same sign. If your *action* disagrees, write the utility you used; the algebra in this appendix is not a policy.

!!! success "Key Takeaway"
    Eighty exercises, one standard: a number, a contrast, an action. Where the chapter asked for a sentence, the solution is a sentence. Where it asked for algebra, the solution is the algebra. Teaching numbers stay teaching numbers. If a solution feels too neat, it is because the loss function was specified; real Friday afternoons are the same loop with a messier \(u\).

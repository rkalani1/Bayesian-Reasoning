# Appendix C — Solutions to Exercises

Solutions to the first four exercises of each chapter, plus each chapter’s “hint for the appendix” exercise where one is flagged (Chapters 14–17). Teaching numbers are the curriculum’s invented values, not estimates from named trials. Algebra is shown; where a `brms` fit was specified but not run, the solution is the number you can obtain by conjugate arithmetic or by the identity the chapter asked for.

---

## Chapter 1 — Why Bayesian Thinking Matters

**C.1.1.** Pre-test 2%, test 95% sensitive and 95% specific, positive result. Natural frequencies in 1,000 people: 20 diseased, of whom 19 test positive; 980 well, of whom 49 test positive. Posterior \(= 19/(19+49) \approx 0.28\), not 0.95. System 1 treated sensitivity as a posterior (base-rate neglect).

**C.1.2.** Audit 14/40. Prior Beta(1, 1) \(\to\) posterior Beta(15, 27), mean \(15/42 = 0.357\). Normal approximation SD \(\approx 0.073\), so \(P(\pi > 0.25 \mid y) \approx 0.93\). Prior Beta(60, 140) \(\to\) Beta(74, 166), mean \(74/240 = 0.308\), SD \(\approx 0.030\), \(P(\pi > 0.25 \mid y) \approx 0.97\). The flat prior is not “more objective”; it is a claim that 1% and 99% were equally plausible before the audit. Objectivity is whether the prior’s implied sample size is defensible, not whether the hyperparameters look empty.

**C.1.3.** Frequentist: “This interval comes from a procedure that covers the true alteplase risk difference in 95% of repetitions; this interval is one draw from that procedure.” Bayesian: “Given the prior we wrote and these data, 95% of the posterior mass on the risk difference sits between these two numbers.” Only the second sentence is a probability statement about the **parameter after these data**. To say it to a family you still have to transport it to *her* and name a utility; the interval alone is not her probability of benefit.

**C.1.4.** “We already have a prior: it is the pre-test we used when we decided she was a candidate. Leaving it implicit does not make it less real; it only makes it un-auditable. Writing it down is how a later paper, a later fellow, or a later lawyer can see what we thought before the next datum arrived. I am not offering legal advice; I am refusing to pretend that silence is neutrality.”

---

## Chapter 2 — Probability, Odds, Uncertainty

**C.2.1.** Odds \(= p/(1-p)\). Then \(\times 4\), then \(p' = o'/(1+o')\).

| Pre-test | Odds | \(\times 4\) | Post-test |
|---|---|---|---|
| 0.05 | 0.053 | 0.211 | 0.17 |
| 0.20 | 0.250 | 1.00 | 0.50 |
| 0.50 | 1.00 | 4.00 | 0.80 |
| 0.80 | 4.00 | 16.0 | 0.94 |

The 0.20 pre-test is moved *onto* a 0.50 threshold; it does not cross a strict \(> 0.50\) rule. The 0.05 pre-test stays far below. The 0.50 and 0.80 start at or above.

**C.2.2.** (Probability of an event) “I assign 0.40 to the event ‘mRS 0–2 at 90 days.’” (Likelihood function) “The likelihood of the observed NIHSS under a good-outcome model is 40% of the likelihood under a poor-outcome model” — almost certainly not what she meant. (Colloquial belief) “I am somewhat less than even-money that things will go well.” She probably intended the first, dressed in the third. Ban “likelihood” for the first meaning.

**C.2.3.** Sn \(=\) Sp \(= 0.95\). PPV \(= \mathrm{Sn}\,\pi / (\mathrm{Sn}\,\pi + (1-\mathrm{Sp})(1-\pi))\).

| \(\pi\) | Monte Carlo / exact PPV | Naive 0.95 |
|---|---|---|
| 0.001 | 0.019 | 0.95 |
| 0.02 | 0.279 | 0.95 |
| 0.20 | 0.826 | 0.95 |

Rounds sentence for the 0.001 row: “In a one-in-a-thousand disease, a 95-percent-accurate positive test is still a 2-percent disease — about one true case in fifty positives.”

**C.2.4.** Aleatory: even with \(\pi\) known, *this* hematoma may or may not expand in the next six hours — a CT **now** does not change that coin. Epistemic: is the spot real, and what is the current volume — a better read (or a second reader) of the film you already have can change that. The fellow’s 2-hour repeat NCCT is waiting to **observe** the coin, not buying a sharper \(\pi\). The epistemic move is the attending read of the spot already on the scan.

---

## Chapter 3 — Bayes’ Theorem

**C.3.1.** Prior 0.02, LR\(^{+}\) \(= 8\). Odds \(= 0.0204 \times 8 = 0.163\), posterior \(\approx 0.14\). That is above a typical LP-for-SAH test threshold and usually below a “skip LP, go straight to CTA/angiography” treat threshold. Next test is LP if CT is the only positive, or CTA if you are chasing aneurysm given a higher clinical concern. Name which threshold you mean: testing versus treating.

**C.3.2.** The exam, the DWI, and the story are not conditionally independent given stroke-versus-mimic. They are three views of one cortical pattern. Multiplying LR \(= 3\) three times pretends you saw three independent assays and produces LR \(= 27\), a fiction. Use the single best LR, or a model that includes their covariance. Agreement is comforting; it is not a factor of 27.

**C.3.3.** Mild stroke, NIHSS 3. Benefit of treating true disabling ischemia is smaller than in NIHSS 14; harm of ICH is not. \(p^{*}\) therefore sits higher — teaching range 0.35–0.50 rather than 0.15. Testing threshold (perfusion) sits below that. Apixaban three hours ago raises \(C\) sharply (the harm term: the cost of treating a patient who would not benefit), which raises both marks and can erase the testing interval: you may wait without perfusion because the treat threshold has climbed above any posterior a perfusion scan can deliver.

**C.3.4.** Hour 18, Sn 0.85, Sp 0.99, prior 0.10. LR\(^{-}\) \(= 0.15/0.99 = 0.152\). Odds \(= 0.111 \times 0.152 = 0.0168\), posterior \(\approx 0.017\). Hour-three teaching LR\(^{-}\) is much smaller (CT is more sensitive early), posterior about 0.005–0.006. Sentence: “A normal scan at three hours would have left the chance of a bleed well under one in a hundred. At eighteen hours the same pictures leave it closer to two in a hundred, which is why a lumbar puncture still earns its keep.”

---

## Chapter 4 — Priors

**C.4.1.** \(\theta \sim \mathcal{N}(0, 0.4^{2})\) on log-OR. Approximate 95% interval on OR: \(\exp(\pm 1.96 \times 0.4) \approx (0.46, 2.19)\). For BAO EVT this is weakly informative leaning skeptical: it centers on no effect and still allows a doubling or a halving. It is not enthusiastic (that would sit above 1 with a tighter upper tail) and not a spike at 0.

**C.4.2.** A worked self-elicitation (teaching): bounds on ARR for independence, BAO EVT, \((-0.05, 0.25)\); quartiles 0.04 and 0.14; median 0.08. A Normal(0.08, \(0.07^{2}\)) matches roughly; a Beta on the two arm-risks would be more honest. What you discover: the interval is wider than the last paper’s confidence interval, which is the point of elicitation — you do not yet have that paper’s \(n\) in *this* population.

**C.4.3.** Six sentences. Anterior-circulation EVT is a different vessel, a different time-density of data, and a different untreated prognosis. Setting the power-prior weight \(a_0 = 1\) declares those trials fully transportable to BAO, which is a scientific claim, not a default. If you believe transport is partial, \(a_0\) is the parameter of that belief and must sit well below 1. A hierarchical \(\tau\) between circulations does the same job with a distribution instead of a scalar. Either is criticizable. \(a_0 = 1\) is not modest; it is maximal borrowing wearing a humble symbol. Write the implied prior interval on the BAO ARR and see whether the committee still wants \(a_0 = 1\).

**C.4.4.** Untreated independence \(\approx 0.20\) with prior \(n = 50\) is Beta(10, 40) on the probability scale. On the `brms` intercept (logit) that is a Normal at \(\text{logit}(0.20) \approx -1.39\) with SD chosen so that the implied prior \(n\) is about 50, roughly `prior(normal(-1.39, 0.35), class = Intercept)` — the 0.35 is the delta-method logit SD of Beta(10, 40), not a round number pulled from the air. Check with a prior-predictive draw on \(\pi\), not by staring at the logit SD.

---

## Chapter 5 — Likelihoods and Conjugate Models

**C.5.1.** Data: 2 sICH in 48. Skeptical Beta(2, 18) \(\to\) Beta(4, 64), mean 0.059. \(P(\theta > 0.06 \mid y) \approx 0.43\). Enthusiastic Beta(2, 98) \(\to\) Beta(4, 144), mean 0.027, \(P(\theta > 0.06 \mid y) \approx 0.02\). The probability moves by about 0.41. In front of a plaintiff expert you defend the prior whose implied sample size and location you can source — the chapter’s historical Beta(8, 142), or the skeptical Beta(2, 18) — not the enthusiastic Beta that buries 2/48 under 100 imaginary safe cases.

**C.5.2.** Posterior Beta(10, 188). \(P(Y^{\star}=0 \mid n^{\star}) = B(10, 188+n^{\star})/B(10, 188) = \prod_{k=0}^{n^{\star}-1}(188+k)/(198+k)\). This product falls through 0.20 near \(n^{\star} = 34\) (teaching: 0.206 at 33, 0.197 at 34). That \(n^{\star}\) is the next-quarter volume at which “we had a clean quarter” stops being surprising under the current posterior. Below that volume, a zero-event quarter is still the mode.

**C.5.3.** Gamma shape-rate. Prior Gamma(4, 2), exposure \(t=2\), \(y=7\). Posterior Gamma(\(4+7\), \(2+2\)) \(=\) Gamma(11, 4), mean \(11/4 = 2.75\) per month. Next month \(t=1\), predictive is Negative-Binomial: \(P(Y=k) = \binom{k+10}{k}(4/5)^{11}(1/5)^{k}\). Summing \(k=0\) to \(5\) gives \(\approx 0.92\), so \(P(Y \geq 6) \approx 0.08\).

**C.5.4.** \(\log 50 \approx 3.912\), \(\log 44 \approx 3.784\), \(\sigma^{2} = 0.1225\). Prior precision \(1/0.0225 \approx 44.4\); likelihood precision \(30/0.1225 \approx 244.9\). Posterior mean of \(\mu = (44.4\times 3.912 + 244.9\times 3.784)/289.3 \approx 3.804\). Posterior median door-to-needle \(= e^{3.804} \approx 45\) minutes. Quote the median because the committee thinks in minutes and the log-normal mean is \(e^{\mu+\sigma^{2}/2}\), a different object.

---

## Chapter 6 — Hierarchical Models

**C.6.1.** Six sentences. The 0.61 is the crude mean of 30 binary outcomes; it is not wrong as a description of those 30. It is noisy as a description of C8’s *underlying* rate. Partial pooling uses the other centers to say how widely true rates wander (\(\tau\)) and then shrinks C8 toward the network mean by an amount that 30 patients and that \(\tau\) justify. 0.74 is the posterior mean of that underlying rate, not a rewrite of your 18/30. If \(\tau\) is large, we barely shrink you; if \(\tau\) is small, 30 is not enough to keep 0.61. I will show you both the crude and the shrunk number, and I will not rank C8 on either without a predeclared rule.

**C.6.2.** If treatment is nearly aliased with center, \(\beta\) in `y ~ treatment + (1 | center)` is identified only by the few off-diagonal patients. Interpretation collapses toward “the four early-adopter centers differ from the four late ones,” which you already knew. Add a center-level covariate for adoption (or `(1 + treatment | center)` if within-center contrast exists) and say that the main-effect \(\beta\) is no longer the network causal effect.

**C.6.3.** Nested: `y ~ treatment + (1 | center/operator)` or equivalently `(1 | center) + (1 | center:operator)`. Crossed (operators at several centers): `y ~ treatment + (1 | center) + (1 | operator)`.

**C.6.4.** `exponential(4)` on the SD (mean 0.25) is much closer to complete pooling than `exponential(0.1)` (mean 10). Defend the tighter prior if eight centers and clinical knowledge say true reperfusion rates do not wander by 20 points; defend the looser one if the network includes a brand-new spoke. Show both \(\tau\) posteriors at the meeting.

---

## Chapter 7 — Computational Inference

**C.7.1.** Six questions. (1) How many *post-warmup* draws, not “iterations”? (2) \(\widehat{R}\) on every parameter you will quote? (3) Bulk and tail ESS? (4) Divergences, and if any, where? (5) Seed, backend, `adapt_delta`? (6) Is this the marginal posterior of the *decision* quantity, or a transformed leftover? No density enters a slide until (1)–(5) are boring.

**C.7.2.** A wide kernel averages two well-separated lumps into a camel that looks like a hill. \(\widehat{R}\) compares between-chain to within-chain variance; here the chain means sit \(\pm 0.5\) from the pooled center, so the between-chain variance is on the order of \(\mathrm{gap}^2/4 = 0.25\) while the within-chain variance is tiny, so \(\widehat{R}\) is large. Unimodality of a smeared plot is not mixing.

**C.7.3.** Three divergences in an intercept-only logistic: rerun with a longer warmup or `adapt_delta = 0.95`; if they vanish, you are done. Two hundred forty divergences with \(\tau\) piled at zero: the geometry is a funnel. Reparameterize (non-centered), put a tighter prior on \(\tau\), or both. Raising `adapt_delta` alone is a delay, not a repair.

**C.7.4.** Tail ESS 220 with an interval that kisses zero is not “statistically significant”; it is an under-resolved tail. Tell the fellow the sign is unstable under the sampling error of the *sampler*. Double the post-warmup draws, check the rank plot of `b_spot`, and only then discuss whether the interval excludes zero — which is still the wrong headline (Chapter 9).

---

## Chapter 8 — Model Checking

**C.8.1.** Three checks before quoting 0.07: (i) calibration in the slice this patient belongs to (ICH score or NIHSS band), not only globally; (ii) prior sensitivity of *that* 0.07, not of a coefficient; (iii) PPC for the event count in that slice. Still missing even then: whether 0.07 sits above this family’s treat/wait threshold. Calibration is not a decision.

**C.8.2.** Strata: ASPECTS 0–4, 5–7, 8–10, crossed with age \(\geq 80\) if \(n\) allows. Discrepancy: observed minus predicted mRS 0–2 count in the ASPECTS 0–4 cell, and a calibration intercept in that cell. If the leftover is systematically negative, the model ignores how bad low ASPECTS is.

**C.8.3.** Exact LOO on the three PH2 deaths tells you whether the model *can* predict a fatal PH2 when it is held out. High \(k\) means those points are already surprising. Deleting them makes the remaining ELPD look fine and hides that the likelihood has no room for the worst ICH. Report the three exact hold-outs and the clinical common cause.

**C.8.4.** Four sentences. The protocol required \(> 0.90\) under *all* pre-specified priors. The skeptical prior gives 0.78. The association is therefore not established by the rule we wrote. I will report both probabilities, refuse a single-prior headline, and not shop for a third prior that restores 0.90.

---

## Chapter 9 — Estimation, ROPE, Bayes Factors

**C.9.1.** “We think it is quite likely the medicine helps a little. On a scale of 42, the average help looks closer to one point than to the two points we had said would matter. Some people will do better than that average, some worse. I would not promise you a recovery you can feel; I would not say it does nothing either.”

**C.9.2.** Abstract the HDI on the OR if you are describing the most credible values; it is the shortest 95% set. The ETI goes further into the right tail and starts higher because of skew. On the log-odds scale the posterior is closer to symmetric, so HDI and ETI nearly agree. Quantile-based intervals survive monotone transforms: exponentiating the log-OR **ETI** gives the ETI on the OR scale. The HDI does not: exponentiating a log-OR HDI gives a 95% interval that is in general neither the OR HDI nor the OR ETI (here it approximates the OR ETI only because the log-scale posterior is nearly symmetric). Compute the HDI on the OR draws if you want an HDI of ORs; exponentiate an ETI if you want OR endpoints of an ETI.

**C.9.3.** A ROPE of \((-0.02, 0.02)\) on a 90-day mRS 0–2 risk difference says a 2-point absolute swing is noise. In mild stroke that may be too tight if the outcome is already common and the harm (ICH) is 2–4 points; it may be too wide if you would treat for a 1-point gain in a low-harm drug. Widen the ROPE if ICH is cheap on your utility; narrow it if even a 1-point gain is worth a large \(N\).

**C.9.4.** A Normal(\(0, 20^{2}\)) prior under \(M_1\) puts nearly all its mass on impossible NIHSS differences (tens of points). That does not help \(M_1\); it dilutes it. The marginal likelihood of \(M_1\) is spread over values the data refute, so the Bayes factor is dragged toward the null: for the vignette (\(\hat\delta = -1.4\), SE \(0.7\)), \(\mathrm{BF}_{01} \approx 4\) — apparent “evidence for no effect” manufactured by a silly alternative (the Jeffreys–Lindley effect from the chapter). The number is mostly a statement about the prior, not the drug. Demand a pre-specified alternative on the scale of the estimand with clinically possible mass — teaching, \(\mathcal{N}(0, 3^{2})\) NIHSS points — under which \(\mathrm{BF}_{10} \approx 1.5\): weak evidence either way, in agreement with the estimation summary.

---

## Chapter 10 — Sample Size and Adaptive Designs

**C.10.1.** “0.93 is the probability the effect is positive *given what we have*. 0.18 is the probability that, if we continue to the maximum \(N\), the *finished* analysis will meet the success rule. Those are different questions. Continuing spends the remaining patients on an 18-percent chance of a label claim. Under the charter, PPoS below 0.25 is stop-for-futility. I vote stop. ‘Almost there’ describes the current sign, not the remaining information.”

**C.10.2.** Beta(3, 3) is a wide design prior; assurance at a max of 80 falls because much of the prior mass sits near 0.5, where the rule rarely fires. Beta(20, 11) is a tight enthusiastic prior; assurance rises, sometimes a lot. For an encephalitis grant defend the wide one, or a mixture with a skeptical spike: you do not yet know this antibody. The tight Beta is a hope, not a design prior.

**C.10.3.** True \(p = 0.45\) is on the boundary of the success event \(P(p>0.45 \mid y) > 0.90\). At one look this is a type-I analogue near **0.10**, not 0.05; more looks inflate it. Simulate the exact schedule; do not guess. Looking every 5 instead of every 10 spends more looks and inflates that rate unless you tighten the threshold.

**C.10.4.** Expect an interaction if intensive BP and a particular reversal agent share a coagulopathy pathway (hematoma expansion). Randomize within cells of the other domain, or model the interaction and keep allocation factorial. Report each domain’s marginal posterior *and* the interaction; a pooled “BP works” headline that averages over reversal strategies is the wrong estimand if the interaction is the biology.

---

## Chapter 11 — Diagnostic Accuracy

**C.11.1.** Spoke-negative: Se \(\sim\) Beta(47, 7), Sp \(\sim\) Beta(23, 7). Draws of LR\(^{-}\) \(= (1-\mathrm{Se})/\mathrm{Sp}\) sit near 0.17 (mean). Teaching pre-test 0.55 \(\to\) posterior LVO probability near 0.17 (a Monte Carlo band of about 0.10–0.28). You still launch after a negative spoke read only if the pre-test is high enough that even LR\(^{-}\) leaves you above the transfer threshold. With a 0.40 launch bar, that pre-test is about 0.80. This NIHSS-12 / AF patient is not there. Do not launch on the negative spoke read alone; the telestroke over-read is the live likelihood.

**C.11.2.** Teaching: of 40 never-transferred spoke-negatives with NIHSS 4–7, perhaps 2–6 had LVO (5–15%). Adding them as unverified negatives increases the apparent TN count and *raises* estimated Sp. DSA-only Sp is therefore biased *down* (the verified non-LVO are the ones odd enough to transfer). Sensitivity is also distorted: missed LVOs never enter \(n_D\). Direction: DSA-only Sp too pessimistic; network Sp after honest imputation higher.

**C.11.3.** AUC of ASPECTS for mRS 0–2 after EVT is a *prognostic* discrimination of outcome given that you already treated. AUC of ASPECTS for LVO is a *diagnostic* discrimination of the state that decides transfer. The transfer decision needs the second (and, honestly, NIHSS plus CTA, not ASPECTS alone). The first belongs in a counseling model after the vessel is known.

**C.11.4.** Raw pooled Se averages readers. The fifth spoke’s 0.72 will shrink toward the network, but not to 0.85, if \(\tau_s\) is real. Quoting the pool as *that spoke’s* Se is a lie to their next patient. Defend a half-normal on \(\tau_s\) with scale 0.4–0.6 on the logit (Worksheet 3, Appendix B): a spoke at 0.72 among four at 0.9 is unusual, not impossible.

---

## Chapter 12 — Survival and Competing Risks

**C.12.1.** Not a composite of “dead or mRS \(\geq 4\)” — nearly everyone in this cohort occupies mRS \(\geq 4\) in the first days, so that “event” fires at time zero and carries no information. Use a Fine–Gray model for the subdistribution of “mRS \(\leq 2\)” (or time to *sustained* mRS \(\leq 3\)) with death as the competing event. Estimand: cumulative incidence of good function at day 90, with death occupying its own incidence. Death is a competitor, not a censor.

**C.12.2.** (a) Cox for death: D is last seen alive at day 40, so the contribution is a survival term \(S_{\text{death}}(40 \mid x_D)\). (b) Cause-specific Cox for time to mRS \(\leq 2\): D has neither the good event nor death by day 40. Administrative censoring at last contact *is* the correct CS contribution, \(S_{\text{cs, good}}(40 \mid x_D)\). Death, had it occurred, would also be a CS-censor for this hazard; it is not a “failure.” A Fine–Gray / CIF likelihood is a different object and would use the subdistribution risk set, not this survival term. (c) Ordinal day-90 mRS with D missing: D contributes the marginal likelihood of the missing ordinal under a named MAR/MNAR model (Chapter 24), or is dropped — which is a different, worse estimand.

**C.12.3.** No recovery before day 30, no death after day 30. Day-90 good-outcome CIF \(= (1-0.28)\times 0.31 = 0.223\). A death-censored \(1-\mathrm{KM}\) is tempted to report 0.31 — the probability among *survivors* — as if the dead had been merely unobserved. That is the number families do not ask for.

**C.12.4.** \(\mathcal{N}(0, 3^{2})\) on the log-odds treatment effect says odds ratios out to \(e^{\pm 6} \approx 400\) are ordinary. That encodes “ICH blood-pressure trials could be miracle or catastrophe.” Accept it only as a sensitivity prior, never as the primary, and only to show the posterior does not depend on the tight \(\mathcal{N}(0, 0.5^{2})\).

---

## Chapter 13 — Bayesian Meta-Analysis

**C.13.1.** Six sentences. \(\mu\) is the average true effect across the studies you already have. \(\theta_{\text{new}}\) is the effect *you* will get, including the extra scatter \(\tau\). Late-window EVT without perfusion is a new imaging gate, so you are \(\theta_{\text{new}}\) under a different \(x\), not a draw of \(\mu\). The prediction interval is the honest one, and it is wider. If that interval still sits above your treat threshold, offer EVT; if it includes harm, do not launch a service on \(\mu\) alone. Buy perfusion or join a registry before you treat \(\mu\) as a promise.

**C.13.2.** SEs \(\times 1/10\) make each study look huge. The likelihood for \(\tau\) becomes a spike near the observed between-study SD. The half-Cauchy versus half-normal debate then *stops* mattering for \(\tau\) and for \(\theta_{\text{new}}\); both priors are overwhelmed. With the original SEs and three studies, the prior on \(\tau\) is most of the result.

**C.13.3.** Cells are 0/90 versus 3/92, so non-events are 90 and 89. Add 0.5 to *each cell*: \((0.5/90.5)/(3.5/89.5) = (0.5\times 89.5)/(3.5\times 90.5) \approx 0.141\), log-OR \(\approx -1.96\). The ratio \((0.5/90.5)/(3.5/92.5)\) is a continuity-corrected *risk ratio*, not an odds ratio — do not put it in an OR forest. Prefer two independent binomials (or a logistic GLM) with a weakly informative prior on the log-OR; zeros stay zeros. Do not put the continuity-corrected \(-1.96\) in a forest plot as if it were data.

**C.13.4.** Put an indicator for “perfusion-gated late window” on \(\mu_i\). Prior on that \(\beta\): \(\mathcal{N}(0, 0.4^{2})\) on the log-OR — wide enough to let C differ, too tight to let three studies invent a 4-fold modifier. C can then sit off the A–B pool without being a separate meta-analysis of one.

---

## Chapter 14 — Decision Theory and Thresholds

**C.14.1.** \(p^{*} = 0.90 = H/(B+H)\) \(\Rightarrow\) \(B/H = (1-0.90)/0.90 = 1/9 \approx 0.11\). You will accept about one benefit per nine harms. That is a banner threshold (treat only if nearly sure), not a sister threshold (accept 1 harm to gain 10 benefits, \(B/H = 10\), \(p^{*} \approx 0.09\)).

**C.14.2.** Teaching \(B=0.40\), \(H=0.30\), \(Se=0.80\), \(Sp=0.70\).

| \(R\) | \(T_t\) | \(T_{tt}\) |
|---|---|---|
| 0 | \(0.09/0.41 = 0.220\) | \(0.21/0.29 = 0.724\) |
| 0.08 | \(0.17/0.41 = 0.415\) | \(0.13/0.29 = 0.448\) |

The interval vanishes when \(T_t \geq T_{tt}\), which solves to \(R \approx 0.086\) (set the two closed forms equal; C.14.6 shows the algebra). A test whose disutility is about a fifth of \(B\) is not worth buying.

**C.14.3.** Three states, three actions (treat, test, wait) produce a tree with six terminal utilities, not two. Thresholds become *surfaces* in the two-simplex of state probabilities. A single \(p^{*}\) exists only when the state is binary. Mild aphasia is exactly this: mimic versus nondisabling ischemia versus disabling ischemia.

**C.14.4.** They will not match. “Hemorrhages per language life saved” elicits \(H/B\) in count units; “chance of recovery you would forgo to avoid a bleed” elicits a probability trade that maps to the same ratio only if the respondent is an expected-utility agent who heard both frames as the same gamble. Framing, numeracy, and the word *hemorrhage* move the number. Record both and notice the preference is unstable — Chapter 14’s cue to stop over-quantifying.

**C.14.6.** Set \(T_t \geq T_{tt}\) and cross-multiply (both denominators are positive):

\[
\bigl[(1-Sp)H + R\bigr]\bigl[Sp\,H + (1-Se)B\bigr] \;\geq\; \bigl[Sp\,H - R\bigr]\bigl[(1-Sp)H + Se\,B\bigr].
\]

The \(Sp(1-Sp)H^2\) terms cancel; collecting the rest gives \(R\,(B+H) \geq B\,H\,(Se+Sp-1)\), so the testing interval vanishes exactly when

\[
R \;\geq\; \frac{B\,H\,(Se+Sp-1)}{B+H}.
\]

The right side is the test’s information value: it scales with the Youden index \(Se+Sp-1\) (zero for a useless test, so *any* risk kills it) and with the stakes \(BH/(B+H)\). Teaching numbers \(B=0.40\), \(H=0.30\), \(Se=0.80\), \(Sp=0.70\): \(R^{*} = 0.12 \times 0.5 / 0.7 \approx 0.086\), matching C.14.2.

---

## Chapter 15 — Decision Curves and VOI

**C.15.1.** Treat-none net benefit is 0. \(\kappa\) beats it when \(Se\,\pi - (1-Sp)(1-\pi)\,p_t/(1-p_t) > 0\). Plug in \(\pi=0.06\), \(Sp=0.75\), \(p_t=0.20\): \(Se\times 0.06 > 0.25\times 0.94\times 0.25 = 0.05875\), so \(Se > 0.979\). At this low prevalence and this threshold, \(\kappa\) needs near-perfect sensitivity to beat doing nothing.

**C.15.2.** Drop \(\pi\) from 0.06 to 0.02. Treat-all’s net benefit becomes negative over a wider range of \(p_t\) (it already crosses zero at \(p_t=\pi\); see C.15.4). \(\kappa\)’s curve drops because true positives are rarer and false positives are not. Treat-all dies first; then \(\kappa\) dies relative to treat-none except at very low \(p_t\).

**C.15.3.** “The fellow’s action flips only if the marker moves a posterior across a threshold; re-estimating AUC on 200 patients can leave calibration and that threshold untouched, so the expected value of that sample for *this* decision is near zero.”

**C.15.4.** Treat-all NB \(= \pi - (1-\pi)\,p_t/(1-p_t)\). Zero when \(\pi(1-p_t) = (1-\pi)p_t\), i.e. \(p_t = \pi\). In harm/benefit language: treat-all is worthwhile only when prevalence exceeds the treat threshold. If disease is rarer than the harm/benefit bar, treating everyone loses.

**C.15.6.** For a binary action, regret in state \(\theta\) is \(\rho(\theta) = \max_a U(a, \theta) - U(a^{\star}, \theta) \geq 0\), the utility you gave up by not knowing \(\theta\). Then \(EVPI = \mathbb{E}\bigl[\max_a U(a,\theta)\bigr] - \mathbb{E}\bigl[U(a^{\star},\theta)\bigr] = \mathbb{E}[\rho(\theta)]\): EVPI *is* expected regret. It is identically zero exactly when \(a^{\star}\) is optimal in every state with positive posterior probability — no revelation of \(\theta\) could change the action. That is the formal version of “the decision is not on a knife edge, so do not buy information.”

---

## Chapter 16 — Bedside Shared Decisions

**C.16.1.** Two spoken arrays of 100. Without EVT: “40 do not survive; 16 are bedridden and need constant care; 22 cannot walk or manage their bodily needs without help; 18 are back to a cane-and-help life; 4 walk independently.” With EVT: “33, 12, 20, 24, 11.” Collapse 0–2 with 3 if the daughter is defending “a life she would recognize” (prestroke 3), and collapse 5 with 6 if “vegetable or dead” is her named harm. Keep 4 visible; it is the state people regret by surprise.

**C.16.2.** “DAWN-positive, we take her” treats a trial-eligibility flag as a command. That is the effective-care error: strong evidence of *average* benefit in a selected population is being used as if the threshold cannot move with prestroke mRS 3, age 89, and the daughter’s utilities. Late-window EVT here is preference-sensitive care. The scan is beautiful. The decision is still hers.

**C.16.3.** The teaching Dirichlet means recover the table: alive and not mRS 5 is \(\operatorname{Beta}(44,56)\) without EVT (mean 0.44) and \(\operatorname{Beta}(55,45)\) with EVT (mean 0.55). The mean increment is 0.11. Independent draws give \(P(\text{EVT better}) \approx 0.94\). That is the number the exercise asked for. To the daughter: “In almost every way we can redraw this table, more people are alive and not needing full care with the procedure — about eleven extra in a hundred.” No “posterior probability.”

**C.16.4.** Best-case: the 90th percentile of the *with-EVT* predictive distribution, states 0–3 heavier. Worst-case: the 10th percentile, states 5–6 heavier. Do not quote the best with-EVT against the worst without-EVT; that is two different worlds. Pair quantiles *within* an action, then show the contrast of medians.

**C.16.6.** “Relative risk of mRS 0–2” compares \(P(\text{mRS 0–2} \mid \text{EVT})\) with \(P(\text{mRS 0–2} \mid \text{no EVT})\) and nothing else. Any summary that depends only on those two numbers corresponds to a utility of the form \(u(\text{state}) = 1\) for mRS 0–2 and \(u = c\) (one constant) for every other state — death, bedridden, full care, and the cane-and-help life the patient already lives are all assigned the *same* value. The daughter named prestroke mRS 3 as the success state and unaware survival as the feared state; the RR of mRS 0–2 is invariant to both. Leading with it therefore smuggles in a utility that erases every value she stated — before the relative framing has even hidden the base rate.

---

## Chapter 17 — Communicating Uncertainty

**C.17.1.** Under 40 words: “With a skeptical Beta(8, 12) prior, 31 of 62 patients were independent; the posterior mean was 0.48 and the pre-specified success rule was not met.” You had to add the prior, the rule, and the miss. You had to delete “uninformative” and “demonstrated benefit.”

**C.17.2.** Beta(39, 43). Mean 0.476. \(P(\theta > 0.50) = 1 - F_{\text{Beta}}(0.50; 39, 43) \approx 0.33\). \(P(\theta > 0.35) \approx 0.99\). Quoting only 0.99 is spin: it is the probability of beating a bar the trial did not care about. Quoting only 0.33 is also spin if you bury the 0.92 against the real bar of 0.40. Report the pre-specified functional.

**C.17.3.** “Thank you — we agree the prior should be labeled precisely. Beta(8, 12) has mean 0.40 and prior sample size 20; it was chosen to encode a skeptical historical independence rate, not to stay out of the way. ‘Weakly informative’ would describe a prior that rules out cartoons while remaining dominated by 62 observations at any plausible mean. This prior can still move the success probability from 0.95 (flat) to 0.92 (ours) to 0.89 (more skeptical) — and the rule fails under all three. We will call it skeptical and show the sensitivity, and we will not call it weakly informative.”

**C.17.4.** Sequential Beta starting at (8, 12), adding one Bernoulli at a time toward 31/62. The mean walks from 0.40 toward 0.48; the 95% band narrows toward 0.37–0.58. A naive reader who ignores the pre-specified \(P(\theta>0.40)>0.95\) rule will declare victory once the posterior mean crosses and stays above 0.45 (the rounded teaching path first touches 0.45 briefly near \(n = 11\); the sustained crossing is near \(n = 20\)). The 95% ET band never excludes 0.40 — it is still 0.37–0.58 at \(n = 62\) — and the pre-specified functional never reaches 0.95. Mark \(n \approx 20\) on the fan and write “mean rule, not the protocol rule.”

**C.17.6.** Let \(\eta \sim \mathcal{N}(0, 10^2)\) and \(\pi = \operatorname{logit}^{-1}(\eta)\). Then \(\pi \notin (0.01, 0.99)\) iff \(|\eta| > \operatorname{logit}(0.99) = \log 99 \approx 4.595\). The two-tailed Normal probability is \(2\Phi(-4.595/10) = 2\Phi(-0.4595) \approx 0.646\), about two-thirds, not more than 80%. The prior is U-shaped on the probability scale. It is not a point mass at 0 and 1, and it is not “uninformative.”

---

## Chapter 18 — Integrated Case Studies

**C.18.1.** Base rate 0.18, examination LR 2.5: prior odds \(= 0.220 \times 2.5 = 0.549\), prior \(= 0.35\). CTA\(+\): posterior \(0.83\). CTA\(-\): posterior \(0.047\). Suite-free treat threshold \(p^{*} \approx 0.17\): 0.35 still exceeds it, so treat-without-CTA remains defensible *if* the suite is free. It is less attractive than at 0.57. A negative CTA now drops you far below threshold, so CTA is mandatory whenever the suite has opportunity cost, and still wise when it does not. New treat-without-test rule: only if delay is costly *and* CTA is unavailable.

**C.18.2.** Point RR \(= e^{-0.35} \approx 0.70\). Expansion under intensive \(\approx 0.56 \times 0.70 = 0.39\). ARR \(\approx 0.17\). With the chapter’s 0.25 conversion to good mRS, functional ARR \(\approx 0.041\) against 0.03 renal harm. The ledger can flip: a 140 target becomes reasonable in the spot-positive stratum *if* you believe the modifier. Say the modifier was elicited, not estimated from this patient.

**C.18.3.** Class-level median RR \(= e^{-0.20} \approx 0.819\). Mixture after P(AF) \(= 0.05\): \(0.05\times 0.50 + 0.95\times 0.819 = 0.803\). Ischemic risk \(5.0\times 0.803 = 4.015\) per 100, ARR \(= 0.985/100\). \(\Delta EU = 0.00985 - 1.8\times 0.004 = +0.0027\). Barely positive. The colleague smuggled cardioembolic mechanism into an ESUS residue class: \(-0.20\) is an AF-trial number wearing an ESUS label.

**C.18.4.** Active \(n=10\), mean \(29.6\); placebo \(n=8\), mean \(0.5\); MLE contrast \(29.1\); variance \(40^{2}(0.1+0.125)=360\). With skeptical \(\mathcal{N}(10, 30^{2})\): posterior precision \(= 1/900 + 1/360 = 0.003889\), mean \(\approx 23.6\), SD \(\approx 16.0\). \(P(\delta > 20) = 1-\Phi((20-23.6)/16) \approx 0.59\). Not a go under the 0.80 rule.

---

## Chapter 19 — Complete Workflow

**C.19.1.** Steps 1, 2, 6, 7, 8, 9 remain (3–5 and 10 are the registry). Question: LP or not. Prior: teaching 0.08 thunderclap. Likelihood: CT at 8 h, LR\(^{-}\) teaching \(\approx 0.10\). Posterior \(\approx 0.009\). Sentence: “The scan makes a bleed very unlikely, under one in a hundred. A lumbar puncture can push that lower still; I do not think we need it unless you want every last bit of certainty.” Update if the sentinel-headache story hardens.

**C.19.2.** (1) Show the expected-utility *surface* over a range of suite-hour prices and mark the cutoff that is stable across the prices they will call plausible. (2) Constrain: maximize expected independents subject to a hard cap (e.g. 8 wasted hours/month) they *will* state. “Pick the cutoff you like” is not on the list.

**C.19.3.** CTA is skipped when LVO seems unlikely, hence when NIHSS is low. Complete cases over-represent high NIHSS and confirmed LVO. The slope in the NIHSS 6–9 slice — the slice a cutoff of 8 uses — is biased, typically flattened at the low end and unusable for calibration. Direction is slice-dependent; the honest statement is “biased, do not use complete cases.” Model the missingness or retrieve the scans.

**C.19.4.** \(\beta \sim \mathcal{N}(0.12, 0.06^{2})\). \(P(\beta \leq 0) = \Phi(-2) \approx 0.023\). Consistent with “NIHSS is a useful enricher”: the prior already says a non-positive slope is surprising. That is informative, and it should be. A prior that put 50% on a useless NIHSS would contradict step 2.

---

## Chapter 20 — Reproducible Pipelines

**C.20.1.** Ignore `.cmdstan/` (toolchain, not a project artifact), `data/raw/`, `.Rproj.user`, `renv/library/`, `.quarto/`. Commit `renv.lock` and `R/`. Commit `fits/*.stan` only if they are the exact Stan that was sampled *and* you want a Stan user to rebuild without `brms`; otherwise ignore them and put `make_stancode()` in the supplement.

**C.20.2.** Three reasons. Private is not access control: forks, departing collaborators, Actions logs. Git history never forgets; deleting the file later leaves the blob. Institutional contracts and HIPAA/GDPR do not exempt “we used a private repo.” Raw extracts live on the approved store; Git gets derived tables.

**C.20.3.** Do not put 1.8 GB on Git. Institutional object storage or Git LFS if allowed; SHA256 in the sidecar. For strangers: commit `summarise_draws` CSV, a thinned `draws.csv` that rebuilds the inline numbers, and a simulated-data script that refits a toy version. The manuscript reads the summaries; the full `.rds` is available on a data-use path.

**C.20.4.**

```r
need <- c("y_ind", "nihss", "age_c", "aspects", "hospital")
stopifnot(all(need %in% names(d)))
stopifnot(is.numeric(d$nihss), all(d$nihss >= 0, d$nihss <= 42, na.rm = TRUE))
```

A rename then dies before Stan compiles a model on the wrong columns.

---


## Chapter 21 — Transporting Evidence and HTE

**C.21.1.** The sentence answered Question 1 (the trial ATE in a DAWN-like frame) and pretended to answer Question 3 (this woman). It did not answer Question 2 either: prestroke mRS 3 is not a trial subgroup with overlap. Six sentences to the daughter: “The scan shows a mismatch like the ones in a late-window trial. That trial enrolled people who were independent before the stroke. She needed a cane and help to bathe. We do not have a trial answer for someone already living that life. Opening the vessel can still help her get back to *her* life; the size of that help is a judgment, not a number we can read off the paper. The decision is yours with her values, not a protocol because a box was ticked.”

**C.21.2.** Trial-weighted ATE \(= 0.28\cdot 0.40 + 0.20\cdot 0.35 + 0.12\cdot 0.20 + 0.04\cdot 0.05 = 0.208\). Hospital-standardized contrast \(= 0.28\cdot 0.15 + 0.20\cdot 0.25 + 0.12\cdot 0.35 + 0.04\cdot 0.25 = 0.144\). The hospital number is still Question 2-for-a-mix, not Question 3: it averages over last year’s admissions, including the 75% who are not this woman. It equals her number (0.04) only if the hospital mix is 100% her phenotype, or if every row has the same risk difference.

**C.21.3.** Hierarchical estimator: the slice log-OR is a noisy draw around a shared mean \(\mu_\beta\); \(\tau_\beta\) is how much genuine modification you will believe across pre-specified slices. With \(n = 16\), the local 1.05 (0.22 to 5.1) is pulled almost to \(\mu_\beta\). If you *refuse* to shrink: “In sixteen patients aged 85 or more the data cannot separate a large benefit from a large harm; we will not export the trial average into this cell.” You are declining exchangeability of the slice with the ATE — the same refusal Chapter 6 makes for a pediatric site in an adult hierarchy.

**C.21.4.** The `brm()` call is a specification. Without the locked teaching file there is no numerical interval to quote as a result. Qualitatively: her posterior predictive under the skeptical \(N(0, 0.25^2)\) interaction is almost the transported ATE; switching to \(N(0, 2^2)\) lets the prestroke-mRS-3 increment roam, so her interval widens and can change sign. That movement is the prior doing the transport. The data past prestroke mRS 3 are too thin to argue.

## Chapter 22 — Causal Target Trials

**C.22.1.** New arrows: treatment \(\to\) PH2 \(\to\) day-90 mRS, and treatment \(\to\) mRS directly. PH2 is a *mediator* of part of the effect, and a *collider* on any open back-door that also points at hemorrhage (severity, anticoagulation, procedure time). It is not a confounder of the ITT contrast: it sits after assignment. Conditioning on it estimates a direct-effect hybrid in the stratum that did not bleed — not the ITT functional the committee asked for. Report PH2 as a secondary harm, not as a covariate.

**C.22.2.** Eligibility: suspected or imaging-confirmed LVO at first medical contact in the network, last-known-well inside the pre-declared window, both routing strategies still available. Strategies: “mothership EVT” versus “spoke thrombolysis then transfer for EVT,” assigned at first medical contact. Time zero: that contact, not hub-door and not puncture. Follow-up: 90-day mRS on everyone, including those who never reach the hub. Estimand: contrast in 90-day ordinal mRS under the two strategies. Immortal-time error: starting the clock at last-known-well and classifying exposure by whether the patient *arrived* at the hub credits transfer survivors to the drip-and-ship arm (they did arrive) and deletes the dead-en-route from it, so the arrival-required strategy looks safer than it is.

**C.22.3.** Crude RD mixes indication and center. The hierarchical intercept without severity absorbs the *time-invariant center confounding* (the \(+8\) in the teaching decomposition) along with center-level sampling noise — that is why the OR fell from 2.1 to 1.4. It leaves confounding by indication (the \(-4\)) and any time-zero misalignment untouched. The standardized RD from the full outcome model is the one that adjusts the back-door set and then g-computes. Tell the committee: the middle number is a partially deconfounded association, not a treatment effect; print the standardized contrast or do not print a contrast.

**C.22.4.** Restricting to “no WLST in 72 hours” conditions on a descendant of early severity and of the treatment decision. It closes the path treatment \(\to\) early course \(\to\) WLST \(\to\) mRS and opens collider paths through whatever predicted withdrawal. Offer the ITT contrast in everyone, with WLST as a secondary event, and accept only *baseline* covariates (age, GCS, volume, anticoagulant, prestroke mRS) on the right-hand side.

## Chapter 23 — Clinical Prediction Models

**C.23.1.** 24-hour NIHSS and TICI are measured *after* the admission note is written. They leak future information into a “baseline” probability, so the apparent AUC is the AUC of a 24-hour model, not of the note. TRIPOD item on predictors (timing of measurement / whether predictors are available at the intended moment of use) should have made the leakage visible even if the software fitted cleanly.

**C.23.2.** You may claim that a spline is slightly better *inside this sample* on PSIS-LOO, with a SE that already includes “no difference.” You may not claim the spline will travel. Two of seven sites preferring linear is a transport warning. Before the spline reaches the note: lock a pre-specified functional form or a hierarchical smoother, check leave-one-hospital-out calibration, and refuse to promote a within-sample ELPD of \(+6\) (SE 4) as a go-live.

**C.23.3.** Mean predicted 0.41 versus observed 0.31 with a slope interval that includes 1 (0.61 to 1.28) is an intercept problem, not a slope collapse. Recalibrate the intercept on the new spoke; do not re-estimate the slope on \(n = 90\). Abstract sentence: “At the new spoke the locked model over-predicted independence (0.41 vs 0.31); the calibration slope was compatible with 1, so we updated the intercept and did not refit coefficients.”

**C.23.4.** Discrimination of 0.81 does not imply the model helps *this* decision. The top calibration bin sitting above the band means the patients you would call “likely independent” are less independent than advertised. The decision curve beats treat-all only below \(p_t = 0.08\); the service will not act unless \(\hat\pi\) for mRS 0–2 is below 0.70, i.e. at thresholds far above where the model has net benefit. Do not put it on the admission note for that action. Build a model for the decision they will actually take, or change the action.

## Chapter 24 — Missing Data and Measurement Error

**C.24.1.** Six sentences: “The estimand is the 90-day ordinal contrast in treated LVO, late versus early window. Complete-case analysis estimates that contrast in the 312 who were found, not in the 400 who were treated. Calling 22% ‘acceptable’ assumes the missing are a coin flip given the covariates you kept — that is MAR, and you did not argue it. Transfers and non-English speakers are over-represented among the 88, so the complete cases are the easy-to-find locals. One MNAR mechanism you cannot rule out from the complete-case table: patients who worsened after a good-looking discharge stop answering the phone. The hole is part of the likelihood, not a footnote.”

**C.24.2.** Complete-case \(P(\text{mRS }0\text{–}2) = 118/312 \approx 0.378\). LOCF adds the 51 discharge 0–2 scores: \(169/400 = 0.423\). Recode the four in-hospital deaths as 6 and shift the 84 living missing one category worse than discharge: with the teaching split 10/16/25 of the 51 discharge 0–2 across mRS 0/1/2, only the 26 at discharge 0–1 remain successes, so independence falls to \((118+26)/400 = 0.36\). Put a MAR imputation plus one named MNAR shift in the abstract. Complete-case and LOCF are labeled sensitivity rows, not “the registry result.”

**C.24.3.** Selection steps: presented with late-window LVO \(\to\) taken for EVT \(\to\) CTP obtained \(\to\) favorable map \(\to\) in the 168. The 0.18 is the association of a favorable map with independence *among imaged, treated, late-window patients*. It is not the effect of treating on a favorable map, and it is not the accuracy of CTP in presenting patients.

**C.24.4.** Sketch: latent true ASPECTS as a varying intercept; resident and attending readings as two observation equations; ordinal mRS on the latent score. In `brms`, a measurement submodel (`me()` if the attending error SD is treated as known; a bivariate or hierarchical measurement model if not) plus `family = cumulative("logit")` for \(Y\). Prior on the resident’s extra error: a half-normal that puts most mass below one ASPECTS point and still allows two. If the over-read subset is “interesting” scans, say so: the attending reading is MNAR with respect to true ASPECTS, and the latent score in the un-over-read majority is identified only by the resident plus that selection story.

## Chapter 25 — GRADE and Evidence-to-Decision

**C.25.1.** Estimand: “posterior probability that late-window EVT beats control on UW-mRS in the *trial-like* populations of A and B.” Certainty: still only moderate-to-high for *that* estimand, because transport and unblinded mRS remain. Strength: Class I is a recommendation, not a posterior. Stratum: A/B, not consecutive late-window LVO. The 0.95 is allowed to support only the estimand sentence.

**C.25.2.** A (0.07 to 0.21): entirely above 0 and above 0.03; not above 0.10. B (0.01 to 0.15): entirely above 0; not above 0.03 or 0.10. C (−0.03 to 0.11): none of the three. Imprecision is location relative to a named threshold, not width. “The interval is wide” does not say whether the whole mass sits above the worthwhile increment.

**C.25.3.** Risk of bias: prior on reader- and center-dependent Se/Sp. Indirectness: transport parameter from comprehensive-center scans to spoke overnight reads. Imprecision: posterior width on the LR, or on post-test probability at the spoke’s pre-test. Yes, a strong recommendation to transfer on a positive flag can coexist with a conditional recommendation to withhold on a negative flag: LR\(^+\) and LR\(^-\) face different thresholds (Chapter 14), and the same Se/Sp posterior can clear one and not the other.

**C.25.4.** Chapter 14’s \(p^{\star} = H/(B+H) = 1/(1+B/H)\) is a *probability* threshold. The teaching increment 0.04 (−0.03 to 0.11) is a UW-mRS contrast. Do not drop \(p^{\star}\) into that interval. On the utility scale, treat when the posterior on (increment − scaled harm) is mostly positive. With increment 0.04 (−0.03 to 0.11) and harm 0.02 (0.01 to 0.04) the net interval includes 0 for any \(B/H\) that does not dwarf the lower tail. In that range the panel owes the fellow a values question and a split recommendation, not a single Class I/III sentence.

## Chapter 26 — Ethics and Adaptive Governance

**C.26.1.** Five contents, short: (1) this is research, not decided care; (2) both treatments are in use and the community of experts is not sure which is better *for people like you*; (3) a computer will tilt future assignments toward whichever arm is looking better, so later patients may not get a 50/50 draw; (4) you can decline and still receive ordinary care; (5) we will stop a bad-looking arm if a pre-set rule says so. Mark: a GCS-13 patient may still miss that “looking better” is a group pattern, not a promise about *their* outcome.

**C.26.2.** The overnight trial updates \(\pi_{\text{comm}}\), not the platform posterior (that already moved \(0.45 \to 0.84\) from the 86 patients). The DSMB recomputes \(\pi_{\text{comm}}\) first: the external interval is a new likelihood on a slightly different population, and community equipoise is the consent object. If the platform continues, tomorrow’s consent should say the community is now more skeptical of evacuation than at launch, name the current 70/30 tilt, and not say the other trial “proved” harm in *this* population.

**C.26.3.** Efficacy \(T\): \(P(\delta > 0.03 \mid y) > 0.99\) and \(n \ge 80\) \(\to\) graduate evacuation. Harm \(T\): \(P(\delta_{\text{dead}} > 0.02 \mid y) > 0.90\) and \(n \ge 60\) \(\to\) drop evacuation. Equity \(T\): expected assignments to the currently inferior arm among age \(\ge 80\) exceed 1.3 times the marginal rate and \(n_{\ge 80} \ge 40\) \(\to\) pause adaptation in that slice and report. If you cannot name the action, you do not yet have a charter item.

**C.26.4.** To the advisor: yes, 32 fewer people on the worse arm when surgery is truly better is a real gain, and the type I move from 0.03 to 0.04 is the price; say whether *that* price is acceptable, not whether RAR is “more ethical” in the abstract. To the IRB: look also at duration (47 vs 48 months — almost no time saved), at the harm row (96 still assigned to worse surgery; futility is not magic), and at the design-prior row (assurance 0.55, 130 on the currently worse arm) — that is the world you are sending patients into. Approve the tilt only if those cells, not the brochure, are the ones you can defend.

## How to use these solutions

If your second decimal disagrees, check odds versus probabilities and whether an LR was treated as independent of a base rate that already contained the same sign. If your *action* disagrees, write the utility you used. These solutions are not institutional policy.

!!! success "Key Takeaway"
    Solutions for the first four exercises of each chapter, one standard: a number, a contrast, an action. Teaching numbers stay teaching numbers. Where the chapter asked for a sentence, the solution is a sentence. Where it asked for algebra, the algebra is here. Real Friday afternoons run the same loop with a messier \(u\).

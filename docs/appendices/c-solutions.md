# Appendix C — Solutions to Exercises

Solutions to the first four exercises of each chapter. Teaching numbers are the curriculum’s invented values, not estimates from named trials. Algebra is shown; where a `brms` fit was specified but not run, the solution is the number you can obtain by conjugate arithmetic or by the identity the chapter asked for.

---

## Chapter 1 — Why Bayesian Thinking Matters

**C.1.1.** Pre-test 2%, test 95% sensitive and 95% specific, positive result. Natural frequencies in 1,000 people: 20 diseased, of whom 19 test positive; 980 well, of whom 49 test positive. Posterior \(= 19/(19+49) \approx 0.28\), not 0.95. System 1 treated sensitivity as a posterior (base-rate neglect).

**C.1.2.** Audit 14/40. Prior Beta(1, 1) \(\to\) posterior Beta(15, 27), mean \(15/42 = 0.357\). Normal approximation SD \(\approx 0.073\), so \(P(\pi > 0.25 \mid y) \approx 0.93\). Prior Beta(60, 140) \(\to\) Beta(74, 166), mean \(74/240 = 0.308\), SD \(\approx 0.030\), \(P(\pi > 0.25 \mid y) \approx 0.97\). The flat prior is not “more objective”; it is a claim that 1% and 99% were equally plausible before the audit. Objectivity is whether the prior’s implied sample size is defensible, not whether the hyperparameters look empty.

**C.1.3.** Frequentist: “If we repeated NINDS-like trials forever and the true risk difference were zero, 95% of such intervals would cover zero; this interval is one draw from that procedure.” Bayesian: “Given the prior we wrote and these data, 95% of the posterior mass on the risk difference sits between these two numbers.” Only the second sentence is about *this* woman’s probable benefit. That is the sentence you can say to a family, once you have translated it into frequencies.

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

**C.2.4.** Aleatory: whether *this* hematoma expands in the next six hours, given everything you already know; a second CT after expansion has happened does not un-expand it. Epistemic: the current volume and the spot-sign status, which a second look (or a better read) can change. The fellow who wants another CTA is trying to buy epistemic reduction. After a good first CTA, further scans mostly wait out aleatory noise.

---

## Chapter 3 — Bayes’ Theorem

**C.3.1.** Prior 0.02, LR\(^{+}\) \(= 8\). Odds \(= 0.0204 \times 8 = 0.163\), posterior \(\approx 0.14\). That is above a typical LP-for-SAH test threshold and usually below a “skip LP, go straight to CTA/angiography” treat threshold. Next test is LP if CT is the only positive, or CTA if you are chasing aneurysm given a higher clinical concern. Name which threshold you mean: testing versus treating.

**C.3.2.** The exam, the DWI, and the story are not conditionally independent given stroke-versus-mimic. They are three views of one cortical pattern. Multiplying LR \(= 3\) three times pretends you saw three independent assays and produces LR \(= 27\), a fiction. Use the single best LR, or a model that includes their covariance. Agreement is comforting; it is not a factor of 27.

**C.3.3.** Mild stroke, NIHSS 3. Benefit of treating true disabling ischemia is smaller than in NIHSS 14; harm of ICH is not. \(p^{*}\) therefore sits higher — teaching range 0.35–0.50 rather than 0.15. Testing threshold (perfusion) sits below that. Apixaban three hours ago raises \(H\) sharply (ICH risk), which raises both marks and can erase the testing interval: you may wait without perfusion because the treat threshold has climbed above any posterior a perfusion scan can deliver.

**C.3.4.** Hour 18, Sn 0.85, Sp 0.99, prior 0.10. LR\(^{-}\) \(= 0.15/0.99 = 0.152\). Odds \(= 0.111 \times 0.152 = 0.0168\), posterior \(\approx 0.017\). Hour-three teaching LR\(^{-}\) is much smaller (CT is more sensitive early), posterior often \(< 0.005\). Sentence: “A normal scan at three hours would have left the chance of a bleed well under one in a hundred. At eighteen hours the same pictures leave it closer to two in a hundred, which is why a lumbar puncture still earns its keep.”

---

## Chapter 4 — Priors

**C.4.1.** \(\theta \sim \mathcal{N}(0, 0.4^{2})\) on log-OR. Approximate 95% interval on OR: \(\exp(\pm 1.96 \times 0.4) \approx (0.46, 2.19)\). For BAO EVT this is weakly informative leaning skeptical: it centers on no effect and still allows a doubling or a halving. It is not enthusiastic (that would sit above 1 with a tighter upper tail) and not a spike at 0.

**C.4.2.** A worked self-elicitation (teaching): bounds on ARR for independence, BAO EVT, \((-0.05, 0.25)\); quartiles 0.04 and 0.14; median 0.08. A Normal(0.08, \(0.07^{2}\)) matches roughly; a Beta on the two arm-risks would be more honest. What you discover: the interval is wider than the last paper’s confidence interval, which is the point of elicitation — you do not yet have that paper’s \(n\) in *this* population.

**C.4.3.** Six sentences. Anterior-circulation EVT is a different vessel, a different time-density of data, and a different untreated prognosis. Setting the power-prior weight \(a_0 = 1\) declares those trials fully transportable to BAO, which is a scientific claim, not a default. If you believe transport is partial, \(a_0\) is the parameter of that belief and must sit well below 1. A hierarchical \(\tau\) between circulations does the same job with a distribution instead of a scalar. Either is criticizable. \(a_0 = 1\) is not modest; it is maximal borrowing wearing a humble symbol. Write the implied prior interval on the BAO ARR and see whether the committee still wants \(a_0 = 1\).

**C.4.4.** Untreated independence \(\approx 0.20\) with prior \(n = 50\) is Beta(10, 40) on the probability scale. On the `brms` intercept (logit) that is a Normal at \(\text{logit}(0.20) \approx -1.39\) with SD chosen so that the implied prior \(n\) is about 50, roughly `prior(normal(-1.39, 0.30), class = Intercept)`. Check with a prior-predictive draw on \(\pi\), not by staring at the logit SD.

---

## Chapter 5 — Likelihoods and Conjugate Models

**C.5.1.** Data: 2 sICH in 48. Skeptical Beta(2, 18) \(\to\) Beta(4, 64), mean 0.059. \(P(\theta > 0.06 \mid y) \approx 0.47\) (near a coin). Enthusiastic Beta(2, 98) \(\to\) Beta(4, 144), mean 0.027, \(P(\theta > 0.06 \mid y) \approx 0.01\). The probability moves by about 0.45. In front of a plaintiff expert you defend the prior whose implied sample size and location you can source — the chapter’s historical Beta(8, 142), or the skeptical Beta(2, 18) — not the enthusiastic Beta that buries 2/48 under 100 imaginary safe cases.

**C.5.2.** Posterior Beta(10, 188). \(P(Y^{\star}=0 \mid n^{\star}) = B(10, 188+n^{\star})/B(10, 188) = \prod_{k=0}^{n^{\star}-1}(188+k)/(198+k)\). This product falls through 0.20 near \(n^{\star} = 34\) (teaching: 0.204 at 33, 0.195 at 34). That \(n^{\star}\) is the next-quarter volume at which “we had a clean quarter” stops being surprising under the current posterior. Below that volume, a zero-event quarter is still the mode.

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

**C.7.2.** A wide kernel averages two well-separated lumps into a camel that looks like a hill. \(\widehat{R}\) compares between-chain to within-chain variance; here between-chain variance is \((1.0)^{2}/4\) of the gap and within-chain variance is tiny, so \(\widehat{R}\) is large. Unimodality of a smeared plot is not mixing.

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

**C.9.2.** Abstract the HDI on the OR if you are describing the most credible values; it is the shortest 95% set. The ETI goes further into the right tail and starts higher because of skew. On the log-odds scale the posterior is closer to symmetric, so HDI and ETI nearly agree — which is a reason to compute on log-odds and *report* OR endpoints of the HDI.

**C.9.3.** A ROPE of \((-0.02, 0.02)\) on a 90-day mRS 0–2 risk difference says a 2-point absolute swing is noise. In mild stroke that may be too tight if the outcome is already common and the harm (ICH) is 2–4 points; it may be too wide if you would treat for a 1-point gain in a low-harm drug. Widen the ROPE if ICH is cheap on your utility; narrow it if even a 1-point gain is worth a large \(N\).

**C.9.4.** A Normal(\(0, 20^{2}\)) prior under \(M_1\) puts almost all mass on cartoon odds ratios. The Bayes factor then “supports \(M_1\)” mostly because \(M_1\) is a huge, silly alternative that the data have nowhere else to go. Demand a prior whose 95% interval lives on clinically possible log-ORs — teaching, \(\mathcal{N}(0, 0.5^{2})\) — and pre-specify it.

---

## Chapter 10 — Sample Size and Adaptive Designs

**C.10.1.** “0.93 is the probability the effect is positive *given what we have*. 0.18 is the probability that, if we continue to the maximum \(N\), the *finished* analysis will meet the success rule. Those are different questions. Continuing spends the remaining patients on an 18-percent chance of a label claim. Under the charter, PPoS below 0.25 is stop-for-futility. I vote stop. ‘Almost there’ describes the current sign, not the remaining information.”

**C.10.2.** Beta(3, 3) is a wide design prior; assurance at a max of 80 falls because much of the prior mass sits near 0.5, where the rule rarely fires. Beta(20, 11) is a tight enthusiastic prior; assurance rises, sometimes a lot. For an encephalitis grant defend the wide one, or a mixture with a skeptical spike: you do not yet know this antibody. The tight Beta is a hope, not a design prior.

**C.10.3.** True \(p = 0.45\) is on the boundary of the success event \(P(p>0.45 \mid y) > 0.90\). The stop-for-efficacy rate is then a type-I analogue and should be small (a few percent) if the rule is calibrated; simulate it, do not guess. Looking every 5 instead of every 10 spends more looks and inflates that rate unless you tighten the threshold. More looks, more false gos.

**C.10.4.** Expect an interaction if intensive BP and a particular reversal agent share a coagulopathy pathway (hematoma expansion). Randomize within cells of the other domain, or model the interaction and keep allocation factorial. Report each domain’s marginal posterior *and* the interaction; a pooled “BP works” headline that averages over reversal strategies is the wrong estimand if the interaction is the biology.

---

## Chapter 11 — Diagnostic Accuracy

**C.11.1.** Spoke-negative: Se \(\sim\) Beta(47, 7), Sp \(\sim\) Beta(23, 7). Draws of LR\(^{-}\) \(= (1-\mathrm{Se})/\mathrm{Sp}\) sit near 0.17 (mean). Teaching pre-test 0.55 \(\to\) posterior LVO probability near 0.17 (a Monte Carlo band of about 0.10–0.28). You still launch after a negative spoke read only if the pre-test is high enough that even LR\(^{-}\) leaves you above the transfer threshold. With a 0.40 launch bar, that pre-test is about 0.80. This NIHSS-12 / AF patient is not there. Do not launch on the negative spoke read alone; the telestroke over-read is the live likelihood.

**C.11.2.** Teaching: of 40 never-transferred spoke-negatives with NIHSS 4–7, perhaps 2–6 had LVO (5–15%). Adding them as unverified negatives increases the apparent TN count and *raises* estimated Sp. DSA-only Sp is therefore biased *down* (the verified non-LVO are the ones odd enough to transfer). Sensitivity is also distorted: missed LVOs never enter \(n_D\). Direction: DSA-only Sp too pessimistic; network Sp after honest imputation higher.

**C.11.3.** AUC of ASPECTS for mRS 0–2 after EVT is a *prognostic* discrimination of outcome given that you already treated. AUC of ASPECTS for LVO is a *diagnostic* discrimination of the state that decides transfer. The transfer decision needs the second (and, honestly, NIHSS plus CTA, not ASPECTS alone). The first belongs in a counseling model after the vessel is known.

**C.11.4.** Raw pooled Se averages readers. The fifth spoke’s 0.72 will shrink toward the network, but not to 0.85, if \(\tau_s\) is real. Quoting the pool as *that spoke’s* Se is a lie to their next patient. Defend a half-normal on \(\tau_s\) with scale 0.4–0.6 on the logit (Worksheet 3, Appendix B): a spoke at 0.72 among four at 0.9 is unusual, not impossible.

---

## Chapter 12 — Survival and Competing Risks

**C.12.1.** Time to the composite “dead or mRS \(\geq 4\),” or a Fine–Gray model for the subdistribution of “mRS \(\leq 2\)” with death as competing. Estimand: cumulative incidence of good function at day 90, with death occupying its own incidence. Death is an event in the first version and a competitor in the second; it is not a censor.

**C.12.2.** (a) Cox for death: D is censored at day 40; contribution \(S_{\text{death}}(40 \mid x_D)\). (b) Cox for time to mRS \(\leq 2\) treating death as competitor: D has not had the event and has not died by 40, so if you *incorrectly* censor at 40 you write \(S_{\text{good}}(40)\); the honest competing-risks contribution is the survival in the good-event *cause-specific* hazard, still at risk. (c) Ordinal day-90 mRS with D missing: D contributes the marginal likelihood of the missing ordinal, or is dropped — which is a different, worse estimand.

**C.12.3.** No recovery before day 30, no death after day 30. Day-90 good-outcome CIF \(= (1-0.28)\times 0.31 = 0.223\). A death-censored \(1-\mathrm{KM}\) is tempted to report 0.31 — the probability among *survivors* — as if the dead had been merely unobserved. That is the number families do not ask for.

**C.12.4.** \(\mathcal{N}(0, 3^{2})\) on the log-odds treatment effect says odds ratios out to \(e^{\pm 6} \approx 400\) are ordinary. That encodes “ICH blood-pressure trials could be miracle or catastrophe.” Accept it only as a sensitivity prior, never as the primary, and only to show the posterior does not depend on the tight \(\mathcal{N}(0, 0.5^{2})\).

---

## Chapter 13 — Bayesian Meta-Analysis

**C.13.1.** Six sentences. \(\mu\) is the average true effect across the studies you already have. \(\theta_{\text{new}}\) is the effect *you* will get, including the extra scatter \(\tau\). Late-window EVT without perfusion is a new imaging gate, so you are \(\theta_{\text{new}}\) under a different \(x\), not a draw of \(\mu\). The prediction interval is the honest one, and it is wider. If that interval still sits above your treat threshold, offer EVT; if it includes harm, do not launch a service on \(\mu\) alone. Buy perfusion or join a registry before you treat \(\mu\) as a promise.

**C.13.2.** SEs \(\times 1/10\) make each study look huge. The likelihood for \(\tau\) becomes a spike near the observed between-study SD. The half-Cauchy versus half-normal debate then *stops* mattering for \(\tau\) and for \(\theta_{\text{new}}\); both priors are overwhelmed. With the original SEs and three studies, the prior on \(\tau\) is most of the result.

**C.13.3.** First table, add 0.5: \((0.5/90.5) / (3.5/92.5) \to\) log-OR \(= \log(0.5\times 92.5 / 3.5\times 90.5) \approx \log(0.146) \approx -1.92\). Prefer two independent binomials (or a logistic GLM) with a weakly informative prior on the log-OR; zeros stay zeros. Do not put the continuity-corrected \(-1.92\) in a forest plot as if it were data.

**C.13.4.** Put an indicator for “perfusion-gated late window” on \(\mu_i\). Prior on that \(\beta\): \(\mathcal{N}(0, 0.4^{2})\) on the log-OR — wide enough to let C differ, too tight to let three studies invent a 4-fold modifier. C can then sit off the A–B pool without being a separate meta-analysis of one.

---

## Chapter 14 — Decision Theory and Thresholds

**C.14.1.** \(p^{*} = 0.90 = H/(B+H)\) \(\Rightarrow\) \(B/H = (1-0.90)/0.90 = 1/9 \approx 0.11\). You will accept about one benefit per nine harms. That is a banner threshold (treat only if nearly sure), not a sister threshold (accept 1 harm to gain 10 benefits, \(B/H = 10\), \(p^{*} \approx 0.09\)).

**C.14.2.** Teaching \(B=0.40\), \(H=0.30\), \(Se=0.80\), \(Sp=0.70\).

| \(R\) | \(T_t\) | \(T_{tt}\) |
|---|---|---|
| 0 | \(0.09/0.41 = 0.220\) | \(0.21/0.29 = 0.724\) |
| 0.08 | \(0.17/0.41 = 0.415\) | \(0.13/0.29 = 0.448\) |

The interval vanishes when \(T_t \geq T_{tt}\), which solves to \(R \approx 0.086\) (set the two closed forms equal; see C.14’s hint exercise). A test whose disutility is a quarter of \(B\) is not worth buying.

**C.14.3.** Three states, three actions (treat, test, wait) produce a tree with six terminal utilities, not two. Thresholds become *surfaces* in the two-simplex of state probabilities. A single \(p^{*}\) exists only when the state is binary. Mild aphasia is exactly this: mimic versus nondisabling ischemia versus disabling ischemia.

**C.14.4.** They will not match. “Hemorrhages per language life saved” elicits \(H/B\) in count units; “chance of recovery you would forgo to avoid a bleed” elicits a probability trade that maps to the same ratio only if the respondent is an expected-utility agent who heard both frames as the same gamble. Framing, numeracy, and the word *hemorrhage* move the number. Record both and notice the preference is unstable — Chapter 14’s cue to stop over-quantifying.

---

## Chapter 15 — Decision Curves and VOI

**C.15.1.** Treat-none net benefit is 0. \(\kappa\) beats it when \(Se\,\pi - (1-Sp)(1-\pi)\,p_t/(1-p_t) > 0\). Plug in \(\pi=0.06\), \(Sp=0.75\), \(p_t=0.20\): \(Se\times 0.06 > 0.25\times 0.94\times 0.25 = 0.05875\), so \(Se > 0.979\). At this low prevalence and this threshold, \(\kappa\) needs near-perfect sensitivity to beat doing nothing.

**C.15.2.** Drop \(\pi\) from 0.06 to 0.02. Treat-all’s net benefit becomes negative over a wider range of \(p_t\) (it already crosses zero at \(p_t=\pi\); see C.15.4). \(\kappa\)’s curve drops because true positives are rarer and false positives are not. Treat-all dies first; then \(\kappa\) dies relative to treat-none except at very low \(p_t\).

**C.15.3.** “The fellow’s action flips only if the marker moves a posterior across a threshold; re-estimating AUC on 200 patients can leave calibration and that threshold untouched, so the expected value of that sample for *this* decision is near zero.”

**C.15.4.** Treat-all NB \(= \pi - (1-\pi)\,p_t/(1-p_t)\). Zero when \(\pi(1-p_t) = (1-\pi)p_t\), i.e. \(p_t = \pi\). In harm/benefit language: treat-all is worthwhile only when prevalence exceeds the treat threshold. If disease is rarer than the harm/benefit bar, treating everyone loses.

---

## Chapter 16 — Bedside Shared Decisions

**C.16.1.** Two spoken arrays of 100. Without EVT: “40 do not survive; 16 need full care; 22 are bedbound but aware; 18 are back to a cane-and-help life; 4 walk independently.” With EVT: “33, 12, 20, 24, 11.” Collapse 0–2 with 3 if the daughter is defending “a life she would recognize” (prestroke 3), and collapse 5 with 6 if “vegetable or dead” is her named harm. Keep 4 visible; it is the state people regret by surprise.

**C.16.2.** “DAWN-positive, we take her” treats a trial-eligibility flag as a command. That is the effective-care error: strong evidence of *average* benefit in a selected population is being used as if the threshold cannot move with prestroke mRS 3, age 89, and the daughter’s utilities. Late-window EVT here is preference-sensitive care. The scan is beautiful. The decision is still hers.

**C.16.3.** Alive and not mRS 5: without EVT, \(1-0.16-0.40 = 0.44\); with EVT, \(1-0.12-0.33 = 0.55\). Teaching draws would put a band around a 0.11 absolute gain. To the daughter: “About 11 more people in 100 are alive and not needing full care with the procedure than without it.” No “posterior.”

**C.16.4.** Best-case: the 90th percentile of the *with-EVT* predictive distribution, states 0–3 heavier. Worst-case: the 10th percentile, states 5–6 heavier. Do not quote the best with-EVT against the worst without-EVT; that is two different worlds. Pair quantiles *within* an action, then show the contrast of medians.

---

## Chapter 17 — Communicating Uncertainty

**C.17.1.** Under 40 words: “With a skeptical Beta(8, 12) prior, 31 of 62 patients were independent; the posterior mean was 0.48 and the pre-specified success rule was not met.” You had to add the prior, the rule, and the miss. You had to delete “uninformative” and “demonstrated benefit.”

**C.17.2.** Beta(39, 43). Mean 0.476. \(P(\theta > 0.50) = 1 - F_{\text{Beta}}(0.50; 39, 43) \approx 0.33\). \(P(\theta > 0.35) \approx 0.99\). Quoting only 0.99 is spin: it is the probability of beating a bar the trial did not care about. Quoting only 0.33 is also spin if you bury the 0.93 against the real bar of 0.40. Report the pre-specified functional.

**C.17.3.** “Thank you — we agree the prior should be labeled precisely. Beta(8, 12) has mean 0.40 and prior sample size 20; it was chosen to encode a skeptical historical independence rate, not to stay out of the way. ‘Weakly informative’ would describe a prior that rules out cartoons while remaining dominated by 62 observations at any plausible mean. This prior can still move the success probability from 0.96 (flat) to 0.93 (ours) to 0.88 (more skeptical). We will call it skeptical and show the sensitivity, and we will not call it weakly informative.”

**C.17.4.** Sequential Beta starting at (8, 12), adding one Bernoulli at a time toward 31/62. The mean walks from 0.40 toward 0.48; the 95% band narrows. A naive reader who ignores the pre-specified \(P(\theta>0.40)>0.95\) rule will declare victory the first time the *mean* crosses 0.45 or the first time the interval excludes 0.40 — on these teaching numbers, well before \(n=62\), and well before the actual functional hits 0.95 (it never does). Mark that \(n\) on the fan and write “not the rule.”

---

## Chapter 18 — Integrated Case Studies

**C.18.1.** Base rate 0.18, examination LR 2.5: prior odds \(= 0.220 \times 2.5 = 0.549\), prior \(= 0.35\). CTA\(+\): posterior \(0.83\). CTA\(-\): posterior \(0.047\). Suite-free treat threshold \(p^{*} \approx 0.17\): 0.35 still exceeds it, so treat-without-CTA remains defensible *if* the suite is free. It is less attractive than at 0.57. A negative CTA now drops you far below threshold, so CTA is mandatory whenever the suite has opportunity cost, and still wise when it does not. New treat-without-test rule: only if delay is costly *and* CTA is unavailable.

**C.18.2.** Point RR \(= e^{-0.35} \approx 0.70\). Expansion under intensive \(\approx 0.56 \times 0.70 = 0.39\). ARR \(\approx 0.17\). With the chapter’s 0.25 conversion to good mRS, functional ARR \(\approx 0.043\) against 0.03 renal harm. The ledger can flip: a 140 target becomes reasonable in the spot-positive stratum *if* you believe the modifier. Say the modifier was elicited, not estimated from this patient.

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
need <- c("y_ind", "nihss", "age_c", "aspecs", "hospital")
stopifnot(all(need %in% names(d)))
stopifnot(is.numeric(d$nihss), all(d$nihss >= 0, d$nihss <= 42, na.rm = TRUE))
```

A rename then dies before Stan compiles a model on the wrong columns.

---

## How to use these solutions

If your second decimal disagrees, check odds versus probabilities and whether an LR was treated as independent of a base rate that already contained the same sign. If your *action* disagrees, write the utility you used. These solutions are not institutional policy.

!!! success "Key Takeaway"
    Eighty solutions, one standard: a number, a contrast, an action. Teaching numbers stay teaching numbers. Where the chapter asked for a sentence, the solution is a sentence. Where it asked for algebra, the algebra is here. Real Friday afternoons run the same loop with a messier \(u\).

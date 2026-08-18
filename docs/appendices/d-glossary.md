# Appendix D — Glossary, Mathematical Notes, Further Reading, Reporting Checklists

## Opening

A shared vocabulary prevents the most expensive errors in this book: calling a p-value a posterior, calling a prior “uninformative,” and calling a hazard ratio a decision.

## Glossary

| Term | Meaning in this book |
| --- | --- |
| Absolute risk | Probability of an event in a defined group. Prefer this in conversations. |
| Adaptive design | A trial that uses accumulating data to change allocation, sample size, or arms by pre-specified rules. |
| Aleatory uncertainty | Irreducible randomness in an outcome given the parameters. |
| Assurance | Expected power, averaging over a prior on the effect. |
| Base rate | Prior incidence or prevalence in the relevant population. |
| Bayes factor | Ratio of marginal likelihoods of two models or hypotheses. |
| Bayes’ theorem | \(p(\theta\mid y)\propto p(y\mid\theta)\,p(\theta)\). |
| Beta–Binomial | Conjugate model for a proportion. |
| Calibration | Agreement between predicted probabilities and observed frequencies. |
| Competing risk | An event that precludes the event of interest (death vs. hematoma evacuation). |
| Conjugate prior | A prior that keeps the posterior in the same family. |
| Credible interval (CrI) | A posterior interval for a parameter. |
| Decision curve | Plot of net benefit versus threshold probability. |
| Diagnostic threshold | Probability above which you test. Distinct from the treatment threshold. |
| Divergence | HMC warning that the geometry was not explored faithfully. |
| Effective sample size (ESS) | MCMC analogue of independent draws. |
| Epistemic uncertainty | Uncertainty about parameters, reducible with data. |
| Exchangeability | A priori symmetry that justifies partial pooling. |
| Expected utility | Probability-weighted value of outcomes. |
| EVPI / EVSI | Expected value of perfect / sample information. |
| Fagan nomogram | Graphical odds-form Bayes for a single LR. |
| Frequentist CI | Interval from a procedure with long-run coverage. Not a posterior. |
| HDI | Highest-density (credible) interval. |
| Hierarchical model | Parameters themselves have a prior with unknowns (partial pooling). |
| Historical borrowing | Using past data as a prior or hierarchical neighbor. |
| Likelihood | \(p(y\mid\theta)\). How the data would look if \(\theta\) were true. |
| Likelihood ratio | How many times more likely the data are under one hypothesis than another. |
| LOO | Leave-one-out cross-validation of predictive density. |
| Loss function | The negative of a utility; what you pay for a wrong act. |
| MCMC | Simulation methods that sample a posterior. |
| MCID | Minimum clinically important difference. Often the ROPE half-width. |
| Net benefit | Decision-analytic score: true positives minus weighted false positives. |
| Odds | \(p/(1-p)\). |
| Partial pooling | Shrinkage of group estimates toward a common mean. |
| Platform trial | A standing protocol that can add or drop arms. |
| Posterior | \(p(\theta\mid y)\). Belief after the data. |
| Posterior predictive | Distribution of new data given the observed data. |
| Power | Frequentist probability of rejecting a false null at a fixed effect. |
| PPC | Posterior predictive check. |
| Predictive probability of success | Chance, given current data, that a trial will meet its success rule. |
| Pre-test probability | The prior, in diagnostic language. |
| Prior | \(p(\theta)\). Belief before these data. |
| Prior-data conflict | Likelihood and prior concentrated in different regions. |
| \(\hat{R}\) | Gelman–Rubin diagnostic comparing within- and between-chain variance. |
| Random effects | Hierarchical variation (e.g. between studies, \(\tau\)). |
| Restricted mean survival | Area under the survival curve to a time horizon. |
| ROPE | Region of practical equivalence. |
| Sequential analysis | Updating a stopping decision as data accrue. |
| Shared decision-making | Using a posterior *and* a patient’s utilities to choose. |
| Shrinkage | Movement of noisy estimates toward the hierarchical mean. |
| Skeptical prior | Prior concentrated near no effect. |
| System 1 / System 2 | Fast pattern match vs. slow formal update. |
| \(\tau\) | Between-group standard deviation in a hierarchical model. |
| Treatment threshold | Probability of disease (or benefit) above which you treat without further testing. |
| Utility | Value of an outcome to the decision maker. |
| Weakly informative prior | Regularizing prior that rules out absurd values without claiming the answer. |
| WAIC | Widely applicable information criterion. |

## Mathematical notes

### Beta

If \(\theta\sim\mathrm{Beta}(\alpha,\beta)\) and you observe \(s\) successes and \(f\) failures,
\[
\theta\mid y \sim \mathrm{Beta}(\alpha+s,\ \beta+f).
\]
Mean \(\alpha/(\alpha+\beta)\). This is the workhorse of Chapters 5 and 11.

### Logit

\[
\mathrm{logit}(p)=\log\frac{p}{1-p},\qquad \mathrm{expit}(x)=\frac{1}{1+e^{-x}}.
\]
Logistic regression in `brms` is linear on the logit scale.

### Odds form of Bayes

\[
\frac{p}{1-p}\Big|_{\text{post}} = \mathrm{LR}\times \frac{p}{1-p}\Big|_{\text{prior}}.
\]

### Pauker–Kassirer treatment threshold

\[
p^* = \frac{H}{H+B}
\]
where \(H\) is the harm of treating the well and \(B\) is the benefit of treating the diseased, on one scale.

### HDI versus equal-tail interval

An equal-tail 95% CrI is the 2.5% and 97.5% quantiles. An HDI is the shortest interval containing 95% of the posterior mass. They coincide for symmetric unimodal posteriors.

## Further reading

- Gelman A, et al. *Bayesian Data Analysis*. 3rd ed.
- McElreath R. *Statistical Rethinking*. 2nd ed.
- Kruschke JK. *Doing Bayesian Data Analysis*. 2nd ed.
- Sox HC, Higgins MC, Owens DK. *Medical Decision Making*. 2nd ed.
- Pauker SG, Kassirer JP. The threshold approach to clinical decision making. *N Engl J Med*. 1980.
- Vickers AJ, Elkin EB. Decision curve analysis. *Med Decis Making*. 2006.
- Bürkner P-C. brms. *J Stat Softw*. 2017.
- Vehtari A, Gelman A, Gabry J. LOO and WAIC. *Stat Comput*. 2017.
- FDA. Guidance for the Use of Bayesian Statistics in Medical Device Clinical Trials. 2010.
- Companion volumes: [CRIT-APP](https://rkalani1.github.io/CRIT-APP/), [ML for Neurologists](https://rkalani1.github.io/ML/).

## Mini reporting checklists

### When you write a Bayesian analysis

| Item | Done? |
| --- | --- |
| Estimand stated in clinical language | |
| Prior specified, justified, and shown | |
| Sensitivity to a skeptical / enthusiastic prior | |
| MCMC diagnostics (\(\hat{R}\), ESS, divergences) | |
| PPC or other check | |
| Posterior summaries: mean/median, CrI, \(P(\theta>\text{MCID})\) | |
| Software, seed, and versions | |
| Decision rule if any (threshold, ROPE) | |

### Pair with design-specific instruments

| Question | Instrument |
| --- | --- |
| Was the trial fair? | CONSORT |
| Was the observational study designed? | STROBE |
| Was the test evaluated honestly? | STARD |
| Was the prediction model transported? | TRIPOD / TRIPOD-AI |
| Was the review complete? | PRISMA |
| Should I believe the claim enough to update? | [CRIT-APP](https://rkalani1.github.io/CRIT-APP/) |

!!! success "Key Takeaway"
    If you can define the prior, the likelihood, the posterior, and the threshold in one sentence each, you are speaking the language of this book. Everything else is technique.

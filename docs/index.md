# Bayesian Clinical Reasoning

<div class="ebook-hero ebook-hero--split" markdown>

<div class="hero-copy" markdown>

<p class="eyebrow">Open teaching ebook · Neurology and clinician-scientists</p>

# Statistics, Decision Analysis, and Evidence

A continuous argument: clinical reasoning is Bayesian updating. Priors are not a confession of bias. They are the pre-test probability you already use — made explicit, checked, and carried through to a threshold and a conversation.

<p class="meta">Rizwan Kalani · CC BY 4.0 · <a href="https://github.com/rkalani1/bayesian-clinical-reasoning">Source</a></p>

</div>

</div>

<p class="ebook-start">
<a href="how-to-use.html">How to read this book</a>
<a class="secondary" href="curriculum/01-why-bayesian-thinking-matters.html">Start Chapter 1</a>
<a class="secondary" href="evidence-register.html">Evidence register</a>
</p>

!!! warning "Educational only — not medical advice"
    This book is for teaching and professional self-study. It is **not medical advice**, **not institutional policy**, and **not a substitute** for primary literature, guidelines, or local standards of care. Vignettes use invented patients and labeled **teaching numbers**. Verify every method and every clinical decision against current sources.

## Who this is for

<div class="route-grid">
<a href="curriculum/01-why-bayesian-thinking-matters.html">
<span class="route-kicker">Beginner</span>
<strong>Students and residents</strong>
<span>Probability language, odds, likelihood ratios, and why the base rate is not optional.</span>
</a>
<a href="curriculum/03-bayes-theorem.html">
<span class="route-kicker">Clinician</span>
<strong>Practicing neurologists</strong>
<span>Diagnostic and treatment thresholds, sequential tests, and how to talk about a posterior.</span>
</a>
<a href="curriculum/06-hierarchical-models.html">
<span class="route-kicker">Researcher</span>
<strong>Trialists and epidemiologists</strong>
<span>Hierarchical models, adaptive designs, meta-analysis, and reporting.</span>
</a>
<a href="curriculum/14-decision-theory-thresholds.html">
<span class="route-kicker">Decision</span>
<strong>Anyone who has to act</strong>
<span>Utilities, net benefit, value of information, and shared decisions under uncertainty.</span>
</a>
</div>

## Companion books

This volume sits between critical appraisal and machine-learning literacy:

- [Critical Appraisal for Neurologists](https://rkalani1.github.io/CRIT-APP/) — can you trust the claim?
- **This book** — how should the claim update what you believe, and what should you do?
- [Machine Learning & AI for Neurologists](https://rkalani1.github.io/ML/) — when the likelihood is a model, not a 2×2 table.

## Contents

<ul class="chapter-list">
<li class="part">Part I — Foundations of Bayesian clinical thinking</li>
<li><a href="curriculum/01-why-bayesian-thinking-matters.html"><span class="num">01</span><span>Why Bayesian thinking matters for clinicians and researchers</span></a></li>
<li><a href="curriculum/02-probability-odds-uncertainty.html"><span class="num">02</span><span>Probability, odds, uncertainty, and the language of clinical reasoning</span></a></li>
<li><a href="curriculum/03-bayes-theorem.html"><span class="num">03</span><span>Bayes’ theorem as the formal engine of diagnostic and therapeutic updating</span></a></li>
<li><a href="curriculum/04-priors.html"><span class="num">04</span><span>Priors: eliciting clinical knowledge, literature, and hierarchical structure</span></a></li>
<li class="part">Part II — Core Bayesian inference with R</li>
<li><a href="curriculum/05-likelihoods-conjugate-models.html"><span class="num">05</span><span>Likelihoods, conjugate models, and closed-form updates</span></a></li>
<li><a href="curriculum/06-hierarchical-models.html"><span class="num">06</span><span>Hierarchical models for patients, centers, and trials</span></a></li>
<li><a href="curriculum/07-computational-inference.html"><span class="num">07</span><span>Computational inference: MCMC, diagnostics, and visualization</span></a></li>
<li><a href="curriculum/08-model-checking.html"><span class="num">08</span><span>Model checking, calibration, and sensitivity to priors</span></a></li>
<li><a href="curriculum/09-estimation-rope-bayes-factors.html"><span class="num">09</span><span>Estimation, credible intervals, ROPE, and Bayes factors</span></a></li>
<li class="part">Part III — Design, evidence synthesis, and advanced methods</li>
<li><a href="curriculum/10-sample-size-adaptive-designs.html"><span class="num">10</span><span>Bayesian sample size, sequential analysis, and adaptive designs</span></a></li>
<li><a href="curriculum/11-diagnostic-accuracy.html"><span class="num">11</span><span>Diagnostic accuracy, ROC, and continuous markers</span></a></li>
<li><a href="curriculum/12-survival-competing-risks.html"><span class="num">12</span><span>Survival, competing risks, and time-to-event models</span></a></li>
<li><a href="curriculum/13-bayesian-meta-analysis.html"><span class="num">13</span><span>Bayesian meta-analysis and evidence synthesis</span></a></li>
<li class="part">Part IV — Decision analysis and clinical action</li>
<li><a href="curriculum/14-decision-theory-thresholds.html"><span class="num">14</span><span>Decision theory, utilities, loss functions, and treatment thresholds</span></a></li>
<li><a href="curriculum/15-decision-curves-voi.html"><span class="num">15</span><span>Decision curve analysis, net benefit, and value of information</span></a></li>
<li><a href="curriculum/16-bedside-shared-decisions.html"><span class="num">16</span><span>From posteriors to bedside decisions and shared decision-making</span></a></li>
<li><a href="curriculum/17-communicating-uncertainty.html"><span class="num">17</span><span>Communicating uncertainty to patients, colleagues, and journals</span></a></li>
<li class="part">Part V — Synthesis and case studies</li>
<li><a href="curriculum/18-integrated-case-studies.html"><span class="num">18</span><span>Integrated case studies in neurology and beyond</span></a></li>
<li><a href="curriculum/19-complete-workflow.html"><span class="num">19</span><span>A complete Bayesian clinical reasoning workflow</span></a></li>
<li><a href="curriculum/20-reproducible-pipelines.html"><span class="num">20</span><span>Reproducible Bayesian research pipelines</span></a></li>
<li class="part">Appendices</li>
<li><a href="appendices/a-r-setup.html"><span class="num">A</span><span>Complete R setup and package cheatsheet</span></a></li>
<li><a href="appendices/b-prior-elicitation.html"><span class="num">B</span><span>Prior elicitation worksheets and default priors</span></a></li>
<li><a href="appendices/c-solutions.html"><span class="num">C</span><span>Solutions to exercises</span></a></li>
<li><a href="appendices/d-glossary.html"><span class="num">D</span><span>Glossary, mathematics, further reading, reporting checklists</span></a></li>
</ul>

## Software

All computational examples use **R**. Primary packages: `brms`, `rstanarm`, `bayesplot`, `tidybayes`, `posterior`, `loo`, `ggplot2`, `dplyr` / `tidyr`. See [Appendix A](appendices/a-r-setup.md).

## License and citation

Prose and figures are [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). Site code is ISC. Cite using [`CITATION.cff`](https://github.com/rkalani1/bayesian-clinical-reasoning/blob/main/CITATION.cff).

# Evidence register

## Opening

This book uses **teaching numbers** unless a fact is public scientific knowledge (for example, that NINDS tPA was a randomized trial of intravenous alteplase). Landmark studies are cited as *design context*, not as extracted copyrighted tables.

## How to read a citation here

| Tag | Meaning |
| --- | --- |
| Design fact | Publicly known structure of a study |
| Teaching number | Invented count or rate for a calculation |
| Method source | Statistical or decision-analytic reference |
| Reporting | A checklist or guidance document |

## Method sources (core)

| Topic | Source |
| --- | --- |
| Bayesian data analysis | Gelman A, et al. *Bayesian Data Analysis*. 3rd ed. CRC Press. |
| Applied Bayesian workflow | McElreath R. *Statistical Rethinking*. 2nd ed. CRC Press. |
| Clinical Bayes and decision | Sox HC, Higgins MC, Owens DK. *Medical Decision Making*. 2nd ed. Wiley. |
| Thresholds | Pauker SG, Kassirer JP. The threshold approach to clinical decision making. *N Engl J Med*. 1980. |
| Decision curves | Vickers AJ, Elkin EB. Decision curve analysis. *Med Decis Making*. 2006. |
| Hierarchical models | Gelman A, Hill J. *Data Analysis Using Regression and Multilevel/Hierarchical Models*. Cambridge. |
| Bayes factors / ROPE | Kruschke JK. *Doing Bayesian Data Analysis*. 2nd ed. Academic Press. |
| Adaptive / platform | FDA. Guidance for the Use of Bayesian Statistics in Medical Device Clinical Trials. 2010. Adaptive designs guidance, 2019. |
| brms / Stan | Bürkner P-C. brms: An R package for Bayesian multilevel models using Stan. *J Stat Softw*. 2017. |
| LOO | Vehtari A, Gelman A, Gabry J. Practical Bayesian model evaluation using leave-one-out cross-validation and WAIC. *Stat Comput*. 2017. |

## Reporting and appraisal

| Instrument | Use |
| --- | --- |
| CONSORT 2010 and Bayesian extensions | Randomized trials |
| STROBE | Observational studies |
| STARD | Diagnostic accuracy |
| TRIPOD / TRIPOD-AI | Prediction models |
| PRISMA | Systematic reviews |
| ROSES-BA / BAYESIAN reporting proposals | Bayesian analyses in medical journals |
| GRADE | Guideline certainty |

## Landmark neurology / stroke *design* facts used as teaching context

These are named so a reader can look up the primary paper. Numerical worked examples in the chapters are **teaching numbers**, not reproductions of trial tables.

| Context | Why it appears |
| --- | --- |
| NINDS tPA, ECASS, IST-3 | Acute reperfusion; harm/benefit language |
| DAWN, DEFUSE-3, late-window EVT | Imaging selection as a likelihood |
| HERMES collaboration | Meta-analysis and borrowing |
| INTERACT2 / ATACH-2 | ICH blood-pressure targets; competing risks |
| ISAT / BRAT | Aneurysm treatment uncertainty |
| REMAP-CAP (design, not results tables) | Platform / response-adaptive randomization |

## Teaching datasets

Chapters generate synthetic patient-level data in R (`set.seed` stated). Do not treat those rows as a registry extract.

## Updates

If a citation is wrong or a teaching number is easy to confuse with a real trial cell, open an issue on [the repository](https://github.com/rkalani1/Bayesian-Reasoning).

!!! success "Key Takeaway"
    Trust the *method* in this book. Do not paste a teaching posterior into a note as if it were a trial result. When you need a number for a patient, go to the primary paper, a living systematic review, or your local data.

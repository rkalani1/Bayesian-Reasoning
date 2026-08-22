# Bayesian Clinical Reasoning

**Statistics, Decision Analysis, and Evidence for Neurologists and Clinician-Scientists**

Live site: [https://rkalani1.github.io/Bayesian-Reasoning/](https://rkalani1.github.io/Bayesian-Reasoning/)

A book that treats clinical reasoning as Bayesian updating — from pre-test probability and priors through hierarchical models in R (`brms`) to decision thresholds, net benefit, and how to talk about uncertainty at the bedside and in a paper.

Twenty-six chapters in six parts, plus four appendices, with exercises and worked solutions. The book is published as the GitHub Pages site above; pushes to `main` rebuild and redeploy it automatically.

Part of a companion series:

- [Critical Appraisal for Neurologists](https://rkalani1.github.io/CRIT-APP/)
- [Machine Learning & AI for Neurologists](https://rkalani1.github.io/ML/)

## Build locally

```bash
python -m venv .venv
source .venv/bin/activate   # Windows: .venv\Scripts\activate
pip install -r requirements.txt
mkdocs serve
```

Then open the URL MkDocs prints (usually `http://127.0.0.1:8000`).

```bash
mkdocs build --strict
```

## GitHub Pages

The live book is published at [https://rkalani1.github.io/Bayesian-Reasoning/](https://rkalani1.github.io/Bayesian-Reasoning/).

## Citation

See [`CITATION.cff`](CITATION.cff).

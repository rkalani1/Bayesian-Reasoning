# Bayesian Clinical Reasoning

**Statistics, Decision Analysis, and Evidence for Neurologists and Clinician-Scientists**

Live site: [https://rkalani1.github.io/bayesian-clinical-reasoning/](https://rkalani1.github.io/bayesian-clinical-reasoning/)

An original, open teaching ebook that treats clinical reasoning as Bayesian updating — from pre-test probability and priors through hierarchical models in R (`brms`) to decision thresholds, net benefit, and how to talk about uncertainty at the bedside and in a paper.

Twenty chapters and four appendices. Interactive reader and calculators (Bayes updater, treatment threshold, decision curve) ship with this workspace; the static book is the GitHub Pages site above.

Part of a companion series:

- [Critical Appraisal for Neurologists](https://rkalani1.github.io/CRIT-APP/)
- [Machine Learning & AI for Neurologists](https://rkalani1.github.io/ML/)

## Educational disclaimer

This book is for teaching and professional self-study only. It is **not medical advice**, **not institutional policy**, and **not a substitute** for primary literature, guidelines, or local standards of care. Vignettes use invented teaching numbers. Verify every method and every clinical decision against current sources.

## Who it is for

- Medical students and residents who want a first rigorous language for uncertainty
- Practicing neurologists and other clinicians who already update informally
- Clinical researchers and trialists
- Epidemiologists and biostatisticians who want a clinical spine for Bayesian methods

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

Every push to `main` runs `.github/workflows/pages.yml` (MkDocs `--strict`, then `actions/deploy-pages`).

The first time, GitHub requires the repository owner to set **Settings → Pages → Build and deployment → Source: GitHub Actions**. The Actions token cannot flip that switch. After that one click, later pushes publish automatically to the live URL above.

## Citation

See [`CITATION.cff`](CITATION.cff).

## License

- **Prose, tables, and figures** under `docs/`: [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)
- **Site code** (theme overrides, scripts): ISC — see [`LICENSE`](LICENSE)

## Author

Rizwan Kalani

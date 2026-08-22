# Appendix A — Complete R Setup and Package Cheatsheet

## Purpose

This appendix is a laboratory manual, not a chapter. Its job is to get a working Bayesian stack onto a machine you control, and to give you a one-screen memory aid for the packages this book actually uses. It will not teach statistics. It will not choose a prior. If a command fails, skip to **Common install failures** before you reinstall the operating system.

Package versions drift. Record what you actually installed in an `renv.lock` (Chapter 20).

---

## What you are installing

| Layer | What it is | Why this book needs it |
|---|---|---|
| R | Language and interpreter | Everything |
| RStudio / Posit Workbench or Positron | Editor, projects, Quarto preview | Not required, strongly preferred |
| Quarto CLI | Computational manuscripts | Chapters 19–20 |
| C++ toolchain | Compiles Stan models | `brms`, `cmdstanr`, `rstan` |
| CmdStan via `cmdstanr` | Stan sampler | Preferred backend |
| R packages | `brms` and friends | Models, plots, draws |

`rstan` (Stan-in-a-package) still works. New projects in this curriculum should use `cmdstanr` as the `brms` backend. Keep `rstan` around only if a legacy script demands it.

---

## Install R

**Linux (Ubuntu/Debian teaching box).**

```bash
# Teaching sketch. Check CRAN's current Ubuntu instructions before running.
sudo apt update
sudo apt install --no-install-recommends r-base r-base-dev
```

You also need a compiler stack Stan can see:

```bash
sudo apt install build-essential g++ libxml2-dev libssl-dev \
  libcurl4-openssl-dev libfontconfig1-dev libharfbuzz-dev \
  libfribidi-dev libfreetype6-dev libpng-dev libtiff5-dev \
  libjpeg-dev
```

**macOS.** Install R from CRAN (the Apple-silicon build if that is your machine). Install the Xcode command-line tools (`xcode-select --install`). A gfortran runtime is required for many CRAN binaries; CRAN’s macOS page links the correct installer.

**Windows.** Install R from CRAN. Install Rtools for the matching R major version (Rtools44 for R 4.4, and so on). Add Rtools to the PATH the way the Rtools installer offers. Restart the machine once. This is not folklore; Windows will not compile Stan without it.

Check the install — `R --version` from a terminal, or from inside an R session:

```r
# Should print an R version >= 4.3 for this book
R.version.string
```

---

## Install RStudio or a Posit editor

Download RStudio Desktop from Posit’s site, or use Positron if that is your laboratory standard. What this book uses from the editor:

- **Projects** (`.Rproj`) so that paths are relative and `renv` binds to the project.
- **Quarto preview** for `reports/manuscript.qmd`.
- **Build / Render** rather than a pile of open scripts.

You can do all of this in a plain editor plus a terminal. Residents usually will not.

---

## Install Quarto

Quarto is a separate CLI. RStudio bundles a copy; a standalone install is more predictable for GitHub Actions.

```bash
# Linux teaching sketch — get the current .deb from quarto.org
# quarto --version   should print 1.4 or newer
```

In R, the `quarto` package is optional glue. The CLI is the thing that must exist.

---

## The Stan toolchain via cmdstanr

Inside a project, after R works:

```r
# Preferred Stan backend for this book.
# Run once per machine, then again after a CmdStan upgrade.

install.packages("cmdstanr",
                 repos = c("https://stan-dev.r-universe.dev",
                           getOption("repos")))

# Puts CmdStan in a user directory, not in the project.
cmdstanr::check_cmdstan_toolchain()
cmdstanr::install_cmdstan()          # downloads and compiles
cmdstanr::cmdstan_version()          # record this in the sidecar
```

Point `brms` at it:

```r
options(brms.backend = "cmdstanr")
# Put that line in .Rprofile of the project, not only in your head.
```

A first compile takes several minutes. Subsequent models using the same translated Stan file are faster. If `install_cmdstan()` dies, see the failures section; do not immediately `install.packages("rstan")` as a consolation prize.

---

## Core packages

Install into an `renv` project (Chapter 20), not into a mysterious user library you will not be able to describe later.

```r
# Teaching package set for Bayesian Clinical Reasoning.
# Snapshot after this succeeds.

pkgs <- c(
  "brms",        # formula interface to Stan
  "cmdstanr",    # already installed above; include in lockfile
  "rstanarm",    # precompiled applied-regression models
  "bayesplot",   # MCMC and PPC plots
  "tidybayes",   # draws into tidy tibbles
  "posterior",   # draws, rhat, ess, intervals
  "loo",         # PSIS-LOO, stacking
  "ggplot2",     # plots
  "dplyr",       # wrangling
  "tidyr",       # pivoting
  "readr",       # CSV
  "tibble",
  "gt",          # tables if you want them
  "quarto"
)
install.packages(pkgs)
# cmdstanr may still need the r-universe repo; install it first as above.
```

`rstan` is not in that list on purpose. If you need it:

```r
install.packages("rstan")
# On some platforms this is the hardest package in the room.
```

---

## Cheatsheet: what each package is for

| Package | One-line job | Typical call in this book |
|---|---|---|
| **brms** | Bayesian regression formulas, many families, multilevel | `brm(y ~ x + (1\|site), family = bernoulli(), prior = ...)` |
| **cmdstanr** | Compile and sample Stan; backend for `brms` | `options(brms.backend = "cmdstanr")` |
| **rstanarm** | Precompiled cousins of common `lm`/`glm`/`lmer` | `stan_glm(y ~ x, family = binomial())` |
| **bayesplot** | Trace plots, rank plots, PPC | `pp_check(fit, type = "dens_overlay")` |
| **tidybayes** | Draws as tibbles; `add_epred_draws` | `add_epred_draws(new, fit)` |
| **posterior** | `rhat`, `ess_*`, `summarise_draws` | `summarise_draws(as_draws_df(fit))` |
| **loo** | Approximate leave-one-out, model compare | `loo(fit1, fit2)` |
| **ggplot2** | Grammar of graphics | `ggplot(d, aes(x, y)) + geom_point()` |
| **dplyr** | Filter, mutate, summarise | `d %>% group_by(site) %>% summarise(n = n())` |
| **tidyr** | Pivot longer/wider, nest | `pivot_longer(d, cols = c(y1, y2))` |

---

## Cheatsheet: brms verbs you will actually type

| Verb | Does |
|---|---|
| `brm(...)` | Fit. Always pass `family`, `prior`, `seed`, `chains`. |
| `prior(normal(0, 1), class = "b")` | A prior statement. Stack with `c()`. |
| `get_prior(formula, data, family)` | See what `brms` will use if you stay silent. |
| `hypothesis(fit, "x > 0")` | Posterior probability of a statement. Prefer computing it on draws. |
| `pp_check(fit)` | Default posterior predictive overlay. |
| `conditional_effects(fit)` | Adjusted predictions, useful and easy to overread. |
| `posterior_epred(fit, newdata)` | Expected predictions, no observation noise. |
| `posterior_predict(fit, newdata)` | Predictive, with observation noise. |
| `as_draws_df(fit)` | Convert to a draws data frame (`posterior`). |
| `loo(fit)` | PSIS-LOO. Read Pareto-\(k\) diagnostics. |
| `add_criterion(fit, "loo")` | Store the loo object on the fit. |
| `file = "fits/name"` | Serialize and skip refit if unchanged. |

---

## Cheatsheet: tidybayes + posterior one-liners

```r
library(posterior)
library(tidybayes)
library(dplyr)

# Convergence and intervals, decision scale later
summarise_draws(as_draws_df(fit), default_summary_measures())

# Linear predictor / expected value at new rows
new %>%
  add_epred_draws(fit) %>%
  median_qi(.epred, .width = c(0.5, 0.9))

# Probability a coefficient exceeds a threshold
mean(as_draws_df(fit)$b_nihss > 0)
```

---

## A five-minute smoke test

After everything installs, run this in a throwaway session. If this fails, stop and fix the toolchain before opening Chapter 8.

```r
# Appendix A smoke test. Seed fixed. Tiny data.
# If this samples, the stack works.

options(brms.backend = "cmdstanr")
library(brms)

set.seed(1)
d <- data.frame(
  y = rbinom(40, 1, 0.3),
  x = rnorm(40)
)

fit <- brm(
  y ~ x,
  data   = d,
  family = bernoulli(),
  prior  = c(prior(normal(0, 1.5), class = Intercept),
             prior(normal(0, 1), class = b)),
  chains = 2, iter = 500, warmup = 250,
  seed   = 1,
  refresh = 0
)

print(fit, digits = 2)
# You are looking for a completed sample, not for a scientific result.
# Pass: all four chains finish, Rhat ~ 1.00 on both rows, zero divergence
# warnings. Anything else: fix the toolchain first (see the failures table).
```

---

## rstan notes (legacy)

- `rstan` compiles via `Rcpp` and a copy of Stan headers shipped in `StanHeaders`.
- On Windows it is the usual source of “I installed Rtools and it still cannot find `g++`.”
- `rstanarm` depends on `rstan` and ships precompiled models; it can work even when you never write a `brm()` call.
- To make `brms` use `rstan` instead of `cmdstanr`: `options(brms.backend = "rstan")`. Use this only as a fallback.

Do not load `rstan` and `cmdstanr` in the same script and then wonder whose `sampling()` you called.

---

## Common install failures

| Symptom | Likely cause | What to do |
|---|---|---|
| `make: g++: No such file` | No C++ compiler | Linux: `build-essential`. macOS: Xcode CLI. Windows: Rtools, then *restart*. |
| `install_cmdstan()` fails at compile | Old compiler, out of RAM, path with spaces | Need g++ ≥ 8; close other apps; install CmdStan to a path without spaces. |
| `brms` error: “CmdStan path has not been set” | `cmdstanr` installed, CmdStan not | `cmdstanr::install_cmdstan()` then `set_cmdstan_path()`. |
| `error in 'stanc': parsing error` after a `brms` upgrade | Stale compiled model in `file =` | Delete the `.rds` and the hidden Stan cache; refit. |
| Windows: Rtools installed, still no compile | PATH / wrong Rtools version | Match Rtools to R. Use the Rtools “put on PATH” box. Restart. |
| macOS: `ld: library not found for -lgfortran` | Missing gfortran runtime | Install the CRAN-recommended gfortran for your R version. |
| `v8` or `libnode` failure (some loo/Stan helper stacks) | Missing JS runtime on Linux | `sudo apt install libv8-dev` or install the binary from RSPM. |
| `renv::restore()` cannot find `cmdstanr` | CRAN does not host it | Add the Stan r-universe repo to `renv` repos; see Chapter 20. |
| Fit “works” but \(\widehat{R}\) is `NA` | Zero iterations / failed chains | Read the sampler printout. Do not interpret a failed object. |
| Everything installed, first `brm()` takes 15 minutes | Cold compile | Expected. Subsequent fits reuse translated code. |
| `Error: C++14 standard requested but CXX14 is not defined` | Old Makevars | In `~/.R/Makevars`, set `CXX14 = g++` (or `clang++`) and retry. |

!!! warning "Common Pitfall"
    Installing the same package into the user library *and* an `renv` library, then wondering which `brms` ran, is the most common silent failure in this course. `renv::status()` at the start of a session. If it is out of sync, stop.

---

## Recommended project `.Rprofile` fragment

```r
# Project .Rprofile fragment. Teaching defaults, not law.
options(
  brms.backend  = "cmdstanr",
  brms.file_refit = "on_change",
  mc.cores      = parallel::detectCores(logical = FALSE),
  digits        = 3,
  dplyr.summarise.inform = FALSE
)
if (file.exists("renv/activate.R")) source("renv/activate.R")
```

`mc.cores` equal to the number of physical cores, not twice that, is the right default for four Stan chains on a laptop you are also using to write notes.

---

## What this book does not ask you to install

- Python, `pymc`, `numpyro`, `arviz`. Different stack, different book.
- `shiny` unless you are building an internal calculator and have a de-identification plan.
- `tidymodels` as a Bayesian engine. It can wrap some of this; we call `brms` directly.
- A GPU Stan build. None of the teaching models need it.

---

## Version floor (teaching)

These are floors, not pins. Pins live in `renv.lock`.

| Piece | Floor |
|---|---|
| R | 4.3 |
| Quarto | 1.4 |
| `brms` | 2.21 |
| `cmdstanr` | 0.8 |
| CmdStan | 2.34 |
| `posterior` | 1.5 |
| `loo` | 2.7 |
| `tidybayes` | 3.0 |
| `bayesplot` | 1.11 |
| `ggplot2` | 3.5 |
| `dplyr` | 1.1 |

---

## Further reading

- CRAN: *R Installation and Administration*. The boring document that actually answers compiler questions.
- Stan Development Team. *CmdStan User’s Guide*. https://mc-stan.org/docs/
- Gabry J, Češnovar R, Johnson A. *cmdstanr* documentation. https://mc-stan.org/cmdstanr/
- Bürkner P-C. brms: An R package for Bayesian multilevel models using Stan. *J Stat Softw*. 2017;80(1):1–28.
- Ushey K, Wickham H. *renv*. https://rstudio.github.io/renv/
- Posit. *RStudio User Guide* and Quarto documentation. https://quarto.org

!!! success "Key Takeaway"
    Install R, a compiler, CmdStan via `cmdstanr`, then `brms` and the tidy/draws ecosystem inside an `renv` project. Record versions. Run the smoke test before you trust a scientific fit. When an install fails, fix the toolchain; do not collect packages. A working stack is part of the prior: it determines whether anyone else can update what you claimed.

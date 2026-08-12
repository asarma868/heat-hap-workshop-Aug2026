# Evaluating Heat Adaptation Interventions

A hands-on R workshop covering three causal designs for evaluating
heat-adaptation programs (like heat action plans and heat advisory
systems): a time-stratified case-crossover, difference-in-differences,
and inverse probability weighting.

**Read online:** https://<your-username>.github.io/heat-hap-workshop/

## What this is

The workshop builds a synthetic, simulated population of psychiatric
emergency department encounters spanning 2010-2020, with a known
intervention effect built in on purpose (a 2016 "policy" that attenuates
the relationship between extreme heat and encounter risk by about a
third). Because the ground truth is known, you can watch each of the
three designs either recover it or fail to, and see directly what each
one does and doesn't control for.

**All data in this workshop is simulated.** Nothing here is a
re-analysis of real patient data, and the estimates produced are not
claims about whether any real intervention worked. The point is
methodological: comparing what a case-crossover, a difference-in-
differences model, and an IPW-weighted model each recover under a known
data-generating process.

## What's in this repo

| File | Purpose |
|---|---|
| `HAP_Evaluation_Workshop.Rmd` | The workshop itself: R Markdown source, built as a [bookdown](https://bookdown.org/) book |
| `_bookdown.yml` | bookdown build configuration |
| `docs/` | The rendered HTML book |

## Following along in the workshop

You don't need to install anything to follow along, just open the
**Read online** link above.

If you'd like to run the code yourself:

1. Clone or download this repo.
2. Open `HAP_Evaluation_Workshop.Rmd` in RStudio.
3. Install the required packages (the exact list is commented at the top
   of the `setup` code chunk):

   ```r
   install.packages(c("bookdown", "dplyr", "tidyr", "tibble", "lubridate",
                       "survival", "MASS", "timeDate", "ggplot2", "broom"))
   ```
4. Click **Knit** (or run `bookdown::render_book("HAP_Evaluation_Workshop.Rmd")`
   from the console). This regenerates the book into `docs/`.

The workshop runs in five parts, roughly 40-45 minutes total:

1. Building the synthetic population (10 min)
2. Time-stratified case-crossover (10 min)
3. Difference-in-differences, with a descriptive check, an event-study
   plot, and a Poisson regression (12 min)
4. Inverse probability weighting for a pre/post comparison (8 min)
5. Comparing all three against the known ground truth (5 min)

## Questions

Open an issue on this repo, or reach out to Amruta

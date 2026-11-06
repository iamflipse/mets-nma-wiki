# Bayesian NMA: How the Network Was Modeled

**Registration:** PROSPERO CRD420251134142.

**Evidence base:** 5 databases (PubMed, Embase, Cochrane CENTRAL, Web of Science, Scopus), inception → December 2025. 34,949 records → 78 RCTs, 193 intervention arms, 8,452 participants (median study duration 16.0 wk, IQR 12–24 wk; mean baseline BMI 31.6 kg/m²). 53–58 studies contributed to each outcome-specific network (53/54 for the 6 primary outcomes).

## Bayesian network meta-analysis (primary method)

- **Software:** R 4.5.2 with **gemtc 1.1.0** + **rjags 4.17**; arm-level mean changes with SEs as data format.
- **Model:** outcome-specific networks, normal likelihood, identity link, common between-study τ.
- **Priors:** relative effect d_k ~ N(0, 10²) (vague normal); τ ~ Uniform(0.01, 10), with prior-sensitivity check using τ ~ LogNormal(−2.01, 1.64).
- **Inference:** posterior median MDs with 95% credible intervals (CrIs); **SUCRA** for ranking.
- **Transitivity:** indirect contrasts only as meaningful when trials are comparable in participant characteristics, baseline risk, duration, supervision, adherence, and outcome measurement.

## Frequentist component NMA (auxiliary)

- **Software:** netmeta 3.2.0.
- **Purpose:** test whether the effect of a combined exercise–dietary intervention equals the **sum of its exercise + diet component effects** (additivity). Additivity tested by comparing the standard NMA model vs the additive CNMA with a Q-statistic difference test (Holm–Bonferroni corrected).
- CNMA results reported as MDs with 95% CIs; component effects interpreted only when the additive model fits.

## Certainty: CINeMA framework

Confidence in Network Meta-Analysis ratings (high/moderate/low/very low) applied per outcome, accounting for indirectness, imprecision, and risk of bias. **Most comparisons rated low or very low.**

**Related:** [CNMA additivity results](cnma-additivity.md) · [Certainty & limitations](certainty-and-limitations.md) · [Full text](../sources/ain-2026-100759-fulltext.md)

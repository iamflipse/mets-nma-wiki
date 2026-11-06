# MetS Lifestyle Interventions Wiki

A curated wiki distilling:

> Chen JF, Qu Y, Cheng Y, Edwards AM, Zhang Y, Sun F, Zheng C (2026). "Exercise, Dietary, and Combined Exercise–Dietary Interventions for Metabolic Syndrome: A Bayesian Network and Component Network Meta-Analysis of Randomized Controlled Trials." *Advances in Nutrition*. doi: [10.1016/j.advnut.2026.100759](https://doi.org/10.1016/j.advnut.2026.100759)

**Public copy:** https://iamflipse.github.io/mets-nma-wiki/ (read-only; static build served from the `gh-pages` branch)

## Layout

- `src/` — wiki pages as markdown (`index.md`, `about.md`, `concepts/`, `sources/`)
- `book/` — mdbook-generated static site (committed for GitHub Pages)
- `tools/mdbook` — mdbook v0.4.21 binary (aarch64 Linux, built from source)

## Rebuild + republish

```sh
./tools/mdbook build -d book
git add -A && git commit -m "update" && git push origin main
# republish gh-pages: check out orphan branch, move book/* to root, force push
touch .nojekyll   # without it the Jekyll build fails on mdbook's JS/JSON assets
```

# Health Domains & ML: A Skill-Building Course

A Quarto website providing 15 self-paced lessons, each pairing a health domain with a statistical or machine-learning model.

Live site: https://jimpleussjr.github.io/bioinformatics-skill-building/

## Local preview

Install [Quarto](https://quarto.org/docs/get-started/), then:

```bash
quarto preview
```

## Build

```bash
quarto render
```

Output goes to `docs/` (configured for GitHub Pages).

## Publish (GitHub Pages)

This repo is configured for classic GitHub Pages from the `main` branch `/docs` folder. After editing lessons:

```bash
quarto render
git add -A
git commit -m "Update site"
git push
```

Pages rebuilds on push.

### Optional: GitHub Actions deploy

A workflow file is provided at `.github/workflows/publish.yml` (gitignored by default because the default token lacks the `workflow` scope). To enable Actions-based deploy:

1. Run `gh auth refresh -h github.com -s workflow` and complete the browser step.
2. Remove `.github/` from `.gitignore`, commit the workflow, and push.
3. In repo settings, set Pages source to "GitHub Actions".

## License

Educational content. Datasets are owned by their respective providers; links only.

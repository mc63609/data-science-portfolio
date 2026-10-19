# data-science-portfolio

My data science portfolio, published with **GitHub Pages**.

**Live site:** https://mc63609.github.io/data-science-portfolio/

## What is in here

| File | Purpose |
|---|---|
| `index.md` | The portfolio page itself — served by GitHub Pages as the site entry file |
| `images/` | Figures from the featured project, exported at 200 dpi |
| `README.md` | This file |

## What the page contains

- A short introduction and my technical skills
- **Project showcase** — *Does body size predict Olympic success?*
  - project title and research question
  - a visualisation (medal rate by height quartile) with an explanation of the findings
  - two supporting charts: sport-level height effects and the Olympic body map
  - a link to the project repository
  - current status: **completed**
- A short "what I would do next" note

## How it is published

GitHub Pages serves this repository directly from the `main` branch, `/ (root)` folder:

1. Repository → **Settings** → **Pages**
2. **Build and deployment** → Source: *Deploy from a branch*
3. Branch: `main`, folder: `/ (root)` → **Save**
4. The site appears at `https://<username>.github.io/data-science-portfolio/` within a minute or two

`index.md` is the entry file, so no build step or theme is required — the page carries its own inline CSS.

## Related repository

The analysis behind the featured project lives in
[`data-science-project`](https://github.com/mc63609/data-science-project):
data, notebook, reproducible script, figures and a README with run instructions.

## Build instructions

This repository is a Quarto website with two computational blog posts,
one in Python and the other in R, both using the Palmer Penguins dataset.

### Requirements
- Quarto (version used: check with `quarto --version`)
- uv (Python package/environment manager)
- R (version used: check with `R --version`)

### Steps to build

1. Clone the repository:
   \`\`\`
   git clone git@github.com:username/username.github.io.git
   cd username.github.io
   \`\`\`
2. Set up the Python environment:
   \`\`\`
   uv sync
   \`\`\`
3. Set up the R environment (from an R console, started in this folder):
   \`\`\`r
   renv::restore()
   \`\`\`
4. Render the site:
   \`\`\`
   uv run quarto render
   \`\`\`
5. The built site lands in `docs/`. Open `docs/index.html` in a browser
   to view it locally.

### Data
Both posts use the Palmer Penguins dataset, bundled with the
`palmerpenguins` package in each language (CC0 licence). No network
access or API keys are needed to rebuild this site.

## Bonus: R and Python interop post

`posts/r-and-python/index.qmd` runs R and Python in the same document,
passing an object between them via `reticulate`. It computes a summary
in R, converts it in Python, then reads the result back into R for a
plot.

This post requires both environments (`uv sync` and `renv::restore()`,
see above) to already be set up before rendering, since `reticulate`
is pointed at this project's `.venv`.

No extra setup is needed beyond the standard build steps — `reticulate`
locates the Python environment automatically via the `here` package,
so it works regardless of where the repository is cloned to.
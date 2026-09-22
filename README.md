# Plentymercies.github.io
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
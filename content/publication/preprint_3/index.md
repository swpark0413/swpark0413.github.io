---
title: "Multivariate Lévy Adaptive B-Spline Regression (working paper)"
authors:
- admin
- Jaeyong Lee
- Jeunghun Oh

date: "2026-10-12T00:00:00Z"
doi: ""

# Schedule page publish date (NOT publication's date).
publishDate: "2026-10-13T00:00:00Z"

# Publication type.
# Accepts a single type but formatted as a YAML list (for Hugo requirements).
# Enter a publication type from the CSL standard.
publication_types: ["article"]

# Publication name and optional abbreviated publication name.
publication: ""
publication_short: ""

abstract: "We propose Multivariate Lévy Adaptive B-Spline Regression (MLABS), a Bayesian nonparametric regression model designed to capture nonlinear effects, interactions, and locally varying features of multivariate functions. MLABS represents the regression function as a random sum of low-order tensor-product B-spline basis functions under a finite Lévy random measure prior. The resulting representation adapts to the complexity and local structure of the regression function while favoring a sparse basis representation. For posterior inference, we develop a reversible-jump Markov chain Monte Carlo (MCMC) algorithm with Bayesian backfitting, collapsed trans-dimensional updates, and residual-guided proposals. These computational strategies are designed to improve posterior exploration across basis configurations of varying dimensions and structures. We also establish approximation bounds for functions with low-order interactions and heterogeneous smoothness. These bounds relate approximation accuracy to the number of basis terms. Simulation studies show that MLABS achieves competitive predictive performance across a wide range of regression settings, including high-dimensional problems. MLABS also demonstrates robust predictive performance across benchmark real datasets. In an environmental-mixture application, it attains predictive accuracy comparable to Bayesian kernel machine regression at substantially lower computational cost."

# Summary. An optional shortened abstract.
# summary: Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis posuere tellus ac convallis placerat. Proin tincidunt magna sed ex sollicitudin condimentum.

tags:
- Bayesian Statistics

featured: false

links:
# - name: Custom Link
#   url: http://example.org
url_pdf: 'https://arxiv.org/abs/2108.11863'
url_code: 'https://github.com/swpark0413/mlabs'
url_dataset: ''
url_poster: ''
url_project: ''
url_slides: ''
url_source: ''
url_video: ''

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
image:
  caption: ''
  focal_point: ""
  preview_only: false

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
# projects:
# - internal-project

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
# slides: example
---

<!-- # This work is driven by the results in my [previous paper](/publication/conference-paper/) on LLMs. -->

<!-- # {{% callout note %}}
# Create your slides in Markdown - click the *Slides* button to check out the example.
# {{% /callout %}} -->

<!-- Add the publication's **full text** or **supplementary notes** here. You can use rich formatting such as including [code, math, and images](https://docs.hugoblox.com/content/writing-markdown-latex/). -->

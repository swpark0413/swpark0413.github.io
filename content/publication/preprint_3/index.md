---
title: "Reflective Hamiltonian Monte Carlo: Mixing Analysis and Application to Sampling on Stiefel Manifold (working paper)"
authors:
- Kwangmin Lee
- Yeonhee Park
- adminc

date: "2026-01-29T21:00:00Z"
doi: ""

# Schedule page publish date (NOT publication's date).
publishDate: "2026-01-29T21:00:00Z"

# Publication type.
# Accepts a single type but formatted as a YAML list (for Hugo requirements).
# Enter a publication type from the CSL standard.
publication_types: ["article"]

# Publication name and optional abbreviated publication name.
publication: ""
publication_short: ""

abstract: "Sampling from distributions with bounded supports is a fundamental challenge in constrained statistical inference. Reflective Hamiltonian Monte Carlo (ReHMC) provides a useful sampling approach for this setting. However, it relies on convexity assumptions on the support and lacks non-asymptotic theoretical guarantees such as mixing-time bounds. To bridge this gap, we propose a convex-container-plus-thinning framework that is applicable to arbitrary target densities with bounded support. We establish the first non-asymptotic total-variation mixing-time bounds for ReHMC, achieving a polynomial dimension dependence of O(d^2) for L-smooth targets, though with exponential dependence on smoothness parameters. Under an additional m-strong convexity assumption, we derive a sharper bound that eliminates this exponential dependence. We further apply this approach to sampling on the Stiefel manifold via a well-conditioned polar reparameterization and demonstrate improved numerical stability and computational efficiency in simulation studies."

# Summary. An optional shortened abstract.
# summary: Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis posuere tellus ac convallis placerat. Proin tincidunt magna sed ex sollicitudin condimentum.

tags:
- Bayesian Statistics

featured: false

links:
# - name: Custom Link
#   url: http://example.org
# url_pdf: 'http://arxiv.org/abs/2412.10753'
# url_code: 'https://github.com/swpark0413/besiw'
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

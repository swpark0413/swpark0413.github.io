---
title: "Bayesian analysis of spiked covariance models: correcting eigenvalue bias and determining the number of spikes (working paper)"
authors:
- Kwangmin Lee
- adminc
- Seongmin Kim
- Jaeyong Lee

date: "2025-08-10T00:00:00Z"
doi: ""

# Schedule page publish date (NOT publication's date).
publishDate: "2025-08-10T00:00:00Z"

# Publication type.
# Accepts a single type but formatted as a YAML list (for Hugo requirements).
# Enter a publication type from the CSL standard.
publication_types: ["article"]

# Publication name and optional abbreviated publication name.
publication: ""
publication_short: ""

abstract: "We study Bayesian inference in the spiked covariance model, where a small number of spiked eigenvalues dominate the spectrum. Our goal is to infer the spiked eigenvalues, their corresponding eigenvectors, and the number of spikes, providing a Bayesian solution to principal component analysis with uncertainty quantification. We place an inverse-Wishart prior on the covariance matrix to derive posterior distributions for the spiked eigenvalues and eigenvectors. Although posterior sampling is computationally efficient due to conjugacy, a bias may exist in the posterior eigenvalue estimates under high-dimensional settings. To address this, we propose two bias correction strategies: (i) a hyperparameter adjustment method, and (ii) a post-hoc multiplicative correction. For inferring the number of spikes, we develop a BIC-type approximation to the marginal likelihood and prove posterior consistency in the high-dimensional regime p > n. Furthermore, we establish concentration inequalities and posterior contraction rates for the leading eigenstructure, demonstrating minimax optimality for the spiked eigenvector in the single-spike case. Simulation studies and a real data application show that our method performs better than existing approaches in providing accurate quantification of uncertainty for both eigenstructure estimation and estimation of the number of spikes."

# Summary. An optional shortened abstract.
# summary: Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis posuere tellus ac convallis placerat. Proin tincidunt magna sed ex sollicitudin condimentum.

tags:
- Bayesian Statistics

featured: false

links:
# - name: Custom Link
#   url: http://example.org
# url_pdf: 'https://arxiv.org/abs/2505.20668'
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

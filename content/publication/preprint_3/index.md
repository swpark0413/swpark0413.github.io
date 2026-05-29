---
title: "Eigenstructure Inference for High-dimensional Covariance with Generalized Shrinkage Inverse-Wishart Prior (working paper)"
authors:
- Seongmin Kim
- Kwangmin Lee
- admin
- Jaeyong Lee

date: "2026-05-19T00:00:00Z"
doi: ""

# Schedule page publish date (NOT publication's date).
publishDate: "2026-05-19T00:00:00Z"

# Publication type.
# Accepts a single type but formatted as a YAML list (for Hugo requirements).
# Enter a publication type from the CSL standard.
publication_types: ["article"]

# Publication name and optional abbreviated publication name.
publication: ""
publication_short: ""

abstract: "In multivariate statistics, estimating the covariance matrix is essential for understanding the dependence structure among variables. In high-dimensional settings, where the number of covariates increases with the sample size, it is well known that the sample covariance matrix becomes inconsistent. In particular, the largest sample eigenvalue tends to be substantially larger than the corresponding population eigenvalue, while the smallest sample eigenvalue tends to be substantially smaller than its population counterpart. This phenomenon has been widely recognized in the literature and is often described as the overdispersion of sample eigenvalues. The inverse-Wishart prior, a standard choice for Bayesian covariance estimation, also suffers from overdispersion in posterior eigenvalues. To address this issue in high-dimensional settings, the shrinkage inverse-Wishart (SIW) prior has recently been proposed. Despite its conceptual appeal and empirical success, however, the asymptotic justification for the SIW prior remains limited. In this paper, we propose a generalized shrinkage inverse-Wishart (gSIW) prior for high-dimensional covariance modeling. By extending the SIW framework, the gSIW prior accommodates a broader class of prior distributions and enables the derivation of theoretical properties under specific parameter choices. In particular, under the spiked covariance assumption, we establish the asymptotic behavior of the posterior distribution for both eigenvalues and eigenvectors by explicitly evaluating posterior expectations for two parameter settings. This explicit analysis provides insights into the large-sample behavior of the posterior that are difficult to obtain through general posterior asymptotic theory. Finally, simulation studies demonstrate that the proposed prior yields accurate estimation of the eigenstructure, particularly for spiked eigenvalues, while also providing competitive uncertainty quantification across a range of high-dimensional settings. For spiked eigenvectors, its performance is generally comparable to that of competing approaches, including the sample covariance estimator."

# Summary. An optional shortened abstract.
# summary: Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis posuere tellus ac convallis placerat. Proin tincidunt magna sed ex sollicitudin condimentum.

tags:
- Bayesian Statistics

featured: false

links:
# - name: Custom Link
#   url: http://example.org
url_pdf: 'https://arxiv.org/abs/2505.20668'
url_code: 'https://github.com/swpark0413/besiw'
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

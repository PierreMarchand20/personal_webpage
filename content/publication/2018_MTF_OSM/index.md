+++
title = "Boundary integral multi-trace formulations and Optimised Schwarz Methods"
date = 2020-06-01T17:07:23+01:00

# Schedule page publish date (NOT publication's date).
publishDate = "2018-06-01T00:00:00Z"

# Authors. Comma separated list, e.g. `["Bob Smith", "David Jones"]`.
authors = ["Xavier Claeys","admin"]

# Publication type.
# Legend:
# 0 = Uncategorized
# 1 = Conference paper
# 2 = Journal article
# 3 = Preprint / Working Paper
# 4 = Report
# 5 = Book
# 6 = Book section
# 7 = Thesis
# 8 = Patent
publication_types = ["2"]

# Publication name and optional abbreviated version.
publication = "_Computers & Mathematics with Applications_, June 2020, Vol. 79, Issue 11, Pages 3241-3256"
publication_short = ""

# Abstract and optional shortened version.
abstract = "In the present contribution, we consider Helmholtz equation with material coefficients being constants in each subdomain of a geometric partition of the propagation medium (discarding the presence of junctions), and we are interested in the numerical solution of such a problem by means of local multi-trace boundary integral formulations (local-MTF). For a one dimensional problem and configurations with two subdomains, it has been recently established that applying a Jacobi iterative solver to local-MTF is exactly equivalent to an Optimised Schwarz Method (OSM) with a non-local impendance. In the present contribution, we show that this correspondance still holds in the case where the subdomain partition involves an arbitrary number of subdomains. From this, we deduce that the depth of the adjacency graph of the subdomain partition plays a critical role in the convergence of linear solvers applied to local-MTF: we prove it for the case of homogeneous propagation medium and show, through numerical evidences, that this conclusion still holds for heterogeneous media. Our study also shows that, considering variants of local-MTF involving a relaxation parameter, there is a fixed value of this relaxation parameter that systematically leads to optimal speed of convergence for linear solvers."

# Summary. An optional shortened abstract.
summary = ""

# Is this a Featured publication? (true/false)
featured = false

# Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["deep-learning"]` references 
#   `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects = []

# Slides (optional).
#   Associate this page with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references 
#   `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
slides = ""

# Tags (optional).
#   Set `tags = []` for no tags, or use the form `tags = ["A Tag", "Another Tag"]` for one or more tags.
tags = ["Domain decomposition", "Optimised Schwarz Method", "Boundary integral formulation", "Multi-domain", "Helmholtz"]

# Links (optional).
url_pdf = "https://www.sciencedirect.com/science/article/pii/S0898122120300328"
url_preprint = "https://hal.inria.fr/hal-01921113/document"
url_code = "https://github.com/PierreMarchand20/MTF_OSM"
url_dataset = ""
url_project = ""
url_slides = ""
url_video = ""
url_poster = ""
url_source = ""

# Custom links (optional).
#   Uncomment line below to enable. For multiple links, use the form `[{...}, {...}, {...}]`.
# links = [{name = "Custom Link", url = "http://example.org"}]
links = [{name = "HAL", url = "https://hal.archives-ouvertes.fr/hal-01921113v1"}]

# Digital Object Identifier (DOI)
doi = "10.1016/j.camwa.2020.01.016"

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
[image]
  # Caption (optional)
  caption = ""

  # Focal point (optional)
  # Options: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight
  focal_point = ""
+++

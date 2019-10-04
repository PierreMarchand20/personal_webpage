+++
title = "Robust coarse spaces for the boundary element method"

# Talk start and end times.
#   End time can optionally be hidden by prefixing the line with `#`.
date = 2019-09-17T00:00:00
date_end = 2019-09-17T00:00:00
all_day = true

# Schedule page publish date (NOT talk date).
publishDate = 2019-02-05T00:00:00

# Authors. Comma separated list, e.g. `["Bob Smith", "David Jones"]`.
authors = []

# Abstract and optional shortened version.
abstract = "Domain Decomposition Methods (DDM), such as Additive Schwarz (AS), can be used to precondition linear systems arising from Boundary Integral Equations (BIE). Introduced in Hahne & Stefan (1996), this approach was widely studied since then and extended in various directions, see e.g. Heuer (1996) and Tran & Stephan (1996). The basic idea is to adapt the classical FEM-based AS (such as presented in Hahne & Stefan (1996)) to the BIE context: this includes a two-level preconditioner relying on a coarse space, which leads to theoretical bounds on the condition number. Regarding the choice of relevant coarse spaces, important progress has been achieved in recent years for the FEM context. For the construction of coarse spaces, the Generalized Eigenproblems in the Overlaps (GenEO) has emerged as one of the most promising approaches for symmetric positive definite problems, see Spillane et al. (2014). Instead of solving a coarse problem on a coarse mesh, GenEO takes eigenvectors of well chosen local eigenproblems as a basis for the coarse space. As one of its interesting features, GenEO is only based on the knowledge of the stiffness matrix elements and discretization agnostic, left apart a few reasonable assumptions. In this talk, we will present recent theoretical and numerical results in 2D and 3D aiming at adapting GenEO to the BIE context for symmetric positive definite problems on closed and open surfaces. Examples of applications are Laplace problems on screens or dissipative Helmholtz problems. This is a joint work with Xavier Claeys and Frédéric Nataf and it is supported by the project NonlocalDD, research grant ANR-15-CE23-0017-01 from the French National Research Agency while the numerical results are obtained using HPC resources from GENCI- CINES (Grant 2017- A0020607330)."
summary = ""

# Name of event and optional event URL.
event = "Parallel Solution Methods for Systems Arising from PDEs "
event_url = "https://conferences.cirm-math.fr/2064.html"

# Location of event.
location = "Luminy, France"

# Is this a featured talk? (true/false)
featured = true

# Projects (optional).
#   Associate this talk with one or more of your projects.
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
tags = []

# Links (optional).
url_pdf = ""
url_slides = "https://www.cirm-math.fr/RepOrga/2064/Slides/Marchand.pdf"
url_video = ""
url_code = ""

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
[image]
  # Caption (optional)
  caption = ""

  # Focal point (optional)
  # Options: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight
  focal_point = ""
+++

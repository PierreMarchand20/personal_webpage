+++
title = "Two-level preconditioning for BEM with GenEO"
date = 2018-09-20T18:17:32+02:00  # Schedule page publish date.
draft = false

# Talk start and end times.
#   End time can optionally be hidden by prefixing the line with `#`.
time_start = 2018-06-27T18:17:32+02:00
time_end = 2018-06-27T18:17:32+02:00

# Authors. Comma separated list, e.g. `["Bob Smith", "David Jones"]`.
authors = ["Pierre Marchand"]

# Abstract and optional shortened version.
abstract = "Domain Decomposition Methods (DDM), such as Additive Schwarz (AS), can be used to precondition linear systems arising from Boundary Integral Equations (BIE). This approach was widely studied since then and extended in various directions. The basic idea is to adapt the classical FEM-based AS to the BIE context: this includes a two-level preconditioner relying on a coarse space, which leads to theoretical bounds on the condition number. Regarding the choice of relevant coarse spaces, important progress has been achieved in recent years for the FEM context. For the construction of coarse spaces, the *Generalized Eigenproblems in the Overlaps* (GenEO) has emerged as one of the most promising approach for symmetric positive definite problems. Instead of solving a coarse problem on a coarse mesh, GenEO takes eigenvectors of well chosen local eigenproblems as a basis for the coarse space. As one of its interesting features, GenEO is only based on the knowledge of the stiffness matrix elements and discretization agnostic, left apart a few reasonable assumptions. In this talk, we will present recent theoretical and numerical results in 2D and 3D aiming at adapting GenEO to the BIE context for symmetric positive definite problems on closed and open surface. Examples of applications are Laplace problems on screens or dissipative Helmholtz problems. This work is supported by the project NonlocalDD, research grant ANR-15-CE23-0017-01 from the French National Research Agency and the numerical results are obtained using HPC resources from GENCI- CINES (Grant 2017-A0020607330)."
abstract_short = ""

# Name of event and optional event URL.
event = "Symposium of the International Association for Boundary Element Methods (IABEM)"
event_url = "https://project.inria.fr/iabem2018/"

# Location of event.
location = "Paris, France"

# Is this a selected talk? (true/false)
selected = false

# Projects (optional).
#   Associate this talk with one or more of your projects.
#   Simply enter your project's filename without extension.
#   E.g. `projects = ["deep-learning"]` references `content/project/deep-learning.md`.
#   Otherwise, set `projects = []`.
projects = []

# Tags (optional).
#   Set `tags = []` for no tags, or use the form `tags = ["A Tag", "Another Tag"]` for one or more tags.
tags = ["BEM","DDM","Boundary integral method","domain decomposition method"]

# Links (optional).
url_pdf = ""
url_slides = ""
url_video = ""
url_code = ""

# Does the content use math formatting?
math = false

# Does the content use source code highlighting?
highlight = true

# Featured image
# Place your image in the `static/img/` folder and reference its filename below, e.g. `image = "example.jpg"`.
[header]
image = ""
caption = ""

+++

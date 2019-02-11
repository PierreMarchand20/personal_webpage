+++
title = "Boundary Integral Equation and Domain Decomposition Methods"
date = 2018-11-27T17:17:10+01:00  # Schedule page publish date.
draft = false

# Talk start and end times.
#   End time can optionally be hidden by prefixing the line with `#`.
time_start = 2018-11-27T17:17:10+01:00
time_end = 2018-11-27T17:17:10+01:00
all_day = true

# Authors. Comma separated list, e.g. `["Bob Smith", "David Jones"]`.
authors = ["moi"]

# Abstract and optional shortened version.
abstract = "Boundary integral equations (BIE) are a reformulation of partial differential equations with non-local integral operators. It has the advantage to reduce the dimension of the geometric domain and to be able to naturally formulate problems on open domains. This kind of reformulation is widely used in acoustic, electromagnetic and mechanics. The matrices obtained after discretisation of these equations have the disadvantage to be fully populated, which leads us to use iterative linear solvers such as conjugated gradient or GMRes to solve the associated linear systems. To stabilize the number of iterations of these solvers with respect to the mesh size, a classical technique is to use a preconditioner. In this talk, after introducing BIE, we will present a method to precondition these matrices using domain decompositions methods and its analysis. This is a joint work with Xavier Claeys and Frédéric Nataf."
abstract_short = ""

# Name of event and optional event URL.
event = "LJLL PhD student seminar"
event_url = "https://www.ljll.math.upmc.fr/gtt/"

# Location of event.
location = "Paris, France"

# Is this a Featured talk? (true/false)
featured = false

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
tags = ["BEM","DDM","Boundary integral method","domain decomposition method"]

# Links (optional).
url_pdf = ""
url_slides = ""
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

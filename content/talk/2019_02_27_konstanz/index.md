+++
title = "Robust coarse spaces for the boundary element method"

# Talk start and end times.
#   End time can optionally be hidden by prefixing the line with `#`.
date = 2019-02-27T00:00:00
date_end = 2019-02-27T00:00:00
all_day = true

# Schedule page publish date (NOT talk date).
publishDate = 2019-02-05T00:00:00

# Authors. Comma separated list, e.g. `["Bob Smith", "David Jones"]`.
authors = []

# Abstract and optional shortened version.
abstract = "Boundary integral equations are reformulations of partial differential equations with non-local integral operators. Widely used in acoustics, electromagnetism and mechanics, they have the advantage to reduce the dimension of the geometric domain and they naturally satisfy conditions at infinity for problems on open domains. But the matrices obtained after discretisation have the disadvantage to be fully populated, which leads us to use iterative linear solvers, such as conjugated gradient or GMRes, to solve the associated linear systems. To stabilise the number of iterations of these solvers with respect to the mesh size, a classical technique is to use a preconditioner. \\ In this talk, we will present a method to precondition these matrices using domain decomposition methods, and more precisely, Schwarz Methods with a particular coarse space named GenEO whose construction is based on Generalized Eigenproblems in the Overlaps. This is a joint work with Xavier Claeys and Frédéric Nataf."
summary = ""

# Name of event and optional event URL.
event = "University of Konstanz"
event_url = ""

# Location of event.
location = "Konstanz, Germany"

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

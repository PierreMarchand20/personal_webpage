+++
title = "ElastoPhi "
date = 2018-09-14T15:20:57+02:00
draft = false

authors = ["Ibtihel Ben Gharbia","Marcella Bonazzoli", "Xavier Claeys","admin", "Pierre-Henri Tournier"]

# Tags: can be used for filtering projects.
# Example: `tags = ["machine-learning", "deep-learning"]`
tags = []

# Project summary to display on homepage.
summary = "Research project conducted during the summer school CEMRACS in 2016"

# Optional image to display on homepage.
#image_preview = "cemracs_2016.jpeg"

# Optional external URL for project (replaces project detail page).
external_link = ""

# Does the project detail page use math formatting?
math = false

# Does the project detail page use source code highlighting?
highlight = true

# Featured image
# To use, add an image named `featured.jpg/png` to your project's folder. 
[image]
  # Caption (optional)
  # caption = "Photo by Toa Heftiba on Unsplash"

  # Focal point (optional)
  # Options: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight
  focal_point = "center"

  # Show image only in page previews?
  preview_only = true

+++

## CEMRACS 2016 Numerical challenges in parallel scientific computing July 18th - August 26th 
I attended a one-week course on HPC and numerical methods, followed by a five-week project supervised by [Xavier Claeys](https://www.ljll.math.upmc.fr/~claeys/), Ibtihel Ben Gharbia and Pierre-Henri Tournier. I worked for six weeks on the project ElastoPhi with [Marcella Bonazzoli](https://www.ljll.math.upmc.fr/bonazzoli/).

We studied the efficiency of a *complexity reduction technique* based on hierarchical matrices and adaptive cross approximation applied to matrices provided by [IFPEN](http://www.ifpenergiesnouvelles.com) (French Institut of Petroleum). Those matrices came from the discretization of an elastostatic problem posed at the surface of highly *irregular crack networks*.

Our *C++ library* is available [here](https://github.com/xclaeys/ElastoPhi). For more details see the corresponding [proceeding](https://hal.archives-ouvertes.fr/hal-01644518).

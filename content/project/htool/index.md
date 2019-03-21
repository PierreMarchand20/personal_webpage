+++
title = "Htool"
date = 2018-09-20T19:04:53+02:00
draft = false

authors = ["admin","Pierre-Henri Tournier"]

# Tags: can be used for filtering projects.
# Example: `tags = ["machine-learning", "deep-learning"]`
tags = []

# Project summary to display on homepage.
summary = "Library for parallel hierarchical matrices"

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
  focal_point = "Left"

  # Show image only in page previews?
  preview_only = false
+++

Htool is an implementation of hierarchical matrices (cf. this [reference](http://www.springer.com/gp/book/9783662473238) or this [one](http://www.springer.com/gp/book/9783540771463)), it was written to test *Domain Decomposition Methods* (DDM) applied to *Boundary Element Method* (BEM). It provides:

- routines to build hierarchical matrix structures (cluster trees, block trees, low-rank matrices and block matrices),
- parallel matrix-vector and matrix-matrix product using MPI and OpenMP,
- preconditioning techniques using domain decomposition methods,
- the possibility to use Htool with any generator of coefficients (e.g., your own BEM library),
- an interface with [HPDDM](https://github.com/hpddm/hpddm) for iterative solvers,
- GUI and several service functions to display informations about matrix structures and timing.

Htool is written by Pierre-Henri Tournier and I, it is available on [GitHub](https://github.com/PierreMarchand20/htool).

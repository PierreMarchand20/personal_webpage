---
title: Robust coarse spaces for the boundary element method
event: 'Parallel Solution Methods for Systems Arising from PDEs '
event_url: 'https://conferences.cirm-math.fr/2064.html'

location: 'CIRM, Luminy, France'

abstract: >-
  Domain Decomposition Methods (DDM), such as Additive Schwarz (AS), can be used
  to precondition linear systems arising from Boundary Integral Equations (BIE).
  Introduced in Hahne & Stefan (1996), this approach was widely studied since
  then and extended in various directions, see e.g. Heuer (1996) and Tran &
  Stephan (1996). The basic idea is to adapt the classical FEM-based AS (such as
  presented in Hahne & Stefan (1996)) to the BIE context: this includes a
  two-level preconditioner relying on a coarse space, which leads to theoretical
  bounds on the condition number. Regarding the choice of relevant coarse
  spaces, important progress has been achieved in recent years for the FEM
  context. For the construction of coarse spaces, the Generalized Eigenproblems
  in the Overlaps (GenEO) has emerged as one of the most promising approaches
  for symmetric positive definite problems, see Spillane et al. (2014). Instead
  of solving a coarse problem on a coarse mesh, GenEO takes eigenvectors of well
  chosen local eigenproblems as a basis for the coarse space. As one of its
  interesting features, GenEO is only based on the knowledge of the stiffness
  matrix elements and discretization agnostic, left apart a few reasonable
  assumptions. In this talk, we will present recent theoretical and numerical
  results in 2D and 3D aiming at adapting GenEO to the BIE context for symmetric
  positive definite problems on closed and open surfaces. Examples of
  applications are Laplace problems on screens or dissipative Helmholtz
  problems. This is a joint work with Xavier Claeys and Frédéric Nataf and it is
  supported by the project NonlocalDD, research grant ANR-15-CE23-0017-01 from
  the French National Research Agency while the numerical results are obtained
  using HPC resources from GENCI- CINES (Grant 2017- A0020607330).
summary: 'We present theoretical and numerical results about a new preconditioner for matrices stemming from the boundary element method.'

date: '2019-09-17T00:00:00'
date_end: ''
all_day: true
publishDate: '2019-02-05T00:00:00'


authors: [Xavier Claeys, admin, Frédéric Nataf]
tags:
  - BEM
  - DDM
  - Boundary integral method
  - domain decomposition method

categories: 
  - conference

featured: true
projects: []
slides: ''

url_pdf: ''
url_slides: 'https://www.cirm-math.fr/RepOrga/2064/Slides/Marchand.pdf'
url_video: ''
url_code: ''
image:
  caption: ''
  focal_point: ''
---
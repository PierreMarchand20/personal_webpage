---
title: 'Applying GMRES to Helmholtz boundary integral equations: how does the number of iterations depend on the frequency in the presence of strong trapping?'
event: Séminaire de l'équipe EDP Analyse Numérique au Laboratoire J. A. Dieudonné
event_url: https://math.unice.fr/~cscheid/seminaire/

location: 'Laboratoire J. A. Dieudonné (online), France'

abstract: >-
  We are interested in solving scattering problems with strong trapping using the Combined Field Integral Equation (CFIE) and the Generalized Minimal Residual method (GMRes). In this talk, we show a new understanding of how the number of GMRes iterations depends on frequency in this situation. The non-normal nature of CFIE makes GMRes the iterative method of choice for solving linear systems stemming from its discretisation. GMRes has the advantage of being able to solve any non-singular linear system, in particular non-normal. But the convergence analysis becomes less straightforward in this case, because it requires more information than just the spectrum. Bounds for GMRes applied to non-normal matrices can be derived using condition number of eigenvalues, numerical range or pseudo-spectrum. But in the case of trapping, an additional difficulty comes from the solution operator whose norm grows exponentially through a sequence of frequencies tending to infinity, with the density of these ``bad'' frequencies increasing as the frequency increases. In this case, the spectrum of the associated matrix has the form of a cluster associated with eigenvalues near the origin. We provide a new analysis of the GMRes convergence taking into account this particular distribution, which allows to show more precisely why the number of iterations grows with the frequency.

summary: 'A new approach to study GMRes applied to Helmholtz boundary integral equation in presence of strong trapping.'

date: '2020-12-17T00:00:00'
date_end: ''
all_day: true
publishDate: '2019-02-05T00:00:00'


authors: [Jeffrey Galkowski, admin, Alastair Spence, Euan Spence]
tags:
  - GMRES
  - CFIE
  - Combined-Field operator
  - BEM
  - Boundary integral method
  - Boundary Integral Equation
  - Strong trapping


categories: 
  - seminar

featured: false
projects: []
slides: ''

url_pdf: ''
url_slides: ''
url_video: ''
url_code: ''
image:
  caption: ''
  focal_point: ''
---
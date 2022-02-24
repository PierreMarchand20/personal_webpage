---
title: "Une analyse de convergence pour GMRES appliquée aux équations intégrales de frontière pour l'équation d'Helmholtz en présence de cavités elliptiques"
event: "Congrès d'Analyse Numérique pour les Jeunes - 2020"
event_url: 'https://indico.math.cnrs.fr/event/6098/'

location: "Congrès d'Analyse Numérique pour les Jeunes - 2020, Online"

abstract: "Dans cet exposé, nous nous intéresserons à la résolution de problèmes de diffraction par formulation intégrale avec la présence de cavités elliptiques. Plus précisément, nous utiliserons une formulation intégrale classique, dite équation combinée des champs (Combined Field Integral Equation, ou CFIE) discrétisée par éléments de frontière et GMRes (Generalized Minimal Residual method) comme méthode de résolution itérative. L'objectif est de présenter une analyse de convergence de GMRes qui met en évidence la dépendance du nombre d'itérations en fonction de la fréquence lorsque la géométrie du problème contient une cavité elliptique.

Le choix de GMRes est naturel du fait de la nature non-normale de l'opérateur CFIE. En effet, GMRes a l'avantage de pouvoir résoudre tout problème non-singulier, et en particulier non-normal. Mais l'analyse de convergence est dans ce cas moins évidente, puisque le spectre de l'opérateur n'est plus suffisant. Des bornes sur la vitesse de convergence de GMRes ont notamment été proposées en utilisant le conditionnement des valeurs propres, l'image numérique de l'opérateur, ou encore le pseudospectrum.

Mais dans le cas où la géométrie contient une cavité elliptique, une difficulté supplémentaire vient de l'opérateur solution dont la norme croît exponentiellement à travers une séquence de fréquences tendant vers l'infini, la densité de ces fréquences de résonance augmentant avec la fréquence. Dans ce cas, le spectre de la matrice associée a la forme d'un cluster avec des outliers près de l'origine. Nous proposons alors une nouvelle analyse de la convergence de GMRes en tenant compte de cette distribution particulière du spectre."

summary: "Une nouvelle approche pour étudier la convergence de la méthode de GMRes appliquée à la résolution de l'équation de Helmholtz par formulation intégrale avec des cavités elliptique."

date: '2020-12-03T00:00:00'
date_end: ''
all_day: true
publishDate: '2020-12-03T00:00:00'


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
  - conference

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
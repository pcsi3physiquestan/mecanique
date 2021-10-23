---
jupytext:
  encoding: '# -*- coding: utf-8 -*-'
  formats: ipynb,md:myst
  split_at_heading: true
  text_representation:
    extension: .md
    format_name: myst
    format_version: 0.13
    jupytext_version: 1.10.3
kernelspec:
  display_name: Python 3
  language: python
  name: python3
---
# Système conservatif: Définition

````{important} __Définition : Système conservatif__

Un système mécanique est dit conservatif si son énergie mécanique est conservé durant le mouvement. Cela implique que les seules forces qui s'appliquent sur le système sont conservatives ou ne travaillent pas.

````


__Intérêt__
Les systèmes conservatifs présentent de nombreux intérêts. Tout d'abord, à l'échelle microscopique, les systèmes sont a priori conservatifs puisque toutes les forces dérivent d'une énergie potentielle. De plus, l'étude des systèmes conservatifs peut se faire à partir d'outils très puissants d'analyse de l'énergie potentielle.


# Systèmes conservatifs: Propriétés générales

## Positivité de l'énergie cinétique

````{important} __Fondamental : Positivité de l'énergie cinétique__

Cette propriété est bien plus générale mais elle a des conséquences particulière dans les mouvements conservatifs. En effet, __l'énergie cinétique est positive ou nulle__.

Il vient que l'énergie potentielle du mobile doit nécessairement être inférieure ou égale à l'énergie mécanique.

Dans le cas d'un système conservatif où l'énergie mécanique est une constante, cela signifie que l'énergie potentielle est majorée et que __les zones de l'espace où l'énergie potentielle est supérieure à l'énergie mécanique sont des zones inaccessibles pour le système. On parle de barrières de potentiels.__

De plus, si le système atteint un point où l'énergie potentielle égale l'énergie mécanique, alors en ces points, la vitesse du mobile s'annule (puisque l'énergie cinétique y est nulle). C'est en général un point de rebroussement du système.
````

## Position d'équilibre

````{important} __Fondamental : Position d'équilibre et énergie potentielle__

Nous étudierons plus en détail cette propriété pour les système conservatifs à 1 degré de liberté mais on peut déjà remarqué que les positions d'équilibre correspondent à des extrema d'énergi potentielle (maximum, minimum ou point col). En effet, la résultante des forces est nulle en une position d'équilibre. Or la force étant moins le gradient de l'énergie potentielle, il vient la propriété précédente (dans un système conservatif, la résultante des forces dérive d'une énergie potentielle).
````


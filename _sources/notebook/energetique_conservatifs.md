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
# Systèmes conservatifs

````{admonition} Compétences
:class: tip
Toutes ces compétences concernent les systèmes conservatifs.

* Déduire d'un graphe d'énergie potentielle le comportement qualitatif: trajectoire bornée ou non, mouvement périodique, positions de vitesse nulle.
* Déduire d'un graphe d'énergie potentielle l'existence de positions d'équilibre, et la nature stable ou instable de ces positions.
* Identifier le cas des petits mouvements autour d'une position d'équilibre stable au modèle de l'oscillateur harmonique
* Mettre en évidence les effets non linéaires lorsqu'on s'éloigne du voisinage d'une position d'équilibre.
* Evaluer l'énergie minimale pour franchir une barrière de potentiel.
````

Dans toute l'étude, on supposera que le système est ponctuel. Plusieurs caractéristiques peuvent se généraliser aux systèmes de points mais ces derniers possédant normalement plusieurs degré de liberté, la généralisation peut devenir quelques fois complexes.


````{important} __Système conservatif__

Un système mécanique est dit conservatif si son énergie mécanique est conservé durant le mouvement. Cela implique que les seules forces qui s'appliquent sur le système sont conservatives ou ne travaillent pas.

````

````{important} __Positivité de l'énergie cinétique__

* Cette propriété est bien plus générale mais elle a des conséquences particulière dans les mouvements conservatifs. En effet, __l'énergie cinétique est positive ou nulle__.
* Il vient que l'__énergie potentielle du mobile doit nécessairement être inférieure ou égale à l'énergie mécanique__.

> Dans le cas d'un système conservatif où l'énergie mécanique est une constante, cela signifie que l'énergie potentielle est majorée et que __les zones de l'espace où l'énergie potentielle est supérieure à l'énergie mécanique sont des zones inaccessibles pour le système. On parle de barrières de potentiels.__

> De plus, si le système atteint un point où l'énergie potentielle égale l'énergie mécanique, alors en ces points, la vitesse du mobile s'annule (puisque l'énergie cinétique y est nulle). C'est en général un point de rebroussement du système.
````

````{important} __Position d'équilibre et énergie potentielle__

Nous étudierons plus en détail cette propriété pour les système conservatifs à 1 degré de liberté mais on peut déjà remarqué que __les positions d'équilibre correspondent à des extrema d'énergiz potentielle__ (maximum, minimum ou point col). 

> En effet, la résultante des forces est nulle en une position d'équilibre. Or la force étant moins le gradient de l'énergie potentielle, il vient la propriété précédente (dans un système conservatif, la résultante des forces dérive d'une énergie potentielle).
````


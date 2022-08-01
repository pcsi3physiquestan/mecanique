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
# Description des actions mécaniques ponctuelles

## Interactions et actions: définitions

````{sidebar} Système d'étude et milieu extérieur
Par la suite, on s'intéressera souvent à un système mécanique donné (système d'étude) qui subit l'influence (des actions) d'autres systèmes (qu'on regroupe sous le terme de "milieu extérieur"). Dans cette vision, on s'intéresse à aux actions du milieu extérieur ou "oubliant" un peu dans l'étude les actions réciproques du système sur le milieu extérieur. C'est pourquoi par la suite, on parlera surtout d'actions et non d'interactions. Il faut néanmoins garder à l'esprit qu'elles existent, même si leur prise en compte n'est pas nécessaire dans l'étude du mouvement du système d'étude.
````
````{topic} Interaction et actions
Soit deux systèmes mécaniques $\Sigma_1$ et $\Sigma_2$ (points matériels ou systèmes de points matériels) possédant des caractéristiques (masse, charge, contact... ) tel que le premier système influe sur le mouvement du second système. Alors le second influe aussi sur le premier système (on parlera par la suite de loi d'action et réaction). On dit que les deux systèmes mécaniques sont en __interactions__.

On peut décrire l'interaction entre deux systèmes mécaniques par __deux actions réciproques__: l'action $\mathfrak{A}_{1 \to 2}$ de $\Sigma_1$ sur $\Sigma_2$ et l'action $\mathfrak{A}_{2 \to 1}$ de $\Sigma_2$ sur $\Sigma_1$.
````


## Actions: Types de description

````{important} __Action ponctuelle__

Une action ponctuelle __d'un système $\Sigma_1$ sur un système $\Sigma_2$__ est une action agissant sur un point (matériel) du système $\Sigma_2$.

> Tout système possédant une extension spatiale, il s'agit d'une modélisation théorique d'une action mécanique.
````

````{margin}
La notion d'action globale aura son utilité pour les _systèmes_ de points matériels.
````
````{important} __Action résultante (ou globale).__

Une action résultante sur un système $\Sigma_2$ est une action du milieu extérieur modélisable par le regroupement __arbitraire__ d'un ensemble d'actions ponctuelles sur le système $\Sigma_2$.
````



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
# Oscillateur harmonique

## Oscillateur harmonique: Equation

````{important} __Equation différentielle d'un oscillateur harmonique__

Un oscillateur harmonique est un système dont l'équation d'évolution s'écrit:

$$
\frac{\rm{d^2}x}{\rm{dt^2}}(t) + \omega_0^2 x(t) = \omega_{0}^2 x_{eq}
$$
On rappelle qu'on peut annuler le second membre __constant__ en procédant à un changement de variable $X = x - x_{eq}$. Pour la suite, on étudiera directement l'équation sans second membre.

````

````{important} __Energie potentielle__

La résultante des forces en mécanique s'écrit donc sous la forme $\overrightarrow{F} = - k x \overrightarrow{e_x}$ et elle dérive d'une énergie potentielle sous la forme $E_p = \frac{1}{2}k x^2$

Attention: ces expressions seront à modifier suivant le système de coordonnées choisi.
````

## Evolution temporelle

````{admonition} Exercice 
:class: attention

1. Donner les deux formes générales de $X(t)$
1. Déterminer les constantes d'intégration sous les deux formes pour des conditions initialles à $t=0$: $x(t=0) = x_0; v(t=0) = v_0$.
1. Vérifier qu'il y a __isochronisme__ des oscillations.
1. Représenter graphiquement l'évolution temporelle de $X(t)$.

````

## Evolution énergétique

````{admonition} Exercice 
:class: attention

On suppose que les oscillations sont d'amplitude $x_0$.

1. Exprimer l'énergie potentielle et l'énergie cinétique au cours du temps.
1. En déduire l'expression de l'énergie mécanique
1. On a représenté graphiquement l'évolution temporelle des grandeurs énergétiques. Commenter les échanges d'énergie.

```{figure} ./images/meca_epec_harmonique.jpg
:name: fig_248
:align: center

```

````


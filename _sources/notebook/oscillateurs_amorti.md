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
# Oscillateur amorti

## Oscillateur amorti: Equation

````{admonition} Définition : Oscillateur amorti
:class: tip

Un oscillateur amorti est un oscillateur donc l'équation s'écrit:

\begin{equation}
\frac{\rm{d^2}x}{\rm{dt^2}}(t) + \frac{\omega_0}{Q} \frac{\rm{d}x}{\rm{dt}}(t)+\omega_0^2 x(t) = \omega_{0}^2 x_{eq}
\end{equation}
On rappelle qu'on réalise souvent un changement de variable pour annuler le second membre constant.

On n'a pas donné ici l'expression avec le coefficient d'amortissement mais on peut réaliser l'étude au moyen de ce dernier aussi.

````

````{admonition} Fondamental : Evolution énergétique
:class: attention

Le théorème de la puissance mécanique donne:

\begin{align*}
\frac{\rm{d}}{\rm{dt}}\left(E_p + E_c\right) &= P(\overrightarrow{f_{fluide}})\\
&= - \lambda v^2\\
&< 0
\end{align*}
On observe que l'énergie mécanique va diminuer au cours du temps. Suivant le régime on pourra observer des échanges amortis entre les deux réservoirs d'énergie que sont l'énergie potentielle et l'énergie cinétique.
````

## Oscillateur amorti: Régimes de fonctionnement

### Régime apériodique

````{admonition} Exercice 
:class: attention

On considère un oscillateur amorti en régime apériodique.

1. Donner l'expression temporelle de X(t) et préciser l'expression des constantes d'intégration pour $X(t=0) = x_0$ et $V(t=0)=V_0$.
1. Estimer le temps caractéristique d'un tel régime en fonction du coefficient d'amortissement.

```{figure} ./images/meca_aperio_tempo.jpg
:name: fig_249
:align: center

```

````

### Régime critique

````{admonition} Exercice 
:class: attention

On considère un oscillateur amorti en régime critique.

1. Donner l'expression temporelle de X(t) et préciser l'expression des constantes d'intégration pour $X(t=0) = x_0$ et $V(t=0)=V_0$.
1. Estimer le temps caractéristique d'un tel régime.

````

### Régime pseudo-périodique

````{admonition} Exercice 
:class: attention

On considère un oscillateur amorti en régime pseudo-périodique.

1. Donner l'expression temporelle de X(t) et préciser l'expression des constantes d'intégration pour $X(t=0) = x_0$ et $V(t=0)=V_0$.
1. Quelles sont les caractéristiques de l'évolution temporelle ?
1. Estimer le temps caractéristique d'un tel régime en fonction du coefficient d'amortissement.
1. Définir le décrément logarithmique et l'exprimer en fonction du coefficient d'amortissement.
1. Commenter l'évolution énergétique représentée ci-dessous.

```{figure} ./images/meca_pseudo_energie.jpg
:name: fig_250
:align: center

```

```{figure} ./images/meca_pseudo_tempo.jpg
:name: fig_251
:align: center

```

````

### Temps caractéristique

````{admonition} Exercice 
:class: attention

Représenter le temps caractéristique du système en fonction du coefficient d'amortissement et commenter ce graphique.

````


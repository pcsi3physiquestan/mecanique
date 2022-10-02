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
# Cinétique du solide

## Quantité de mouvement

````{margin}
Il s'agit d'une définition opératoire qui nous permettra de calculer les quantités de mouvement d'un solide décrit comme un ensemble de solides. On ne sera par contre pas amené à calculer des sommes continues.
````
````{important} __Quantité de mouvement d'un système de points__

La quantité de mouvement dans un référentiel R d'un système de points matériels S est la somme des quantités de mouvements dans le même référentiel des points qui le composent.

Il peut s'agir d'une somme discrète ou continue suivant la description du système.

````


````{important} __Quantité de mouvement et centre d'inertie__

La quantité du mouvement dans un référentiel R d'un système S est égale à la quantité de mouvement qu'aurait un point matériel fictif situé au centre d'inertie G et dont la masse serait la masse totale du système.

$$
\overrightarrow{p_{S/\mathfrak{R}}} = M \overrightarrow{v_{G/\mathfrak{R}}}
$$
````

````{admonition} Démonstration
:class: note
>\begin{align*}
\overrightarrow{P_{S/R}} &= \iiint_{P \in S} \rho(P) \overrightarrow{v}(P) d \tau(P)\\
&= \iiint_{P \in S} \rho(P) \frac{d \overrightarrow{OP}}{dt} d \tau(P)\\
&= \frac{d}{dt}(\iiint_{P \in S} \rho(P) \overrightarrow{OP} d \tau(P))\\
&= \frac{d}{dt}(M \overrightarrow{OG}) = M \overrightarrow{v_{G/R}}
\end{align*}
````

## Moment cinétique d'un solide

````{important} __Moment cinétique par rapport à un point__

Le moment cinétique $\overrightarrow{\sigma_{S/A}}$ d'un système S dans un référentiel R par rapport à un point A est la somme des moments cinétiques des différents points du système par rapport au même point A.

````

````{important} __Moment cinétique par rapport à un axe__

Le moment cinétique $\overrightarrow{\sigma_{S/\Delta}}$ d'un système S dans un référentiel R par rapport à un point $\Delta$ est la somme des moments cinétiques des différents points du système par rapport au même point $\Delta$.

````

````{topic} ATTENTION

On ne peut relier a priori le moment cinétique du solide à la vitesse du centre d'inertie par une formule faisant inervenir un produit vectoriel (définition du moment cinétique d'un point matériel). Le moment cinétique d'un solide ne peut se calcule que de trois manière:

* Cas général: par sommation discrète ou continue à partir du moment de chaque point
* Cas d'une translation: seul cas où l'on peut se ramener au mouvement du centre d'inertie (cf. suite)
* Cas d'une rotation:  une expression du moment cinétique sera donnée par la suite.

````

## Energie cinétique d'un système de points matériels

````{important} __Energie cinétique d'un système de point matériel__

L'énergie cinétique $E_{C/R}$ du système S dans le référentiel R est la somme des énergie cinétique de l'ensemble des points qui composent le système S.

````

````{topic} Termes de l'énergie cinétique (Admis)
L'énergie cinétique d'un solide __indéformable__ se décompose en deux termes:

* le premier décrit le mouvement de translation global du solide (mouvement du centre d'inertie).
* le second correspond à la rotation du solide sur lui-même.

Il existe des expressions pour chaque terme mais ils ne sont aps à connaître dans le cas général. Nous étudierons des expressions particulières de l'énergie cinétique dans le cas de la translation et de la rotation.
````

````{topic} ATTENTION

Comme pour le moment, il n'y a pas a priori de relation entre l'énergie cinétique totale d'un système et la vitesse du centre d'inertie. Elle ne peut s'établir que dans un cas particulier.

````


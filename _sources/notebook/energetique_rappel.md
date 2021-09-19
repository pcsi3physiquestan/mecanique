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
# Energie cinétique: Rappels

## Rappel: Energie cinétique d'un point matériel

_Soit un point matériel M de masse m animé d'une vitesse $\overrightarrow{v_{M/\mathfrak{R}}}$ dans un référentiel $\mathfrak{R}$. L'énergie cinétique du point matériel dans le référentiel $\mathfrak{R}$ est définie comme $E_{c/\mathfrak{R}}(M) = \frac{1}{2}m v_{M/\mathfrak{R}}^2$_

## Energie cinétique: Cas d'un solide

_Soit un solide __indéformable__ animé d'une vitesse de translation $\overrightarrow{v_{/\mathfrak{R}}}$ dans un référentiel $\mathfrak{R}$. L'énergie cinétique du solide (somme de l'énergie cinétique de toutes ses composantes) a pour expression $E_c = \frac{1}{2}M v_{/\mathfrak{R}}^2$ où M est la masse totale._

_Soit un solide __indéformable__ en rotation autour d'un axe fixe $\Delta$ dans un référentiel $\mathfrak{R}$ à la vitesse angulaire $\omega_{/\\Delta}$. L'énergie cinétique du solide (somme de l'énergie cinétique de toutes ses composantes) a pour expression $E_c = \frac{1}{2} J_{\Delta} \omega_{/\Delta}^2$ où $J_{\Delta}$ est le moment d'inertie du solide sur l'axe $\Delta$_

````{dropdown} Remarque

__Solide indéformable__
L'hypothèse d'un solide indéformable suppose notamment qu'il n'y a pas d'agitation thermique au sein du solide. En pratique, elle toujours présente et la contribution énergétique associée est contenue dans un terme énergétique supplémentaire appelée énergie interne. Comme nous le verrons en thermodynamique, cette part de l'énergie est liée à la température du solide. Cela revient à considérer ici que la température des solides ne varient de manière significative.

````

## Indépendance de la variation d'énergie cinétique vis-à-vis du chemin parcouru.

````{admonition} Fondamental : Indépendance de l'énergie cinétique vis-à-vis du chemin parcouru.
:class: attention

Considérons un système mécanique évoluant d'un état A (vitesse et position donnée) à un état B (vitesse et position donnée). On peut définir l'énergie cinétique à chaque état A et B indépendamment des états précédents ou succédants aux états A et B et la __variation__ d'énergie cinétique de A à B ne dépend pas du chemin parcouru pour passer de l'état A à l'état B. On dit que l'énergie cinétique est une fonction d'état.
````

````{admonition} Fondamental : Notation
:class: attention

Les fonctions d'états sont des différentielles exactes d'un point de vue mathématique. Cela implique une notation particulière lorsqu'on travaille avec la __variation__ de l'énergie cinétique:

* pour une variation finie, c'est-à-dire un déplacement sur une distance qui ne tend pas vers 0, on note la variation d'énergie cinétique $\Delta E_c$. (L'important c'est le $\Delta$).
* pour une variation infinitésimale, c'est-à-dire un déplacement sur une distance qui tend vers 0, on note la variation d'énergie cinétique $dE_c$. (L'important, c'est le $d$ qui représente une différentielle).
````


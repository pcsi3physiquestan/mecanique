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
# Cinématique et cinétique des systèmes de points

````{margin}
Une bonne partie des démonstration seront faites pour des systèmes discrets pour les propriétés sont généralisables aux systèmes continus.

````
````{important} __Système de points matériel__

Un système de points matériels S (ou solide déformable) est un ensemble de points matériels dont on décrit le mouvement.

On distingue deux types de descriptions:

* Les systèmes discrets, composés d'un ensemble de point matériels séparables les uns des autres. Ils sont décrits par une ensemble de points $\{M_i\}$ et leurs caractéristiques cinématiques (vitesse $\{\overrightarrow{v_i(M_i)}\}$et cinétiques (masse $\{m_i\}$ et les caractéristiques qui en découlent).
* Les systèmes continus, pour lesquels la matière forme un ensemble dont les caractéristiques peuvent être décrites par des fonctions continues (ou au moins continues par morceaux):champ de vitesse ($\overrightarrow{v_{/\mathfrak{R}}}(M)$ avec $M \in S$) et masse d'un petit volume de matière $d\tau(M)$ autour de chaque point M ($\rho(M) d\tau(M)$ avec $\rho(M)$ la __masse volumique__  autour du point M).
````

```{sidebar} Regroupement
Le regroupement d'un ensemble de points matériel dans un même système est arbitraire (choix de la personne travaillant sur le problème) mais répond à une réflexion physique:les points font partie du même objet, de la même pièce physique, sont du même type... ).

_On pourra être amenés à considérer un solide comme un ensemble de sous-systèmes dont on connaît les caractéristiques._
```
````{important} __Solide indéformable__

Un solide indéformable est un système de points tel que, quelque soit les deux points $P_i$ et $P_j$ du solides, à tout instants, la _distance_ $P_i P_j$ est constante.

````
```{topic} Direction
Dans un solide __indéformable__, la distance entre les points doit être constantes, mais la direction du vecteur associé peut varier, c'est le cas quand le solide tourne sur lui-même. Si nous utiliserons principalement des solides continus par la suite, un solide peut aussi être un ensemble discrets de points matériels.
```




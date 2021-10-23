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
# Mouvement des planètes et lois de Kepler

## Enoncé des lois de Kepler


__Position du problème.__
Nous sommes dans le cas où le potentiel newtonien est attractive. Dans un premier temps, nous nous intéresserons au mouvement des planètes du système solaire de sorte que nous noterons $M_S$ la masse de l'astre attracteur fixe (le soleil, S) et $M_P$ la masse de la planète considérée. La force de gravitation s'écrit alors: $\overrightarrow{F} = - \frac{G M_S M_P}{r^2} \overrightarrow{u_r}$.

On peut donc utiliser les résultats précédents en prenant $K = G M_S M_P >0$.


````{important} __Fondamental : Hypothèses des lois de Kepler__

* Les planètes et le Soleil présentent une symétrie sphérique.
* Le mouvement d'une planète est uniquement lié à l'interaction entre cette planète et le Soleil. On exclut toute influence des autres planètes et objets célestes.
* La masse des planètes est négligeable devant celle du Soleil.
````

````{dropdown} Remarque

__Sur les hypothèses__
Sur la symétrie sphérique: Ceci reste une approximation au 1er ordre et quelques écarts aux lois énoncées peuvent s'expliquer par la non-sphéricité des planètes. Nous verrons dans le cours d'électromagnétisme que cela permet d'assimiler les planètes et le Soleil à des points matériels.

Sur la seule interaction considérée: Cette hypothèse est cruciale car il est aujourd'hui encore impossible d'étudier un problème à N corps de manière analytique. Elle est plus ou moins critiquable (notamment lorsqu'il s'agit de comparer l'effet du Soleil et celui des satellites des planètes) mais suffit en première approximation.

Comparaison des masses: Outre la justification (incomplète) de la seconde hypothèse, cette dernière hypothèse permet de justifier le fait qu'on suppose le Soleil fixe (c'est-à-dire peu perturbé par les actions réciproques des planètes). Nous verrons que cela revient à considérer que le Soleil est au barycentre des masses du système solaire.

Les deux dernières hypothèses sont justifiées en observant que la masse du Soleil ($M_S = 2 \times 10^{30} \rm{kg}$) est grande devant les autres masses (à titre d'exemple, la masse de Jupiter est dix fois plus petite et la masse de la Terre dix mille fois plus petite: $M_T = 6 \times 10^{24} \rm{kg}$).

````

````{important} __Fondamental : Lois de Kepler__

* 1ère loi: Le centre des planètes décrit une ellipse dont l'un des foyers est le Soleil.
* 2ème loi: Les rayons vecteurs balaient des aires égales pour des intervalles de temps égaux.
* 3ème loi: Le rapport entre le carré de la période T de révolution de la planète autour su Soleil et le cube du demi-grand axe a de la trajectoire est indépendant de la planète.
````

## Cas des deux premières lois


__Démonstration des deux premières lois.__
Les deux premières lois se démontrent rapidement. Les hypothèses permettent de considérer le Soleil fixe et la seule force qui s'applique sur la force (attraction du Soleil) est une force centrale.

Il vient, de la conservation du moment cinétique, que le mouvement vérifie la loi des aires.

De plus, la force est newtonienne donc la trajectoire est une conique. Comme le mouvement est confiné, c'est un état lié, donc une ellipse.


## Energie mécanique


Avant de s'intéresser à la troisième loi de Kepler, nous allons déjà exprimer l'énergie mécanique des planètes. On rappelle que la trajectoire est elliptique. Nous allons étudier deux cas: le cas général et le cas particulier du cercle (excentricité nulle).


_On rappelle que le point le plus éloigné est appelé __aphélie__ et que le point le plus proche est appelé __périhélie__._

_On rappelle aussi que dans le cours générale sur les coniques, une relation entre le demi-grand axe $a$ et l'excentricité a été démontrée. On notera aussi b le demi-petit axe._

````{important} __Fondamental : Relation énergie mécanique et demi-grand axe.__

L'énergie mécanique dans une trajectoire elliptique a pour expression:

\begin{equation}
E_m = - \frac{K}{2a}
````


__Démonstration__
Cette démonstration est à faire en exercice. Elle doit être connue.

Indice: Les caractéristiques de conservation des intégrales premières sont à utiliser entre le périhélie et l'aphélie.


````{important} __Fondamental : Cas circulaire__

Si la trajectoire est circulaire, alors $E_m = -E_c = \frac{E_p}{2} = - \frac{K}{2R}$ avec R le rayon du cercle.
````


__Démonstration__
Cette démonstration est à faire en exercice. Elle doit être connue.

Indice: Exprimer, au moyen du PFD, une relation entre la vitesse et le rayon. En déduire l'expression de $E_m$.


## Troisième loi de Kepler

````{important} __Fondamental : Cas d'un mouvement circulaire__

Note: C'est le cas à connaître.

On applique le principe fondamental de la dynamique à la planète dans le référentiel héliocentrique:

\begin{align*}
- R \dot\theta^2 \overrightarrow{e_r} &= -\frac{GM_S}{R^2}\overrightarrow{e_r}\\
\frac{4\pi^2}{T^2} &= \frac{GM_S}{R^3}\\
\frac{T^2}{R^3} &= \frac{4\pi^2}{GM_S}
\end{align*}
Il vient que le rapport $\frac{T^2}{R^3}$ ne dépend pas des caractristiques de la planète: il est le même quelque soit la planète considérée.
````

````{admonition} Complément : Cas elliptique
:class: hint, dropdown
Le cas elliptique n'est pas à connaître. Sa preuve est donnée à titre d'information.
````


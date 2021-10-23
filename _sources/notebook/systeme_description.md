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
# Description d'un système de points

## Solide déformable et indéformable

````{important} __Définition : Système de points matériel__

Un système de points matériels S (ou solide déformable) est un ensemble de points matériels dont on décrit le mouvement.

On distingue deux types de descriptions:

* Les systèmes discrets, composés d'un ensemble de point matériels séparables les uns des autres. Ils sont décrits par une ensemble de points $\{M_i\}$ et leurs caractéristiques cinématiques (vitesse $\{\overrightarrow{v_i(M_i)}\}$et cinétiques (masse $\{m_i\}$ et les caractéristiques qui en découlent).
* Les systèmes continus, pour lesquels la matière forme un ensemble dont les caractéristiques peuvent être décrites par des fonctions continues (ou au moins continues par morceaux):champ de vitesse ($\overrightarrow{v_{/\mathfrak{R}}}(M)$ avec $M \in S$) et masse d'un petit volume de matière $d\tau(M)$ autour de chaque point M ($\rho(M) d\tau(M)$ avec $\rho(M)$ la __masse volumique__  autour du point M).

````


Le regroupement d'un ensemble de points matériel dans un même système est arbitraire (choix de la personne travaillant sur le problème) mais répond à une réflexion physique:les points font partie du même objet, de la même pièce physique, sont du même type... )

On pourra être amenés à considérer un solide comme un ensemble de sous-systèmes dont on connaît les caractéristiques.


````{important} __Définition : Solide indéformable__

Un solide indéformable est un système de points tel que, quelque soit les deux points $P_i$ et $P_j$ du solides, à tout instants, la distance $P_i P_j$ est constante.

````

````{attention}

Dans un solide, la distance entre les points doit être constantes, mais la direction du vecteur associé peut varier, c'est le cas quand le solide tourne sur lui-même. Si nous utiliserons principalement des solides continus par la suite, un solide peut aussi être un ensemble discrets de points matériels.

````

## Masse et centre d'inertie

````{important} __Définition : Masse totale__

On définit la masse totale M du système S comme la somme de toutes les masses des points matériels composant le solide.

````

>__Expression mathématique__
>Dans le cadre d'une description discrète, la masse totale est simplement $M = \sum\limits_{i=1}^{n} m_i$.
>
>Dans le cadre d'une description continu, la masse totale devient une intégrale: $M = \iiint_{P \in S} \rho(P) d \tau(P)$. A l'heure actuelle, il n'est pas demandé de savoir calculer une telle intégrale. Il suffit de comprendre qu'on somme des petits volumes infinitésimaux $d\tau(M)$ coefficientés (ici par la masse volumique).


````{important} __Définition : Centre d'inertie__

On définit le centre d'inertie G du système S comme le barycentre des points du solide affectés de leur masse.

Cas d'un système discret:

\begin{equation}
\overrightarrow{OG} = \frac{1}{M}\sum\limits_{i=1}^{n} m_i \overrightarrow{OP_i}
\end{equation}
Cas continu:

\begin{equation}
\overrightarrow{OG} = \frac{1}{M}\iiint_{P \int S} \rho(P) \overrightarrow{OP} d \tau(P)
\end{equation}
````


>__Interprétation qualitative de la position du centre d'inertie__
>On remarquera que le centre d'inertie est décalé vers les zones plus massiques et que sa position respecte les symétries de masse du système.


# Description d'un mouvement

## Description d'un mouvement: généralités


__Champ de vitesse__
Le champ des vitesses d'un solide dans un référentiel R est la description de la vitesse de l'ensemble des points qui composent le solide. Il s'agit soit d'un ensemble discret de vecteurs vitesse affectés à chaque point, soit d'un champ vectoriel qui associe à chaque point P une vitesse correspondant à la vitesse du petit élément de matière autour du point P.



__Description générale__
Puisque tous les points du solides sont contraints à se déplacer ensemble, il vient que les mouvements des points du solide sont reliés les uns aux autres. Il suffit en réalité de connaître deux paramètres du mouvement global du solide pour pouvoir déterminer la vitesse de n'importe quel point du solide. Pour s'en convaincre - ce n'est pas une preuve - on peut remarquer que le mouvement d'un solide, à un instant t peut se décomposer en deux parties:

* un mouvement de translation globale du solide.
* un mouvement de rotation autour d'un axe (différent à chaque instant) appelé axe instantané de rotation.

Selon cette image, le mouvement d'un solide peut être décrit entièrement au moyen:

* De la vitesse en un point du solide.
* De la vitesse angulaire de rotation du solide autour de l'axe instantané de rotation. Celle-ci sera décrite par un vecteur rotation: $\overrightarrow{\Omega}$ contenant à la fois l'information sur la direction de l'axe et sur la vitesse angulaire.

En physique nous n'utiliserons que deux cas particuliers: la translation seule et la rotation autour d'un axe fixe.


````{admonition} Complément : Composition des vitesse (HP)
:class: hint, dropdown
Soit un solide donc le vecteur taux de rotation à un instant t est $\overrightarrow{\Omega}$ et donc la vitesse en un point A du solide est connue par: $\overrightarrow{v_{A/R}}(t)$. Alors la vitesse en tout point B du solide est connue et donnée par la relation:

\begin{equation}
\overrightarrow{v_{B/R}} = \overrightarrow{v_{A/R}} + \overrightarrow{\Omega} \wedge \overrightarrow{AB}
\end{equation}
Cette formule est valable quelque soit le mouvement du solide. Néanmoins, elle n'est pas à connaître et ne peut être appliquée directement en physique. Elle est par contre probablement à connaître et à savoir utiliser en SI. Les conséquences et définitions associées qui auront pu être vues en SI (centre instantanée de rotation, détermination graphique d'une vitesse... ) ne sont pas à connaître en physique. Par contre, les cas particuliers qui vont être présentés ensuite sont à connaître.
````

## Mouvement de translation

````{important} __Définition : Translation__

Un solide est en translation si pour tout point P du solide, la vitesse $\overrightarrow{v_{P/R}}$ est identique.

````

````{attention}

Une translation ne signifie pas que le solide va forcément tout droit (ne pas confondre mouvement de translation et mouvement rectiligne). Ainsi, un solide peut avoir un mouvement de translation circulaire: c'est le cas des nacelles de grande roue.

````

## Mouvement de rotation autour d'un axe fixe

````{important} __Définition : Rotation autour d'un axe fixe__

On peut définir le concept de rotation en rapport avec les composantes du torseur cinématique (cf SI). Pour nous, la description d'un solide en rotation autour d'un axe fixe est visuelle: il tourne sur lui-même.

````

````{important} __Fondamental : Champ de vitesse d'un solide en rotation__

Soit un solide en rotation autour d'un axe fixe, à un instant t, tous les points du solide ont la même vitesse angulaire $\omega(t)$. On peut alors définir un vecteur $\overrightarrow{\Omega}(t)$ appelé vecteur rotation du solide tel que pour tout point P du solide, la vitesse $\overrightarrow{v_{P/R}}$ s'écrit:

\begin{equation}
\overrightarrow{v_{P/R}} = \overrightarrow{\Omega} \wedge \overrightarrow{AP}
\end{equation}
où A est un point de l'axe de rotation.
````

>__Démonstration__
>Pour les différentes preuves de ce chapitre, nous choisissons soit le cas discret, soit le cas continu. Mais les deux démonstrations sont possibles et il faut savoir traiter chaque cas.
>
>La vitesse angulaire est la même pour tout point du solide (sinon il se déformerait). On se place dans un système de coordonnées cylindriques d'axe $Az$ l'axe de rotation et de centre A. Pour un point P à un distance $r$ de l'axe:
>
>\begin{align*}
\overrightarrow{\Omega} \wedge \overrightarrow{AP} &= \omega \overrightarrow{e_z} \wedge (r \overrightarrow{e_r} + z \overrightarrow{e_z}) \\
&= r \omega \overrightarrow{e_{\theta}} \\
&= \overrightarrow{v_{P/R}}
\end{align*}

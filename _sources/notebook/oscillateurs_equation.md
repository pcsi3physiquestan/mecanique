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
# Mise en équation

Le but de cette partie est de voir des exemples de mise en équation sur le cas simple du système masse-ressort.

Nous aborderons aussi quelques éléments de modélisation des systèmes atomiques.


## Oscillateur harmonique

````{admonition} Exercice 
:class: attention

__L'équation d'un oscillateur harmonique est un système dont l'évolution est régit par une équation différentielle de la forme:__

\begin{equation}
\frac{\rm{d^2}x}{\rm{dt^2}}(t) + \omega_0^2 x(t) = \omega_{0}^2 x_{eq}
\end{equation}
On considère un ressort de raideur k et de longueur $l_0$ accroché d'un côté à un point A de côte $x_A$ fixe et de l'autre à une masse m assimilable à un point matériel noté M. Le point M glisse sans frottements sur un axe Ox de sorte que le ressort reste horizontal. On note x la position du point M par rapport à un point O de référence. Pour cet exercice, le point O est confondu avec le point A.

1. Exprimer l'équation d'évolution de x(t).
1. En comparant l'équation d'un oscillateur LC en électrocinétique à celle obtenue ici. Proposer des grandeurs analogues entre k,m,L et C

````
````{dropdown} Ecart à l'équilibre

Par la suite, on fera en sorte que le second membre soit nul à l'équilibre (très important pour le cas des régimes forcés sinusoïdaux). Pour cela __on réalise le changement de variabme:__ $X = x - x_{eq}$. Cela revient à s'intéresser à l'écart à la position d'équilibre.

L'équation différentielle de vient alors $\frac{\rm{d^2}x}{\rm{dt^2}} + \omega_0^2 x = 0$
````

## Oscillateur amorti

````{admonition} Exercice 
:class: attention

Un oscillateur (linéaire) amorti possède comme équation différentielle:

\begin{equation}
\frac{\rm{d^2}x}{\rm{dt^2}}(t) + \frac{\omega_0}{Q} \frac{\rm{d}x}{\rm{dt}}(t)+\omega_0^2 x(t) = \omega_{0}^2 x_{eq}
\end{equation}
On reprend le cas précédent du système masse-ressort mais on suppose que le système est soumis à une force de frottement fluide de la forme $-\lambda \overrightarrow{v}$.

1. Déterminer la nouvelle équation qui régit l'évolution de x. Introduire les expressions de la pulsation propre et du facteur de qualité.
1. Déduire une analogie avec la résistance électrique d'un circuit RLC série.
1. Retrouver, en utilisant l'analogie précédente les valeurs de la pulsation propre, du facteur de qualité et du coefficient d'amortissement.

_Remarque: Comme précédemment, on réalisera un changement de variable $X = x - x_{eq}$ pour s'affranchir du second membre constant et étudier uniquement les variations autour de la position d'équilibre._

````

## Oscillateur forcé


Nous allons étudier deux manières de forcer un oscillateur: par une force extérieure sinusoïdale ou en faisant bouger l'autre extrémité du ressort.


````{admonition} Exercice 
:class: attention

On considère l'oscillateur amorti étudié précédemment. On applique à la masse m une force supplémentaire $\overrightarrow{F}(t) = F_m \cos \omega t \overrightarrow{e_x}$.

On pose X(t) l'écart à la position d'équilibre.

1. Etablir l'équation différentielle qui régit l'évolution de X(t)
1. En déduire la représentation complexe $\underline{X}$ de X(t). Commenter le comportement fréquentielle de la réponse en élongation.

````

````{admonition} Exercice 
:class: attention

On considère à nouveau l'oscillateur amorti mais sans la force ajotée précédemment. Par contre, on fait bouger le point A de sorte que $\overrightarrow{OA} = x_m\cos \omega t \overrightarrow{e_x}$.

On pose X(t) l'écart à la position d'équilibre lorsque $\overrightarrow{OA} = 0$.

1. Etablir l'équation différentielle qui régit l'évolution de X(t)
1. En déduire la représentation complexe $\underline{X}$ de X(t). Commenter le comportement fréquentielle de la réponse en élongation.

````
````{dropdown} Remarque

__Force de frottement fluides__
Il arrive que le fluide ne soit pas au repos dans le référentiel galiléen mais dans un référentiel mobile (cas de l'accéléromètre).Il faut alors faire attention au fait que la vitesse dans la force de frottements fluide doit être par rapport au fluide.
````

## Monde microscopique


__Modélisation en terme d'oscillateur__
De nombreux phénomènes microscopiques comme les liaisons intramoléculaires peuvent être modélisées par des oscillateurs.

* Force de rappel: Comme on l'a vu précédemment, tant que les vibrations atomiques sont faibles, on peut les assimiler à des oscillations autour d'une position d'équilibre stable. Dans le cadre des petits mouvements, la force est assimilable à une force de rappel.
* Cas forcé - Excitation sinusöïdale: Si l'on place la molécule dans un rayonnement électromagnétique de pulsation $\omega$, le champ électrique va exercer une force sinusoïdale sur le système forçant les oscillations.
* Amortissement fluide: les causes de l'amortissement fluide à l'échelle microscopique sont purement relativiste. En effet, on peut montrer en mécanique relativiste qu'une particule chargé accéléré émet un rayonnement et perd donc de l'énergie. Elle sera donc freinée (on parle de freinage par rayonnement). On peut modéliser cet effet par une force de frottement fluide.



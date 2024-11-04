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
# Activités - Mouvement circulaire

````{important} __Mouvement circulaire__

Un mouvement est dit __circulaire__ si le point M se déplace sur un cercle (ou une portion de cercle) fixe dans le référentiel R. On parle alors de __trajectoire circulaire__. C'est aussi un mouvement à 1 degré de liberté.
````

## Etude d'un mouvement circulaire
On suppose qu'on sait que la trajectoire est circulaire de rayon $R_0$ et de centre $O$. On note $M$ le point mobile et $m$ sa masse.

````{admonition}  __Exercice__
:class: attention
1. Quel type de coordonnée est-il préférable de choisir. Préciser alors l'expression du vecteur position, du vecteur vitesse et du vecteur accélération.
2. Que vaut l'accération normale? l'accélération tangentielle ? Que devient chaque terme dans le cas d'un mouvement uniforme?
3. Dans un mouvement circulaire dont l'axe de rotation est porté par le vecteur $\overrightarrow{e_z}$, on définit le __vecteur tournant__ $\overrightarrow{\Omega} = \dot \theta \overrightarrow{e_z}$. Exprimer le vecteur vitesse en fonction de $\overrightarrow{\Omega}$ et $\overrightarrow{OM}$ puis le vecteur accélération sous la forme de deux termes faisant intervenir $\overrightarrow{\Omega}, \overrightarrow{OM}$ et $\frac{{\rm d}\overrightarrow{OM}}{\rm dt}$. Donner une interprétation à ces deux termes.
4. Exprimer le moment cinétique du point M calculé au point O en fonction de $m, R_0$ et $\dot \theta$.
````


````{important} __A retenir__

* Si l'on sait que la trajectoire est circulaire et centre O, alors les coordonnées utiles sont les coordonnées cylindriques d'axe Oz perpendiculaire au plan du cercle.
* On a alors les relations:

\begin{align*}
\overrightarrow{OM} &= R_0 \overrightarrow{e_r}\\
\overrightarrow{v_{M/\mathfrak{R}}} &= R_0 \dot \theta \overrightarrow{e_{\theta}}\\
\overrightarrow{a_{M/\mathfrak{R}}} &= \underbrace{- R_0 \dot \theta ^2 \overrightarrow{e_r}}_{normale=radiale} + \underbrace{R_0 \ddot \theta \overrightarrow{e_{\theta}}}_{tangentielle=orthoradiale}
\end{align*}
* Dans le cas uniforme, l'accélération tangentielle/orthoradiale est nulle.
* On peut exprimer la vitesse et l'accélération en fonction du vecteur tournant:
\begin{align}
    \overrightarrow{v_{M/R}} &= \overrightarrow{\Omega} \wedge \overrightarrow{OM}\\
    \overrightarrow{a_{M/R}} &= \underbrace{\frac{d \overrightarrow{\Omega}}{dt} \wedge \overrightarrow{OM}}_{normale=radiale} + \underbrace{\overrightarrow{\Omega} \wedge \overrightarrow{v}}_{tangentielle=orthoradiale}
\end{align}
````

## Aller plus loin - Equation cartésienne d'un cercle

````{admonition}  __Exercice__
:class: attention

Il peut arriver qu'on ne sache pas à l'avance que la trajectoire est un cercle et qu'on ait choisi de travailler coordonnées cartésiennes. Il est important de savoir reconnaître une trajectoire circulaire par son cartésienne et par son équation paramétrique dans le plan.

1. Pour rappel, un cercle de centre $M_0(x_0, y_0)$ et rayon $R$ correspond à l'ensemble des points M(x,y) tels que $M_0 M^2 = R^2$.
    1. Calculer la distance $M_0 M$. En déduire l'__équation cartésienne__ d'un cercle.
2. On suppose maintenant que le cercle est de centre $O(0,0)$ et que le mobile se déplace sur le cercle de manière uniforme à une vitesse angulaire $\omega$.
    1. Que valent $r(t)$ et $\theta(t)$ en coordonnées polaires de centre $O$? On prendra $\theta(t=0)=0$.
    2. En déduire $x(t)$ et $y(t)$ en fonction de $R, \omega$ et du temps.
    3. Que deviennent $x(t)$ et $y(t)$ si le centre du cercle est maintenant $M_0(x_0, y_0)$.
````

````{important} __A retenir__

On retiendra les deux formes d'équations correspondant à une trajectoire circulaire de manière à pouvoir les reconnaître et en extraire les caractéristiques (centre et rayon):
* __Equation cartésienne__ : $(x - x_0)^2 + (y - y_0)^2 = R^2$
* __Equation paramétrique cartésienne__ (cas uniforme): $x(t) = R \cos \omega t + x_0; y(t) = R \sin _omega t + y_0$
Dans les deux cas, le rayons est $R$ et le centre $(x_0, y_0)$.
````


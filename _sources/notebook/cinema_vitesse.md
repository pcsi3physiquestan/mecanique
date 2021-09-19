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
# Vecteur vitesse

## Vecteur vitesse: Définition

````{admonition} Définition : Vecteur vitesse
:class: tip

Soit O un point fixe du référentiel R et M un point mobile. La vitesse du point M dans le référentiel R est définit comme la dérivée temporelle du vecteur position dans le référentiel R.

\begin{equation}
\overrightarrow{V_{M/R} = {(\frac{d \overrightarrow{OM}}{dt})}_{R}}
\end{equation}
````

````{admonition} Attention : 
:class: note

Il est important de préciser le référentiel d'étude: il définit les vecteurs qu'on considère fixe. Dans un premier temps, il n'y aura qu'un seul référentiel.

````

## Expression du vecteur vitesse

````{admonition} Fondamental : Expressions du vecteur vitesse
:class: attention

Le vecteur vitesse s'exprime.

En coordonnées cartésiennes:

\begin{equation}
\overrightarrow{v_{M/\mathfrak{R}}} = \dot x \overrightarrow{e_x} + \dot y \overrightarrow{e_y} + \dot z \overrightarrow{e_z}
\end{equation}
En coordonnées cyindriques:

\begin{equation}
\overrightarrow{v_{M/\mathfrak{R}}} = \dot r \overrightarrow{e_r} + r \dot \theta \overrightarrow{e_\theta} + \dot z \overrightarrow{e_z}
\end{equation}
En coordonnées spheriques:

\begin{equation}
\overrightarrow{v_{M/\mathfrak{R}}} = \dot r \overrightarrow{e_r} + r \dot \theta \overrightarrow{e_\theta} + r \sin{\theta} \dot \varphi \overrightarrow{e_\varphi}
\end{equation}
````


__Démonstration__
On peut démontrer ces expressions de deux manières: soit en dérivant le vecteur position (il faut tenir compte des dérivées des vecteurs des bases locales, nous le verrons en traitant le cas du vecteur accélération) ou en utilisant l'expression du vecteur déplacement élémentaire. Nous présentons ce dernier cas. On rappelle que le déplacement élémentaire s'exprime (respectivement en coordonnées cartésiennes, cylindriques, sphériques):

\begin{equation}
\overrightarrow{dOM} = dx \overrightarrow{e_x} + dy \overrightarrow{e_y} + dz \overrightarrow{e_z}
\end{equation}
\begin{equation}
\overrightarrow{dOM} = dr \overrightarrow{e_r} + r d \theta \overrightarrow{e_{\theta}} + dz \overrightarrow{e_z}
\end{equation}
\begin{equation}
\overrightarrow{dOM} = dr \overrightarrow{e_r} + r d \theta \overrightarrow{e_{\theta}} + r \sin \theta d\varphi \overrightarrow{e_{\varphi}}
\end{equation}
Ici, on rapport le déplacement élémentaire à la variation temporelle dt pendant lequel le déplacement se fait, ce qui revient à rapporter chaque différentielle ($dx, dy, d\theta, dr...$) par dt, c'est-à-dire les remplacer par les dérivées. On obtient bien les expressions données.


````{admonition} Attention : 
:class: note

Dans le cadre d'une démonstration des expressions des vecteurs vitesses, il __faut redémontrer l'expression des déplacements élémentaires.__

````


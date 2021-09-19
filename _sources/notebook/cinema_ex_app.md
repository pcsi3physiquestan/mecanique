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
# Exercices d'application

Ces exercices d'application directe sont à faire à la suite du cours pour vérifier votre compréhension des méthodes. Vous pourrez confronter votre travail avec celui de vos camarades et poser des questions sur cet exercice en classe mais il ne sera pas donné de correction complète.


## Relations dans l'ellipse

````{admonition} Exercice 
:class: attention

Démontrer les relations suivantes dans l'ellipse:

\begin{align*}
a = \frac{p}{1 - e^{2}}\\
c^{2} = a^{2} - b^{2}\\
e = c / a
\end{align*}

````
## Chute d'une règle

````{admonition} Exercice 
:class: attention

Une barre rectiligne AB de longueur fixe $2b$ se déplace dans le référentiel R repéré par $(O, \overrightarrow{u_x}x,\overrightarrow{u_y},\overrightarrow{u_z})$ de telle sorte que:

* son extrémité A se trouve sur le demi-axe positif Oz.
* son extrémité B décrit le demi-cercle de plan (xOy) de centre $I(0,b,0)$ et de rayon $b$, à la vitesse angulaire (par rapport à I) $\omega$ constante et positive. A l'instant $t=0$, B se trouve en O.

On note $\phi$ l'angle $(\overrightarrow{IO}, \overrightarrow{IB})$.

```{figure} ./images/td_regle.jpg
:name: fig_225
:align: center

```

```{figure} ./images/td_regl_e2.jpg
:name: fig_226
:align: center

```

1. Déterminer la durée T du mouvement 
1. Déterminer une relation simple entre $\phi$ et $\theta$. 
1. Etablir les expressions en fonction du temps $t$ des coordonnées polaires $r$ et $\theta$ de B (cf. Figure).
1. Déterminer l'angle $\alpha=(\overrightarrow{AO}, \overrightarrow{AB})$ en fonction de $\omega$ et $t$.
1. Calculer les coordonnées cylindriques $(R, \Theta)$ puis cartésiennes $X,Y$ et $Z$ du milieu J de la barre. 
1. Déterminer la vitesse $\overrightarrow{v_J}$ et l'accélération $\overrightarrow{a_J}$ de J, ainsi que leur normes.

````
````{dropdown}
 

```{admonition} Fondamental : Eléments de réponse (sans justification)
:class: attention

$\theta(t) = \frac{\omega}{2}t$ et $r(t) = b \sqrt{2 (1 - \cos \omega t)}$et $z(t) = 2b^2 (1 + \cos \omega t)$
```
````

## Rotation de la Terre

````{admonition} Exercice 
:class: attention

On assimile la Terre à une sphère de rayon $R_T = 6400 \rm{km}$ et tournant sur son axe en 24h à vitesse angulaire constante $\omega$. On considère un point M situé à une colatitude $\theta$. L'axe (Oz) de référence étant l'axe de révolution de la Terre.

1. Déterminer $\omega$.
1. Déterminer la position, la vitesse et l'accélération de M en fonction de $\omega, R_T$ et t. On prendra soin de définir correctement le repère de projection. 
````

````{dropdown}
 

```{admonition} Fondamental : Eléments de réponse (sans justification)
:class: attention

$\omega = 0.72 \times 10^{-4} rad.s^{-1}$
```
````


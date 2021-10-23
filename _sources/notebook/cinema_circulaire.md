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
# Cas du mouvement circulaire

## Mouvement circulaire: Généralités

_On rappelle qu'un mouvement circulaire est un mouvement dont la trajectoire est portée par un cercle fixe dans le référentiel $\mathfrak{R}$ considéré. On notera $R_0$ le rayon du cercle._


````{important} __Fondamental : Système de coordonnées et expressions__

Les coordonnées utiles pour un tel mouvement sont les coordonnées cylindriques d'axe Oz perpendiculaire au plan du cercle. On a alors les relations:

\begin{align*}
\overrightarrow{OM} &= r \overrightarrow{e_r}\\
\overrightarrow{v_{M/\mathfrak{R}}} &= r \dot \theta \overrightarrow{e_{\theta}}\\
\overrightarrow{a_{M/\mathfrak{R}}} &= - r \dot \theta ^2 \overrightarrow{e_r} + r \ddot \theta \overrightarrow{e_{\theta}}
\end{align*}
````
````{important} __Fondamental : Accélération tangentielle et normale__

Remarquons que la direction radiale $e_{r}$ est  toujours perpendiculaire au mouvement et la direction orthoradiale $e_{\theta}$ est  toujours tangente au mouvement. Il vient que:

* L'accélération tangentielle vaut: $\overrightarrow{a_T} = R_0 \ddot \theta  \overrightarrow{e_{\theta}} = \frac{dv}{dt}$ où $v$ est la composante de l'accélération sur $e_{\theta}$.
* L'accélération normale vaut: $\overrightarrow{a_N} = -R_0 \dot \theta^2 \overrightarrow{e_r} = - \frac{v^2}{R} \overrightarrow{e_r}$
````

````{important} __Définition : Vecteur tournant__

On définit le vecteur tournant comme: $\overrightarrow{\Omega} = \omega \overrightarrow{e_z}$

````

````{important} __Fondamental : Expressions en fonction du vecteur tournant.__

\begin{align}
    \overrightarrow{v_{M/R}} &= \overrightarrow{\Omega} \wedge \overrightarrow{OM}\\
    \overrightarrow{a_{M/R}} &= \frac{d \overrightarrow{\Omega}}{dt} \wedge \overrightarrow{OM} + \overrightarrow{\Omega} \wedge \overrightarrow{v}
\end{align}
__Vous devez savoir prouver ces formules.__
````

## Cas d'un mouvement circulaire uniforme

````{important} __Fondamental : Expressions__

Dans le cas d'un mouvement circulaire uniforme, il vient que l'accélération est purement centripète: elle est bien orthogonale au mouvement. Son expression est alors: $\overrightarrow{a_{M/\mathfrak{R}}} = - \frac{v^2}{R} \overrightarrow{e_r}$
````

## Exemple: Cas d'un satellite géostationnaire.

````{admonition} Exercice 
:class: attention

Un satellite géostationnaire est un satellite en orbite circulaire autour de la terre à une altitude $h=r-R_T$ où $R_T$ est le rayon de la Terre (r est le rayon de l'orbite). L'orbite est équatoriale et il reste fixe par rapport à un point de la Terre. Il est soumis à une accélération dans le référentiel géocentrique:

\begin{equation}
\overrightarrow{a} = - g_0 {(\frac{R_T}{r})}^2 \overrightarrow{e_r}
\end{equation}
Calculer r avec $g_0 = 9,8 \rm{m.s^{-1}}$ et $R_T = 6400 \rm{km}$.
````

````{dropdown} Résolution

>On peut utilise directement le fait que l'accélération radiale s'écrit $- r \dot \theta^2 \overrightarrow{e_r}$
>
>Un satellite géostationnaire doit tourner autour de la terre en 24h, soit une vitesse angulaire $\dot \theta = \frac{2 \pi}{T_0}$ avec $T_0 = 24 \rm{h} = 86400 \rm{s}$.
>
>Il vient:
>
>\begin{align*}
r &= {\left(\frac{g_0 R_T^2T_0^2}{4 \pi^2 }\right)}^{\left(1/3\right)}\\
&= 42 \times 10^3 \rm{km}
\end{align*}
````


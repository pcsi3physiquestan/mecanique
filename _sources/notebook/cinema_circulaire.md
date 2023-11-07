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


````{important} __Système de coordonnées et expressions__

Les coordonnées utiles pour un tel mouvement sont les coordonnées cylindriques d'axe Oz perpendiculaire au plan du cercle. On a alors les relations:

\begin{align*}
\overrightarrow{OM} &= R_0 \overrightarrow{e_r}\\
\overrightarrow{v_{M/\mathfrak{R}}} &= R_0 \dot \theta \overrightarrow{e_{\theta}}\\
\overrightarrow{a_{M/\mathfrak{R}}} &= - R_0 \dot \theta ^2 \overrightarrow{e_r} + R_0 \ddot \theta \overrightarrow{e_{\theta}}
\end{align*}
````
````{important} __Accélération tangentielle et normale__

Remarquons que la direction radiale $e_{r}$ est  toujours perpendiculaire au mouvement et la direction orthoradiale $e_{\theta}$ est  toujours tangente au mouvement. Il vient que:

* L'accélération tangentielle vaut: $\overrightarrow{a_T} = R_0 \ddot \theta  \overrightarrow{e_{\theta}} = \frac{dv}{dt} \overrightarrow{e_\theta}$ où $v$ est la __composante__ de l'accélération sur $e_{\theta}$.
* L'accélération normale vaut: $\overrightarrow{a_N} = -R_0 \dot \theta^2 \overrightarrow{e_r} = - \frac{v^2}{R_0} \overrightarrow{e_r}$
````

````{important} __Vecteur tournant__

On définit le vecteur tournant comme: $\overrightarrow{\Omega} = \omega \overrightarrow{e_z}$

\begin{align}
    \overrightarrow{v_{M/R}} &= \overrightarrow{\Omega} \wedge \overrightarrow{OM}\\
    \overrightarrow{a_{M/R}} &= \frac{d \overrightarrow{\Omega}}{dt} \wedge \overrightarrow{OM} + \overrightarrow{\Omega} \wedge \overrightarrow{v}
\end{align}
__Vous devez savoir prouver ces formules.__
````

## Cas d'un mouvement circulaire uniforme

````{important} __Expressions__

Dans le cas d'un mouvement circulaire uniforme, il vient que l'accélération est purement centripète: elle est bien orthogonale au mouvement. Son expression est alors: $\overrightarrow{a_{M/\mathfrak{R}}} = - \frac{v^2}{R} \overrightarrow{e_r}$
````


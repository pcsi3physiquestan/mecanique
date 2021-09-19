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
# Mouvement uniformément accéléré


Nous allons ici étudié le cas simple d'un mouvement uniformément accéléré. Ses caractéristiques sont à savoir redémontrer.


````{admonition} Exercice 
:class: attention

On considère un point M donc le vecteur accélération est constant. Déterminer l'équation horaire du point M pour une vitesse initiale $\overrightarrow{v_0}$ et une position initiale $M_0$ à $t = 0$.

````
````{dropdown}
 


La direction du vecteur accélération étant constante, on va particulariser cet axe en le choisissant comme axe Oz. On pose le point O confondu avec $M_0$ et on choisit un système de coordonnées cartésiennes dont l'axe Ox est tel que le vecteur vitesse initiale soit plan xOz. On peut donc écrire  que:

\begin{align*}
\overrightarrow{a} &= a_0 \overrightarrow{e_z}\\
\overrightarrow{v} &= v_{0x} \overrightarrow{e_x} + v_{0z} \overrightarrow{e_z}
\end{align*}

Par projection, on trouve que:

\begin{align*}
\frac{\rm{d}v_x}{\rm{dt}} &= 0\\
\frac{\rm{d}v_y}{\rm{dt}} &= 0\\
\frac{\rm{d}v_z}{\rm{dt}} &= a_0
\end{align*}
soit par intégration:

\begin{align*}
v_x &= v_{0x} \Longrightarrow x(t) = v_{0x} t + x_0\\
v_x &= 0 \Longrightarrow x(t) = y_0\\
v_x &= v_{0z} + a_0t \Longrightarrow x(t) = \frac{a_0}{2} t^2 + v_{0z} t + z_0
\end{align*}
Comme nous le verrons, on peut montrer qu'une telle équation est celle d'une parabole.

````


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
# Entrainement

````{admonition} Disques couplés 
:class: attention

On considère deux disques horizontaux tournant autour d'un axe vertical $\Delta$ en leur centre. Les disques sont homogènes, de moment d'inertie par rapport à $\Delta$, $J_1$ et $J_2=J_1$ et la liaison avec l'axe est parfaite. On repère leur rotation autour de l'axe par deux angles $\theta_1$ et $\theta_2$.

On relie un fil de torsion de constante C d'un côté au bâti et de l'autre eu premier disque puis un deuxième fil de torsion de même constante C d'un côté au premier disque et de l'autre au second disque et enfin un dernier fil de torsion de même constante C d'un côté au deuxième disque et de l'autre au bâti.

1. Déterminer les deux équations différentielles couplées qui régissent les évolutions de $\theta_1$ et $\theta_2$.
1. On cherche des configurations pour lesquelles les deux disques oscilles de manièrent sinusoïdales à la même pulsation $\omega$. Montrer qu'il n'existe que deux pulsations possibles  et  dont on déterminera les expressions. Décrire le mouvement global pour chaque pulsation.

````
_Point utile pour cet exercice_
* _$\Longrightarrow$ Bilan des actions mécanique._
* _$\Longrightarrow$ Théorème du moment cinétique._
* _$\Longrightarrow$ Moment de torsion._
* _$\Longrightarrow$ Oscillateur forcée._



````{topic} Eléments de réponse (sans justification)

\begin{align*}
J_1 \ddot \theta_1 =  - C \theta_1 + C \left(\theta_2 - \theta_1\right)\\
J_2 \ddot \theta_2 =  - C \theta_2 + C \left(\theta_1 - \theta_2\right)\\
\end{align*}
\begin{align*}
\omega &= \sqrt{\frac{3C}{J_1}}\\
\omega &= \sqrt{\frac{C}{J_1}}
\end{align*}
````

````{admonition} Entraînement par frottements 
:class: attention

On considère un système constitué de deux disques en rotation autour d'un axe $\Delta$ (les moments d'inertie des deux disques par rapport à l'axe sont notés $J_1$ et $J_2$) au moyen d'une liaison pivot parfaite. A l'instant initial, les deux disques sont éloignés et sans contact et le premier tourne avec une vitesse angulaire $\omega_0$ et le second est immobile. On approche doucement les deux disques jusqu'à ce qu'ils soient en contact.

1. Déterminer la vitesse angulaire de l'ensemble des deux disques à la fin de la manipulation. Ce résultat dépend-t-il de la nature des frottements entre les deux disques?
1. Faire un bilan d'énergie mécanique pour chaque disque séparément puis pour l'ensemble des deux disques. Commenter les résultats.
````
_Point utile pour cet exercice_
* _$\Longrightarrow$ Solide déformable._
* _$\Longrightarrow$ Conservation du moment cinétique._

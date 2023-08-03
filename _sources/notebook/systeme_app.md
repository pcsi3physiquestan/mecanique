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
# Application

## Solides en rotation indéformables
````{admonition} Rotation d'un moteur 
:class: attention

On considère un solide (rotor) de forme cylindrique de rayon R et de masse M uniformément répartie. Il est en liaison pivot avec un axe fixe (stator) et on suppose cette liaison parfaite. On suppose que l'axe Oz de la liaison pivot est horizontal. On utilise un système de coordonnées cylindriques d'axe Oz et l'angle $\theta$ associé à un point du cylindre permet de repérer la rotation de ce dernier.

Les propriétés magnétiques du rotor (non étudié en détail ici) fait qu'un champ magnétique extérieur au système impose une action modélisable par un __couple__ de moment $\overrightarrow{\Gamma} = \Gamma_m \overrightarrow{e_z}$ et que le cylindre est plongé dans un fluide dont l'action est aussi modélisable par un __couple__ de moment $\overrightarrow{\Gamma_f} = - K \dot \theta \overrightarrow{e}_z$

1. Faire un bilan des actions mécaniques sur le cylindre.
1. Etablir l'équation d'évolution de la vitesse angulaire $\omega$ du cylindre. En déduire que le système tend vers une vitesse de rotation limite qu'on déterminera.
1. Etablir $\omega(t)$ en supposant que le rotor est initialement immobile.
1. *On se place dans le régime stationnaire où $\omega = cste$, déduire du mouvement du centre d'inertie la force résultant exercée par la liaison pivot.
````
_Point utile pour cet exercice_
* _$\Longrightarrow$ Bilan des actions mécanique._
* _$\Longrightarrow$ Théorème du moment cinétique._
* _$\Longrightarrow$ Moment d'inertie._
* _$\Longrightarrow$ Détermination d'une action._

__Les deux exercices suivants sont des classiques à maitriser.__
````{admonition} Pendule pesant 
:class: attention

On considère une tige de longueur $L$ et de masse $M$ attaché à une extrémité à un bati par une liaison pivot parfaite d'axe Oz horizontal (on donne le moment de la tige par rapport à Oz: $J_{Oz} = \frac{M L^2}{3}$), l'autre extrémité étant laissé libre. Une masse ponctuelle $m$ est accrochée à la tige à une distance $l$ de l'axe Oz. Déterminer la période des petites oscillations en fonction de la longueur $l$.

````

````{admonition} Pendule de torsion 
:class: attention

On considère une tige de longueur $L$ et de masse $M$ uniformément répartie. Elle est attaché en son milieu à un fil de torsion de constante $C$ dont l'autre extrémité est attachée à un bati. On suppose que la tige reste toujours horizontale et qu'elle ne fait que tourner autour de l'axe du fil de torsion noté $Oz$ (vers le haut).

On repère l'angle que fait la tige avec un axe horizontal de référence et $\theta = 0$ lorsque le fil de torsion est au repos.

Montrer qu'on a un oscillateur harmonique et déterminer sa pulsation propre en notant J le moment d'inertie de la tige suivant l'axe Oz.
````
_Point utile pour cet exercice_
* _$\Longrightarrow$ Bilan des actions mécanique._
* _$\Longrightarrow$ Théorème du moment cinétique._
* _$\Longrightarrow$ Moment de torsion._


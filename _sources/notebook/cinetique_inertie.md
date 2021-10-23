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
# Point matériel et inertie

````{admonition} Définition : Point matériel
:class: tip

Un point matériel est une modélisation idéalisée d'un objet ponctuel matériel, c'est-à-dire d'une portion infinitésimale de matière.

Un point matériel ne nécessite que la données de 3 coordonnées de repérage dans l'espace et de masse (cf. suite).

````


__Utilisation du point matériel__
Le point matériel possède trois utilité:

* toutes les lois fondamentales de la mécanique concerne le système "point matériel"
* il sert à la description d'un système mécanique qui sera constitué d'un ensemble de points matériels (cf. suite).
* il permet la modélisation simplifiée d'un système mécanique qu'on va __assimilé__ à un point matériel seul. Il s'agit d'une modélisation qui n'est valable que si la rotation ou la déformation du système mécanique n'a pas d'influence sur le mouvement global du système mécanique (ou n'existe pas).


````{admonition} Modélisation valable et non valable par un point matériel seul.
:class: attention

Un ballon lancé dans l'air peut être assimilé à un point matériel si l'influence de l'air (frottements) est négligées où si la rotation du ballon est relativement faible. Son mouvement sera identique au point considérée. Nous verrons par la suite que le point auquel on assimile le ballon est son centre d'inertie.

Un ballon qui roule sur un plan incliné ne peut être assimilé à un point. En effet, la nature du contact entre le ballon et le plan (roulement sans glissement ou non... ) a une influence essentielle sur le mouvement du ballon. On doit tenir compte de la rotation du ballon.

````

````{admonition} Définition : Masse intertielle.
:class: tip

La capacité que possède un objet matériel à résister à toute variation de mouvement est appelé __inertie__.

Pour un point matériel, la propriété d'inertie est représentée par une grandeur scalaire positive appelée masse inertielle  dans l'unité est le kg. Plus la masse inertielle d'un objet est grande, plus il est difficile de modifier sa vitesse.

La masse est inertielle est indépendante du temps et du référentiel considéré: il s'agit d'une caractéristique propre au point matériel. Pour un système fermé (n'échangeant pas de matière), elle est conservée.

````


Par la suite, on parlera de "masse" sans préciser qu'il s'agit de masse inertielle.


````{admonition} Exemple 
:class: attention

Un joueur de ping-pong peut renvoyer sans problème une balle de ping-pong avec sa raquette mais ne pourra renvoyer une boule de billard, même si les deux ont la même vitesse.

De même, il est plus facile de mettre en mouvement ou d'arrêter le mouvement d'une poussette avec ses simple bras que celui d'une voiture.

Dans les deux cas, la voiture et la boule de billard résistent plus à une variation de leur vitesse (norme ou orientation): le paramètre qui caractérise cette différence est leur masse.

````


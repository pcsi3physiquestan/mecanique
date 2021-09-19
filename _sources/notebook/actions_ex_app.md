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


## Expérience de Milikan

````{admonition} Exercice 
:class: attention

On place des goutellettes d'huile chargée de masse m et de charge q entre deux plaques et on maintient les deux plaques distantes d'une distance d à une différence de potentiel U orienté de la plaque du haut vers la plaque vers le bas. Il reigne alors entre les plaque un chaque électrique $\overrightarrow{E} = \frac{U}{d}\overrightarrow{e_z}$ avec $\overrightarrow{e_z}$ un vecteur unitaire vertical orienté vers le haut. On suppose le champ de pesanteur uniforme.

Exprimer la charge q en fonction des autres grandeurs introduites et de l'intensité du champ de pesanteur.

````

## Mouvement d'une planète

````{admonition} Exercice 
:class: attention

Le mouvement d'une planète du système solaire, dans les hypothèses des lois de Kepler est une ellipse dont l'un des foyers des le Soleil. Dans ce cadre d'hypothèses, la seule action subit par la planète est l'action gravitationnelle exercée par le Soleil. La planète et le Soleil sont assimilés à des points matériels.

1. Représenter qualitativement la trajectoire de la planète dans le référentiel héliocentrique. En quel point de l'ellipse la force gravitationnelle est-elle la plus forte ? la plus faible ?
1. Représenter deux points où la planète est accéléré, deux points où la planète est ralentie et deux points où l'accélération est normale à la vitesse. Que se passe-t-il en ces points ?
1. Que vaut le moment de la force gravitationnelle calculée au Soleil ? On remarquera que malgré sa valeur, le mouvement de rotation de la planète autour du Soleil évolue.

````
````{dropdown}
 


__Éléments de réponse (sans justification)__
1. La force est (en norme) la plus forte au point le plus proche du Soleil (appelé périhélie) et elle est la plus faible au point le plus éloigné du Soleil (appelé aphélie).
1. Accéléré quand l'angle entre la vitesse et l'accélération est aigu, ralenti quand il est obtu. L'accélération est normale à la vitesse à l'aphélie et au pérhélie : en ces points, la vitesse atteint un extremum.
1. Il est nul (vecteur $\overrightarrow{SP}$ parallèle à la force gravitationnelle).


```{dropdown} Remarque

__Conservation du moment cinétique__
Comme on le verra par la suite, la nullité du moment résultant des forces extérieures conduit à la conservation du moment cinétique. Cette propriété aura de nombreuse conséquences sur l'étude du mouvement des planètes.

```
````



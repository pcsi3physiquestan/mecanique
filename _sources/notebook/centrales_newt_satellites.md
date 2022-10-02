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
# Activités : Mouvement des satellites

On s'intéresse maintenant au mouvement des satellites. On s'intéressera dans le cours uniquement au mouvement des satellites autour de la Terre. Cette étude peut être généralisée. On notera $M_T$ la masse de la Terre et $m$ la masse du satellite. On veut s'intéresser à quelques données utiles lors de l'étude du mouvement des satellites.


## Mouvement des satellites: Définitions


__Position du problème__
Le mouvement des satellites se fait sur des distances très grandes (ex: l'altitude d'un satellite géostationnaire est de 36000km), pour économiser le carburant (économie d'énergie ET de poids), les ingénieurs tirent en général partie des interactions gravitationnelles. En effet, on a vu que la vitesse initiale pour une distance donnée définissait l'énergie mécanique du système. Celle-ci permet de prévoir les altitudes maximale et minimale atteintes par le satellite. On peut donc, en allumant de manière très ponctuelle les moteurs du satellite, lui faire parcourir des très grandes distances: on réalise une économie de carburant. D'une manière générale, le mouvement des satellites correspond à la modification ponctuelle de la vitesse.

```{figure} ./images/meca_transfert_sat.jpg
:name: fig_261
:align: center

```

En général, la mise en orbite "haute" d'un satellite se fait de la manière suivante: un lanceur place le satellite sur une orbite circulaire "basse" proche de la surface de la Terre. Ensuite, un moteur transfert le satellite sur une orbite elliptique dont le périgée (point de l'orbite le plus proche) est sur l'orbite basse (point de départ) et l'apogée (point de l'orbite le plus éloigné) est sur l'orbite haute finale. Quand le satellite arrive à l'apogée, un moteur dit d'apogée modifie à nouveau la vitesse du satellite pour le placer sur l'orbite haute.

On définit alors certaines grandeurs utiles pour la réflexion.


````{important} __Vitesses cosmiques__

On définit la première vitesse cosmique par la vitesse qu'aurait un satellite en orbite basse, c'est-à-dire telle que $h \ll R_T$.

On définit la seconde vitesse cosmique comme la vitesse minimale à transmettre à une satellite en orbite basse pour qu'il se libère de l'attraction terrestre, c'est-à-dire qu'il puisse atteindre l'infini.

````

````{important} __Orbite géostationnaire__

L'orbite géostationnaire correspond à une orbite où le satellite tourne avec la même période que la Terre sur elle-même et est fixe par rapport à un point du globe.

````

## Etude du mouvement des satellites

````{admonition} Exercice 
:class: attention

1. Exprimer la première vitesse cosmique $v_1$ en fonction de $G, M_T$ et $R_T$
1. Exprimer la seconde vitesse cosmique $v_2$ en fonction de $G, M_T$ et $R_T$
1. Préciser l'intérêt de connaître les deux vitesses cosmiques.
1. Montrer que l'orbite d'un satellite géostationnaire est nécessairement contenue dans le plan équatorial.
1. Déterminer le rayon de l'orbite géostationnaire.

On distingue différents types de satellites en fonction des __altitudes__ de leur orbite:

* Orbite polaire: en orbite basse entre 300 et 1000km avec une inclinaison proche de 90 degrés. Ce sont des orbites qui permettent de passee toujours à la même heure solaire au dessu d'un lieu donné ce qui en fait une orbite idéale pour l'observation de la Terre.
* Orbite basse: entre 250km et 2000km. Ce sont principalement des satellites scientifiques (comme Hubble)
* Orbite moyenne: jusqu'à 20000km On y trouve notamment les satellites GPS (à 20000km) et pour Internet (à 8063km).
* Orbite haute: jusqu'à l'orbite géostationnaire. On y trouve principalement des satellites de communication russes. Note: ces trajetoires ne sont pas toujours circulaire et c'est l'apogée qui se trouve à ces altitudes

6. Déterminer les vitesses limites des satellites en orbite basse circulaire et les durées limites de ces orbites.
1. Déterminer la vitesses des satellites GPS et Internet ainsi que la durée de leur orbite (ce sont des trajectoires circulaires).

````

## Satellite géostationnaire

````{admonition} Exercice 
:class: attention

On souhaite transférer un satellite depuis une orbite circulaire rasante de rayon $R_T$ autour de la Terre sur son orbite géostationnaire de rayon $R_G$. On fera l'étude dans le référentiel géocentrique dans lequel la Terre tourne sur elle-même à la vitesse angulaire $\Omega$. On suppose que le satellite a une masse de $m=1,5\rm{t}$ donc petite devant la masse de la Terre. On note O le centre de la Terre.

Le transfert s'effectue de son orbite basse géostationnaire s'effectue de la manière suivante: on communique au satellite une brusque variation de vitesse en un point P de sa trajectoire en éjectant des gaz pendant un intervalle de temps très court dans le sens opposé à la vitesse du satellite. Il suit alors une orbite elliptique et lorsque sa trajectoire croise la droite OP au point A, on lui communique un supplément de vitesse pour le stabiliser sur l'orbite géostationnaire.

1. En utilisant la conservation de l'énergie mécanique sur la trajectoire elliptique, établir l'expression de l'énergie mécanique en fonction de $G,M_T ,m$ et $a$ le demi grand axe de l'ellipse.
1. Donner la valeur de l'énergie mécanique sur l'ellipse de transfert.
1. Etablir l'expression de la vitesse du satellite sur la trajectoire elliptique en fonction de $R_G, R_T, r, G$ et $M_T$.
1. Donner la valeur de vitesse qu'il faut imposer en P. Déterminer la variation de l'énergie mécanique en P.
1. Donner la valeur de vitesse qu'il faut imposer en A. Déterminer la variation de l'énergie mécanique en A.
1. Déterminer la durée du mouvement.
````


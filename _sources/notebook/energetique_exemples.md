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
# Exemples

## Toboggan circulaire

````{admonition} Exercice 
:class: attention

On considère une masse m ponctuelle qui se déplace sans frottements sur une demie-sphère de centre O et de rayon R. Elle est soumise à un champ de pesanteur g et est lâchée du sommet avec une vitesse très faible vers la droite. La masse décolle-t-elle de la sphère? On utilisera deux méthodes différentes (utilisant respectivement le TEC puis le TEM) pour répondre à la question.

````
````{dropdown}
 

>__Condition de décollement et paramétrage__
>
>La condition de décollement est on le rappelle l'annulation de la composante normale de la réaction du toboggan sur la masse. Remarquons déjà que le TEC/TEM n'apporterons pas d'information sur cette composante. Elle est en effet perpendiculaire au moins (donc elle ne travaille pas) et dirigée vers le centre du cercle formé par le toboggan (donc de moment nul en ce centre). Il faut donc commencer par appliquer un PFD au point matériel M dans le référentiel du toboggan supposé galiléen.
>
>On utilise un système de coordonnées cylindriques d'axe Oz perpendiculaire au plan du mouvement (le mouvement est plan puisque les deux forces sont dans un même plan et la vitesse initiale dans le même plan) où O est le centre de la sphère. La vitesse s'écrit alors $\overrightarrow{v} = R \dot \theta \overrightarrow{e_\theta}$ et l'accélération $\overrightarrow{a} = - R \dot \theta^2 \overrightarrow{e_r} + R \ddot \theta \overrightarrow{e_\theta}$.
>
>Les deux forces qui s'appliquent sont le poids $\overrightarrow{P} = -mg \cos \theta \overrightarrow{e_r} + mg \sin \theta \overrightarrow{e_\theta}$ et la réaction du toboggan supposée normale par l'absence des frottements $\overrightarrow{R} = R \overrightarrow{e_r}$. La condition de contact s'écrit $R > 0$. L'annulation coïncidera avec le décollage.
>
>On applique donc le PFD.
>

````


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
# Activité : Solide en rotation autour d'un axe fixe

Il s'agit ici de reprendre certaines idées générales et de préciser le cas d'étude des systèmes __déformables__ en rotation.


## Solide indéformable

### Rappel

On rappelle quelques éléments utiles:

* le moment cinétique du solide sur l'axe s'écrit comme le produit de la vitesse angulaire autour de l'axe par le moment d'inertie du système sur l'axe.
* Le TMC permet de relier la vitesse de rotation aux différents moments s'appliquant sur le solide.
* Le TRD sert en général à déterminer certaines force résultante comme celle de la liaison pivot.
* La liaison pivot possède a priori un moment non nul sur son axe. Il n'est nul que si la liaison pivot est parfaite.
* On a déjà étudié le cas des pendules pesant et de torsion.

### Equivalience TMC-TEC

````{important} __A retenir : Equivalence__

Pour un solide __indéformable__ en __rotation autour d'un axe fixe__ dans un référentiel galiléen, le théorème de l'énergie cinétique et le théorème du moment cinétique sont équivalents.
````

_Le démontrer_

## Solide déformable

Nous allons nous intéresser au cas d'un assemblement de solide pouvant bouger les uns par rapport aux autres. L'ensemble sera en rotation autour d'un axe fixe mais les différentes partie ne tourneront pas forcément à la même vitesse.


### Solide déformable: Théorèmes généraux

````{important} __Fondamental : TEC et TMC__

Si le solide est déformable, __le TEC et le TMC ne sont plus équivalents__.

En général, le TEC/TEM n'apporte pas d'information à cause de puissances des forces intérieures qui ne sont pas quantifiables. On utilisera plutôt le TMC.

Dans le cadre du programme, on sera en général amené à montrer que le moment cinétique est conservé.
````

### Utilisation de la conservation du moment cinétique

````{admonition} Exercice 
:class: attention

Observer l'expérience du tabouret d'inertie et proposer une modélisation permettant de l'expliquer.

````

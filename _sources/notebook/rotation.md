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
# Solide en rotation autour d'un axe fixe

Nous avons déjà établi les principales caractéristiques du mouvement des solides dans le cadre du programme et notamment les cas du pendule pesant et de torsion.

Il s'agit ici de reprendre certaines idées générales et de préciser le cas d'étude des systèmes __déformables__ en rotation.


## Solide indéformable

### Rappel

On rappelle quelques éléments utiles:

* le moment cinétique du solide sur l'axe s'écrit comme le produit de la vitesse angulaire autour de l'axe par le moment d'inertie du système sur l'axe.
* Le TMC permet de relier la vitesse de rotation aux différents moments s'appliquant sur le solide.
* Le TRD sert en général à déterminer certaines force résultante comme celle de la liaison pivot.
* La liaison pivot possède a priori un moment non nul sur son axe. Il n'est nul que si la liaison pivot est parfaite.
* On a déjà étudié le cas des pendules pesant et de torsion.

### Types d'études


On va différencier plusieurs types d'étude:

* Solide indéformable de type pendule: déjà étudié précédemment.
* Solide indéformable de type moteur: nous étudierons  un chapitre complet sera proposé plus tard dans l'année sur les moteurs électriques.


### Equivalience TMC-TEC

````{important} __Fondamental : Equivalence__

Pour un solide __indéformable__ en __rotation autour d'un axe fixe__ dans un référentiel galiléen, le théorème de l'énergie cinétique et le théorème du moment cinétique sont équivalents.
````


__Démonstration__
Nous allons partir du théorème du moment cinétique et procéder par égalité.

\begin{align*}
\frac{\rm{d}J\omega}{\rm{dt}} &= M_{ext,\Delta}\\
\frac{\rm{d}J\omega}{\rm{dt}}\omega &= M_{ext,\Delta}\omega \\
\frac{\rm{d}}{\rm{dt}}\left(\frac{1}{2}J\omega^2\right) &= P_{ext}
\end{align*}
La dernière ligne correspond au théorème de l'énergie cinétique puisque __pour un système indéformable__, la puissance des forces intérieures est nulle.


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

## Exercices d'application

### Pendule pesant

````{admonition} Exercice 
:class: attention

On considère une tige de longueur $L$ et de masse $M$ attaché à une extrémité à un bati par une liaison pivot parfaite d'axe Oz horizontal (on donne le moment de la tige par rapport à Oz: $J_{Oz} = \frac{M L^2}{3}$), l'autre extrémité étant laissé libre. Une masse ponctuelle $m$ est accrochée à la tige à une distance $l$ de l'axe Oz. Déterminer la période des petites oscillations en fonction de la longueur $l$.

````

### Entraînement par frottements

````{admonition} Exercice 
:class: attention

On considère un système constitué de deux disques en rotation autour d'un axe $\Delta$ (les moments d'inertie des deux disques par rapport à l'axe sont notés $J_1$ et $J_2$) au moyen d'une liaison pivot parfaite. A l'instant initial, les deux disques sont éloignés et sans contact et le premier tourne avec une vitesse angulaire $\omega_0$ et le second est immobile. On approche doucement les deux disques jusqu'à ce qu'ils soient en contact.

1. Déterminer la vitesse angulaire de l'ensemble des deux disques à la fin de la manipulation. Ce résultat dépend-t-il de la nature des frottements entre les deux disques?
1. Faire un bilan d'énergie mécanique pour chaque disque séparément puis pour l'ensemble des deux disques. Commenter les résultats.

````



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
# Etude des pendules

````{admonition} Objectifs
:class: tip
* Etablir l'équation du mouvement du pendule simple
* Etablir l'équation du mouvement du pendule pesant.
* Justifier l'analogie avec l'oscillateur harmonique dans le cadre de l'approximation linéaire (pendule simple ou pesant)
* Etablir l'équation du portrait de phase dans le cadre des faibles oscillations et le tracer.
* Lire et interpréter le portrait de phase: bifurcation entre un mouvement pendulaire et un mouvement révolutif.
* Mettre en évidence le non isochronisme des oscillations
* Etablir l'équation du mouvement d'un pendule de torsion
* Expliquer l'analogie entre le pendule de torsion et l'oscillateur harmonique
* Etablir une intégrale première du mouvement.
````

## Pendule simple

Un pendule simple est constitué d'un fil parfait (ou d'une tige parfaite) de longueur L au bout duquel on attache une masse m assimilable à un point matériel (noté M). Dans cet exercice, on considère le cas d'une tige rigide.

Ici, l'autre extrémité de la tige est attachée à un point O fixe dans le référentiel terrestre supposé galiléen.

Le champ de pesanteur est supposé uniforme.


### PFD

````{admonition} Exercice 
:class: attention

1. Proposer un paramétrage adapté au problème.
1. Etablir l'équation qui régit l'évolution du pendule au moyen du principe fondamental de la dynamique.

````

### TMC

````{admonition} Exercice 
:class: attention

En utilisant le même paramétrage que dans l'exercice précédent, établir à nouveau l'équation d'évolution du pendule mais en utilisant le théorème du moment cinétique.

````

### TEM

````{admonition} Exercice 
:class: attention

En utilisant le même paramétrage que dans l'exercice précédent, établir à nouveau l'équation d'évolution du pendule mais en utilisant le théorème de la puissance mécanique.

Reconnaître une intégrale première du mouvement, c'est-à-dire une __grandeur ne dépendant que de la position et de sa dérivée première__ et qui est __constante au cours du mouvement__.

````

## Pendule pesant

Dans le cas du pendule pesant, on considère cette fois que la tige possède une masse. On modélise alors le solide tige+masse par un solide indéformable de masse M.

Elle est accrochée au bati par une liaison pivot (supposée parfaite) d'axe Oz horizontal et on note J le moment de l'ensemble tige+masse sur l'axe Oz. On note de plus a=OG la distance du centre d'inertie de l'ensemble tige+masse à l'axe Oz.


### TMC

````{admonition} Exercice 
:class: attention

1. Proposer un paramétrage pour étudier le mouvement du pendule pesant.
1. Etablir l'équation du mouvement du pendule au moyen du théorème du moment cinétique.

````

### TEM

````{admonition} Exercice 
:class: attention

Etablir l'équation du mouvement du pendule au moyen du théorème de la puissance mécanique.

````

## Petits mouvements

````{admonition} Exercice 
:class: attention

On considère le pendule simple ou le pendule pesant dont l'équation différentielle est de forme identique.

1. Linéariser l'équation d'évolution pour des petits mouvements autour de la position d'équilibre stable. Comment appelle-t-on un tel système ?
1. Préciser la forme temporelle de l'évolution du système ainsi que la période des oscillations.
1. La période des oscillations dépend-t-elle des conditions initiales (dans l'hypothèse des petites mouvements). On parle __d'isochronisme__ des oscillations.

````

## Etude générale

On considère à nouveau le pendule simple ou pesant mais on ne suppose plus qu'on est aux petits angles.


### Etude énergétique

````{admonition} Exercice 
:class: attention

En étudiant l'énergie potentielle du pendule simple et/ou du pendule pesant, montrer:

1. l'existence de deux types de mouvements suivant l'énergie mécanique: un mouvement pendulaire et un mouvement circulaire complet.
1. L'existence de deux positions d'équilibre: l'une stable et l'autre instable.
1. Si le mobile part du point le plus bas avec une vitesse linéaire $v_0$. Déterminer l'angle $\theta_{\max}$ le plus haut qu'il peut atteindre en fonction de $v_0$ ainsi que la valeur minimale de $v_0$ permettant en pendule de faire des tours complet.
1. Reconnaître sur le graphique ci-après les différents cas: petits mouvements, grands mouvements pendulaire, tours complets.

```{figure} ./images/meca_simple_phase2.png
:name: fig_255
:align: center

```

````

### Anisochronisme

````{admonition} Exercice 
:class: attention

On considère que le pendule est lâché d'un angle $\theta_0 > 0$ avec la verticale descendante sans vitesse initiale.

1. Quelle est la nature du mouvement: pendulaire ou tour complet ?
1. A l'aide du théorème de l'énergie mécanique, exprimer la vitesse angulaire à un instant t où le pendule fait un angle $\theta$ avec la verticale descendante.
1. Déduire de l'équation précédente que la période d'oscillation T est: $T = 4 \int_0^{\theta_0} \frac{d \theta}{\sqrt{\frac{2g}{l} (cos \theta - cos \theta_0)}}$
1. La période des oscillations est-elle indépendante de l'amplitude des oscillations? On parle d'__anisochronisme__ des oscillations.
1. On a représenté ci-après le rapport $T/T_0$ en fonction de l'angle $\theta_0$ (noté $\theta_{\max}$). Commenter cette courbe.

```{figure} ./images/meca_anaharmonicite_pendule.jpg
:name: fig_256
:align: center

```

````

## Pendule de torsion

On attache un fil de torsion (de constante C) à un plafond fixe dans le référentiel terrestre supposé galiléen RT. à son autre extrémité est attaché un solide S. L'ensemble du système ne peut que tourner autour de l'axe du fil de torsion.

### TMC

````{admonition} Exercice 
:class: attention

On note $\theta$ l'angle que fait S avec un axe arbitraire et $\theta_0$ l'angle au repos.

1. Déterminer l'équation d'évolution de l'angle $\theta$ en supposant qu'il n'y a aucun frottement au moyen du théorème du moment cinétique. Comment appelle-t-on un tel système?

````
### TEM

````{admonition} Exercice 
:class: attention

On note $\theta$ l'angle que fait S avec un axe arbitraire et $\theta_0$ l'angle au repos.

1. Déterminer l'équation d'évolution de l'angle $\theta$ en supposant qu'il n'y a aucun frottement au moyen du théorème de la puissance mécanique
1. Montrer que l'on peut déterminer une intégrale première du mouvement dont on exprimera la forme à tout instant puis en fonction des conditions initiales: $\theta(0) = \theta_1$ et $\dot \theta = 0$.

````



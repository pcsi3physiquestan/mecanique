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
# Actions et interactions

## Interactions et actions: définitions


__Interaction et actions__
Soit deux systèmes mécaniques $\Sigma_1$ et $\Sigma_2$ (points matériels ou systèmes de points matériels) possédant des caractéristiques (masse, charge, contact... ) tel que le premier système influe sur le mouvement du second système. Alors le second influe aussi sur le premier système (on parlera par la suite de loi d'action et réaction). On dit que les deux systèmes mécaniques sont en __interactions__.

 On peut décrire l'interaction entre deux systèmes mécaniques par __deux actions réciproques__: l'action $\mathfrak{A}_{1 \to 2}$ de $\Sigma_1$ sur $\Sigma_2$ et l'action $\mathfrak{A}_{2 \to 1}$ de $\Sigma_2$ sur $\Sigma_1$.


````{admonition} Attention : Action et force
:class: note

Attention, un action n'est PAS une force. Comme nous le verrons par la suite la force est __un des éléments permettant de modéliser une action__.

````

````{dropdown} _Remarque : Système d'étude et milieu extérieur_

Par la suite, on s'intéressera souvent à un système mécanique donné (système d'étude) qui subit l'influence (des actions) d'autres systèmes (qu'on regroupe sous le terme de "milieu extérieur"). Dans cette vision, on s'intéresse à aux actions du milieu extérieur ou "oubliant" un peu dans l'étude les actions réciproques du système sur le milieu extérieur. C'est pourquoi par la suite, on parlera surtout d'actions et non d'interactions. Il faut néanmoins garder à l'esprit qu'elles existent, même si leur prise en compte n'est pas nécessaire dans l'étude du mouvement du système d'étude.

````

## Actions: Types de description

````{important} __Définition : Action ponctuelle__

Une action ponctuelle __d'un système $\Sigma_1$ sur un système $\Sigma_2$__ est une action agissant sur un point (matériel) du système $\Sigma_2$.

Tout système possédant une extension spatiale, il s'agit d'une modélisation théorique d'une action mécanique.

````


__Vision différentielle__
Une action ponctuelle peut décrire l'action sur un système qui est un point matériel (!) ou l'action sur une portion infinitésimale de système, c'est-à-dire un petit volume $d\tau$ autour d'un point M qu'on ramène par la pensée à une action sur le point M de masse $\rho(M) d \tau$.

Cette dernière vision (qui ne sera pas développée de manière calculatoire) permet d'appréhender des actions plus complexes par le calcul différentiel (calcul intégral principalement).


````{important} __Définition : Action résultante (ou globale).__

Une action résultante sur un système $\Sigma_2$ est une action du milieu extérieur modélisable par le regroupement __arbitraire__ d'un ensemble d'actions ponctuelles sur le système $\Sigma_2$.

````

````{admonition} Attention : Arbitraire mais réfléchi... 
:class: note

En effet, un système $\Sigma_2$ subit de nombreuses actions de la part du milieu extérieur. On va pouvoir regrouper ses actions en des actions résultantes mais ces regroupement ne se font pas de manière aléatoire. Un regroupement possède un sens physique: en général, on __doit__ par exemple pouvoir attribuer toutes les actions ponctuelles à un même système $\Sigma_1$ qu'on peut parfaitement définir, de sorte qu'on puisse parler de __l'action résultante du système $\Sigma_1$ sur le système $\Sigma_2$.__

Il arrive par contre qu'on différencie en deux groupes des actions provenant d'un même système. Par exemple, considérons deux boules massiques et chargées. La première exerce sur chaque point de la seconde des actions de gravitation et des actions électriques. Même si l'origine de ces actions reste la première boule, on distinguera deux actions résultantes: l'action électrique résultante de la boule 1 sur la boule 2 et l'action gravitationnelle résultante de la boule 1 sur la boule 2.

Dans tous les cas:

* ces regroupements doivent permettre de définir __quel système exerce l'action sur le système d'étude__.
* ces regroupements doivent avoir un sens physique (regroupement par type d'actions ou par portion du système concerné par l'action... )

````


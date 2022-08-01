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
# Modélisation des actions globales

## Généralités
```{margin}
Il arrivera que des actions ponctuelles s'appliquent sur un solide (tension d'un fil, ressort...)
```
````{important} __Action résultante (ou globale).__

Rappel : Une action résultante sur un système $\Sigma_2$ est une action du milieu extérieur modélisable par le regroupement __arbitraire__ d'un ensemble d'actions ponctuelles sur le système $\Sigma_2$.
````

````{topic} Arbitraire mais réfléchi...

En effet, un système $\Sigma_2$ subit de nombreuses actions de la part du milieu extérieur. On va pouvoir regrouper ses actions en des actions résultantes mais ces regroupement ne se font pas de manière aléatoire. Un regroupement possède un sens physique: en général, on __doit__ par exemple pouvoir attribuer toutes les actions ponctuelles à un même système $\Sigma_1$ qu'on peut parfaitement définir, de sorte qu'on puisse parler de __l'action résultante du système $\Sigma_1$ sur le système $\Sigma_2$.__

Il arrive par contre qu'on différencie en deux groupes des actions provenant d'un même système. Par exemple, considérons deux boules massiques et chargées. La première exerce sur chaque point de la seconde des actions de gravitation et des actions électriques. Même si l'origine de ces actions reste la première boule, on distinguera deux actions résultantes: l'action électrique résultante de la boule 1 sur la boule 2 et l'action gravitationnelle résultante de la boule 1 sur la boule 2.

Dans tous les cas:

* ces regroupements doivent permettre de définir __quel système exerce l'action sur le système d'étude__.
* ces regroupements doivent avoir un sens physique (regroupement par type d'actions ou par portion du système concerné par l'action... )

````

```{margin}
Dans les calculs du moment résultant, il est important de différencier le pôint de calcul (identique) du point d'application (qui varie avec l'action ponctuelle).
```
````{important} Description mathématique
Une action globale ou action résultante peut être décrite par __deux__ éléments:
* la __force résultante__ : somme de toutes les forces ponctuelles associées aux actions ponctuelles qu'on a regroupées
* le __moment résultant__ en un point arbitraire A : somme de tous les moments des actions ponctuelles regroupées calculés tous au même point A.

_La donnée des deux éléments de l'action est appelé __torseur__ de l'action._
````


````{attention}
Le moment résultant __ne peut être déduire de la force résultante__.
````


## Eléments utiles (en ligne)
````{topic} Cas rencontrés
Vous rencontrerez trois façon de présenter les actions globales:
* Les actions globales usuelles : vous devrez connaître par coeur __une partie__ des caractéristiques (force et/ou moment) d'un certain nombre d'actions globales (poids, torsion...)
    * ATTENTION : Souvent, vous ne connaitrez pas toutes les caractéristiques (seulement la force résultante ou seulement le moment, voire une seule composante du moment)
* Les actions de contact : Comme pour les actions ponctuelles, on ne connait en général pas grand chose sur les actions de contact, sauf en cas d'absence de frottement qui supprimera __une__ composante de la force ou du moment résultant.
    * Il pourra aussi y avoir l'application des lois de Coulomb
    * En général, la recherche des composantes inconnues se fait, comme avec les points matériels par l'application d'un théorème fondamental.
* Les actions à calculer : plus rares mais il arrivera que vous deviez calculer par intégration la force résultante ou le moment résultant. Les méthodes d'intégration seront vues plus tard.
````

````{sidebar} Cas d'un moment nul
Le transfert des moment devient intéressant avec le cas où une action possède un moment nul en un point C (_on parle de glisseur_). Le transfert des moments en un point B quelconque devient alors:

$$
\overrightarrow{M}_B = \overrightarrow{BC}\wedge \overrightarrow{F}
$$

__Tout se passe alors _comme si(=mathématiquement et pas physiquement)_ on avait une action ponctuelle de force $\overrightarrow{F}$ appliquée au point C.__

Cette observation sera par exemple utile avec l'action de la pesanteur qui est souvent présentée comme _"s'appliquant au centre de gravité"_ par abus de langage.
````
````{topic} Transfert de moment
Cette relation n'est pas au programme mais sera utile pour expliquer certains éléments : si l'on connait la force résultante $\overrightarrow{F}$ d'une action et le moment résultant de l'action en un point A $\overrightarrow{M}_A$, alors le moment résultant en un point B sera :

$$
\overrightarrow{M}_B = \overrightarrow{M}_A + \overrightarrow{BA}\wedge \overrightarrow{F}
$$
````

````{topic} Représentation graphique
En général, il l'on connait un point de moment nul pour une action globale, on représentera cette action par sa force résultante en ce point. 

_Il n'est par contre pas nécessaire de chercher un tel point (qui peut ne pas exister) pour faire une représentation graphique._ __On se rappellera par contre que le point où l'on dessine la force n'est PAS FORCEMENT UN POINT DE MOMENT NUL.__
````
## Cas particuliers

```{margin}
La démonstration de l'indépendance du moment est directe avec le transfert de moment précédent.
```
````{important} __Couple__

Un couple est une action résultante dont la __force résultante__ est nulle.

> Le moment résultant d'un couple est indépendant du point considéré.
````
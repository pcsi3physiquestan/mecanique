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
````{important} __Description mathématique__

Une action globale ou action résultante peut être décrite par __deux__ éléments:
* la __force résultante__ $\overrightarrow{F}_{\Sigma_1 \to \Sigma}$: somme de toutes les forces ponctuelles associées aux actions ponctuelles qu'on a regroupées
* le __moment résultant__ $\overrightarrow{M}_{A,\Sigma_1 \to \Sigma}$ en un point arbitraire A : somme de tous les moments des actions ponctuelles regroupées calculés tous au même point A.

_La donnée des deux éléments de l'action est appelé __torseur dynamique__ de l'action._

```{topic} __Notation de torseurs dynamiques__
On note les torseurs dynamiques comme les torseurs cinématiques mais il ne contiennent pas les mêmes grandeurs.

$$
\mathcal{T}_A(\mathcal{A_{\Sigma_{ext} \to \Sigma}}) =
\begin{cases}
  &\overrightarrow{F}_{\Sigma_1 \to \Sigma}\\
  &\overrightarrow{M}_{A,\Sigma_1 \to \Sigma}
\end{cases}
$$
```
````

````{attention}
Le moment résultant __ne peut être déduire de la force résultante__.
````

```{sidebar} Cas d'un moment nul
Le transfert des moments devient intéressant avec le cas où une action possède un moment nul en un point C (_on parle de glisseur_). Le transfert des moments en un point B quelconque devient alors:

$$
\overrightarrow{M}_B = \overrightarrow{BC}\wedge \overrightarrow{F}
$$

__Tout se passe alors _comme si(=mathématiquement et pas physiquement)_ on avait une action ponctuelle de force $\overrightarrow{F}$ appliquée au point C.__

Cette observation sera par exemple utile avec l'action de la pesanteur qui est souvent présentée comme _"s'appliquant au centre de gravité"_ par abus de langage.

_On pourra écrire la relation précédente comme le passage du torseur au point C au torseur au point B comme avec un torseur cinématique._

On peut donc passer d'un torseur en A de moment nul à un torseur en B:

$$
\mathcal{T}_{A}(\Sigma_1 \to \Sigma)=
\begin{cases}
  &\overrightarrow{F}_{\Sigma_1 \to \Sigma}\\
  &\overrightarrow{M}_{A,\Sigma_1 \to \Sigma} = 0
\end{cases}
\Longrightarrow
\mathcal{T}_{B}(\Sigma_1 \to \Sigma)=
\begin{cases}
  &\overrightarrow{F}_{\Sigma_1 \to \Sigma}\\
  &\overrightarrow{M}_{B,\Sigma_1 \to \Sigma} = \overrightarrow{BC}\wedge \overrightarrow{F}_{\Sigma_1 \to \Sigma}
\end{cases}
$$

```
````{topic} Transfert de moment

A l'image des torseurs cinématiques qu'on peut décider d'exprimer en différents points, on peut exprimer le torseur dynamique d'une action mécanique en un autre point B. Cela revient à exprimer le moment de l'action en un autre B.

Si on ne peut déterminer un moment à partir de la force résultante seule, on peut obtenir le moment en un point B connaissant la force résultant ET le moment en un point A. Cette relation n'est pas au programme mais sera utile pour expliquer certains éléments :

$$
\overrightarrow{M}_B = \overrightarrow{M}_A + \overrightarrow{BA}\wedge \overrightarrow{F}
$$
````

## Différents types d'actions rencontrées (en ligne)
````{topic} Cas rencontrés
Vous rencontrerez trois façon de présenter les actions globales:
* Les actions globales usuelles : vous devrez connaître par coeur __tout ou une partie__ des caractéristiques (force et/ou moment) d'un certain nombre d'actions globales (poids, torsion...)
    * ATTENTION : Souvent, vous ne connaitrez pas toutes les caractéristiques (seulement la force résultante ou seulement le moment, voire une seule composante du moment)
* Les actions de contact : Comme pour les actions ponctuelles, on ne connait en général pas grand chose sur les actions de contact, sauf en cas d'absence de frottement qui supprimera __une__ composante de la force ou du moment résultant.
    * Il pourra aussi y avoir l'application des lois de Coulomb
    * En général, la recherche des composantes inconnues se fait, comme avec les points matériels par l'application d'un théorème fondamental.
* Les actions à calculer : plus rares pour l'instant mais il arrivera que vous deviez calculer par intégration la force résultante ou le moment résultant. Les méthodes d'intégration seront vues plus tard.
````


````{topic} Représentation graphique
En général, il l'on connait un point de moment nul pour une action globale, on représentera cette action par sa force résultante en ce point. 

_Il n'est par contre pas nécessaire de chercher un tel point (qui peut ne pas exister) pour faire une représentation graphique._ __On se rappellera par contre que dans ce cas le point où l'on dessine la force n'est PAS FORCEMENT UN POINT DE MOMENT NUL.__
````

## Cas particuliers

```{margin}
La démonstration de l'indépendance du moment est directe avec le transfert de moment précédent.
```
````{important} __Couple__

Un couple est une action résultante dont la __force résultante__ est nulle.

> Le moment résultant d'un couple est indépendant du point considéré.
````
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
# Méthodes : Actions
## Forces et mouvement.
_On se propose d'étudier qualitativement l'effet d'une action sans utiliser les théorèmes._


````{admonition} Exercice 
:class: attention

On considère un point matériel M de masse m se déplaçant sur un plan incliné faisant un angle $\alpha$ avec l'horizontale. Il est soumis à deux actions: son poids $\overrightarrow{P}$ d'amplitude $mg$ dirigé verticalement vers le bas et l'action du plan incliné $\overrightarrow{R}$ qu'on suppose perpendiculaire au plan.

1. Proposer un système de coordonnées permettant d'étudier le mouvement de M sur le plan (on suppose que M reste sur le plan incliné). Préciser les expressions vectorielles des forces modélisant les deux actions qui s'appliquent sur le point M.
1. Déduire des contraintes imposées l'expression de $\overrightarrow{R}$.
1. Justifier qualitativement que le point matériel M va glisser le long du plan.

````
````{topic} Correction
>__1. Paramétrage__
>
>On va choisir un système de coordonnées cartésiennes dont l'un des axes (Ox) est suivant le plan incliné.
>
```{figure} ./images/plan_modelisation.png
:name: fig_228
:align: center

```
>
>Le poids s'écrira donc: $\overrightarrow{P} = - mg \cos \alpha \overrightarrow{e_y} + mg \sin \alpha \overrightarrow{e_x}$.
>
>La réaction du support s'écrit: $\overrightarrow{R} = R_y \overrightarrow{e_y}$. Nous ici dans un cas où l'on n'a pas d'expression connue des composantes de la force. Par contre, on connaît que __certaines composantes sont nulles__. C'est souvent le cas pour les actions dites "de contact".
>
>__2. Contrainte cinématique__
>
>Ici, le mouvement de M est contraint à reste sur le plan incliné. Il vient une accélération nulle suivant l'axe Oy. Sans quantifier complètement la relation accélération-force, on peut déjà observer que cela implique que la somme des forces suivant l'axe Oy est nulle (il faut que leur action de déviation dans cette direction se compense). Soit: $R_y = - P_y = mg \cos \alpha$ et donc $\overrightarrow{R} = mg \cos \alpha \overrightarrow{e_y}$
>
>Remarque: on pourrait faire une construction graphique pour déterminer graphiquement les caractéristiques de $\overrightarrow{R}$.
>
>__3. Influence sur le mouvement__
>
>A nouveau, on sait que la force résultante suivant Ox donne la tendance générale du mouvement. Ici seul le poids possède une composante suivant Ox et elle est positive. Le point M aura donc tendance à être dirigé vers le bas de la pente.
>
>Attention, on rappelle que l'inertie peut permettre au point M de monter dans un premier temps si sa vitesse initiale était vers le haut. Mais va être ralenti et finira par redescendre.
>
>__Modélisation ponctuelle__
Le système précédente est probablement une modélisation ponctuelle d'un système mécanique plus étendu (un cube, une luge... ). On rappelle qu'une telle modélisation est valable seulement si le système de se déforme pas et ne risque pas de tourner sur lui-même.
````

## Utilisation du moment
````{admonition} Exercice 
:class: attention

Dans tout le problème, on travaille dans le référentiel terrestre $\mathfrak{R}_T$.

On considère une petite masse m assimilable à un point matériel M accrochée à une tige rigide de longueur l sans masse dont l'autre extrémité est relié à un point fixe O. On considère que la tige ne se déforme pas et qu'elle exerce une action ponctuelle sur la masse dont la force est dirigé le long de la tige. L'ensemble est placé dans un champ de pesanteur $\overrightarrow{g}$ de sorte que le point M.

On supposera que le mouvement de M reste dans un plan vertical contenant le point O.

1. Proposer un paramétrage adapté à l'étude du mouvement du point M puis déterminer dans ce système de coordonnées les vecteurs position, vitesse et accélération ainsi que le moment cinétique calculé par rapport au point O.
1. Faire un bilan des actions appliquées sur le point M et donner l'expression vectorielle des forces associées. (Remarque: pour un point matériel, on parle aussi de bilan des forces).
1. Calculer le moment de chaque action/force par rapport au point O et commenter leurs expressions. En déduire qualitativement l'évolution du mouvement du point M (on distinguera deux types de mouvement possibles).
1. Peut-on déterminer, sans le PFD, l'expression de la force exercée par la tige sur le point M ? Pourquoi ?
````
````{topic} Correction
>__1. Paramétrage__
>
>Le point M se déplace dans un plan à une distance constante du point O, sa trajectoire est donc portée par un cercle de centre O et de rayon l. On va donc travailler dans un système de coordonnées cylindriques d'axe Oz perpendiculaire au cercle trajectoire. On a pris l'origine des angles sur la verticale descendante.
>
```{figure} ./images/pendule_param.png
:name: fig_229
:align: center
```
>
>On peut alors écrire:
>
>\begin{align*}
\overrightarrow{OM} &= l \overrightarrow{e_r}\\
\overrightarrow{v_{M/\mathfrak{R}_T}} &= l \dot \theta \overrightarrow{e_{\theta}}\\
\overrightarrow{a_{M/\mathfrak{R}_T}} &= - l \dot \theta^2 \overrightarrow{e_r} + l \ddot \theta \overrightarrow{e_{\theta}}\\
\overrightarrow{L_{O/\mathfrak{R}_T}}(M) &= m l^2 \dot \theta \overrightarrow{e_z}\\
\end{align*}
>Il est vivement conseillé de s'entraîner à retrouver les expressions précédentes.
>
>__2. Bilan des forces__
>
>On est dans un champ de pesanteur, donc le poids s'applique sur le point M. Son expression est $\overrightarrow{P} = mg \overrightarrow{e_x} = mg \cos \theta \overrightarrow{e_r} - mg \sin \theta \overrightarrow{e_{\theta}}$.
>
>De plus, la tige exerce une action supposée ponctuelle dont l'expression est $\overrightarrow{T} = T \overrightarrow{e_r}$. Comme dans l'exemple du plan incliné, on ne connaît pas l'expression de T mais on sait que l'action est dirigée suivant $\overrightarrow{e_r}$. Ici T est de signe quelconque puisque la tige peut tirer ou pousser le point M. Si ça avait été un fil T aurait forcément été négatif (un fil ne peut pousser).
>
>__3. Calcul des moments des actions__
>
>Avec les expressions précédentes, il vient:
>
>\begin{align*}
\overrightarrow{M_{O}(\mathfrak{A(poids)})} &= \overrightarrow{OM} \wedge \overrightarrow{P}\\
&= l \overrightarrow{e_r} \wedge \left(mg \cos \theta \overrightarrow{e_r} - mg \overrightarrow{e_{\theta}}\right)\\
&= -mgl \sin \theta \overrightarrow{e_z}\\
\overrightarrow{M_{O}(\mathfrak{A(tige)})} &= \overrightarrow{OM} \wedge \overrightarrow{T}\\
&= l \overrightarrow{e_r} \wedge \left(T \overrightarrow{e_r}\right)\\
&= 0
\end{align*}
>On remarque que le moment de la tige __au point O__ est nul. C'est logique car la force exercée par l'action __ponctuelle__ exercée par la tige est dirigée vers le point O de sorte qu'elle n'a aucun effet sur la rotation de M autour de O. D'un point de vue mathématique pour faire le calcul du moment, on pourra directement remarquer que la force est dirigée vers O, donc le produit vectoriel est nul.
>
>Le moment du poids est non nul ce qui est logique parce que le poids agit sur la rotation (sa composante suivant $\overrightarrow{e_{\theta}}$). On peut remarquer que le poids tend à ramener le point M vers $\theta = 0$ (point le plus bas) de sorte que le moment du poids doit être négatif quand $\theta > 0$ et positif quand $\theta < 0$. C'est ce qu'on trouve.
>
>__4. Force et accélération__
>
>On ne peut pas déterminer pour l'instant l'expression de T comme on l'a fait précédemment pour la réaction d'un support. En effet, il n'y a pas de mouvement radiale (suivant $\overrightarrow{e_r}$) mais c'est un mouvement __courbe__. Le mouvement est donc __dévié__ dans la direction $- \overrightarrow{e_r}$ à chaque instant (son accélération suivant $\overrightarrow{e_r}$ est non nulle et négative).
>
>Il vient que la somme des forces suivant $\overrightarrow{e_r}$ __ne doit pas être nulle__ ce qui nous empêche de déterminer complètement l'expression de T. Grâce au principe fondamentale de la dynamique, on pourra obtenir une expression faisant intervenir l'accélération. Quant au calcul de cette dernière, nous évoquerons le cas de ce système plus tard.

````

## Détermination de la force de rappel
_On va présenter ici une méthode permettant de déterminer l'expression de la force de rappel élastique._


````{admonition} Exercice 
:class: attention

On considère deux ressorts horizontaux de raideur identique k et de longueur à vide $l_0$. Ils sont attachées comme représentés ci-dessous. Déterminer la force exercée par chaque ressort sur le point matériel M en fonction de la coordonnées x de M.

```{figure} ./images/ressort_exo.png
:name: fig_235
:align: center
```
````
````{topic} Résolution
>__Expression des longueurs__
>
>On va exprimer les longueurs (grandeurs positives) de chaque ressort en fonction des coordonnées. On note $l_1 = AM$ et $l_2 = MB$ les longueurs des ressorts.
>
>. Il est conseillé d'utiliser des grandeurs algébriques pour déterminer ces longueurs. Ici, il vient:
>
>\begin{align*}
l_1 = \overline{AM} = \overline{AO} + \overline{OM} = L + x\\
l_2 = \overline{MB} = \overline{MO} + \overline{BM} = L - x
\end{align*}
>Les allongements sont donc:
>
>\begin{align*}
\Delta l_1 = l_1 - l_0 = L + x - l_0\\
\Delta l_2 = l_2 - l_0 = L - x - l_0
\end{align*}
>
```{dropdown} _Remarque : Longueur et allongement_

Il peut être préférable dans certains cas de determiner directement l'allongement directement.
```
>
>__Expression du vecteurs unitaires directeurs__  
>
>Il s'agit d'exprimer ce vecteur dans la base d'étude choisi. Ici, pour le ressort 1, le vecteur unitaire doit être suivant $+ \overrightarrow{e_x}$ pour être orienté vers l'extérieur depuis le point M.
>
>Pour le ressort 2, $\overrightarrow{u_{\Delta}} = - \overrightarrow{e_x}$.
>
>
>__Expression complète__
>
>Il vient l'expression des forces de rappel appliquées sur le point M:
>
>\begin{align*}
\overrightarrow{F_1} = -k \left(L + x - l_0\right) \overrightarrow{e_x}\\
\overrightarrow{F_2} = k \left(L - x - l_0\right) \overrightarrow{e_x}\\
\end{align*}

````


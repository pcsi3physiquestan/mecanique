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
# Action ponctuelle: Modélisation et typologie

Comme nous l'avons vu, l'action ponctuelle possède une grande importance car une action résultante est définie initialement comme un regroupement d'actions ponctuelles. Nous allons donc voir comment modéliser mathématiquement une action ponctuelle. Nous nous en servirons dans ce chapitre pour décrire des actions usuelles ponctuelles comme les interactions fondamentales (gravitation et électromagnétiques) ainsi que quelques actions dont la modélisation ponctuelle reste valable pour la grande majorité des systèmes d'étude.

Nous verrons dans le cas où le système est un point matériel comment on peut déterminer certaines caractéristiques des actions inconnues en statique ou prévoir l'évolution qualitative du mouvement en dynamique. Nous introduirons enfin le moment des forces qui aura, comme nous le verrons par la suite un effet sur la rotation du système et donc sur le moment cinétique du système.


## Action ponctuelle: Modélisation mathématique

````{admonition} Fondamental : Modélisation d'une action ponctuelle
:class: attention

Soit une action ponctuelle $\mathfrak{A}_{1 \to 2}$ d'un système $\Sigma_1$ sur un système $\Sigma_2$. On modélise mathématiquement cette action par deux caractéristiques:

* sa force $\overrightarrow{F}(\mathfrak{A}_{1 \to 2})$ (noté souvent simplement $\overrightarrow{F}$) qui donne la direction et le sens vers laquelle l'action tend à entraîner le système et avec quelle intensité elle tend à entraîner le système.
* son point d'application.
````

````{admonition} Attention : 
:class: note

La force $\overrightarrow{F}$ donne la direction et le sens vers laquelle l'action tend à entraîner le système mais cela ne veut pas dire que le sytèmeva aller dans sa direction. Son inertie peut lui permettre de continuer dans une autre direction. Il sera simplement dévié (plus ou moins fortement suivant son inertie et l'intensité de la force).

Exemple: Un objet lancé vers le haut subit l'action de la pesanteur dirigée vers le bas mais il continue à monter (en étant par contre ralenti).

````


Il est important de noter la présence de __deux__ caractéristiques: force ET point d'application car pour les actions globales, il faudra aussi __deux__ caractéristiques pour décrire une action globale. Sauf que ce ne sera pas les mêmes.

Il est néanmoins courant de voir des abus de langage confondant l'action ponctuelle et la force ("Un système subit une force"). C'est abus ne porte pas trop à conséquence, tant qu'on travaille avec des systèmes ponctuels (cf. suite). Il faudra faire attention lorsqu'on travaille avec une action résultante sur un système de points matériels.



__Point d'application et système ponctuel__
Dans le cas d'un système constitué d'un unique point matériel M, le point d'application est nécessairement le point M (et les actions du milieu extérieur sont toutes nécessairement des actions ponctuelles).


````{dropdown} Remarque

__Indépendance vis-à-vis du référentiel__
Par principe physique, les caractéristiques d'une action sont indépendante du référentiel considéré.

````

## Forces et mouvement.


Déduire le mouvement d'un système mécanique des actions qui s'appliquent sur lui de manière quantitative nécessite les lois fondamentales de la dynamique que nous verrons plus tard. Néanmoins, on peut déjà réaliser quelques études semi qualitatives.

On va utiliser le fait que __la force modélise la direction et le sens dans laquelle l'acion tend à faire se diriger le système__ c'est-à-dire son centre d'inertie.


````{admonition} Exercice 
:class: attention

On considère un point matériel M de masse m se déplaçant sur un plan incliné faisant un angle $\alpha$ avec l'horizontale. Il est soumis à deux actions: son poids $\overrightarrow{P}$ d'amplitude $mg$ dirigé verticalement vers le bas et l'action du plan incliné $\overrightarrow{R}$ qu'on suppose perpendiculaire au plan.

1. Proposer un système de coordonnées permettant d'étudier le mouvement de M sur le plan (on suppose que M reste sur le plan incliné). Préciser les expressions vectorielles des forces modélisant les deux actions qui s'appliquent sur le point M.
1. Déduire des contraintes imposées l'expression de $\overrightarrow{R}$.
1. Justifier qualitativement que le point matériel M va glisser le long du plan.

````
````{dropdown}
 

__1. Paramétrage__

On va choisir un système de coordonnées cartésiennes dont l'un des axes (Ox) est suivant le plan incliné.

```{figure} ./images/plan_modelisation.png
:name: fig_228
:align: center

```

Le poids s'écrira donc: $\overrightarrow{P} = - mg \cos \alpha \overrightarrow{e_y} + mg \sin \alpha \overrightarrow{e_x}$.

La réaction du support s'écrit: $\overrightarrow{R} = R_y \overrightarrow{e_y}$. Nous ici dans un cas où l'on n'a pas d'expression connue des composantes de la force. Par contre, on connaît que __certaines composantes sont nulles__. C'est souvent le cas pour les actions dites "de contact".


__2. Contrainte cinématique__

Ici, le mouvement de M est contraint à reste sur le plan incliné. Il vient une accélération nulle suivant l'axe Oy. Sans quantifier complètement la relation accélération-force, on peut déjà observer que cela implique que la somme des forces suivant l'axe Oy est nulle (il faut que leur action de déviation dans cette direction se compense). Soit: $R_y = - P_y = mg \cos \alpha$ et donc $\overrightarrow{R} = mg \cos \alpha \overrightarrow{e_y}$

Remarque: on pourrait faire une construction graphique pour déterminer graphiquement les caractéristiques de $\overrightarrow{R}$.


__3. Influence sur le mouvement__

A nouveau, on sait que la force résultante suivant Ox donne la tendance générale du mouvement. Ici seul le poids possède une composante suivant Ox et elle est positive. Le point M aura donc tendance à être dirigé vers le bas de la pente.

Attention, on rappelle que l'inertie peut permettre au point M de monter dans un premier temps si sa vitesse initiale était vers le haut. Mais va être ralenti et finira par redescendre.



__Modélisation ponctuelle__
Le système précédente est probablement une modélisation ponctuelle d'un système mécanique plus étendu (un cube, une luge... ). On rappelle qu'une telle modélisation est valable seulement si le système de se déforme pas et ne risque pas de tourner sur lui-même.

````

## Action ponctuelle: Moment d'une action

### Moment d'une action: définition

````{admonition} Définition : Moment d'une action ponctuelle/d'une force par rapport à un point.
:class: tip

Soit une action ponctuelle $\mathfrak{A}_{1 \to 2}$ d'un système $\Sigma_1$ sur un système $\Sigma_2$ modélisée par une force $\overrightarrow{F}$ et un point d'application A.

Soit un point B de l'espace. On définit le moment $\overrightarrow{M_B}(\overrightarrow{F})$ (ou $\overrightarrow{M_B}(\mathfrak{A}_{1 \to 2})$) de l'action $\mathfrak{A}_{1 \to 2}$ (ou moment de la force $\overrightarrow{F}$) par rapport au point B par:

\begin{equation}
\overrightarrow{M_B}\left(\overrightarrow{F}\right) = \overrightarrow{BA} \wedge \overrightarrow{F}
\end{equation}
````


Par abus de langage (quasi systématique), on parle de moment d'une force et non de moment d'une action. Cela ne pose de problème pour des actions ponctuelles car __pour une action ponctuelle__, le moment se déduit de la force (cf. expression précédente). Il faudra néanmoins faire attention à cet abus de langage pour des actions globales (résultantes) car alors __le moment ne se déduit plus de la force__.


````{admonition} Définition : Moment d'une action ponctuelle/force par rapport à un axe.
:class: tip

Soit une action ponctuelle $\mathfrak{A}_{1 \to 2}$ d'un système $\Sigma_1$ sur un système $\Sigma_2$ modélisée par une force $\overrightarrow{F}$ et un point d'application A.

Soit un axe $\Delta$ orienté par un vecteur unitaire $\overrightarrow{u_{\Delta}}$. On définit le moment $M_{\Delta}(\overrightarrow{F})$ (ou $M_{\Delta}(\mathfrak{A}_{1 \to 2})$) de l'action $\mathfrak{A}_{1 \to 2}$ (ou moment de la force $\overrightarrow{F}$) par rapport à l'axe $\Delta$ par:

\begin{equation}
M_{\Delta}\left(\overrightarrow{F}\right) = \overrightarrow{u_{\Delta}} \cdot \left(\overrightarrow{BA} \wedge \overrightarrow{F}\right)
\end{equation}
où B est un point de l'axe $\Delta$.

````

### Moment d'une force: Interprétation


__Interprétation du moment cinétique par rapport à un axe.__
Dans toute la suite on travaillera implicitement dans un référentiel $\mathfrak{R}$.

Pour interprêter le moment cinétique par rapport à un axe orienté $\Delta$, on va se placer dans un repère cylindrique d'axe $\Delta$ centré en un point O de l'axe.

On considère pour simplifier un point matériel M subissant une action modélisée par une force $\overrightarrow{F}$ (appliquée donc au point M). On note l'expression de $\overrightarrow{F} = F_r \overrightarrow{e_r} + F_{\theta} \overrightarrow{e_{\theta}} + F_z \overrightarrow{e_z}$.

On peut donc calculer le moment de la force (!) $\overrightarrow{F}$ sur $\Delta$:

\begin{align*}
L_{\Delta/R} &= \overrightarrow{u_{\Delta}} \cdot \overrightarrow{L_{O/R}}(M)\\
&= m\overrightarrow{e_z} \cdot ((r \overrightarrow{e_r} + z \overrightarrow{e_z}) \wedge (\dot r \overrightarrow{e_r} + r \dot \theta \overrightarrow{e_{\theta}} + \dot z \overrightarrow{e_z}))\\
&= m r^2 \dot \theta
\end{align*}
On observe que:

* Le moment de la force $\overrightarrow{F}$ sur l'axe $\Delta$ n'est pas nul si la composante orthoradiale $F_{\theta}$ est non nulle.
Or la composante orthoradiale correspond à la (seule) composante de $\overrightarrow{F}$ qui tend à faire tourner le point M autour de l'axe $\Delta$ (la composante suivant Oz tend à le faire longer l'axe Oz et la composante suivant $\overrightarrow{e_r}$ ne fait qu'éloigner ou rapprocherle point M de l'axe.

Le moment d'une action sur un axe donne donc une information sur __la possibilité que possède cette action (seule) à faire tourner le système autour de l'axe considéré.__.

* Il est __algébrique__ et le moment de l'action est positif $F_{\theta} > 0$ c'est-à-dire si l'action tend à faire tourner le système suivant les$\theta$ positifs (on généralisera en remarquant qu'il s'agit de faire tourner le système dans un sens en cohérence avec l'orientation de l'axe considéré).
A l'inverse, si $F_{\theta} < 0$, l'action tend à faire tourner le système en sens inverse.

Et si la composante orthoradiale est nulle, cela signifie que l'action n'a pas d'effet sur la rotation autour de l'axe. Elle ne fait qu'éloigner/rapprocher le système de l'axe ou le faire longer l'axe.

* On remarquera que le moment de l'action est aussi plus important quand r est grand. Si l'on fait le parallèle avec la force, on comprend que plus le moment est grand, plus il sera capable de modifier la rotation du système autour de l'axe considéré. Or on observe expérimentalement que plus l'action est loin de l'axe de rotation, plus elle a d'effet sur le système (principe du bras de levier utilisé par Archimède), il est donc normal que le moment de la force soit proportionnel à la distance r à l'axe.


````{admonition} Attention : 
:class: note

Il s'agit d'une tendance pour l'action considéré et cela ne donne d'information que sur la tendanceà faire tourner le système autour d'un axe donné. Mais cela ne veut pas dire que le système est en rotation autour de l'axe (bien que très on souvent on utilise les calculs de moments pour des systèmes en rotation, la définition du moment est valable quelque soit le mouvement), il peut même être immobile (les considérations sur les moments sont très important en statique des systèmes de points).

Comme pour la force, le moment donne une tendance qui sera réalisée ou non suivant l'existance d'autres actions et suivant l'inertie et le mouvement initial du système.

````


__Généralisation__
Si le calcul (et la définition !) du moment diffère pour des systèmes de points et des actions résultantes, l'interprétation physique du moment d'une action sur un axe restera identique. Le moment d'une action sur un axe donnera toujours l'information sur la tendance que possède cette action à faire tourner le système autour de l'axe considéré.

Le moment d'une action par rapport à un point B, à l'image du moment cinétique, donne l'information sur la rotation autour du point. Ses projections dans différentes directions de l'espace donne les effets sur les rotations dans chaque direction considérée.


### Utilisation du moment


Nous allons voir comment calculer un moment d'une action/d'une force puis comment l'utiliser de manière qualitative.


````{admonition} Exercice 
:class: attention

Dans tout le problème, on travaille dans le référentiel terrestre $\mathfrak{R}_T$.

On considère une petite masse m assimilable à un point matériel M accrochée à une tige rigide de longueur l sans masse dont l'autre extrémité est relié à un point fixe O. On considère que la tige ne se déforme pas et qu'elle exerce une action ponctuelle sur la masse dont la force est dirigé le long de la tige. L'ensemble est placé dans un champ de pesanteur $\overrightarrow{g}$ de sorte que le point M.

On supposera que le mouvement de M reste dans un plan vertical contenant le point O.

1. Proposer un paramétrage adapté à l'étude du mouvement du point M puis déterminer dans ce système de coordonnées les vecteurs position, vitesse et accélération ainsi que le moment cinétique calculé par rapport au point O.
1. Faire un bilan des actions appliquées sur le point M et donner l'expression vectorielle des forces associées. (Remarque: pour un point matériel, on parle aussi de bilan des forces).
1. Calculer le moment de chaque action/force par rapport au point O et commenter leurs expressions. En déduire qualitativement l'évolution du mouvement du point M (on distinguera deux types de mouvement possibles).
1. Peut-on déterminer pour l'instant l'expression de la force exercée par la tige sur le point M ? Pourquoi ?

````
````{dropdown}
 

__1. Paramétrage__

Le point M se déplace dans un plan à une distance constante du point O, sa trajectoire est donc portée par un cercle de centre O et de rayon l. On va donc travailler dans un système de coordonnées cylindriques d'axe Oz perpendiculaire au cercle trajectoire. On a pris l'origine des angles sur la verticale descendante.

```{figure} ./images/pendule_param.png
:name: fig_229
:align: center

```

On peut alors écrire:

\begin{align*}
\overrightarrow{OM} &= l \overrightarrow{e_r}\\
\overrightarrow{v_{M/\mathfrak{R}_T}} &= l \dot \theta \overrightarrow{e_{\theta}}\\
\overrightarrow{a_{M/\mathfrak{R}_T}} &= - l \dot \theta^2 \overrightarrow{e_r} + l \ddot \theta \overrightarrow{e_{\theta}}\\
\overrightarrow{L_{O/\mathfrak{R}_T}}(M) &= m l^2 \dot \theta \overrightarrow{e_z}\\
\end{align*}
Il est vivement conseillé de s'entraîner à retrouver les expressions précédentes.


__2. Bilan des forces__

On est dans un champ de pesanteur, donc le poids s'applique sur le point M. Son expression est $\overrightarrow{P} = mg \overrightarrow{e_x} = mg \cos \theta \overrightarrow{e_r} - mg \sin \theta \overrightarrow{e_{\theta}}$.

De plus, la tige exerce une action supposée ponctuelle dont l'expression est $\overrightarrow{T} = T \overrightarrow{e_r}$. Comme dans l'exemple du plan incliné, on ne connaît pas l'expression de T mais on sait que l'action est dirigée suivant $\overrightarrow{e_r}$. Ici T est de signe quelconque puisque la tige peut tirer ou pousser le point M. Si ça avait été un fil T aurait forcément été négatif (un fil ne peut pousser).


__3. Calcul des moments des actions__

Avec les expressions précédentes, il vient:

\begin{align*}
\overrightarrow{M_{O}(\mathfrak{A(poids)})} &= \overrightarrow{OM} \wedge \overrightarrow{P}\\
&= l \overrightarrow{e_r} \wedge \left(mg \cos \theta \overrightarrow{e_r} - mg \overrightarrow{e_{\theta}}\right)\\
&= -mgl \sin \theta \overrightarrow{e_z}\\
\overrightarrow{M_{O}(\mathfrak{A(tige)})} &= \overrightarrow{OM} \wedge \overrightarrow{T}\\
&= l \overrightarrow{e_r} \wedge \left(T \overrightarrow{e_r}\right)\\
&= 0
\end{align*}
On remarque que le moment de la tige __au point O__ est nul. C'est logique car la force exercée par l'action __ponctuelle__ exercée par la tige est dirigée vers le point O de sorte qu'elle n'a aucun effet sur la rotation de M autour de O. D'un point de vue mathématique pour faire le calcul du moment, on pourra directement remarquer que la force est dirigée vers O, donc le produit vectoriel est nul.

Le moment du poids est non nul ce qui est logique parce que le poids agit sur la rotation (sa composante suivant $\overrightarrow{e_{\theta}}$. On peut remarquer que le poids tend à ramener le point M vers $\theta = 0$ (point le plus bas) de sorte que le moment du poids doit être négatif quand $\theta > 0$ et positif quand $\theta < 0$. C'est ce qu'on trouve.


__4. Force et accélération__

On ne peut pas déterminer pour l'instant l'expression de T comme on l'a fait précédemment pour la réaction d'un support. En effet, il n'y a pas de mouvement radiale (suivant $\overrightarrow{e_r}$ mais c'est un mouvement __courbe__. Le mouvement est donc __dévié__ dans la direction $- \overrightarrow{e_r}$ à chaque instant (son accélération suivant $\overrightarrow{e_r}$ est non nulle et négative).

Il vient que la somme des forces suivant $\overrightarrow{e_r}$ __ne doit pas être nulle__ ce qui nous empêche de déterminer complètement l'expression de T. Grâce au principe fondamentale de la dynamique, on pourra obtenir une expression faisant intervenir l'accélération. Quant au calcul de cette dernière, nous évoquerons le cas de ce système plus tard.

````

### Méthode: Cas d'un système de points.


Cet exercice présente trois points importants: la capacité à paramétrer correctement un problème, le calcul d'un moment d'une force et l'analyse physique d'un système en rotation par étude des moments. Nous en profiterons pour aborder qualitativement deux notions importantes: la notion d'équilibre et la notion de stabilité.


````{admonition} Exercice 
:class: attention

On considère un cube de côté a et de répartition de masse homogène fixé sur un axe passant par le centre du cube et perpendiculaire à deux des faces du cube. Le cube ne peut ainsi que tourner autour de cet axe supposé fixe dans un référentiel $\mathfrak{R}$. Tous les éléments cinématiques et cinétiques devront être établis dans ce référentiel qu'on supposera galiléen. A ce stade, cela signifiera que l'intuition physique sur l'effet d'une action sur le solide est celle que nous pouvons avoir habituellement.

```{figure} ./images/moment_cube.png
:name: fig_230
:align: center

```

On attache un fil tendu à un coin du cube noté A. On considère que la liaison entre le cube et le fil se résume à un seul point de sorte qu'on puisse considérer l'action du ressort sur le cube comme ponctuelle. La force appliqué par le fil sur le cube est toujours horizontale et de norme $F_0$.

1. Paramétrer le problème (proposer un système de coordonnées et des paramètre utile au problème) pour pouvoir étudier la rotation du cube autour de son axe. Proposer alors une expression du moment cinétique du cube,de son énergie cinétique et de sa quantité de mouvement. On notera J le moment d'inertie du cube sur l'axe de rotation et M sa masse totale.
1. Exprimer le moment de la force exercé par le ressort sur le cube exprimé au centre du cube. Commenter suivant les valeurs des paramètres introduits la tendance qu'aura cette force à agir sur la rotation du cube.
1. On admet que la seule action dont le moment sur l'axe de rotation est non nul est la tension du fil étudié précédemment. Quelles sont les positions d'équilibre du système ? Si l'on écarte légèrement le cube de chacune de ces positions, aura-t-il tendance a revenir à la position d'équilibre ? (On parle de stabilité des positions d'équilibre).
1. On néglige l'action de la pesanteur. Quelle autre action s'exerce sur le cube ? En raisonnant sur les moments de manière analogique au raisonnement qu'on pourrait avoir sur des forces, justifier que le moment de cette action sur un axe vertical passant par O est nécessairement non nul.

````
````{dropdown}
 

__1. Paramétrage__

Pour étudier un système en rotation autour d'un axe fixe, le système de coordonnées le plus judicieux est un système de coordonnées cylindrique d'axe Oz l'axe de rotation. On a représenté ci dessous le système. On repère l'angle $\theta$ permettant de repérer l'orientation du cube par l'angle $(\overrightarrow{e_x},\overrightarrow{OA})$ de manière à pouvoir utiliser cet angle pour les calculs de moments.

```{figure} ./images/moment_cube_2.png
:name: fig_231
:align: center

```

On peut alors écrire les éléments cinétiques du cube:

\begin{align*}
L_{Oz}(cube) &= J \dot \theta \\
E_{c,cube} &= \frac{1}{2} \dot \theta^2\\
\overrightarrow{P_{cube/\mathfrak{R}}} = M \overrightarrow{v_{G}} = \overrightarrow{0}
\end{align*}
__Le cube étant de masse répartie de manière homogène, le centre d'inertie est situé au point O, centre du cube__. Fixé sur l'axe Oz, le centre d'inertie est donc immobile, d'où la quantité de mouvement nulle.

Les deux autres expressions sont les expressions déjà données __dans le cas d'un solide en rotation autour d'un axe fixe__.


__2. Calcul de moment de l'action/la force__

L'action du fil sur le cube est une action ponctuelle dont la force s'écrit $\overrightarrow{F} = F_0 \overrightarrow{e_x}$ et dont le point d'application est A. Le moment de l'action du fil sur le cube calculé sur l'axe Oz s'écrit (O est un point de l'axe...  Oz):

\begin{align*}
M_{fil \to cube,Oz} &= \overrightarrow{e_z} \cdot \left(\overrightarrow{OA} \wedge \overrightarrow{F}\right)\\
&= \overrightarrow{e_z} \cdot \left(\left(\frac{a}{\sqrt{2}} \overrightarrow{e_r} + \frac{a}{2} \overrightarrow{e_z}\right) \wedge F_0 \overrightarrow{e_x}\right)\\
&= \overrightarrow{e_z} \cdot \left(\frac{aF_0}{2} \overrightarrow{e_y} - \frac{a}{\sqrt{2}} \wedge F_0 \sin \theta  \overrightarrow{e_z} \right)\\
&= - \frac{a}{\sqrt{2}} F_0 \sin \theta \\
\end{align*}

__3. Analyse du moment__  

On remarque que si $\theta$ est positif, le moment de l'action est négatif: l'action du fil aura tendance à faire tourner le cube dans le sens des $\theta$ décroissants. A l'inverse, si $\theta$ est négatif, le moment de l'action est positif: l'action du fil aura tendance à faire tourner le cube dans le sens des $\theta$ croissants. C'est cohérent avec le schéma représenté ci-dessous.

```{figure} ./images/moment_cube_signe.png
:name: fig_232
:align: center

```


__3. Positions d'équilibre et stabilité__

Seule les actions possédant un moment non nul sur l'axe Oz peuvent agir sur la rotation du cube autour de Oz. Si seul l'action du fil possède un effet, alors les angles pour lesquels ce moment est nul seront les positions d'équilibre (on peut faire le parallèle avec la translation d'un système: les positions d'équilibre sont les points la résultante des forces est nul). L'expression précédente montre que les deux positions correspondent aux angles $\theta = 0$ et $\theta = \pi$. On a représenté les positions d'équilibre ci-dessous.

```{figure} ./images/moment_cube_equilibre.png
:name: fig_233
:align: center

```

On remarque que si l'on écarte légèrement le cube de sa position d'équilibre $\theta = 0$ vers des angles positifs, l'angle va décroitre sous l'effet de l'action du fil (cf. schéma ou signe du moment) et il va donc avoir tendance à revenir vers la position d'équilibre. A l'inverse, si $\theta$ est négatif, l'angle va croitre (schéma ou signe du moment) et va aussi revenir vers la position d'équilibre. Donc  lorsqu'on écarte le système de cette position d'équilibre, il tend à y revenir, on dit que la position d'équilibre est __stable__.

A l'inverse si l'on écarte le cube de sa position d'équilibre $\theta = \pi$, on remarque qu'il va s'éloigner de cette position. En effet, pour $\theta < \pi$, le moment est négatif et l'angle va encore décroître. Et pour $\theta > + pi$, le moment est positif et l'angle va croître. Dans les deux cas, on s'éloigne de la position d'équilibre: la position est dite __instable__.

On pourra faire le parallèle avec le sommet d'une bosse et le creux d'un trou pour une bille. Les deux sont des positions d'équilibre mais la première est instable alors que la seconde est stable. Dans ce cas, c'est un raisonnement sur la force résultante (pesanteur + réaction du sol) là on raisonne ici sur le moment.


__4. Détermination (qualitative) d'un moment en statique__

Le cube tourne d'une axe fixe. L'axe est en contact avec le cube et exerce une action (de contact) sur le cube. C'est la somme des deux actions (fil sur cube et axe sur cube) qui permet d'étudier le mouvement du cube. On remarquera que l'action de contact se fait en de nombreux points (à la surface de contact), il s'agit donc d'une __action résultante__.

Nous n'avons pas appris à calculer le moment d'une telle action mais si l'on considère que les moments ont un effet sur la rotation et que c'est le moment résultant de la somme de toutes les actions sur le cube qui détermine le mouvement du cube (par analogie avec l'effet des forces sur la translation du cube), on peut raisonner qualitativement.

Ici le cube ne peut tourner que suivant l'axe Oz. Cela signifie que la rotation suivant l'axe Oy est bloquée. Donc le moment résultant suivant l'axe Oy de toute les actions sur le cube devraient être nul (comme l'immobilité de translation suivant un axe Ox correspondrait à une somme des forces nulles suivant Ox). Or le moment de l'action du fil sur le cube sur Ox est non nul, il vaut: $\frac{aF_0}{2}$ (cf. le calcul précédent du moment). Il vient, pour que la somme des moments des moments soit nul que le moment de l'action de l'axe sur le cube doit être non nul suivant l'axe Oy.

Il est important de pouvoir comprendre le raisonnement précédent de manière qualitative. On a représenté ci-dessous un vue de "dessus" (suivant Oy). On observe que si l'on permettait au cube de tourner autour de Oy (au lieu de Oz), on remarque graphiquement que la tension du fil ferait effectivement tourner le cube autour de Oy. Il faut donc une action contraire qui s'oppose à cette rotation: l'axe de rotation doit donc exercer une action de moment contraire (donc non nul) suivant Oy.

```{figure} ./images/moment_cube_dessus.png
:name: fig_234
:align: center

```

````

## Actions ponctuelles usuelles

Nous allons présenter ici les actions usuelles dont les caractéristiques des forces doivent être connues.

Il s'agit pour la plupart d'action ponctuelle s'exerçant sur des points matériels, il ne sera donc en général pas précisé le point d'application parce qu'il est alors évident.

On distingue les interactions à distance et les interactions de contact. Les premières regroupent des interactions fondamentales (gravitation et électromagnétisme) et des dérivées (pesanteur). Les secondes, représentent des actions résultant de multiples actions (principalement électrostatiques) à l'échelle microscopique. On parle aussi d'actions surfaciques puisque les actions microscopiques se font en surface. Il s'agit donc d'action globales mais dans certains cas, on peut les assimiler à des actions ponctuelles: quand le contact se fait sur une surface très petite (qu'on peut considérer à un point) ou quand on assimile le système à un point matériel.


### Force de Lorentz


__Champ électromagnétique__
Initialement, les champs électriques $\overrightarrow{E}$ et magnétiques $\overrightarrow{B}$ sont la conséquence de la présence de charges (pour le champ électrique) en mouvement (pour le champ magnétique) et vont agir sur d'autres particules chargées. On peut les voir comme des intermédiaires de calcul dont l'interaction électromagnétique entre deux systèmes chargées: on s'intéresse d'un côté aux charges qui crée le champ puis on s'intéresse à l'action du champ sur les particules dont on veut étudier le mouvement.

On peut donc "oublier" les éléments qui causent l'existence des champs électromagnétiques en posant leur existence et s'intéresser uniquement à leur action sur des particules chargés. Quand on continue en physique, on peut observer que les champs électromagnétiques ne sont pas que des "intermédiaires de calcul" mais possède leur réalité propre et leurs caractéristiques propres qui permet de les étudier indépendamment du reste (cf. deuxième année). On va ici simplement s'intéresser à l'action ponctuelle d'un champ électromagnétique sur une particule chargée (donc ponctuelle).


````{admonition} Définition : Force de Lorentz
:class: tip

Soit un point matériel M chargé de charge q et un champ électromagnétique donc les expressions vectorielles au point M sont $\overrightarrow{E}(M)$ et $\overrightarrow{B}(M)$. Alors le champ électromagnétique exerce une action dont la force, appelée force de Lorentz s'écrit:

\begin{equation}
\overrightarrow{F}_{Lorentz} = q \left(\overrightarrow{E}(M) + \overrightarrow{v_{M/\mathfrak{R}}} \wedge \overrightarrow{B}(M)\right)
\end{equation}
où $\overrightarrow{v_{M/\mathfrak{R}}}$ est la vitesse du point M dans le référentiel d'étude.

````


__Dépendance vis à vis du référentiel__
Normalement, une action ne peut dépendre du référentiel d'étude. Or ici, la partie magnétique de la force de Lorentz dépend explicitement du référentiel. C'est un problème qui ne peut être résolu que par l'introduction de la mécanique relativiste (hors programme). Néanmoins, on peut raisonner sur la partie magnétique tant qu'on reste dans un même référentiel (galiléen) en restant dans le cadre de la mécanique classique. C'est dans ce cadre qu'on raisonnera en classe préparatoire.


### Forces newtoniennes


__Forces newtoniennes__
Les forces dites newtoniennes sont des interactions dont la force décroît en $\frac{1}{r^2}$ où r est la distance entre les deux points matériels en interaction. On distingue deux interactions newtoniennes: les interactions coulombiennes entre deux particules chargées (elles correspondent à un cas particulier de la force de Lorentz) et les interactions gravitationnelles entre deux particules massiques.

Il s'agit de deux des 4 interactions fondamentales (les deux autres, l'interaction forte et l'interaction faible n'ont pas d'effet significatifs dans le cadre de la mécanique classique, elles ont un rôle à l'échelle du noyau).


````{admonition} Définition : Interactions gravitationnelles
:class: tip

Soit deux points matériels $M_1$ et $M_2$ de masses respectives $m_1$ et $m_2$. Les deux masses sont en interaction dites gravitationnelles. L'action de $M_1$ sur $M_2$ est modélisée par une force dirigée de $M_2$ vers $M_1$ dont l'expression est:

\begin{align*}
\overrightarrow{F_{grav,1 \to 2}} &= - G m_1 m_2 \frac{\overrightarrow{M_1 M_2}}{M_1 M_2^3}\\
&= - \frac{G m_1 m_2}{r^2} \overrightarrow{u_{1 \to 2}}
\end{align*}
où G est la constante de gravitation universelle dont l'expression est $G = 6.67 \times 10^{-11} \rm{m^{3}.kg^{-1}.s^{-2}}$.

Dans la seconde expression, r est la distance $M_1 M_2$ et $\overrightarrow{u_{1 \to 2}}$ est le vecteur unitaire porté par la droite orientée de $M_1$ vers $M_2$.

````


On remarquera que l'interaction gavitationnelle est toujours attractive.

L'action de $M_2$ sur $M_1$ est l'opposé (principe des actions réciproques).


````{admonition} Définition : Champ de gravitation
:class: tip

Soit un point $M_1$ de masse $m_1$. On dit que le point $M_1$ créé dans tout point P de l'espace un __champ de gravitation__ $\overrightarrow{\mathfrak{G}_{M_1}}(P)$ dont l'expression est:

\begin{align*}
\overrightarrow{\mathfrak{G}_{M_1}}(P) &= - G m_1 \frac{\overrightarrow{M_1 P}}{M_1 P^3}
\end{align*}
Si l'on place en un point P un point matériel $M_2$ de masse $m_2$, alors le point $M_2$ subira une action gravitationnelle de la part de $M_1$: $\overrightarrow{F_{grav,1 \to 2}} = m_2 \overrightarrow{\mathfrak{G}_{M_1}}(P = M_2)$.

Le champ de gravitation permet de séparer la cause (présence d'une masse) de la conséquence (action sur une autre masse). Cela devient très utile quand on travaille avec non plus des points mais des __systèmes de points matériels__ qui créent le champ de gravitation. Ce dernier étant la somme (possiblement continue = intégrale !) des champ de gravitation créé par chaque points du système, on peut séparément calculer le champ de gravitation puis dans un second temps calculer l'action sur un système (un point - action ponctuelle ou un système de points - action résultante de l'ensemble des action gravitationnelle sur chaque point du système).

````

````{admonition} Définition : Interactions coulombiennes (ou électrostatiques)
:class: tip

Soit deux points matériels $M_1$ et $M_2$ chargés de charges respectives $q_1$ et $q_2$. Les deux charges sont en interaction dites coulombiennes. L'action de $M_1$ sur $M_2$ est modélisée par une force portée par la droite $M_1 M_2$ dont l'expression est:

\begin{align*}
\overrightarrow{F_{elec,1 \to 2}} &= - \frac{q_1 q_2}{4 \pi \epsilon_0} \frac{\overrightarrow{M_1 M_2}}{M_1 M_2^3}\\
&= - \frac{q_1 q_2}{4\pi \epsilon_0 r^2} \overrightarrow{u_{1 \to 2}}
\end{align*}
où $\epsilon_0$ est la __permittivité électrique du vide__ dont l'expression est $\epsilon_0 = 8.85 \times 10^{-12} \rm{s^{4}.A^{2}.kg^{-1}.m^{-3}}$ soit $\frac{1}{4 \pi \epsilon_0} = 8.99 10^{9} S.I.$.

Dans la seconde expression, r est la distance $M_1 M_2$ et $\overrightarrow{u_{1 \to 2}}$ est le vecteur unitaire porté par la droite orientée de $M_1$ vers $M_2$.

````


On remarquera que l'interaction coulombienne peut être attractive si les charges sont opposées et répulsive si les charges sont de même signe.

L'action de $M_2$ sur $M_1$ est l'opposé (principe des actions réciproques).


````{admonition} Définition : Champ électrique
:class: tip

Soit un point $M_1$ de charge $q_1$. On dit que le point $M_1$ créé dans tout point P de l'espace un __champ électrique__ $\overrightarrow{E_{M_1}}(P)$ dont l'expression est:

\begin{align*}
\overrightarrow{E_{M_1}}(P) &= - \frac{q_1}{4 \pi \epsilon_0} \frac{\overrightarrow{M_1 P}}{M_1 P^3}
\end{align*}
Si l'on place en un point P un point matériel $M_2$ de charge $q_2$, alors le point $M_2$ subira une action coulmbienne de la part de $M_1$: $\overrightarrow{F_{grav,1 \to 2}} = q_2 \overrightarrow{E_{M_1}}(P = M_2)$.

Le champ électrique permet, comme le champ de gravitation, de séparer la cause (présence d'une charge) de la conséquence (action sur une autre charge). Cela devient très utile quand on travaille avec non plus des points mais des __systèmes de points matériels chargés__ qui créent le champ électrique. Ce dernier étant la somme (possiblement continue = intégrale !) des champs électrique créé par chaque points du système, on peut séparément calculer le champ électrique puis dans un second temps calculer l'action sur un système (un point - action ponctuelle ou un système de points - action résultante de l'ensemble des action gravitationnelle sur chaque point du système).

Comme cela a été évoqué dans précédemment, les champs (et notamment le champ électrique) peut être étudié pour lui-même sans tenir compte de la cause de ce champ électrique. C'est le cas des ondes électromagnétiques.

````

````{dropdown} Remarque

__Interaction électrique ou électromagnétique__
Le champ électrique présenté précédemment et le même que celui présenté dans la force de Lorentz. Seule son expression va différer suivant que ce champ soit créé par une seule charge (cas évoqué ci-dessus) ou par un ensemble de charge (cas qui sera étudié en deuxième année au moyen des relations fondamentales de l'électromagnétisme). Dans tous les cas, on voit qu'une charge q ponctuelle placée en un point P subira une force électrique $\overrightarrow{F} = q \overrightarrow{E}$.

Comme on l'a dit précédemment, si les charges sont en mouvement, elles vont aussi créer un champ magnétique qui va agir sur les autres charges en mouvement. Dans le cas d'une interactions entre deux charges ponctuelles, on peut montrer que la partie magnétique de l'interaction de Lorentz est alors négligeable devant la partie électrique. C'est pourquoi lors de l'interaction entre deux particules chargées, on considère simplement la partie magnétique de la force de Lorentz qui s'exprime comme l'interaction coulombienne.

````


__Forces newtoniennes__
Comme on peut le voir, l'interaction coulombienne et l'interaction gravitationnelle 


### Pesanteur sur un point matériel

````{admonition} Définition : Champ de pesanteur
:class: tip

A la surface de la Terre, tout corps massique est attiré vers "le bas" par une action appelée poids. Pour un point matériel M de masse m, la force qui s'applique s'écrit $\overrightarrow{P} = m \overrightarrow{g}$ où $\overrightarrow{g}$ est le champ de pesanteur au point M. Il est dirigé vers "le bas" (en réalité, il permet de définir la verticale (principe du fil à plomb)).

Le champ de pesanteur résulte de l'action gravitationnelle de la Terre sur le point M et de l'effet de rotation du référentiel terrestre (rotation de la Terre sur elle-même). Comme c'est l'action gravitationnelle qui prédomine au voisinage de la surface terrestre (cf. deuxième année), on confond souvent la pesanteur à la gravitation.

````


__Caractère uniforme__
En général, on considère le champ de pesanteur comme uniforme. En effet, si l'on considère la part gravitationnelle qui est prépondérante à la surface, elle a pour intensité $\frac{GM_T m}{(R_T + h)^2}$ où h est l'altitude et $R_T$ le rayon terrestre. Une variation de 1\% de cette force par rapport au niveau de la mer correspond à une altitude $h = 9 R_T = 57600 \rm{km}$ ! Pour des systèmes dont la taille est de l'ordre du mètre ne montant pas plus haut qu'une centaine de mètres, on peut largment considérer que le champ de pesanteur est uniforme.


### Tension d'un fil

````{admonition} Définition : Tension d'un fil ou d'une tige rigide.
:class: tip

La tension d'un fil ou d'une tige rigide est l'action qu'exerce un fil/une tige sur un système accroché au fil/à la tige (c'est une action de contact). Dans le cas d'un fil/une tige fin(e) dont la torsion n'a pas d'influence (ou qui ne se tord pas), on peut assimiler cette action à une action ponctuelle.

La force exercée par le fil/la tige n'a pas d'expression connue a priori mais on sait que dans le cas d'un fil, elle est alors nécessairement vers le fil et non vers le système accroché (un fil ne peut que tirer le système). Pour une tige, la force peut être dans les deux directions.

````

````{admonition} Fondamental : Cas d'une fil/d'une tige parfaite
:class: attention

Un fil/une tige parfaite est un fil/tige sans masse. Dans ce cas la tension exercée en chaque point du fil/tige sur l'autre partie du fil est la même en tout point du fil/tige est égale à la tension exercée à chaque extrémité du fil/tige sur les systèmes accrochée. De plus la tension du fil/tige est alors tangente au fil/tige.
````


__Démonstration__
La démonstration fait intervenir le principe fondamentale de la dynamique: $\frac{\rm{d}\overrightarrow{p}}{\rm{dt}} = \sum \overrightarrow{F_{ext \to systeme}}$. Si l'on considère une portion de fil, les deux actions qui s'appliquent sur la portion de fil sont la tension de partie de fil à gauche et la tension de la partie du fil à droite. Comme le fil est sans masse, la quantité de mouvement est nulle, il vient donc que les deux tensions du fil sont opposées de même intensité. Par symétrie, il vient que les tensions seront tangentes au fil.

Pour les portions de fils aux extrémités, le même raisonnement conduit à dire que l'action des systèmes accrochés aux extrémités sur le fil sont modélisées par des forces égales entre elles et égales à la tension du fil en chaque point. Par principe des actions réciproques, l'action du fil sur les systèmes accrochés aux extrémités est modélisée par une force d'intensité égale à cette tension.


### Action d'un ressort: Force de rappel élastique

````{admonition} Définition : Action d'un ressort
:class: tip

Soit un système accroché à un ressort. En général, on considère le point d'accroche comme ponctuel et la force exercée par le ressort à son extrémité sur le système comme tangente au ressort. Si le ressort est de masse négligeable (cas usuel), alors la force exercée par le ressort sur un système accroché à son extrémité s'écrit si sa longueur est l:

\begin{equation}
\overrightarrow{F_{ressort\to extremite}} = -k \left(l - l_0\right) \overrightarrow{u_{ext}} = - k \Delta l \overrightarrow{u_{ext}}
\end{equation}
où $l_0$ est la longueur à vide du ressort, k sa raideur et $\overrightarrow{u_{ext}}$ un vecteur unitaire tangent à l'axe de ressort et dirigé vers l'extérieur du ressort.

$\Delta l = l - l_0$ est appelé allongement du ressort.

````


__Analyse de l'expression__
On remarquera que la longueur à vide est bien la longueur que possède le ressort au repos __lorsqu'aucune action n'est exercée à ses extrémités__ (donc lorsqu'il n'exerce aucune action à ses extrémités.

La raideur donne une information sur la facilité qu'on peut avoir à tendre ou compresser le ressort: plus la raideur est grande, plus la force nécessaire pour étendre ou compresser le ressort devra être grande.

On parle de __force de rappel__. En effet, lorsque le ressort est comprimé, l'allongement est négatif et la force est dirigée vers l'extérieur: le ressort essaie de se détendre. Lorsque le ressort est étendu, l'allongement est positif et la force est dirigée vers l'intérieur: le ressort essaie de se contracter. Dans tous les cas, le système accroché tend à être __rappelé__ vers la position à vide par le ressort.


````{admonition} Attention : Position au repos et position à vide
:class: note

Il ne faut pas confondre la position au repos et la position à vide. En effet, la longueur du ressort au repos d'un système complet (ressort + système accroché au bout du ressort) n'est pas nécessairement la longueur à vide. On peut penser à un ressort vertical au bout duquel on a attaché une masse. Au repos, la longueur du ressort sera différente de la longueur à vide: le ressort sera étiré ou compressé suivant que la masse soit accrochée au dessus ou au dessous.

````

__Utilisation de cette expression__

Pour pouvoir utiliser cette expression, il faut exprimer les différentes caractéristiques (longueur ou allongement et vecteur unitaire) dans le système de coordonnées choisi.

Il est important, lorsqu'on a établi l'expression d'une force de rappel d'un ressort __de vérifier sa cohérence__: position de la longueur à vide correcte, force correspondant bien à une force de rappel.


### Méthode: Détermination de la force de rappel


On va présenter ici une méthode permettant de déterminer l'expression de la force de rappel élastique.


````{admonition} Exercice 
:class: attention

On considère deux ressorts horizontaux de raideur identique k et de longueur à vide $l_0$. Ils sont attachées comme représentés ci-dessous. Déterminer la force exercée par chaque ressort sur le point matériel M en fonction de la coordonnées x de M.

```{figure} ./images/ressort_exo.png
:name: fig_235
:align: center

```

````
````{dropdown}
 

__Expression des longueurs__

On va exprimer les longueurs (grandeurs positives) de chaque ressort en fonction des coordonnées. On note $l_1 = AM$ et $l_2 = MB$ les longueurs des ressorts.

. Il est conseillé d'utiliser des grandeurs algébriques pour déterminer ces longueurs. Ici, il vient:

\begin{align*}
l_1 = \overline{AM} = \overline{AO} + \overline{OM} = L + x\\
l_2 = \overline{MB} = \overline{MO} + \overline{BM} = L - x
\end{align*}
Les allongements sont donc:

\begin{align*}
\Delta l_1 = l_1 - l_0 = L + x - l_0\\
\Delta l_2 = l_2 - l_0 = L - x - l_0
\end{align*}

```{dropdown} Remarque

__Longueur et allongement__
Il peut être préférable dans certains cas de determiner directement l'allongement directement.
```

__Expression du vecteurs unitaires directeurs__  

Il s'agit d'exprimer ce vecteur dans la base d'étude choisi. Ici, pour le ressort 1, le vecteur unitaire doit être suivant $+ \overrightarrow{e_x}$ pour être orienté vers l'extérieur depuis le point M.

Pour le ressort 2, $\overrightarrow{u_{\Delta}} = - \overrightarrow{e_x}$.


__Expression complète__

Il vient l'expression des forces de rappel appliquées sur le point M:

\begin{align*}
\overrightarrow{F_1} = -k \left(L + x - l_0\right) \overrightarrow{e_x}\\
\overrightarrow{F_2} = k \left(L - x - l_0\right) \overrightarrow{e_x}\\
\end{align*}

````


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
# Généralités sur les actions à distance


__Actions volumiques__
Les actions à distance sont en général des actions volumiques (si elle s'exercent à distance, tous les points du solide sont a priori concernés). La force et le moment résultant découle alors d'une intégration __en volume__ (triple intégrale). Il n'est pas nécessaire de savoir (pour l'instant) calculer ces intégrales.

En général, on donne (ou il doit être connu), un point où le moment résultant est nul (appelé parfois par abus de langage "point d'application").

En général, la force résultante se calcule à partir de l'expression usuelle des forces ponctuelles associées aux actions ponctuelles usuelles (gravitation... )


````{admonition} Exercice Actions à distance usuelles
:class: attention

Les actions à distance usuelles sont:

* l'action électromagnétique: on distinguera l'action du champ électrique et l'action du champ magnétique. L'action de ce dernier fera l'objet d'un chapitre complet en fin d'année car elle possède des propriétés pariculières.
* l'action gravitationnelle: on peut définir un point appelé centre de gravité où le moment est nul. Dans le cas d'un champ de gravitation uniforme ou variant peu sur la taille de l'objet, ce point d'application peut être assimilé au centre d'inertie.
* l'action de la pesanteur: par approximation, le point de moment nul usuel et le centre de gravité, souvent assimilé au centre d'inertie sous l'hypothèse d'un champ uniforme. Dans le cas d'un champ uniforme, __on doit pouvoir caractériser complètement l'action du champ de pesanteur: point de moment nul ET résultante des forces.__

````

# Actions globales de contact

Les actions de contact sont en général surfacique: on va sommer les actions ponctuelles en surface (double intégale) en se restreignant évidemment à la surface de contact ! On ne cherchera pas à calculer ces intégrales. L'expression des caractéristiques de ces actions de contacts se fait de deux manières:

* Cas d'action d'un fluide (liquide ou gaz). Comme on va le voir, on dispose souvent d'expression de la résultante des forces. En première année, on utilise principalement ces actions dans le cadre d'une modélisation ponctuelle du système mécanique de sorte que le moment résultant n'est pas donné (l'action devenant par modélisation...  ponctuelle).
* Cas d'action d'un solide (on parle de liaison). Dans le cadre du programme, les caractéristiques:

* sont inconnues et ne peuvent être déterminées que par l'utilisation de théorème (comme le PFD (ou plutôt TRD... ) qui permet de déterminer certaines composantes des forces et moments résultants.
* possèdent des composantes nulles par hypothèse (cas d'absence de frottements)
* sont établies ou encadrées (inégalité) grâce aux lois de Coulomb (cf. suite)



## Modélisation des actions ponctuelles de contact

````{admonition} Fondamental : Composante tangentielle et composante normale
:class: attention

En un point de contact M entre le système et le solide/fluide (qu'on appellera $\Sigma_{ext}$), l'action ponctuelle (modélisée par la force $\overrightarrow{F}(M)$ peut-être décomposée en deux composantes:

* une composante normale à la surface de contact $\overrightarrow{F_{\perp}}(M)$
* une composante tangentielle à la surface de contact $\overrightarrow{F_{//}}(M)$

```{figure} ./images/contact_modelisation.png
:name: fig_236
:align: center

```
````

````{admonition} Fondamental : Interprétation des composantes.
:class: attention

La __composante normale__ correspond à une "réaction de non interpénétration", le système extérieur tend à pousser le système au point M. Cela peut-être une tendance légère (cas d'un système extérieur déformable) ou une contrainte forte (le mouvement du système étudié dans la direction normale au point de contact est alors nul. Au jouant sur la géométrie du contact dans le second cas, on arrive à créer des __liaisons__ dont les mouvements possibles (__degré de liberté__) sont définies précisément (surface de contact cylindrique conduit à un pivot glissant, surface de contact plan sur plan conduit à...  un mouvement plan).

Il vient que (sauf cas de surface adhésive non étudié dans le cadre du programme), la composante normale de la force modélisant l'action ponctuelle du système $\Sigma_1$ sur le système $\Sigma_2$ en un point de contact M est toujours dirigée __vers l'intérieur du système____$\Sigma_2$__ (qui subit l'action).

La __composante tangentielle__ correspond à une action s'opposant au __mouvement relatif__ des deux systèmes en contacts (ou à la mise en mouvement relatif). On parle de __frottements__ (fluide ou solide suivant le cas). Lorsqu'on point M de contact, la composantre tangentielle s'oppose à la vitesse du système $\Sigma_2$ par rapport au système $\Sigma_1$ ($\overrightarrow{v}(M \in \Sigma_2 / M \in \Sigma_1)$. Lorsqu'il y a immobilité, elle s'oppose à la mise en mouvement (ou est nulle cf. suite).
````


Il n'y a pas d'expression simple a priori de cette action ponctuelle qui dépend de la géométrie au point de contact mais aussi du reste du contact, des autres actions qui s'appliquent sur les deux systèmes, de la nature des matériaux qui forment le système... 

On peut néanmoins obtenir plusieurs informations sur la force et moment résultant de l'action globale suivant les cas (solides ou fluide, géométrie du contact... ). C'est ce que nous ferons par la suite.


## Action d'un fluide

### Modélisation de l'action d'un fluide


__Interprétation des composantes__
La composante normale de l'action d'une fluide est appelé force(action) de __pression__. Un chapitre complet sera destiné à l'étude des forces de pression. Dans le cadre actuel de la mécanique, on se bornera à citer son existence.

La composante tangentielle de l'action d'un fluide correspond aux __frottements__ fluides. Comme il sera expliqué en deuxième année, cette composante tangentielle est toujours fonction du différentiel du vitesse au voisinage du point de contact. En première année, le fluide étant supposé au repos loin du système mobile, cela ramène à dire que la composante tangentielle est fonction de la vitesse du système étudié dans le référentiel d'étude. On distingue deux cas:

* le système est en translation dans le fluide. On travaille alors (dans le cadre du programme de première année) avec un modèle de point matériel pour le système et on donne directement la force exercée par le fluide appelée force de frottements (la composante normale représentant les forces de pression n'a plus de sens pour un point matériel). Celle-ci est toujours opposée à la vitesse. Il existe plusieurs expressions qui seront discutées par la suite.
* le système est en rotation autour d'un axe fixe et donc en rotation par rapport au fluide. On donne alors le moment résultant de l'action du fluide sur le système calculé sur l'axe de rotation. Correspondant à des frottements, ce moment s'oppose à la vitesse angulaire $\dot \theta$ du fluide. En général (cas dit laminaire), le moment sur l'axe a pour expression $- K \dot \theta$.


### Expression de la force de frottements fluides


__Type de régimes__
La force de frottements fluide va dépendre du comportement du fluide qui de la géométrie du système (même si quand on passe à une modélisation ponctuelle du système cette dépendance reste) et à sa vitesse par rapport au fluide ainsi qu'à la __viscosité__ du fluide.

On distingue deux types de régimes extrêmes: le régime laminaire (aux faibles vitesses) où l'écoulement du fluide épouse la forme de l'obstacle (ici le système mobile) et le régime turbulant (aux fortes vitesses) où l'écoulement du fluide possède un caractère tourbillonnaire (vortex). La transition du premier régime au second régime n'est pas brusque et des phénomènes très particuliers peuvent se produire pour des vitesses intermédiaires (ces cas ne seront pas étudiés en classe préparatoire).


````{admonition} Fondamental : Force de frottements fluide - Cas laminaire
:class: attention

Aux faibles vitesses, la force de frottements fluides est proportionnelle à la vitesse du fluide: $\overrightarrow{F} = - \lambda \overrightarrow{v_{systeme/fluide}}$. Cette expression est valable pour un système en translation. Dans le cas d'un système en rotation au tour d'un axe fixe, c'est le moment sur l'axe qui est opposé à la vitesse angulaire.
````

````{admonition} Fondamental : Force de frottements fluide - Cas turbulent
:class: attention

Aux fortes vitesses, la force de frottements fluides est proportionnelle au carré de la vitesse du fluide: $\overrightarrow{F} = -k \left \| v\right \| \overrightarrow{v}$. Cette expression est valable pour un système en translation. Le cas d'un système en rotation ne sera pas traité.
````

## Action de contact solide

### Lois phénoménologiques de Coulomb


Il n'y a pas de modèle théorique complet permettant de déterminer les actions de contact solide. Il existe par contre une loi phénoménologique (déduite de l'expérience) qui permet de les modéliser. Plus précisément, on va, au niveau __des actions ponctuelles__, relier la composante normale et la composante tangentielle.


````{admonition} Fondamental : Lois phénoménologiques de Coulomb
:class: attention

En un point de contact solide-solide, la force de contact $\overrightarrow{R}$ se décompose en deux composantes, l'une tangentielle $\overrightarrow{R_T}$ et l'autre normale $\overrightarrow{R_N}$ ($\overrightarrow{R} = \overrightarrow{R_N} + \overrightarrow{R_T}$). On déduit expérimentalement les comportements suivants:

* La composante normale est telle qu'elle empêche l'interpénétration des systèmes (contrainte cinématique). Elle est dirigée vers l'intérieur du solide qui subit l'action. Son annulaion signifie la perte de contact.
* en cas d'immobilité relative des deux solides, L'action complète est telle qu'elle permet l'immobilité relative (somme des forces nulle ET somme des moments nulle si l'on est dans un référentiel galiléen). La composante tangentielle est de norme nécessairement __inférieure__ à $\left \| \overrightarrow{R_T}\right \| < \mu_S \left \| \overrightarrow{R_N}\right \|$ où $\mu_S$ est appelé coefficient de frottement statique. Lorsque cette condition est mise en défaut, alors le système se met en mouvement.
* en cas de mouvement relatif des deux solides (on dit qu'il y a glissement au point M), la composante tangentielle s'oppose à la vitesse relative au point M. Sa norme est __égale__ à $\left \| \overrightarrow{R_T}\right \| = \mu_D \left \| \overrightarrow{R_N}\right \|$ où $\mu_D$ est appelé coefficient de frottement dynamique.
* Quelque soit le système, $\mu_D < \mu_S$, c'est-à-dire qu'il est plus facile de maintenir un solide en mouvement par rapport à un autre solide malgré les frottements que de mettre en mouvement le solide.
````

````{attention}

Il faut faire attention à plusieurs points:

* la condition d'immobilité est une __inéquation__. Elle ne permet PAS de déterminer la force ou le moment de l'action. Ces derniers se détermine par application des théorèmes fondamentaux dans un cas statique (immobilité relative des deux solides).
* Dans tous les cas, la composante normale se déduit de la contrainte cinématique imposée.
* La condition de contact est importante pour déterminer s'il y a décollement.
* Il faut faire attention à l'orientation de la composante tangentielle qui change en fonction de la vitesse. Cela signifie qu'on doit souvent faire l'étude du mouvement par phase en fonction du sens de déplacement.

````


__Modélisation ponctuelle__
Dans la plupart des exemples qui seront données en première année, les lois de Coulomb seront appliquées à des systèmes en translation modélisés par des points matériels. Dans ces conditions, seule la force résultante (qui se résume à une force ponctuelle puisque le système est ...  ponctuel) est utile (et le point d'application qui devient évident). Les composantes normales et tangentielles sont alors définies par rapport au support en contact.

On peut néanmoins noter que par intégration des données précédentes, on pourrait étudier (HP) des actions résultantes sur un système de points matériels dans des mouvements plus complexes.


### Liaisons normalisée et géométrie

````{admonition} Exercice Liaison et géométrie
:class: attention

Les caractéristiques d'une action de contact solide __résulante__ vont dépendre de la géométrie de la surface de contact. En effet, certaines géométries vont empêcher certains mouvements. Cela signifie que la force résultante et le moment résultant peuvent être non nuls pour empêcher ces mouvements.

Par exemple, deux solides $\Sigma_1$ et $\Sigma_2$ dont la surface de contact est une sphère (ou portion de sphère) ne peuvent que tourner l'un par rapport à l'autre, les mouvements de translation relatifs (sans perte de contact) sont impossibles. Si une autre action $\mathfrak{A}_{ext \to \Sigma_1}$ extérieur tend à faire translater le solide $\Sigma_1$, alors l'action de $\Sigma_2$ sur $\Sigma_1$ va tendre à s'opposer à l'action $\mathfrak{A}_{ext \to \Sigma_1}$.

A l'inverse la géométrie de la surface de contact va laisser des mouvements possibles, on parle de degré de liberté de la liaison. Dans l'exemple précédente, toutes les rotations sont possibles.

__On ne peut a priori déduire des degrés de liberté des informations sur la force résultante ou sur le moment résultante__.

Par contre, si __la liaison est sans frottements__ (on dit que la liaison est parfaite), alors il vient que certaines composantes des éléments modélisant l'action seront nuls: les éléments qui s'opposent au mouvement selon les degrés de liberté. Dans l'exemple précédent, les éléments s'opposant à la rotation relative des solides sont nuls __si la liaison est sans frottements__: c'est le moment résultant exprimé au centre de la sphère de contact.

````


__Liaisons normalisée__
En général, on travaille avec des géométries simples et usuelles pour les surfaces de contact. On parle de liaison normalisée (celle présentée précédemment est la liaison rotule ou sphérique). Ces liaisons seront vues en SI. En physique la seule à connaître est la liaison pivot qui sera présentée par la suite.


### Liaison pivot

````{admonition} Définition : Liaison pivot
:class: tip

La liaison pivot est une liaison où le seul degré de liberté est la rotation entre les deux solides. Elles est réalisée par une surface de contact cylindrique (qui permet une rotation suivant UN axe) fermé latéralement (pour empêcher la translation suivant l'axe de rotation).

En physique, on travaille en générale avec un solide mobile (le rotor) en liaison pivot avec le bati (stator - en général le référentiel associé au bati est un référentiel galiléen __en physique__).

````

````{admonition} Fondamental : Caractéristiques d'une liaison pivot
:class: attention

On rappelle que les caractéristiques modélisant une action globale sont la force et le moment résultant exprimé en un point. En général, pour une liaison pivot, on essaie d'exprimer le moment de la liaison sur un point de l'axe de rotation de la liaison.

A priori, toutes les composantes de la force et du moment résultant __peuvent être non nulles__. On distingue néanmoins:

* les composantes de la force résultante qui peuvent être non nuls pour empêcher les translations. Elles s'opposent à la force résultante des autres actions sur le rotor.
* les composantes du moment résultant dans les directions __perpendiculaires__ à l'axe de rotation empêchent les rotations suivant les autres axes. Elles s'opposent au moment des autres actions sur ces mêmes axes.
* la composante du moment résultant sur l'axe de rotation. Elle agit sur le (seul) mouvement du rotor à savoir le mouvement de rotation suivant l'axe. Elle peut a priori avoir un effet moteur ou résistant suivant l'expression de ce moment.
````

````{admonition} Fondamental : Liaison pivot parfaite
:class: attention

Une liaison pivot parfaite est une liaison pivot sans frottements, le moment résultant de la liaison __sur l'axe de rotation__ est nulle.
````


__Explication__
Dans une liaison pivot, la surface de contact est un cylindre. S'il n'y a pas de frottements, alors il n'y a pas de composantes tangentielles pour chaque action ponctuelles de contact.

Dans le cas des surfaces planes extrêmes, la force ponctuelle est donc suivant l'axe de rotation: son moment est nul.

Dans le cas de la surface latérales en forme de cylindre, la force ponctuelle est dirigée vers l'axe de rotation: son moment est nul.

Il vient que le moment résultant sera nul.


````{admonition} Attention : Erreurs classiques
:class: note

Attention, la nullité du moment sur l'axe __n'est pas liée__ à l'orientation de la force résultante. On rappelle __qu'il n'y a pas de lien directe entre force résultante et moment résultant__.

De même seul le moment suivant l'axe de rotation est nul __dans le cas sans frottements__. Les moments suivant un axe quelconque (perpendiculaire ou même parallèle mais non confondu avec l'axe de rotation) sont a priori non nulle. De même la force résultante est a priori non nulle.

````

### Action d'un fil de torsion


__Fil de torsion__
Un fil de torsion est un fil dont la section n'est pas négligeable et qui peut se tordre suivan son axe. Son élasticité implique qu'il va tendre à se détendre exerçant pour cela un moment à ses extrémités proportionnel à l'angle de torsion.

```{figure} ./images/meca_fil_torsion.jpg
:name: fig_237
:align: center

```


````{admonition} Fondamental : Action d'un fil de torsion
:class: attention

Soit un fil pouvant se tordre suivant son axe. On suppose qu'il ne flambe pas. Pour un angle de torsion $\theta - \theta_0$ du fil, ce dernier exerce à ses extrémités une action dont le moment suivant l'axe de torsion est:

\begin{equation}
\Gamma_{axe} = - C \left(\theta - \theta_0\right)
\end{equation}
où C est appelée constante de torsion du fil.

On remarquera qu'une telle action est sembable à une action de rappel élastique. Pour le ressort, le rappel se fait suivant ue translation. Ici le rappel concerne une rotation.

L'angle $\theta$ repère la torsion du fil. La présence de l'angle $\theta_0$ permet de placer l'origine des angles en un point où le fil est déjà tordu. Cela peut-être utile lorsque l'on étudie plusieurs fil de torsion.

On parle de moment de rappel ou par abus de langage de couple de rappel.
````

````{attention}

Malgré l'appellation abusive qu'on peut trouver de "couple" de rappel, cette action n'est a priori PAS un couple. Il n'y a aucune raison pour que la force résultante de l'action du fil sur le système à ses extrémités soit nulle.

On pourra s'en convaincre en avec le cas d'une masse M suspendue à un fil de torsion. Il n'y a pas de mouvement verticale, donc la composante de la résultante des forces appliqué sur la masse M doit être nulle sur l'axe verticale. Or il y a deux actions: la pesanteur (verticale donc) et l'action du fil de torsion: ce dernier doit avoir une résultante des forces nulle verticalement.

````


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
# Mouvement à force centrales : Généralités

````{admonition} Objectifs
:class: hint
* Déduire du théorème du moment cinétique la conservation du moment cinétique
* Connaître les conséquences de la conservation du moment cinétique: mouvement plan et loi des aires
* Exprimer la conservation de l'énergie mécanique et construire une énergie potentielle effective.
* Décrire qualitativement le mouvement radial à l'aide de l'énergie potentielle.
* Relier le caractère borné à la valeur de l'énergie mécanique
````

Dans tout le chapitre, le système sera un point matériel noté M.


## Intégrale première du mouvement

Une intégrale première du mouvement est une grandeur dépendant de la position et de sa dérivée temporelle et qui est constante au cours du mouvement.

````{admonition} Exercice 
:class: attention

On a vu que pour un système conservatif, l'énergie mécanique, qui ne dépend que de la vitesse (par l'énergie cinétique) et de la position (par l'énergie potentielle) est une intégrale première du mouvement.

````


__Intérêt__
Les intégrales premières du mouvement sont extrêmement importantes car elles permettent d'établir des équations d'ordre 1. On peut alors utiliser comme conditions initiales, non pas les données de positions et de vitesses mais les valeurs de ces intégrales premières du mouvement.


## Mouvement à force centrale: Définition

````{admonition} Définition : Mouvement à force centrale: Définition
:class: tip

Un mouvement à force centrale est un mouvement dont la résultante des forces est toujours dirigée vers un même point O.

````

````{dropdown} Remarque

On appelle le point O le __centre de force__ car en effet le point O est responsable de la force. Suivant que la force soit dirigée vers le point O ou vers l'extérieur, on dira qu'elle est attractive ou répulsive.

````


__Paramétrage__
La symétrie du problème pousse à prendre un repère centré au point O. On pourrait penser qu'un repère sphérique est approprié, mais comme nous le verrons par la suite, un repère cylindrique sera plus apprioprié.


## Conservation du moment cinétique

### Conservation du moment cinétique

````{admonition} Fondamental : Conservation du moment cinétique
:class: attention

Dans un mouvement à force centrale dont le centre de force est le point O, alors le moment cinétique au point O est une intégrale première du mouvement.

Cela signifie qu'il est constant au cours du mouvement.
````


__Démonstration__
On va appliquer au système M le théorème du moment cinétique au point O. La résultante des forces étant portée par la droite OM, son moment en O est nul. Il vient que la dérivée du moment cinétique est nulle: le moment cinétique est donc une constante du mouvement.

Par définition, le moment cinétique dépend de la position et de la vitesse. C'est donc une intégrale première du mouvement.


### Planéité du mouvement

````{admonition} Fondamental : Planéité du mouvement
:class: attention

Un mouvement à force centrale est un mouvement plan: la trajectoire du mobile est contenu dans le plan passante par le centre de force O et perpendiculaire au moment cinétique.
````


__Démonstration__
Nous avons démontré que le moment cinétique était un vecteur constant. Or par définition du moment cinétique, le vecteur position pris au point O est perpendiculaire au moment cinétique. Il vient que le vecteur position est à tout instant perpendiculaire au même vecteur: il est contenu dans le plan passant par O et perpendiculaire au moment cinétique.


````{admonition} Fondamental : Paramétrage
:class: attention

La planéité du mouvement et le caractère centrale de la force explique le choix du paramétrage. Par la suite, on va travailler dans un repère cylindrique centré au point O et d'axe Oz suivant le moment cinétique. On notera le moment cinétique au point O: $\overrightarrow{L_O} = L_O \overrightarrow{e_z}$.

On peut alors exprimer le moment cinétique dans le système de coordonnées:

\begin{align*}
\overrightarrow{L_O} &= \overrightarrow{OM} \wedge m \overrightarrow{v_{M}}\\
&= r \overrightarrow{e_r} \wedge m \left(\dot r \overrightarrow{e_r} + r \dot \theta \overrightarrow{e_{\theta}}\right)\\
&= m r^2 \dot \theta^2 \overrightarrow{e_z}
\end{align*}
On remarquera que le moment cinétique est une donnée constante qui peut être utilisée comme "donnée initiale" comme on le verra par la suite. Son expression montre que l'on relie l'évolution angulaire au rayon. Il vient qu'on par d'un système à 2 degré de liberté (rotation autour de O donné par $\dot \theta$ et éloignement/rapprochement de O donné par $r$) et qu'on lie l'évolution des mouvements. On pourra donc, en introduisant le moment cinétique $L_O$ éliminer la vitesse angulaire dans les équations.
````

### Loi des aires

````{admonition} Fondamental : Loi des aires
:class: attention

Dans un mouvement à force centrale, la vitesse aréolaire, c'est-à-dire l'aire parcourue par le vecteur position par unité de temps est constante.
````


__Démonstration__
Durant un temps dt, le mobile passe du point $M(t)$ au point $M(t+dt)$. L'aire balayée est donc l'aire du triangle $OM(t)M(t+dt)$. L'aire de ce triangle s'écrit:

\begin{align*}
d\mathfrak{A} &= \frac{1}{2} \left\vert \overrightarrow{OM}\wedge\overrightarrow{M(t)M(t+dt)} \right\vert \\
&= \frac{1}{2m} \left\vert \overrightarrow{OM}\wedge m\overrightarrow{v_M}dt \right\vert \\
&= \frac{1}{2m}\left\vert \overrightarrow{L_O} \right\vert dt \\
\frac{\rm{d}\mathfrak{A}}{\rm{dt}} &= \frac{1}{2m} L_O
\end{align*}
Le moment cinétique étant constant, il vient que la vitesse aréolaire est constante. La loi des aires est bien vérifiée.


````{admonition} Définition : Constante des aires
:class: tip

On définit la constante des aires comme la grandeur $C = r^2 \dot\theta$. Dans un mouvement à force centrale, il s'agit évidemment d'une constante et la vitesse aréolaire s'écrit $\frac{\rm{d}\mathfrak{A}}{\rm{dt}} = \frac{1}{2}C$.

````

## Cas conservatifs

### Cas des mouvements conservatifs: généralités

````{admonition} Fondamental : Force centrale conservatives
:class: attention

Une force centrale conservative ne dépend que de la coordonnées radiale. On peut donc écrire $\overrightarrow{F} = F(r) \overrightarrow{e_r}$ et l'énergie potentielle associée $E_p(r)$ est telle que $F(r) = - \frac{\rm{d}E_p}{\rm{dr}}(t)$.
````


__Démonstration__
La force est uniquement suivant $\overrightarrow{e_r}$ par définition d'une force centrale. Il vient (gradient) que les dérivées partielles de l'énergie potentielle par rapport à $\theta$ et z sont nulles: l'énergie potentielle ne dépend que de r. En dérivant, il vient que la force ne dépend aussi que de r.



__Conservation de l'énergie mécanique__
La seule force est conservative, donc l'énergie mécanique est une constante: c'est une intégrale première du mouvement. Comme nous l'avons expliqué, nous n'utiliserons que très rarement des données initiales sur la vitesse et la position. Elles seront remplacées par les données de l'énergie mécanique et du moment cinétique qui sont des constantes du mouvement.

A un instant t quelconque, l'énergie mécanique s'écrit:

\begin{equation}
E_m = \frac{1}{2}m \dot r^2 + \frac{1}{2}m r^2 \dot \theta^2 + E_p(r)
\end{equation}


__Interprétation de l'énergie cinétique.__
L'énergie cinétique se réécrit:

\begin{equation}
E_c = \frac{1}{2}m \dot r^2 + \frac{1}{2}m r^2 \dot \theta^2
\end{equation}
On distingue donc deux termes. La premier correspond à l'éloignement/rapprochement du mobile. On l'appelera énergie cinétique radiale. Le second correspond à la rotation du mobile autour de O, on l'appelera énergie cinétique orthoradiale (ou de rotation).


### Energie potentielle effective


__But__
Le but est d'éliminer la vitesse angulaire pour n'avoir une énergie mécanique s'exprimant uniquement en fonction du rayon et de sa dérivée temporelle. On introduira alors l'énergie mécanique sous la forme:

\begin{align*}
E_m &= E_{c,r} + E_{p,eff}(r)\\
&= \frac{1}{2}m \dot r^{2} + E_{p,eff}(r)
\end{align*}
L'intérêt de pouvoir utiliser la positivité de l'énergie cinétique radiale pour obtenir des informations. Comme nous allons le voir, nous obtiendrons plus d'informations qu'avec la seule positivité de l'énergie cinétique complète.


````{admonition} Fondamental : Expression de l'énergie potentielle effective.
:class: attention

Dans le cadre d'un mouvement à force centrale, on peut réécrire l'énergie mécanique sous la forme:

\begin{align*}
E_m &= E_{c,r} + E_{p,eff}(r)\\
&= \frac{1}{2}m \dot r^{2} + E_{p,eff}(r)
\end{align*}
où l'énergie potentielle effective a pour expression:

\begin{align*}
E_{p,eff}(r) &= E_{c,\theta} + E_{p}(r)\\
&= \frac{1}{2}m r^{2}\dot \theta^{2} + E_{p}(r)\\
&= \frac{L_0^{2}}{2m r^{2}} + E_p(r)\\
&= \frac{mC^{2}}{2r^{2}} + E_p(r)
\end{align*}
où $C$ est la constante des aires et $L_O$ est la composante du moment cinétique.
````


__Interprétation__
Nous allons détailler les caractéristiques qu'on peut déduire de l'énergie potentielle effective mais comme nous l'avons dit, on peut déjà remarquer que $\frac{1}{2}m \dot r^{2}$ est positif ou nul. Cela implique que __l'énergie potentielle effective est nécessairement inférieure à l'énergie mécanique.__

Comme pour le cas des mouvements conservatifs, cela va interdire certaines zones. Mais cette condition est plus contraignante car l'énergie potentielle effective est plus grande que l'énergie potentielle (le terme d'énergie cinétique orthoradiale est positive - strictement si le moment cinétique est non nul).


````{dropdown} Remarque

__Barrière de potentiel en r=0.__
Le terme ajouté $\frac{1mC^2}{2r^2}$ tend vers $+ \infty$ en $r=0$. Cela signifie que ce terme énergétique tend à __empêcher le mobile d'atteindre le centre de force__ en lui opposant une barrière d'énergie infinie.

A partir du moment où le mobile tourne, il faudra une énergie potentielle tendant très rapidement vers $- \infty$, c'est-à-dire que la force doit être __très__ attractive, pour que cette barrière infinie soit compensée et que le centre de force soit accessible. Dans de nombreux cas usuels, la barrière infinie n'est pas compensée.

````

````{dropdown} Remarque

__Effet centrifuge__
De manière plus générale, on remarque que la conservation de l'énergie mécanique permet d'écrire:

\begin{align*}
\frac{\rm{d}E_m}{\rm{dt}} &=0\\
\frac{\rm{d}E_{c,r}}{\rm{dt}} + \frac{\rm{d}E_{p,eff}}{\rm{dt}}&=0\\
m \frac{\rm{d}r}{\rm{dt}}\frac{\rm{d^2}r}{\rm{dt^2}} &= - \frac{\rm{d}E_{p,eff}}{\rm{dr}}\dot r\\
m \frac{\rm{d^2}r}{\rm{dt^2}} &= - \frac{\rm{d}E_{p,eff}}{\rm{dr}}\\
\end{align*}
On observe que la monotonie de l'énergie potentielle effective donne la tendance qu'aura le système à être attiré ou repoussé par le centre de force. Attention: On parle d'une tendance nuancée par l'inertie du système.

Or l'énergie potentielle effective se décompose en deux termes:

* l'énergie potentielle dont la monotonie décrit le caractère attractif ou répulsif de la force
* l'énergie cinétique orthoradiale. Celle-ci est strictement décroissante. Cela signifie que la rotation du mobile autour du point tend à l'éloigner du centre de force: on parlera d'__effet centrifuge__.

Cet effet centrifuge explique la difficulté pour atteindre le centre de force. En effet, plus on se rapproche, plus la vitesse angulaire augmente (conséquence de la conservation du moment cinétique), ce qui rend plus difficile de s'approcher encore.

````

### Analyse semi-qualitatives

#### Positivité de l'énergie cinétique

\begin{rappel}{Energie cinétique radiale}
On rappelle que l'énergie cinétique radiale est nécessairement positive ou nulle. Cela permet de déterminer des zones accessibles. Nous allons préciser ici ce principe en remarquant que les zones accessibles sont un peu particulières. Ici le système est à deux degrés de liberté: sa position radiale et sa position angulaire.
\end{rappel}

````{admonition} Fondamental : Zones accessibles
:class: attention

Les zones où $E_{p,eff}(r) > E_m$ sont inaccessibles. Cela correspond à des __rayons__ inaccessibles soit à des __zones limitées par des cercles.__. Les zones accessibles et inaccessibles sont dont définies comme des zones comprises entre des cercles de centre O où $E_ {p,eff}(r) = E_m$.

Si la trajectoire est limitée par un rayon maximal, l'état sera __lié.__

Si la trajectoire n'est pas limitée par un rayon maximal, l'état sera de __diffusion.__

```{figure} ./images/meca_force_centrale_traj.jpg
:name: fig_257
:align: center

```

Les rayons extrêmes atteints seront données par l'équation $E_{p,eff} = E_m$. De même, le mobile ne peut change la variation de r (passer d'éloignement à rapprochement ou inversement) qu'aux position extrêmes car ce sont les positions où la vitesse __radiale__ s'annule. La trajectoire est y est tangente au cercle.
````

````{admonition} Attention : Positions extrêmes et vitesse
:class: note

Aux rayons extrêmes, __seule la vitesse radiale s'annule__. La vitesse totale n'est __pas nulle__. En effet, si le moment cinétique n'est pas nulle, il vient que la vitesse orthoradiale ne s'annule jamais.

Nous verrons même des exemples où la vitesse sera maximale pour l'un des deux rayons extrêmes.

````

#### Caractéristiques différentes

````{admonition} Fondamental : Minimum d'énergie potentielle effective
:class: attention

__Le minimum d'énergie potentielle effective ne correspond pas à une position d'équilibre possible du système.__ On rappelle que le moment cinétique est non nul, donc il y a toujours le mouvement de rotation.

__Au minimum d'énergie potentielle effective, la vitesse n'est pas non plus maximale__ (cf. remarque précédente). Seule la vitesse radiale y est maximale.

Par contre, si l'énergie mécanique égale la valeur minimale de l'énergie potentielle effective, alors un seul rayon est accessible: __la trajectoire sera donc un cercle__.
````

````{admonition} Fondamental : Mouvement uniforme
:class: attention

Dans le cas d'un mouvement circulaire, la trajectoire est uniforme. En effet, le moment cinétique est conservé et le rayon étant constant, il vient que la vitesse angulaire est aussi constante, soit un mouvement uniforme dans le cas d'un mouvement circulaire.
````

````{dropdown} Remarque

__Cercles__
Bien qu'il n'apparaissent souvent qu'un seul minimume sur les tracés d'énergie potentielle effective, il existe en réalité une infinité de trajectoires circulaires possibles suivant la valeur du moment cinétique. Une variation de ce dernier fait varier le tracé même de $E_{p,eff}(r)$ et donc la position du minimum.

On déduit en général, non pas une valeur de R, mais une relation entre le rayon du cercle et la vitesse (constante on le rappelle) du mobile.

````

#### Forces centrales particulières

````{admonition} Exercice 
:class: attention

On considère une force centrale dont l'énergie potentielle s'écrit comme $E_p = - \frac{K}{r^n}$ avec K réel et n réel.

1. Préciser suivant que K soit positif ou négatif le caractère attractif ou répulsif de la force associée.
1. Représenter l'énergie potentielle effective suivant le signe de K et suivant les valeurs de n ($n \in \mathbb{Z}$) et préciser s'il est possible:
1. d'atteindre l'infini
1. d'atteindre le centre de force
1. d'observer une trajectoire circulaire (on ne demande pas une expression du rayon)

1. Préciser quelles valeurs de K et n correspondent à des cas physiques usuels.

````

_On ne justifiera pas ici les tracés. Il est __vivement conseillé__ d'essayer de les tracer seul._
````{dropdown}
 


```{figure} ./images/meca_force_centrale_Krn.png
:name: fig_258
:align: center

```

Les réponses ne sont pas justifiés.

* Si K est positif et n négatif ou K est négatif et n est positif, la force est répulsive. Sinon la force est répulsive. (S'intéresser à la monotonie de l'énergie potentielle __seule__).
* On distingue différents cas:
* Atteindre l'infini: ce n'est possible que s'il n'y a pas de barrière de potentiel infini en $r=+\infty$. C'est toujours réalisé pour n positif ou pour n négatif et K négatif.
On distinguera le cas répulsif où quelque soit l'énergie mécanique, le système sera dans un état de diffusion des cas attractif où suivant la valeur de l'énergie mécanique, le système sera dans un état lié ou de diffusion.

Si K est positif et n négatif, alors l'énergie potentielle tendant vers l'infini aux grands rayons, le mobile est nécessairement dans un état lié.

* Atteindre le centre de force: ce n'est possible que s'il n'y a pas de barrière de potentiel infini en $r=0$. Le seul cas permettant de compenser l'effet centrifuge du terme d'énergie cinétique orthoradiale est le cas où K et positif et $n > 2$. Le tracé montre qu'il faut alors une énergie mécanique suffisante car il existe une barrière d'énergie potentielle.
Le cas $n = 2$ est un cas limite permettant les deux possibilités suivantes les valeurs de K et$L_O$.

* l'existence d'une trajectoire circulaire nécessite un extremum d'énergie potentielle. Ce n'est possible que pour une force attractive. Si n est supérieur à 2, cet état a peu de chance d'être observé car un léger écart va l'éloigner de la trajectoire circulaire.

* Cas newtonien (coulombien ou gravitationnelle): $n=1$ (force en $1/r^2$). Cas de Van der Waals: $n=6$ (force en $1/r^7$) en tenant compte des aspects statistiques.

````

## Cas d'une force de rappel élastique

````{admonition} Exercice 
:class: attention

On s'intéresse au cas d'un point matériel M relié à un ressort de raideur k et de longueur à vide nulle. Il est libre de se mouvoir dans toutes les directions de l'espace. On néglige l'action de la pesanteur. On pose un repère cylindrique de sorte que les conditions initiales soient:

\begin{align*}
\overrightarrow{OM}(t=0) = r_0 \overrightarrow{e_r}\\
\overrightarrow{v_M}(t=0) = v_1 \overrightarrow{e_r} + v_0 \overrightarrow{e_{\theta}}
\end{align*}
1. Justifier la conservation du moment cinétique et de l'énergie mécanique.
1. Déterminer l'expression de ces deux grandeurs en fonction des conditions initiales.
1. Montrer que l'énergie mécanique se ramène à la dépendance du rayon r seul en introduisant une énergie potentielle effective. Discuter de la nature du mouvement. Que se passe-t-il si  $v_0=0$?
1. Déterminer les rayons extrêmaux ainsi que la vitesse maximale du mobile.
1. Déterminer la relation entre $v_0$ et $r_0$ pour observer un mouvement circulaire. Commenter le caractère uniforme/accéléré/décéléré d'un tel mouvement.

````
````{dropdown}
 


__Elément de réponse__
On ne donne pas ici les réponses complètes:

\begin{enumerate}
* Appliquer le théorème du moment cinétique puis le théorème de l'énergie cinétique.
* $L_O = mr_0 v_0$ et $E_m = \frac{1}{2}m (v_1^2 +v_0^2)+ \frac{1}{2}k r_0^2$
* On montrera que le système est toujours dans un état lié. Si la vitesse orthoradiale est nulle initialement, elle le restera et le moment cinétique est nul. Le mouvement est alors rectiligne et symétrique en O le centre de force (pas de barrière de potentiel en r=0).
* L'équation $E_m =E_{p,eff}$ aboutit à la résolution d'un trinôme du second degré.
* La conservation du moment cinétique implique que le mouvement est uniforme. $v_0 = \sqrt{\frac{k}{m}}r_0$


```{dropdown} Remarque

__Traitement complet__
En pratique, on traite le cas de l'oscillateur spatial étudié ici différemment en utilisant un système de coordonnées cartésien. Cela permet de montrer que la trajectoire est elliptique.

```
````

## Travaux dirigés

### Point matériel lié à un fil

````{admonition} Exercice 
:class: attention

Un point matériel M de masse m se déplace sans frottement sur un plan horizontal. Il est attaché à un fil de masse négligeable. Le plan est percé au point O choisi pour origine, le fil traverse le plan en O; un opérateur exerce sur l'autre extrémité du fil une force de traction de module F constant.

A t=0, le point M se trouve sur l'axe Ox à une distance D de O, sa vitesse est alors $V_0$, colinéaire à Oy.

1. Montrer que le moment cinétique $\overrightarrow{L_O}$ en O de M se conserve pendant toute la durée de la traction. Calculer son module et sa direction. Définir la vitesse aréolaire et montrer que le mouvement de M se fait suivant la loi des aires, à savoir que la vitesse aréolaire est constante. 
1. Déterminer l'énergie mécanique $E_m$ de M; on montrera que la force de traction dérive d'une énergie potentielle $E_p$ que l'on exprimera en utilisant les coordonnées cylindriques. On prendra $E_p=0$ pour $OM=0$.
1. Montrer que l'on peut se ramener à un problème à un degré de liberté et définir une fonction énergie potentielle effective. 
1. Etudier ses variations en fonction de r=OM. Montrer qu'elle passe par un minimum pour $r_1 = \left(\frac{m V_0^2 D^2}{F}\right)^{1/3}$.
1. Tracer le graphe correspondant et faire apparaître l'énergie mécanique. Déterminer graphiquement les deux distances extrêmes de M à O; à quelle condition sur F la position initiale est-elle le point de la trajectoire le plus éloigné de O? Le point matériel peut-il arriver jusqu'à O?
1. Quelle valeur donner à F pour observer un mouvement circulaire? Montrer qu'il est alors nécessaire uniforme.

````

### Mouvemnt d'une bille dans un cône

````{admonition} Exercice 
:class: attention

On considère un matériel M glissant sans frottements à l'intérieur d'un cône dont la génératrice fait un angle $\alpha$ avec l'axe Oz vertical dirigé vers le haut, O étant le sommet du cône. On suppose le champ de pesanteur uniforme $\overrightarrow{g} = - g \overrightarrow{e_z}$. On se place en coordonnées cylindriques d'axe Oz et de centre O. On travaille dans le référentiel terrestre qu'on supposera galiléen.

1. Déterminer la relation entre les coordonnées r et z. En déduire l'expression de la vitesse $\overrightarrow{v}$ et de l'accélération $\overrightarrow{a}$ en fonction de r et $\theta$.
1. En déduire, en utilisant le principe fondamental de la dynamique que:

$$M \ddot r = - \frac{mg}{tan \alpha} + mr \dot \theta^2$$
avec $M = m (1+ \frac{1}{\tan^2 \alpha})$

3. Exprimer le moment cinétique $\overrightarrow{J_O}$ par rapport au point O en fonction de $m, r, z$ et $\theta$. Montrer que la composante suivant Oz, notée $J_z$ est conservée au cours du mouvement.
1. En exprimant $\dot \theta$ en fonction de $J_z$, montrer que l'équation différentielle sur r peut s'écrire sous la forme: $M \ddot r = - \frac{dV_{eff}(r)}{dr}$
où $V_{eff}(r)$ est un potentiel effectif que l'on exprimera en fonction de $\alpha$, m,g, et $J_z$. Tracer les allures de $V_{eff}(r)$ pour $J_z = 0$ et pour $J_z \neq 0$.

ATTENTION: Nous allons à partir de ce point réaliser une étude à partir du potentiel effectif comme elle a été faite en cours pour le cas des mouvements à force centrale. On remarquera néanmoins que le mouvement n'est PAS ici un mouvement à force centrale. On pourra s'en convaincre en remarquant par exemple que la composante du moment cinétique projeté sur $\overrightarrow{e_{\theta}}$ n'est pas conservée (TMC) ou simplement parce que le mouvement n'est pas plan. La méthode d'analyse mathématique ne reste pas moins utilisable A CONDITION DE PROUVER QU'ON PEUT L'UTILISER.

5. Calculer l'énergie mécanique et montrer qu'elle peut s'écrire sous la forme: $E_m = \frac{1}{2} M \dot r^2 + V_{eff}(r)$. Justifier le fait que l'énergie mécanique est conservée. On vérifiera que cette conservation permet bien de retrouver l'équation différentielle établie à la question précédente.
5. On s'intéresse uniquement aux trajectoires dont les conditions initiales sont de la forme $r(0) = r_0, \overrightarrow{v}(0) = v_0 \overrightarrow{e_{\theta}}$.
    1. Exprimer $J_z$ en fonction de ces conditions initiales. 
    1. A quelle condition sur $v_0$ la bille atteint-elle le fond du cône? Quelle est alors la trajectoire.
    1. Déterminer $v_0$ pour que la trajectoire soit un cercle de rayon $r_0$ et d'altitude constante.
    1. Montrer graphiquement que dans le cas général et si $J_z \neq 0$ le mouvement est dans un état lié dont les rayons extrêmes sont $r_{\min}$ et $r_{\max}$ qu'on repérera graphiquement.

````



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
# Théorèmes en mécanique du solide

## Théorème de la résultante cinétique

_Le but est de voir comment on peut appliquer le principe fondamental de la dynamique à un système de points matériel. On peut l'énoncer de manière identique mais comme on va le voir, on peut "simplifier" légèrement son énoncé._

_Forces extérieures et intérieures_
On rappelle que pour un système de points matériels (solide déformable ou indéformable), on distingue les forces __intérieures__ exercées par une partie du système sur une autre partie du système et les forces __extérieures__ exercées par le milieu extérieur sur le système.

````{important} __Théorème de la résultante dynamique__

La dérivée temporelle de la quantité de mouvement total d'un système de points matériel dans un référentiel galiléen est égale à la somme des forces __extérieures__ qui s'appliquent sur le solide.
````

````{topic} Démonstration
>Considérons chaque point $M_i$ de masse $m_i$du système. On peut appliquer le principe fondamental de la dynamique à chaque point. Le bilan des forces sur un point $M_i$ se divise en deux parties: les actions extérieures, modélisées par des forces $\overrightarrow{F}_{ext \to M_i}$ et les actions intérieures au système. Si l'on somme tous ces PFD, il vient:
>
>* le terme de gauche est la somme des dérivées des quantités de mouvement soit la dérivée de la quantité de mouvement totale.
>* le terme de droite contient la somme de toutes les actions extérieures au système (qui seront regroupées en actions résultantes) et la somme des actions intérieures. Or pour chaque action du point $M_j$ sur le point $M_i$ à l'intérieur du système, il y aura aussi l'action du point $M_i$ sur le point $M_j$ et le principe des actions réciproques implique que les forces associées à ces deux actions sont opposées: elles vont s'annuler. De cette somme, il ne restera donc bien que la résultante des forces extérieures.
````

````{sidebar} Insuffisance du théorème de la résultante cinétique (TRC)

En somment les PFD, on perd les points d'application des forces ce qui rend le TRC insuffisant a priori pour décrire complètement le mouvement d'un solide. En effet, le TRD __ne donne que le mouvement du centre d'inertie (mouvement de translation globale du système)__. Il ne donne pas d'information sur la déformation du système, ni même sur sa rotation sur lui-même (ou autour d'un autre point).

Le TRD, ne sera suffisant que si le mouvement est une translation pure (et on retrouve l'idée de modélistion ponctuelle du système).

````
````{topic} Conséquences
Une des conséquences est qu'il n'est pas nécessaire de tenir compte des actions intérieures, ce qui simplifie énormément le problème car ces dernières sont très nombreuses et souvent d'expression inconnues (on pensera aux actions de cohésion d'un solide).

De plus, ce théorème de la résultante cinétique justifie la possible modélisation d'un système en volume par un point matériel qui sera le centre d'inertie. En effet, par la modélisation en point matériel, on perd complètement l'information sur les actions intérieures. Mais vu qu'elle n'agit pas sur la quantité de mouvement total, on ne perd rien. De plus, la quantité de mouvement totale égale la masse totale multipliée par la vitesse du centre d'inertie, donc assimiler le système au centre d'inertie donnera la même information.
````

## Théorème du moment cinétique: Application au solide.

````{important} __TMC appliqué à un solide.__

La dérivée temporelle du moment cinétique d'un système de points matériel par rapport à un point/un axe fixe dans un référentel $\mathfrak{R}$ est égal à la somme du moment des actions extérieures calculé au point point/axe.
````

````{topic} Démonstration
>__Démonstration__
>On va démontrer le cas du TMC par rapport à un point A. Le cas sur une axe étant similaire. Comme pour le cas du TRC, on peut appliquer le théorème du moment cinétique à chaque point $M_i$ du système. On distingue encore les actions extérieures et les actions intérieures. On rappelle que pour deux points $M_i$ et $M_j$ du système. Les forces de $M_i$ sur $M_j$ et de $M_i$ sur $M_j$ sont opposées et portées par la droite $M_i M_j$.
>
>On somme l'ensemble des théorèmes du moment cinétique ponctuels et on s'intéresse aux actions intérieures. On va particulariser les moments des actions de $M_i$ sur $M_j$ et de $M_j$ sur $M_i$. La somme donne:
>
>\begin{align*}
\overrightarrow{M_{A/\mathfrak{R}}\left(\overrightarrow{F_{M_j\to M_i}}\right)} + \overrightarrow{M_{A/\mathfrak{R}}\left(\overrightarrow{F_{M_i\to M_j}}\right)} &= \overrightarrow{AM_i} \wedge \overrightarrow{F_{M_j\to M_i}} + \overrightarrow{AM_j} \wedge \overrightarrow{F_{M_i\to M_j}}\\
&= \left(\overrightarrow{AM_i} - \overrightarrow{AM_j}\right) \wedge \overrightarrow{F_{M_j\to M_i}}\\
&= \overrightarrow{M_j M_i} \wedge \overrightarrow{F_{M_j\to M_i}}\\
&= 0
\end{align*}
>Le dernier produit vectoriel est nul car la troisième loi de Newton donne que la force de $M_j$ sur $M_i$ est portée par la droite $M_j M_i$. Il vient que le moment résultant des actions intérieures est nul.
````

````{sidebar} TMC et TRC
Pour un système de points matériels, le TMC __ne se déduit pas__ du théorème de la résulante cinétique.

Les deux théorèmes vont être complémentaires: le premier donne le mouvement du centre d'inertie et le second le mouvement de rotation autour de l'axe considéré.
````
```{topic} __Interprétation__

Le moment cinétique d'un solide contient deux termes: l'information sur la rotation du centre d'inertie autour de l'axe d'étude et l'information sur la rotation du solide sur lui-même. Dans le cadre du programme, le moment cinétique se ramènera directement à l'information sur la rotation su solide complet autour de l'axe fixe considéré.

Dans ce cadre, l'interprétation du moment cinétique reste la même: on relie le mouvement de rotation sur l'axe à l'influence des actions extérieures sur ce mouvement (par le moment résultant de ces actions).
```

## Energétique

### Travail d'une action globale

````{important} __Travail et puissance d'une action globale__

Le travail (élémentaire ou fini) d'une action globale est la somme des travaux (élémentaires ou fini) de chaque action ponctuelle.

La puissance transmise par une action globale dans un référentiel donné est la somme des puissances transmises par chaque action ponctuelle dans le même référentiel.

````

````{topic} Calcul et interprétation
On ne donne pas de méthode de calcul générale car on ne calculera pas __pour l'instant__ de sommation des travaux et puissance d'une action globale. On verra des expressions simplifiées dans les cas de translation et rotation.

On peut par contre toujours interprêter ces grandeurs comme des échanges énergétiques. Comme on le verra avec le théorème de l'énergie cinétique, ces échanges vont faire varier l'énergie cinétique du système. La limite de cette interprétation dans le cas général est que pour un solide, cette influence peut agir sur l'énergie cinétique associée à la translation, associée à la rotation, ou à la déformation du système.

Nous allons simplement traiter les deux premiers cas de manière mathématisée. Certains cas correspondant à la déformation seront présentés par la suite.
````


#### Cas particuliers.

````{important} __Cas d'un solide en translation (à connaître)__

Dans le cas d'un solide indéformable en translation, la puissance transmise par une action globale peut se réécrire comme $P_{\mathfrak{R}} = \overrightarrow{F} \cdot \overrightarrow{v_{M/\mathfrak{R}}}$ avec M un point quelconque du solide (on prend en général le centre d'inertie mais de toute façon, tous les points ont la même vitesse puisque le solide est en translation) et $\overrightarrow{F}$ la force résultante de l'action globale.

Le travail élémentaire s'écrit $\delta W = \overrightarrow{F} \cdot \overrightarrow{dOM}$ avec M un point quelconque du solide.
````

````{topic} Démonstration (cette démonstration n'est pas à connaître)__
>Considérons une action globale d'un système $\Sigma_{ext}$ sur le système étudié $\Sigma$ décomposée en une somme d'action ponctuelle sur les points M de $\Sigma$. On modélise chaque action ponctuelle par une force $\overrightarrow{F_{\Sigma_1 \to M}}$, le puissance transmise par l'action ponctuelle s'écrit $\overrightarrow{F_{\sigma \to M}} \cdot \overrightarrow{v_M}$. On remarquera que la vitesse de tous les points M est identique (on la notera $\overrightarrow{v_{trans/\mathfrak{R}}}$).
>
>\begin{align*}
P_{/\mathfrak{R}}(\mathfrak{A_{globale}}) &= \sum\limits_{M} \left(\overrightarrow{F_{\Sigma_1 \to M}} \cdot \overrightarrow{v_{M/\mathfrak{R}}}\right)\\
&=\sum\limits_{M} \left(\overrightarrow{F_{\Sigma_1 \to M}}\right) \cdot \overrightarrow{v_{trans/\mathfrak{R}}}\\
&= \overrightarrow{F_{\Sigma_1 \to \Sigma}} \cdot \overrightarrow{v_{trans/\mathfrak{R}}}
\end{align*}
>La démonstration pour le travail est identique.
````

````{important} __Cas d'un solide en rotation autour d'un axe fixe (à connaître)__

Dans le cas d'un solide indéformable en rotation autour d'un axe $\Delta$ fixe dans un référentiel $\mathfrak{R}$, la puissance transmise par une action globale peut se réécrire comme $P_{\mathfrak{R}} = M_\Delta \omega_\Delta$ avec $\omega_\Delta$ la vitesse angulaire de rotation du solide autour de l'axe $\Delta$ (__c'est une grandeur algébrique__) et $M_\Delta$ le moment résultant de l'action globale sur l'axe $\Delta$.

Le travail élémentaire s'écrit $\delta W = M_\Delta d\theta_\Delta$ avec $d\theta_\Delta$ une variation infinitésimale de l'angle $\theta_\Delta$ orienté suivant $\Delta$ et représentant la rotation du solide autour de l'axe.
````

````{topic} Démonstration (cette démonstration n'est pas à connaître)__
>Considérons une action globale d'un système $\Sigma_{ext}$ sur le système étudié $\Sigma$ décomposée en une somme d'action ponctuelle sur les points M de $\Sigma$. On modélise chaque action ponctuelle par une force $\overrightarrow{F_{\Sigma_1 \to M}}$, le puissance transmise par l'action ponctuelle s'écrit $\overrightarrow{F_{\sigma \to M}} \cdot \overrightarrow{v_M}$. On remarquera que la vitesse de tous les points M peut s'écrire (solide en rotation) $\overrightarrow{v_M} = \overrightarrow{\Omega} \wedge \overrightarrow{OM}$ (O est un point de l'axe et $\overrightarrow{\Omega}$ le vecteur taux de rotation).
>
>\begin{align*}
P_{/\mathfrak{R}}(\mathfrak{A_{globale}}) &= \sum\limits_{M} \left(\overrightarrow{F_{\Sigma_1 \to M}} \cdot \left(\overrightarrow{\Omega}\wedge \overrightarrow{OM}\right)\right)\\
P_{/\mathfrak{R}}(\mathfrak{A_{globale}}) &= \sum\limits_{M} \left(\overrightarrow{\Omega} \cdot \left(\overrightarrow{OM} \wedge \overrightarrow{F_{\Sigma_1 \to M}}\right)\right)\\
P_{/\mathfrak{R}}(\mathfrak{A_{globale}}) &= \overrightarrow{\Omega} \cdot \sum\limits_{M} \left(\overrightarrow{M_{O}}\left(\overrightarrow{F_{\Sigma_1 \to M}}\right)\right)\\
P_{/\mathfrak{R}}(\mathfrak{A_{globale}}) &= \omega_{\Delta} \overrightarrow{u_{\Delta}} \cdot \overrightarrow{M_{O}}\left(\overrightarrow{F_{\Sigma_1 \to \Sigma}}\right)\\
P_{/\mathfrak{R}}(\mathfrak{A_{globale}}) &= \omega_{\Delta} M_{\Delta}\left(\overrightarrow{F_{\Sigma_1 \to \Sigma}}\right)
\end{align*}
````

#### Forces conservatives
Il existe des forces globales conservatives. Le travail global peut alors être écrit comme l'opposé d'une fonction (énergie potentielle) ne dépendant que de la position du solide.

#### Cas usuels

````{sidebar} Liaison pivot. Cas général
Dans le référentiel du stator, la puissance transmise au rotor par l'intermédiaire de la liaison pivot s'écrit comme on la vue précédemment au moyen du moment sur l'axe et de la vitesse angulaire.
````
````{important} __Cas d'une liaison parfaite.__

Si la liaison pivot est parfaite, alors la puissance (et le travail) transmis par la liaison pivot dans le référentiel du stator est nulle. La preuve est triviale.
````

````{important} __Action de la pesanteur__

L'action de la pesanteur dérive d'une énergie potentielle. Si le champ de pesanteur est uniforme : $E_p  = mg z_G$ où $z_G$^est __l'altitude__ du centre d'inertie G.
````

````{important} __Action d'un fil de torsion__
L'action d'un fil de torsion de constante de torsion $C$ dérive d'une énergie potentielle dont l'expression est:

$$
E_p = \frac{1}{2} C (\theta - \theta_0)^2
$$
où $\theta - \theta_0$ est l'angle de torsion du fil.
````

### Théorèmes énergétiques

````{important} __Théorème de l'énergie cinétique/mécanique. Cas général.__

La variation d'énergie cinétique d'un système de points d'un état A à un état B est égale au travail des forces qui s'appliquent sur le système sur le même chemin, qu'elles __soient extérieures ou intérieures__.

La variation d'énergie mécanique d'un système de points d'un état A à un état B est égale au travail des forces non conservatives qui s'appliquent sur le système sur le même chemin, qu'elles __soient extérieures ou intérieures__.
````

````{margin}
Cette fois, on __doit tenir compte des actions intérieures__ dont le travail est a priori non nul.
````

````{important} __Théorème de l'énergie cinétique/mécanique. Cas d'un solide indéformable.__

Dans le cas d'un solide __indéformable, le travail des forces intérieures est nul.__
````

````{admonition} Démonstration
:class: note
>Nous allons démontrer que dans le cas général le travail des forces intérieures est a priori non nul et qu'il s'annule dans le cas d'un solide indéformable.
>
>Considérons deux points $M_1$ et $M_2$ du solide en interaction. On note $\overrightarrow{f_{1 \rightarrow 2}}$ la force exercée par $M_1$ sur $M_2$ et $\overrightarrow{f_{2 \rightarrow 1}}$ la force exercée par $M_2$ sur $M_1$. On a (troisième loi de Newton): $\overrightarrow{f_{1 \rightarrow 2}} = -\overrightarrow{f_{2 \rightarrow 1}}$. La puissance totale associée à ces deux forces s'écrit:
>
>\begin{align*}
P &= \overrightarrow{f_{1 \rightarrow 2}} \cdot v_{M_2/R} + \overrightarrow{f_{2 \rightarrow 1}} \cdot v_{M_1/R}\\
&= \overrightarrow{f_{1 \rightarrow 2}} \cdot {(\frac{d \overrightarrow{M_1 M_2}}{dt})}_{R}\\
\overrightarrow{f_{1 \rightarrow 2}} &= f_{1 \rightarrow 2} \overrightarrow{u_{1 \rightarrow 2}}\\
\overrightarrow{M_1 M_2} &= M_1 M_2 \overrightarrow{u_{1 \rightarrow 2}}\\
{(\frac{d \overrightarrow{M_1 M_2}}{dt})}_{R} &= \frac{d M_1 M_2}{dt} \overrightarrow{u_{1 \rightarrow 2}} + M_1 M_2 {(\frac{d \overrightarrow{u_{1 \rightarrow 2}}}{dt})}_R
\end{align*}
>où $\overrightarrow{u_{1 \rightarrow 2}}$ est le vecteur unitaire allant de $M_1$ vers $M_2$.
>
>Le première terme correspond à la variation de la distance entre les deux points, le second à la rotation d'un point par rapport à l'autre. La puissance des forces intérieurs pour ces deux points s'écrit donc: $P = f_{1 \rightarrow 2} \frac{d M_1 M_2}{dt}$
>
>Si le mobile se déforme, cette expression est a priori non nulle.
>
>Si le solide est indéformable, cette expression est toujours nulle.
````

````{topic} Cas d'un solide déformable isolé.

Une grandeur conservative est une grandeur qui reste constante lorsque le système est isolé. Initialement, on a construit l'énergie mécanique comme une grandeur conservative. Et cela est vraie pour un point matériel ou un solide indéformable.

Par contre, on remarque que cela n'est plus vrai pour un système indéformable: un système isolé peut voir son énergie mécanique augmenter ou diminuer sous l'influence des forces. Cette limite peut paraître anodine mais elle est l'une des bases de l'élaboration du premier principe de la thermodynamique: on va rechercher une grandeur énergétique plus générale qui restera conservative lorsqu'on tient compte de la déformation du système (fondamentale pour les gaz) en ajoutant à l'énergie mécanique un terme énergétique supplémentaire appelé énergie interne.

A notre échelle, on verra des effets de la déformabilité des solides lorsqu'on étudiera le cas des solides déformables en rotation.

````

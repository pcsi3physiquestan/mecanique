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
# Travail et puissance des actions mécaniques

## Travail et puissance d'une action ponctuelle

````{important} __Définition : Travail élémentaire d'une action ponctuelle__

Considérons une action ponctuelle exercée par un système $\Sigma_1$ sur un point matériel M de masse m et modélisée par une force $\overrightarrow{F}$. On définit le travail élémentaire de cette action sur un déplacement élémentaire $\overrightarrow{dOM}$ par:

\begin{equation}
\delta W (\overrightarrow{F}) = \overrightarrow{F} \cdot \overrightarrow{dOM}
\end{equation}
Ce travail correspond à l'énergie apportée par le système $\Sigma_1$ au système ponctuel M lorsque ce dernier se déplace de manière infinitésimale de $\overrightarrow{dOM}$.

Ce __transfert__ d'énergie __dépend a priori du déplacement élémentaire considéré__.

````

````{important} __Définition : Travail sur un déplacement fini d'une action ponctuelle__

Considérons une action ponctuelle exercée par un système $\Sigma_1$ sur un point matériel M de masse m et modélisée par une force $\overrightarrow{F}$. Si le point M se déplace sur un chemin $\Gamma$. On définit le travail $W(\overrightarrow{F})$ de cette action sur un déplacement fini le long du chemin $\Gamma$ par la somme (intégrale) des travaux élémentaires le long de chemin:

\begin{equation}
W_{\Gamma} (\overrightarrow{F}) = \int_{M \in \Gamma} \overrightarrow{F} \cdot \overrightarrow{dOM}
\end{equation}
Ce travail correspond à l'énergie apportée par le système $\Sigma_1$ au système ponctuel M lorsque ce dernier se déplace sur le chemin $\Gamma$.

Ce __transfert__ d'énergie __dépend a priori du chemin parcouru__.

````

````{important} __Définition : Puissance transmise par une action ponctuelle__

Considérons une action ponctuelle exercée par un système $\Sigma_1$ sur un point matériel M de masse m et modélisée par une force $\overrightarrow{F}$. Si à un instant t, le point M possède une vitesse $\overrightarrow{v_{M/\mathfrak{R}}}$ dans un référentiel $\mathfrak{R}$, on définit la puissance $P_{\mathfrak{R}}(\overrightarrow{F})$ par cette action au système M dans le référentiel $\mathfrak{R}$ par:

\begin{equation}
P_{/\mathfrak{R}} (\overrightarrow{F}) = \overrightarrow{F} \cdot \overrightarrow{v_{M/\mathfrak{R}}}
\end{equation}
Cette puissance correspond à la puissance apportée par le système $\Sigma_1$ au système ponctuel M à un instant t dans le référentiel $\mathfrak{R}$.

Ce __transfert__ d'énergie __dépend a priori du référentiel considéré__.

````


__Action et force__
Lorsqu'il s'agit d'une action ponctuelle, on parle aussi de travail ou puissance d'une force. Tant qu'on fait attention au point d'application, cela ne porte pas à conséquence. Il faut néanmoins garder à l'esprit que cet abus de langage devient très trompeur pour des actions globales où le travail et la puissance d'une action __ne se déduit plus de la force seule.__


````{important} __Fondamental : Relation puissance-travail__

On a la relation suivante pour une même action:

\begin{equation}
P_{/\mathfrak{R}}(\overrightarrow{F}) = \frac{\delta W (\overrightarrow{F})}{\rm{d}t}
\end{equation}
Remarque: Le point pour l'expression du déplacement élémentaire doit être fixe dans $\mathfrak{R}$.

Cette expression se démontre en remarquant que $\overrightarrow{v_{M/\mathfrak{R}}} = \frac{\rm{d}\overrightarrow{OM}}{\rm{dt}}_{\mathfrak{R}}$
````

## Méthode: Calcul du travail d'une force.


Nous allons voir ici la méthode permettant de calculer le travail d'une force. Dans le cadre du programme, le point centrale est le paramétrage. Il permet d'obtenir une expression simple de l'intégrale à calculer.


````{admonition} Exercice 
:class: attention

On considère un point M sur une trajectoire circulaire dans un plan vertical. On repère l'angle $\theta$ que fait le vecteur position $\overrightarrow{OM}$ (O est le centre du cercle) par rapport au point le plus bas du cercle. Déterminer le travail du poids sur M lorsqu'il passe du point $\theta = 0$ au point $\theta = \theta_1$.

````
````{dropdown} Résolution
 
>__Plan du calcul__  
>
>On va détailler le calcul en deux étapes: on calcule le travail infinitésimal sur un déplacement élémentaire le long du cercle pour une position d'angle $\theta$ quelconque. On va alors trouver une expression de la forme $f(\theta)d\theta$. Il suffira alors de l'intégrer en choisissant correctement les bornes d'intégration en fonction du chemin choisi.
>
>
>
>__Travail infinitésimal__
>Le déplacement élémentaire __sur le cercle__ s'écrit $\overrightarrow{dOM} = R d\theta \overrightarrow{e_\theta}$. Quant à la force, elle s'écrit $\overrightarrow{P} = mg \cos \theta \overrightarrow{e_r} - mg \sin \theta \overrightarrow{e_\theta}$. Le travail élémentaire s'écrit donc: $\delta W = -mgR \sin \theta d \theta$
>
>
>
>__Intégration__
>L'expression du travail infinitésimal fait apparaître que l'intégration sera suivant $\theta$ (en effet, c'est en faisant varier cet angle qu'on décrit entièrement la trajectoire de M sur le cercle). Les bornes d'intégration sous le point de départ et d'arrivée soit $\theta = 0$ et $\theta = \theta_1$. Il vient:
>
>\begin{align*}
W &= \int_{\theta=0}^{\theta=\theta_1} - mgR \sin \theta d\theta \\
&= mgR \left(\cos \theta_1 - 1\right)
\end{align*}

```{admonition} Analyse du résultat
:class: hint, dropdown
On pourra vérifier ici l'homogénéité en utilisant le fait que mgz est homogène à une énergie (potentiel de pesanteur). Donc l'expression précédente est bien homogène à un terme énergétique comme doit l'être un transfert d'énergie mécanique (un travail).

On remarquera aussi que ce travail est __négatif__. Ce qui veut dire que le système a perdu de l'énergie sous l'effet du poids. En effet, en montant, il est ralenti: le poids a alors un effet __résistant__. Si le mouvement s'était effectué dans l'autre sens, le travail (transfert d'énergie mécanique) aurait été positif: le système aurait gagné de l'énergie. Le poids aura alors eu un effet __moteur__.
```
````

## Interprétation du travail et de la puissance


__Interprétation__
Comme on l'a dit dans la définit, le travail correspond à l'apport d'énergie sur un trajet donné par le milieu extérieur par l'intermédiaire de l'action considéré. De même la puissance d'une action correspond à la puissance transmise à un instant donné.

On peut distinguer deux cas:

* la puissance transmise est négative. Cela correspond un angle __obtu__ entre la vitesse de M et la force: on est dans une configuration où l'action tend à ralentir le mobile. D'un point de vue énergétique, il lui enlève la puissance. On dit que l'action est __résistante__.
* la puissance transmise est positive. Cela correspond un angle __aigu__ entre la vitesse de M et la force: on est dans une configuration où l'action tend à accélérer le mobile. D'un point de vue énergétique, il lui fournit la puissance. On dit que l'action est __motrice__.

Ces interprétations s'appliquent aussi au travail et la dénomination moteur/résistant restera valable pour des actions résultantes.


## Travail et chemin

````{attention}
__Dépendance et notation__


Le travail d'une action __dépend du chemin considéré__. Il ne s'agit donc PAS de la variation d'une grandeur d'état (c'est-à-dire définie pour un état donné de position et vitesse).

Le travail correspond donc à une grandeur mathématique particulière. Le travail infinitésimal doit donc être noté $\delta W$ (l'important c'est le $\delta$) et le travail sur un déplacement fini W (l'important est l'absence de $\Delta$).

Il est important de faire la différence avec les grandeurs d'état (comme l'énergie cinétique) dont on calcule une __variation__ (notée avec un d ou $\Delta$ suivant que la transformation soit infinitésimale ou finie) et les grandeurs d'échange comme le transfert d'énergie mécanique (ou travail) dont le __transfert__ est noté avec un $\delta$ ou rien.

````

````{admonition} Dépendance
:class: attention

On peut se rendre compte de cette dépendance en prenant le cas d'une action de contact sur un plan horizontal. La loi de Coulomb prévoit que la composante tangentielle est constante est toujours opposée au mouvement. Le travail d'un point A à un point B sera donc dépendant de la distance parcourue pour aller de A à B et donc du chemin parcouru.

````

## Cas des actions globales

### Travail d'une action globale: Définition et expression générale

````{important} __Définition : Travail et puissance d'une action globale__

Le travail (élémentaire ou fini) d'une action globale est la somme des travaux (élémentaires ou fini) de chaque action ponctuelle.

La puissance transmise par une action globale dans un référentiel donné est la somme des puissances transmises par chaque action ponctuelle dans le même référentiel.

````


__Calcul et interprétation__
On ne donne pas de méthode de calcul générale car on ne calculera pas de sommation des travaux et puissance d'une action globale. On verra des expressions simplifiées dans les cas de translation et rotation.

On peut par contre toujours interprêter ces grandeurs comme des échanges énergétiques. Comme on le verra avec le théorème de l'énergie cinétique, ces échanges vont faire varier l'énergie cinétique du système. La limite de cette interprétation dans le cas général est que pour un solide, cette influence peut agir sur l'énergie cinétique associée à la translation, associée à la rotation, ou à la déformation du système.

Nous allons simplement traiter les deux premiers cas de manière mathématisée. Certains cas correspondant à la déformation seront présentés par la suite.


### Travail d'une action globale - Cas particuliers.

````{important} __Fondamental : Cas d'un solide en translation (à connaître)__

Dans le cas d'un solide indéformable en translation, la puissance transmise par une action globale peut se réécrire comme $P_{\mathfrak{R}} = \overrightarrow{F} \cdot \overrightarrow{v_{M/\mathfrak{R}}}$ avec M un point quelconque du solide (on prend en général le centre d'inertie mais de toute façon, tous les points ont la même vitesse puisque le solide est en translation) et $\overrightarrow{F}$ la force résultante de l'action globale.

Le travail élémentaire s'écrit $\delta W = \overrightarrow{F} \cdot \overrightarrow{dOM}$ avec M un point quelconque du solide.
````


>__Démonstration (cette démonstration n'est pas à connaître)__
>Considérons une action globale d'un système $\Sigma_{ext}$ sur le système étudié $\Sigma$ décomposée en une somme d'action ponctuelle sur les points M de $\Sigma$. On modélise chaque action ponctuelle par une force $\overrightarrow{F_{\Sigma_1 \to M}}$, le puissance transmise par l'action ponctuelle s'écrit $\overrightarrow{F_{\sigma \to M}} \cdot \overrightarrow{v_M}$. On remarquera que la vitesse de tous les points M est identique (on la notera $\overrightarrow{v_{trans/\mathfrak{R}}}$).
>
>\begin{align*}
P_{/\mathfrak{R}}(\mathfrak{A_{globale}}) &= \sum\limits_{M} \left(\overrightarrow{F_{\Sigma_1 \to M}} \cdot \overrightarrow{v_{M/\mathfrak{R}}}\right)\\
&=\sum\limits_{M} \left(\overrightarrow{F_{\Sigma_1 \to M}}\right) \cdot \overrightarrow{v_{trans/\mathfrak{R}}}\\
&= \overrightarrow{F_{\Sigma_1 \to \Sigma}} \cdot \overrightarrow{v_{trans/\mathfrak{R}}}
\end{align*}
>La démonstration pour le travail est identique.


````{important} __Fondamental : Cas d'un solide en rotation autour d'un axe fixe (à connaître)__

Dans le cas d'un solide indéformable en rotation autour d'un axe $\Delta$ fixe dans un référentiel $\mathfrak{R}$, la puissance transmise par une action globale peut se réécrire comme $P_{\mathfrak{R}} = M_\Delta \omega_\Delta$ avec $\omega_\Delta$ la vitesse angulaire de rotation du solide autour de l'axe $\Delta$ (__c'est une grandeur algébrique__) et $M_\Delta$ le moment résultant de l'action globale sur l'axe $\Delta$.

Le travail élémentaire s'écrit $\delta W = M_\Delta d\theta_\Delta$ avec $d\theta_\Delta$ une variation infinitésimale de l'angle $\theta_\Delta$ orienté suivant $\Delta$ et représentant la rotation du solide autour de l'axe.
````


>__Démonstration (cette démonstration n'est pas à connaître)__
>Considérons une action globale d'un système $\Sigma_{ext}$ sur le système étudié $\Sigma$ décomposée en une somme d'action ponctuelle sur les points M de $\Sigma$. On modélise chaque action ponctuelle par une force $\overrightarrow{F_{\Sigma_1 \to M}}$, le puissance transmise par l'action ponctuelle s'écrit $\overrightarrow{F_{\sigma \to M}} \cdot \overrightarrow{v_M}$. On remarquera que la vitesse de tous les points M peut s'écrire (solide en rotation) $\overrightarrow{v_M} = \overrightarrow{\Omega} \wedge \overrightarrow{OM}$ (O est un point de l'axe et $\overrightarrow{\Omega}$ le vecteur taux de rotation).
>
>\begin{align*}
P_{/\mathfrak{R}}(\mathfrak{A_{globale}}) &= \sum\limits_{M} \left(\overrightarrow{F_{\Sigma_1 \to M}} \cdot \left(\overrightarrow{\Omega}\wedge \overrightarrow{OM}\right)\right)\\
P_{/\mathfrak{R}}(\mathfrak{A_{globale}}) &= \sum\limits_{M} \left(\overrightarrow{\Omega} \cdot \left(\overrightarrow{OM} \wedge \overrightarrow{F_{\Sigma_1 \to M}}\right)\right)\\
P_{/\mathfrak{R}}(\mathfrak{A_{globale}}) &= \overrightarrow{\Omega} \cdot \sum\limits_{M} \left(\overrightarrow{M_{O}}\left(\overrightarrow{F_{\Sigma_1 \to M}}\right)\right)\\
P_{/\mathfrak{R}}(\mathfrak{A_{globale}}) &= \omega_{\Delta} \overrightarrow{u_{\Delta}} \cdot \overrightarrow{M_{O}}\left(\overrightarrow{F_{\Sigma_1 \to \Sigma}}\right)\\
P_{/\mathfrak{R}}(\mathfrak{A_{globale}}) &= \omega_{\Delta} M_{\Delta}\left(\overrightarrow{F_{\Sigma_1 \to \Sigma}}\right)
\end{align*}

### Cas de la liaison pivot. Cas parfait


__Cas de la liaison pivot. Cas général.__
Dans le référentiel du stator, la puissance transmise au rotor par l'intermédiaire de la liaison pivot s'écrit comme on la vue précédemment au moyen du moment sur l'axe et de la vitesse angulaire.


````{important} __Fondamental : Cas d'une liaison parfaite.__

Si la liaison pivot est parfaite, alors la puissance (et le travail) transmis par la liaison pivot dans le référentiel du stator est nulle. La preuve est triviale.
````


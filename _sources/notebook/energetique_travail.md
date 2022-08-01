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

````{important} __Travail élémentaire d'une action ponctuelle__

Considérons une action ponctuelle exercée par un système $\Sigma_1$ sur un point matériel M de masse m et modélisée par une force $\overrightarrow{F}$. On définit le travail élémentaire de cette action sur un déplacement élémentaire $\overrightarrow{dOM}$ par:

$$
\delta W (\overrightarrow{F}) = \overrightarrow{F} \cdot \overrightarrow{dOM}
$$
Ce travail correspond à l'énergie apportée par le système $\Sigma_1$ au système ponctuel M lorsque ce dernier se déplace de manière infinitésimale de $\overrightarrow{dOM}$.

Ce __transfert__ d'énergie __dépend a priori du déplacement élémentaire considéré__.
````

````{important} __Travail sur un déplacement fini d'une action ponctuelle__

Considérons une action ponctuelle exercée par un système $\Sigma_1$ sur un point matériel M de masse m et modélisée par une force $\overrightarrow{F}$. Si le point M se déplace sur un chemin $\Gamma$. On définit le travail $W(\overrightarrow{F})$ de cette action sur un déplacement fini le long du chemin $\Gamma$ par la somme (intégrale) des travaux élémentaires le long de chemin:

$$
W_{\Gamma} (\overrightarrow{F}) = \int_{M \in \Gamma} \overrightarrow{F} \cdot \overrightarrow{dOM}
$$
Ce travail correspond à l'énergie apportée par le système $\Sigma_1$ au système ponctuel M lorsque ce dernier se déplace sur le chemin $\Gamma$.

Ce __transfert__ d'énergie __dépend a priori du chemin parcouru__.
````

````{important} __Puissance transmise par une action ponctuelle__

Considérons une action ponctuelle exercée par un système $\Sigma_1$ sur un point matériel M de masse m et modélisée par une force $\overrightarrow{F}$. Si à un instant t, le point M possède une vitesse $\overrightarrow{v_{M/\mathfrak{R}}}$ dans un référentiel $\mathfrak{R}$, on définit la puissance $P_{\mathfrak{R}}(\overrightarrow{F})$ par cette action au système M dans le référentiel $\mathfrak{R}$ par:

$$
P_{/\mathfrak{R}} (\overrightarrow{F}) = \overrightarrow{F} \cdot \overrightarrow{v_{M/\mathfrak{R}}}
$$
Cette puissance correspond à la puissance apportée par le système $\Sigma_1$ au système ponctuel M à un instant t dans le référentiel $\mathfrak{R}$.

Ce __transfert__ d'énergie __dépend a priori du référentiel considéré__.
````

````{important} __Relation puissance-travail__

On a la relation suivante pour une même action:

$$
P_{/\mathfrak{R}}(\overrightarrow{F}) = \frac{\delta W (\overrightarrow{F})}{\rm{d}t}
$$
Remarque: Le point pour l'expression du déplacement élémentaire doit être fixe dans $\mathfrak{R}$.

Cette expression se démontre en remarquant que $\overrightarrow{v_{M/\mathfrak{R}}} = \frac{\rm{d}\overrightarrow{OM}}{\rm{dt}}_{\mathfrak{R}}$
````

````{topic} Interprétation
Comme on l'a dit dans la définit, le travail correspond à l'apport d'énergie sur un trajet donné par le milieu extérieur par l'intermédiaire de l'action considéré. De même la puissance d'une action correspond à la puissance transmise à un instant donné.

On peut distinguer deux cas:
* la puissance transmise est négative. Cela correspond un angle __obtu__ entre la vitesse de M et la force: on est dans une configuration où l'action tend à ralentir le mobile. D'un point de vue énergétique, il lui enlève la puissance. On dit que l'action est __résistante__.
* la puissance transmise est positive. Cela correspond un angle __aigu__ entre la vitesse de M et la force: on est dans une configuration où l'action tend à accélérer le mobile. D'un point de vue énergétique, il lui fournit la puissance. On dit que l'action est __motrice__.

Ces interprétations s'appliquent aussi au travail et la dénomination moteur/résistant restera valable pour des actions résultantes.
````

## Travail et chemin

````{attention}
__Dépendance et notation__

Le travail d'une action __dépend du chemin considéré__. Il ne s'agit donc PAS de la variation d'une grandeur d'état (c'est-à-dire définie pour un état donné de position et vitesse).

Le travail correspond donc à une grandeur mathématique particulière. Le travail infinitésimal doit donc être noté $\delta W$ (l'important c'est le $\delta$) et le travail sur un déplacement fini W (l'important est l'absence de $\Delta$).

Il est important de faire la différence avec les grandeurs d'état (comme l'énergie cinétique) dont on calcule une __variation__ (notée avec un d ou $\Delta$ suivant que la transformation soit infinitésimale ou finie) et les grandeurs d'échange comme le transfert d'énergie mécanique (ou travail) dont le __transfert__ est noté avec un $\delta$ ou rien.
````

````{topic} Dépendance
On peut se rendre compte de cette dépendance en prenant le cas d'une action de contact sur un plan horizontal. La loi de Coulomb prévoit que la composante tangentielle est constante est toujours opposée au mouvement. Le travail d'un point A à un point B sera donc dépendant de la distance parcourue pour aller de A à B et donc du chemin parcouru.
````


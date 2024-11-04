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
# Théorèmes énergétiques

## Théorème de l'énergie cinétique

````{important} __Théorème de l'énergie cinétique__

Soit un point matériel M de masse m. La variation d'énergie cinétique du point M dans un référentiel galiléen entre deux instants est égale à la somme du travail de toutes les forces qui s'exercent sur le point M entre les deux instants considérés.

\begin{align*}
\Delta E_{C,A \rightarrow B} &= W_{A \rightarrow B} (\overrightarrow{F})\\
dE_c &= \delta W(\overrightarrow{F})
\end{align*}
où $\overrightarrow{F}$ est la résultante totale des forces s'appliquant sur le point matériel M. La première écriture consiste à appliquer le théorème de l'énergie cinétique sur un chemin fini d'un point A à un point B (on a rappelle que le travail des forces dépend a priori du chemin choisi). La seconde traite le cas d'un déplacement infinitésimal.
````

````{important} __Théorème de la puissance cinétique__

En référentiel galiléen (sous les mêmes hypothèses que précédemment):

\begin{align*}
\frac{\rm{d}E_{c/\mathfrak{R}}}{\rm{dt}} &= P_{/\mathfrak{R}}(\overrightarrow{F})
\end{align*}
````

````{topic} Démonstration
>\begin{align*}
m \frac{d \overrightarrow{v_{M/R}}}{dt} &= \overrightarrow{F}\\
m \frac{d \overrightarrow{v_{M/R}}}{dt} \cdot \overrightarrow{v_{M/R}} &= \overrightarrow{F} \cdot \overrightarrow{v_{M/R}}\\
\frac{d}{dt}(\frac{1}{2} m v^2) &= P_R(\overrightarrow{F})\\
dE_c &= \delta W(\overrightarrow{F})
\end{align*}
L'expression intégrale s'obtient en intégrant la dernière équation sur le chemin choisi.
````


## Théorème de l'énergie mécanique

````{important} __Théorème de l'énergie mécanique__

Dans un référentiel galiléen, la variation d'énergie mécanique d'un point matériel M de masse m entre deux points A et B d'un système est égale au travail des seules forces non-conservatives sur le trajet entre A et B.

_On peut déduire du théorème précédent le théorème de la puissance mécanique._
````

````{topic} Démonstration
>\begin{align*}
\Delta E_{c,A \rightarrow B} &= W_{A \rightarrow B}(\overrightarrow{F_c}) + W_{A \rightarrow B}(\overrightarrow{F_{nc}})\\
\Delta E_{c,A \rightarrow B} &= - \Delta E_{p,A \rightarrow B} + W_{A \rightarrow B}(\overrightarrow{F_{nc}})\\
\Delta E_{c,A \rightarrow B} + \Delta E_{p,A \rightarrow B} &= W_{A \rightarrow B}(\overrightarrow{F_{nc}})
\end{align*}
````

## Interprétation des théorèmes (en ligne)

```{image} ./images/qr_code/qr_energie_theoreme.png
:name: qr_energie_theoreme
:width: 150px
:align: right
:target: energetique_theoremes.html#interpretation-des-theoremes-en-ligne
```

````{topic} Interprétation du théorème de l'énergie cinétique
Le théorème de l'énergie cinétique montre que les actions sur le système participe à la modification du mouvement et plus précisément ici la modification de la vitesse.

Une force dont la puissance est positive va augmenter l'énergie cinétique: c'est une force __motrice__ (elle forme un angle aigu avec la vitesse). Une force dont la puissance est négative va diminuer l'énergie cinétique: c'est une force __résistance__ (elle forme un angle obtu avec la vitesse). Une force qui __ne travaille pas__, c'est-à-dire dont la puissance transmise est nulle ne modifie pas la vitesse __en norme__ du système (la force est alors perpendiculaire à la vitesse).

On remarquera qu'on n'obtient que l'information sur la __norme__ de la vitesse (le TEC est scalaire). Ce théorème donne donc moins d'informations que le PFD pour un point matériel. Par contre, pour un solide, l'information donnée sera complémentaire du TRD.

Si l'on fait le parallèle avec l'électrocinétique, il faut noter que le théorème de l'énergie cinétique revient à étudier le système __en convention récepteur__. Les puissances considérées sont toutes des puissances reçues par le système.
````

````{topic} Interprétation du théorème de l'énergie mécanique
Le théorème de l'énergie mécanique consiste à particulariser certaines forces (les forces conservatives) et voir les échanges d'énergie avec le milieu extérieur, non plus comme un apport du milieu extérieur mais comme une variation d'un terme énergétique propre au système (sous l'effet d'un champ de pesanteur, le système possède __son__ énergie potentielle de pesanteur).

On interprète alors le théorème de l'énergie mécanique comme un échange entre deux réservoir d'énergie: l'énergie potentielle et l'énergie cinétique. Cet échange est "perturbé" par un apport/retrait possible d'énergie du milieu extérieur par les forces non conservatives. Comme on l'a évoqué précédemment, le premier __échange__ est réversible lorsqu'on passe d'un état A à une état B et inversement alors que le second __transfert__ n'est a priori pas réversible.
````

````{topic} Force conservative ou pas ?
Est-ce grave de calculer un travail pour une force conservative au lieu d'utiliser l'énergie potentielle dans un TEM ? La réponse est non. TEC et TEM sont équivalent donc on peut utiliser les deux. On peut utiliser le TEM et "oublier" qu'une force est conservative. La seule règle est de ne pas oublier de considérer le transfert d'énergie (pas énergie potentielle ou calcul de travail) et de le compter qu'une seule fois (si on calcule le travail du poids, il ne faut en plus compter la variation d'énergie potentielle). Néanmoins, il est conseiller d'avoir le réflexe d'utiliser au maximum la variation d'énergie potentielle plutôt le calcul de travail pour une force conservatives en physique. En effet:
* le calcul d'une variation d'énergie potentielle est en général plus direct.
* l'utilisation de l'énergie potentielle en physique permet, comme on l'a expliqué précédemment de particulariser les échanges qui pourront se faire de manière réversible. Leur utilisation permet une interprétation directe en ce sens.
* Comme on le verra par la suite, la reconnaissance des forces conservatives permet d'étudier les systèmes dits "conservatifs" (où toutes les forces sont conservatives) en tirant beaucoup d'information de l'énergie potentielle. Cela devient très important à l'échelle microscopique où toutes les forces sont conservatives. Le passage à la mécanique quantique fait d'ailleurs intervenir une grandeur (l'hamiltonien) qui tire partie de cette propriété pour établir la base même de la mécanique quantique.
````



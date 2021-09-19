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

````{admonition} Fondamental : Théorème de l'énergie cinétique
:class: attention

Soit un point matériel M de masse m. La variation d'énergie cinétique du point M dans un référentiel galiléen entre deux instants est égale à la somme du travail de toutes les forces qui s'exercent sur le point M entre les deux instants considérés.

\begin{align*}
\Delta E_{C,A \rightarrow B} &= W_{A \rightarrow B} (\overrightarrow{F})\\
dE_c &= \delta W(\overrightarrow{F})
\end{align*}
où $\overrightarrow{F}$ est la résultante totale des forces s'appliquant sur le point matériel M. La première écriture consiste à appliquer le théorème de l'énergie cinétique sur un chemin fini d'un point A à un point B (on a rappelle que le travail des forces dépend a priori du chemin choisi). La seconde traite le cas d'un déplacement infinitésimal.
````

````{admonition} Fondamental : Théorème de la puissance cinétique
:class: attention

En référentiel galiléen (sous les mêmes hypothèses que précédemment):

\begin{align*}
\frac{\rm{d}E_{c/\mathfrak{R}}}{\rm{dt}} &= \delta P_{/\mathfrak{R}}(\overrightarrow{F})
````

__Démonstration__
\begin{align*}
m \frac{d \overrightarrow{v_{M/R}}}{dt} &= \overrightarrow{F}\\
m \frac{d \overrightarrow{v_{M/R}}}{dt} \cdot \overrightarrow{v_{M/R}} &= \overrightarrow{F} \cdot \overrightarrow{v_{M/R}}\\
\frac{d}{dt}(\frac{1}{2} m v^2) &= P_R(\overrightarrow{F})\\
dE_c &= \delta W(\overrightarrow{F})
\end{align*}
L'expression intégrale s'obtient en intégrant la dernière équation sur le chemin choisi.


## Théorème de l'énergie mécanique

````{admonition} Fondamental : Théorème de l'énergie mécanique
:class: attention

Dans un référentiel galiléen, la variation d'énergie mécanique d'un point matériel M de masse m entre deux points A et B d'un système est égale au travail des seules forces non-conservatives sur le trajet entre A et B.
````


__Démonstration__
\begin{align*}
\Delta E_{c,A \rightarrow B} &= W_{A \rightarrow B}(\overrightarrow{F_c}) + W_{A \rightarrow B}(\overrightarrow{F_{nc}})\\
\Delta E_{c,A \rightarrow B} &= - \Delta E_{p,A \rightarrow B} + W_{A \rightarrow B}(\overrightarrow{F_{nc}})\\
\Delta E_{c,A \rightarrow B} + \Delta E_{p,A \rightarrow B} &= W_{A \rightarrow B}(\overrightarrow{F_{nc}})
\end{align*}
````{dropdown} Remarque

__Théorème de la puissance mécanique__
On peut déduire du théorème précédent le théorème de la puissance mécanique.

````

## Interprétation des théorèmes


__Interprétation du théorème de l'énergie cinétique__
Le théorème de l'énergie cinétique montre que les actions sur le système participe à la modification du mouvement et plus précisément ici la modification de la vitesse.

Une force dont la puissance est positive va augmenter l'énergie cinétique: c'est une force __motrice__ (elle forme un angle aigu avec la vitesse). Une force dont la puissance est négative va diminuer l'énergie cinétique: c'est une force __résistance__ (elle forme un angle obtu avec la vitesse). Une force qui __ne travaille pas__, c'est-à-dire dont la puissance transmise est nulle ne modifie pas la vitesse __en norme__ du système (la force est alors perpendiculaire à la vitesse).

On remarquera qu'on n'obtient que l'information sur la __norme__ de la vitesse (le TEC est scalaire). Ce théorème donne donc moins d'informations que le PFD pour un point matériel. Par contre, pour un solide, l'information donnée sera complémentaire du TRD.

Si l'on fait le parallèle avec l'électrocinétique, il faut noter que le théorème de l'énergie cinétique revient à étudier le système __en convention récepteur__. Les puissances considérées sont toutes des puissances reçues par le système.



__Interprétation du théorème de l'énergie mécanique__
Le théorème de l'énergie mécanique consiste à particulariser certaines forces (les forces conservatives) et voir les échanges d'énergie avec le milieu extérieur, non plus comme un apport du milieu extérieur mais comme une variation d'un terme énergétique propre au système (sous l'effet d'un champ de pesanteur, le système possède __son__ énergie potentielle de pesanteur).

On interprète alors le théorème de l'énergie mécanique comme un échange entre deux réservoir d'énergie: l'énergie potentielle et l'énergie cinétique. Cet échange est "perturbé" par un apport/retrait possible d'énergie du milieu extérieur par les forces non conservatives. Comme on l'a évoqué précédemment, le premier __échange__ est réversible lorsqu'on passe d'un état A à une état B et inversement alors que le second __transfert__ n'est a priori pas réversible.



__Force conservative ou pas ?__
Est-ce grave de calculer un travail pour une force conservative au lieu d'utiliser l'énergie potentielle dans un TEM ? La réponse est non. TEC et TEM sont équivalent donc on peut utiliser les deux. On peut utiliser le TEM et "oublier" qu'une force est conservative. La seule règle est de ne pas oublier de considérer le transfert d'énergie (pas énergie potentielle ou calcul de travail) et de le compter qu'une seule fois (si on calcule le travail du poids, il ne faut en plus compter la variation d'énergie potentielle). Néanmoins, il est conseiller d'avoir le réflexe d'utiliser au maximum la variation d'énergie potentielle plutôt le calcul de travail pour une force conservatives en physique. En effet:

* le calcul d'une variation d'énergie potentielle est en général plus direct.
* l'utilisation de l'énergie potentielle en physique permet, comme on l'a expliqué précédemment de particulariser les échanges qui pourront se faire de manière réversible. Leur utilisation permet une interprétation directe en ce sens.
* Comme on le verra par la suite, la reconnaissance des forces conservatives permet d'étudier les systèmes dits "conservatifs" (où toutes les forces sont conservatives) en tirant beaucoup d'information de l'énergie potentielle. Cela devient très important à l'échelle microscopique où toutes les forces sont conservatives. Le passage à la mécanique quantique fait d'ailleurs intervenir une grandeur (l'hamiltonien) qui tire partie de cette propriété pour établir la base même de la mécanique quantique.


## Applications des théorèmes aux solides

````{admonition} Fondamental : Théorème de l'énergie cinétique/mécanique. Cas général.
:class: attention

La variation d'énergie cinétique d'un système de points d'un état A à un état B est égale au travail des forces qui s'appliquent sur le système sur le même chemin, qu'elles __soient extérieures ou intérieures__.

La variation d'énergie mécanique d'un système de points d'un état A à un état B est égale au travail des forces non conservatives qui s'appliquent sur le système sur le même chemin, qu'elles __soient extérieures ou intérieures__.
````


__Démonstration__
La démonstration s'obtient par simple sommation du TEC/TEM pour chaque point du système.


````{admonition} Attention : Travail des forces intérieures
:class: note

Il est important de noter la différence entre ce théorème et le cas du Théorème de la résultante dynamique ou le théorème du moment cinétique. Cette fois, on __doit tenir compte des actions intérieures__ dont le travail est a priori non nul.

````

````{admonition} Fondamental : Théorème de l'énergie cinétique/mécanique. Cas d'un solide indéformable.
:class: attention

Dans le cas d'un solide __indéformable, le travail des forces intérieures est nul.__
````


__Démonstration__
Nous allons démontrer que dans le cas général le travail des forces intérieures est a priori non nul et qu'il s'annule dans le cas d'un solide indéformable.

Considérons deux points $M_1$ et $M_2$ du solide en interaction. On note $\overrightarrow{f_{1 \rightarrow 2}}$ la force exercée par $M_1$ sur $M_2$ et $\overrightarrow{f_{2 \rightarrow 1}}$ la force exercée par $M_2$ sur $M_1$. On a (troisième loi de Newton): $\overrightarrow{f_{1 \rightarrow 2}} = -\overrightarrow{f_{2 \rightarrow 1}}$. La puissance totale associée à ces deux forces s'écrit:

\begin{align*}
P &= \overrightarrow{f_{1 \rightarrow 2}} \cdot v_{M_2/R} + \overrightarrow{f_{2 \rightarrow 1}} \cdot v_{M_1/R}\\
&= \overrightarrow{f_{1 \rightarrow 2}} \cdot {(\frac{d \overrightarrow{M_1 M_2}}{dt})}_{R}\\
\overrightarrow{f_{1 \rightarrow 2}} &= f_{1 \rightarrow 2} \overrightarrow{u_{1 \rightarrow 2}}\\
\overrightarrow{M_1 M_2} &= M_1 M_2 \overrightarrow{u_{1 \rightarrow 2}}\\
{(\frac{d \overrightarrow{M_1 M_2}}{dt})}_{R} &= \frac{d M_1 M_2}{dt} \overrightarrow{u_{1 \rightarrow 2}} + M_1 M_2 {(\frac{d \overrightarrow{u_{1 \rightarrow 2}}}{dt})}_R
\end{align*}
où $\overrightarrow{u_{1 \rightarrow 2}}$ est le vecteur unitaire allant de $M_1$ vers $M_2$.

Le première terme correspond à la variation de la distance entre les deux points, le second à la rotation d'un point par rapport à l'autre. La puissance des forces intérieurs pour ces deux points s'écrit donc: $P = f_{1 \rightarrow 2} \frac{d M_1 M_2}{dt}$

Si le mobile se déforme, cette expression est a priori non nulle.

Si le solide est indéformable, cette expression est toujours nulle.


````{dropdown} Remarque

__Cas d'un solide déformable isolé.__
Une grandeur conservative est une grandeur qui reste constante lorsque le système est isolé. Initialement, on a construit l'énergie mécanique comme une grandeur conservative. Et cela est vraie pour un point matériel ou un solide indéformable.

Par contre, on remarque que cela n'est plus vrai pour un système indéformable: un système isolé peut voir son énergie mécanique augmenter ou diminuer sous l'influence des forces. Cette limite peut paraître anodine mais elle est l'une des bases de l'élaboration du premier principe de la thermodynamique: on va rechercher une grandeur énergétique plus générale qui restera conservative lorsqu'on tient compte de la déformation du système (fondamentale pour les gaz) en ajoutant à l'énergie mécanique un terme énergétique supplémentaire appelé énergie interne.

A notre échelle, on verra des effets de la déformabilité des solides lorsqu'on étudiera le cas des solides déformables en rotation.

````


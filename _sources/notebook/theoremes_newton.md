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
# Lois de Newton et conséquences

## Lois de Newton


__Système d'étude__
Les postulats fondamentaux de la mécanique sont énoncés pour des points matériels. Nous déduirons les conséquences sur les solides par la suite.


````{admonition} Définition : Système isolé et pseudo-isolé
:class: tip

Un point matériel qui n'est soumis à aucune force est dit isolé.

Un point matériel soumis à un ensemble de forces dont la résultante (i.e. la somme) est nulle est dit pseudo-isolé.

````

````{admonition} Fondamental : Première loi de Newton (Principe d'inertie)
:class: attention

Il existe une classe de référentiels, appelés référentiels galiléens, dans lesquels un point matériel isolé ou pseudo-isolé possède un mouvement rectiligne uniforme.
````


Il n'existe pas de référentiel strictement galiléen connu. On peut néanmoins considérer que les référentiels courant (terrestre, géocentrique, héliocentrique... ) sont des référentiels galiléens suivant les mouvements considérés (il ne faut pas qu'ils soient trop longs).


````{admonition} Fondamental : Deuxième loi de Newton (Principe fondamental de la dynamique)
:class: attention

Dans un référentiel galiléen, la variation de la quantité de mouvement d'un point matériel M au cours du temps est égale à la somme des forces s'exerçant sur les systèmes:

\begin{align*}
{(\frac{d \overrightarrow{p_{M/\mathfrak{R}}}}{dt})}_{\mathfrak{R}} &= \sum \overrightarrow{F_{ \rightarrow M}}\\
m{(\frac{d \overrightarrow{v_{M/\mathfrak{R}}}}{dt})}_{\mathfrak{R}} &= \sum \overrightarrow{F_{ \rightarrow M}}
\end{align*}
La deuxième expression n'est valable que si le système est fermé, c'est-à-dire qu'il n'échange pas de matière avec l'extérieur.
````

````{admonition} Fondamental : Troisième loi de Newton (Lois des actions réciproques)
:class: attention

Si un point matériel A exerce sur un point B une force $\overrightarrow{f_{A \rightarrow B}}$ alors le point B exerce sur le point A une force $\overrightarrow{f_{B \rightarrow A}}$ telle que:

* $\overrightarrow{f_{B \rightarrow A}} = - \overrightarrow{f_{A \rightarrow B}}$
* $\overrightarrow{f_{B \rightarrow A}}$ et $\overrightarrow{f_{A \rightarrow B}}$ sont sur la même droite: la droite (AB)
````

## Relativité galiléenne

````{admonition} Définition : Référentiels galiléens usuels
:class: tip

Il n'existe pas de référentiel galiléen strict connu. Néanmoins, de nombreux référentiels peuvent être considérés comme galiléen sur des périodes de temps suffisamment courte.

* Le référentiel héliocentrique dans lequel le Soleil et 3 étoiles lointaines sont supposées fixes (sur plusieurs années voire plusieurs décennies)
* Le référentiel géocentrique dans lequel la Terre et 3 étoiles lointaines sont supposées fixes (quelques mois). Il est translation quasi-circulaire par rapport au référentiel héliocentrique
* Le référentiel terrestre dont laquelle la Terre (en tant que solide) est supposée fixe pour des courtes expériences (quelques heures). Il est rotation autour de l'axe des pôles dans le référentiel géocentrique.
* A une échelle plus petite, le référentiel lié au noyau atomique pourra être considéré comme galiléen sur des temps très courts.

````

````{admonition} Fondamental : Infinité des référentiels galiléens.
:class: attention

Tout référentiel en translation rectiligne uniforme avec un référentiel galiléen est aussi un référentiel galiléen.
````


__Démonstration__
Considérons un référentiel galiléen noté $\mathfrak{R_G}$ et un second référentiel $\mathfrak{R}$ en translation rectiligne uniforme à la vitesse $\overrightarrow{v_{R/RG}}$ par rapport à $\mathfrak{R_G}$.

Première méthode: On considère un point matériel isolé. Il possède un mouvement de translation rectiligne uniforme (à la vitesse $\overrightarrow{v_0}$) dans $\mathfrak{R_G}$ car ce référentiel est galiléen. Dans $\mathfrak{R}$, sa vitesse est: $\overrightarrow{v_{/R}} = \overrightarrow{v_0} + \overrightarrow{v_{R/RG}} = \overrightarrow{cste}$: il possède aussi un mouvement rectiligne uniforme dans $\mathfrak{R}$ donc $\mathfrak{R}$ est aussi galiléen.

Deuxième méthode:] On considère un point matériel soumise un ensemble de force dont la résultante est $\overrightarrow{F}$. Le principe fondamental dans $\mathfrak{R_G}$ s'écrit: $m \overrightarrow{a_{RG}} = \overrightarrow{F}$

Or:

\begin{align*}
&m \overrightarrow{a_{\mathfrak{R}}} = m \frac{d \overrightarrow{v_{\mathfrak{R}}}}{dt} = m \frac{d \overrightarrow{v_{\mathfrak{RG}}} + \overrightarrow{v_{R/RG}}}{dt} = m \frac{d \overrightarrow{v_{\mathfrak{RG}}}}{dt} = m \overrightarrow{a_{\mathfrak{RG}}}\\
&\Longrightarrow m \overrightarrow{a_{\mathfrak{R}}} = \overrightarrow{F}
\end{align*}
En particulier si le mobile est isolé ($\overrightarrow{F} = 0$), l'accélération dans $\mathfrak{R}$ est nulle et le système est donc dans un mouvement de translation rectiligne uniforme: c'est un référentiel galiléen.



__Principe de relativité galiléenne.__
La deuxième méthode est ce qu'on appelle le __principe de relativité galiléenne__: Les lois de la dynamique sont les mêmes quel que soit le référentiel galiléen considéré.


## Théorème de la résultante cinétique


__Application des lois de Newton à un solide.__
Le but est de voir comment on peut appliquer le principe fondamental de la dynamique à un système de points matériel. On peut l'énoncer de manière identique mais comme on va le voir, on peut "simplifier" légèrement son énoncé.


\begin{rappel}{Forces extérieures et intérieures}
On rappelle que pour un système de points matériels (solide déformable ou indéformable), on distingue les forces __intérieures__ exercées par une partie du système sur une autre partie du système et les forces __extérieures__ exercées par le milieu extérieur sur le système.
\end{rappel}

````{admonition} Fondamental : Théorème de la résultante dynamique
:class: attention

La dérivée temporelle de la quantité de mouvement total d'un système de points matériel dans un référentiel galiléen est égale à la somme des forces __extérieures__ qui s'appliquent sur le solide.
````


__Démonstration__
Considérons chaque point $M_i$ de masse $m_i$du système. On peut appliquer le principe fondamental de la dynamique à chaque point. Le bilan des forces sur un point $M_i$ se divise en deux parties: les actions extérieures, modélisées par des forces $\overrightarrow{F}_{ext \to M_i}$ et les actions intérieures au système. Si l'on somme tous ces PFD, il vient:

* le terme de gauche est la somme des dérivées des quantités de mouvement soit la dérivée de la quantité de mouvement totale.
* le terme de droite contient la somme de toutes les actions extérieures au système (qui seront regroupées en actions résultantes) et la somme des actions intérieures. Or pour chaque action du point $M_j$ sur le point $M_i$ à l'intérieur du système, il y aura aussi l'action du point $M_i$ sur le point $M_j$ et le principe des actions réciproques implique que les forces associées à ces deux actions sont opposées: elles vont s'annuler. De cette somme, il ne restera donc bien que la résultante des forces extérieures.



__Conséquences__
Une des conséquences est qu'il n'est pas nécessaire de tenir compte des actions intérieures, ce qui simplifie énormément le problème car ces dernières sont très nombreuses et souvent d'expression inconnues (on pensera aux actions de cohésion d'un solide).

De plus, ce théorème de la résultante cinétique justifie la possible modélisation d'un système en volume par un point matériel qui sera le centre d'inertie. En effet, par la modélisation en point matériel, on perd complètement l'information sur les actions intérieures. Mais vu qu'elle n'agit pas sur la quantité de mouvement total, on ne perd rien. De plus, la quantité de mouvement totale égale la masse totale multipliée par la vitesse du centre d'inertie, donc assimiler le système au centre d'inertie donnera la même information.


````{admonition} Attention : Insuffisance du théorème de la résultante cinétique (TRC).
:class: note

En somment les PFD, on perd les points d'application des forces ce qui rend le TRC insuffisant a priori pour décrire complètement le mouvement d'un solide. En effet, le TRD __ne donne que le mouvement du centre d'inertie (mouvement de translation globale du système)__. Il ne donne pas d'information sur la déformation du système, ni même sur sa rotation sur lui-même (ou autour d'un autre point).

Le TRD, ne sera suffisant que si le mouvement est une translation pure (et on retrouve l'idée de modélistion ponctuelle du système).

````


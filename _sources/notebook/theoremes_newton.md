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

```{margin} Système d'étude
Les postulats fondamentaux de la mécanique sont énoncés pour des points matériels. Nous déduirons les conséquences sur les solides par la suite.
```

````{important} __Système isolé et pseudo-isolé__
* Un point matériel qui n'est soumis à aucune force est dit isolé.
* Un point matériel soumis à un ensemble de forces dont la résultante (i.e. la somme) est nulle est dit pseudo-isolé.
````

````{important} __Première loi de Newton (Principe d'inertie)__
Il existe une classe de référentiels, appelés référentiels galiléens, dans lesquels un point matériel isolé ou pseudo-isolé possède un mouvement rectiligne uniforme.
````

````{important} __Deuxième loi de Newton (Principe fondamental de la dynamique)__

Dans un référentiel galiléen, la variation de la quantité de mouvement d'un point matériel M au cours du temps est égale à la somme des forces s'exerçant sur les systèmes:

\begin{align*}
{(\frac{d \overrightarrow{p_{M/\mathfrak{R}}}}{dt})}_{\mathfrak{R}} &= \sum \overrightarrow{F_{ \rightarrow M}}\\
m{(\frac{d \overrightarrow{v_{M/\mathfrak{R}}}}{dt})}_{\mathfrak{R}} &= \sum \overrightarrow{F_{ \rightarrow M}}
\end{align*}
La deuxième expression n'est valable que si le système est fermé, c'est-à-dire qu'il n'échange pas de matière avec l'extérieur.
````

````{important} __Troisième loi de Newton (Lois des actions réciproques)__

Si un point matériel A exerce sur un point B une force $\overrightarrow{f_{A \rightarrow B}}$ alors le point B exerce sur le point A une force $\overrightarrow{f_{B \rightarrow A}}$ telle que:

* $\overrightarrow{f_{B \rightarrow A}} = - \overrightarrow{f_{A \rightarrow B}}$
* $\overrightarrow{f_{B \rightarrow A}}$ et $\overrightarrow{f_{A \rightarrow B}}$ sont sur la même droite: la droite (AB)
````

## Relativité galiléenne

````{important} __Référentiels galiléens usuels__

Il n'existe pas de référentiel galiléen strict connu. Néanmoins, de nombreux référentiels peuvent être considérés comme galiléen sur des périodes de temps suffisamment courte.

* Le référentiel héliocentrique dans lequel le Soleil et 3 étoiles lointaines sont supposées fixes (sur plusieurs années voire plusieurs décennies)
* Le référentiel géocentrique dans lequel la Terre et 3 étoiles lointaines sont supposées fixes (quelques mois). Il est translation quasi-circulaire par rapport au référentiel héliocentrique
* Le référentiel terrestre dont laquelle la Terre (en tant que solide) est supposée fixe pour des courtes expériences (quelques heures). Il est rotation autour de l'axe des pôles dans le référentiel géocentrique.
* A une échelle plus petite, le référentiel lié au noyau atomique pourra être considéré comme galiléen sur des temps très courts.

````

````{important} __Infinité des référentiels galiléens.__

Tout référentiel en translation rectiligne uniforme avec un référentiel galiléen est aussi un référentiel galiléen.
````

>__Démonstration__
>Considérons un référentiel galiléen noté $\mathfrak{R_G}$ et un second référentiel $\mathfrak{R}$ en translation rectiligne uniforme à la vitesse $\overrightarrow{v_{R/RG}}$ par rapport à $\mathfrak{R_G}$.
>
>Première méthode: On considère un point matériel isolé. Il possède un mouvement de translation rectiligne uniforme (à la vitesse $\overrightarrow{v_0}$) dans $\mathfrak{R_G}$ car ce référentiel est galiléen. Dans $\mathfrak{R}$, sa vitesse est: $\overrightarrow{v_{/R}} = \overrightarrow{v_0} + \overrightarrow{v_{R/RG}} = \overrightarrow{cste}$: il possède aussi un mouvement rectiligne uniforme dans $\mathfrak{R}$ donc $\mathfrak{R}$ est aussi galiléen.
>
````{margin} Principe de relativité galiléenne
La deuxième méthode est ce qu'on appelle le __principe de relativité galiléenne__: Les lois de la dynamique sont les mêmes quel que soit le référentiel galiléen considéré.
````
>Deuxième méthode: On considère un point matériel soumise un ensemble de force dont la résultante est $\overrightarrow{F}$. Le principe fondamental dans $\mathfrak{R_G}$ s'écrit: $m \overrightarrow{a_{RG}} = \overrightarrow{F}$
>
>Or:
>
>\begin{align*}
&m \overrightarrow{a_{\mathfrak{R}}} = m \frac{d \overrightarrow{v_{\mathfrak{R}}}}{dt} = m \frac{d \overrightarrow{v_{\mathfrak{RG}}} + \overrightarrow{v_{R/RG}}}{dt} = m \frac{d \overrightarrow{v_{\mathfrak{RG}}}}{dt} = m \overrightarrow{a_{\mathfrak{RG}}}\\
&\Longrightarrow m \overrightarrow{a_{\mathfrak{R}}} = \overrightarrow{F}
\end{align*}
>En particulier si le mobile est isolé ($\overrightarrow{F} = 0$), l'accélération dans $\mathfrak{R}$ est nulle et le système est donc dans un mouvement de translation rectiligne uniforme: c'est un référentiel galiléen.

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
# Position et trajectoire

## Vecteur position

### Vecteur position: Définition

````{important} __Définition : Vecteur position__

On définit la position d'un point matériel M dans un référentiel $\mathfrak{R}$ à l'aide du vecteur position $\overrightarrow{OM}$ où O est un __point fixe__ du référentiel.

````


Normalement, on prend comme point O, le centre du repère choisi comme associé au référentiel d'étude.


````{important} __Définition : Equation horaire et trajectoire__

L'évolution du mouvement du point matériel $OM(t)$ est appelée équation horaire. Elle est aussi définit par les composantes du vecteur position dans la base de projection. La courbe paramètrée (ou trace) ainsi définie est appelée trajectoire.

On peut être amené à tracer des trajectoires en utilisant la représentation paramétrique (coordonnées en fonction d'un même paramètre, le temps) ou cartésienne (une coordonnée cartésienne en fonction d'un autre) ou polaire (une coordonnée polaire en fonction d'une autre).

````

### Expression du vecteur position

````{important} __Fondamental : Expressions__

On peut exprimer le vecteur position dans les différents repères. Les vecteurs des bases locales sont exprimées au point M mobile:

* Coordonnées cartésiennes: $x_M(t) \overrightarrow{e_x} + y_M(t) \overrightarrow{e_y} + z_M(t) \overrightarrow{e_z}$.
* Coordonnées cylindrique: $r_M(t) \overrightarrow{e_r} + z_M(t) \overrightarrow{e_z}$.
* Coordonnées sphériques: $r_M(t) \overrightarrow{e_r}$.
````

````{attention}
On rappelle que les bases cylindriques et sphériques sont des bases __locales__ dont les vecteurs vont varier lorsque le point M se déplace. Il faudra donc tenir compte de leur dérivées temporelles.

````

## Trajectoires usuelles

Il est important de pouvoir reconnaître un certain nombre de trajectoires usuelles à partir de leur équation paramétrique, cartésienne ou polaire. Nous allons présenter ici les trajectoires les plus utiles ainsi que leur caractéristiques.


### Trajectoire rectiligne

````{important} __Définition : Mouvement rectiligne__

Un mouvement rectiligne est un mouvement dont la trajectoire est portée par une droite (ou un segment) fixe dans le référentiel d'étude. Il se fait suivant une direction de l'espace: c'est un mouvement à 1 degré de liberté.

````

````{admonition} Choix du système de coordonnées
:class: hint, dropdown
En général, on prévoit par une étude physique que le mouvement sera rectiligne. On va donc choisir un système de coordonnées cartésiennes (ou à la limite cylindriques) dont un axe est confondu avec le support de la trajectoire.
````

````{attention}

Un trajectoire rectiligne ne signifie pas que le mobile va toujours dans le même sens. Il peut rebrousser chemin.

````

### Trajectoire circulaire

````{important} __Définition : Mouvement circulaire__

Un mouvement est dit circulaire si le point M se déplace sur un cercle (ou une portion de cercle) fixe dans le référentiel R. C'est aussi un mouvement à 1 degré de liberté.

````

````{admonition} Choix du système de coordonnées
:class: hint, dropdown
On va donc choisir un système de coordonnées cylindriques (ou polaires) de centre O le centre du cercle et d'axe Oz perpendiculaire au plan du cercle. On étudiera plus en détail les caractéristiques d'un tel mouvement.
````

````{important} __Fondamental : Equation cartésienne et paramétrique__

On peut être amené à obtenir une trajectoire circulaire sans l'avoir prévu et en ayant utilisé au départ des coordonnées cartésiennes. Il est important de reconnaître qu'une équation cartésienne ou paramétrique est l'équation d'un cercle.

Ainsi, si l'on peut mettre le couple de coordonnées cartésiennes $(x(t);y(t))$ sous la forme:

\begin{align*}
x(t) = R \cos \omega t + x_0\\
y(t) = R \sin \omega t + y_0
\end{align*}
Et on peut aussi écrire l'équation d'un cercle sous la forme:

\begin{equation}\label{eq_cercle_cartesienmtex_234}
{(x - x_0)}^2 + {(y - y_0)}^2 = R^2
\end{equation}
Dans les deux cas, il s'agit de l'équation d'un cercle de rayon R et de centre C dont les coordonnées sont $C(x_0,y_0)$
````

### Trajectoire elliptique

````{important} __Définition : Ellipse__

Une ellipse est une courbe fermée qu'on peut caractériser/reconnaître de plusieurs manières:

* Lieu géométrique (peu usité): Soit deux points, appelées foyers, $F_1$ et $F_2$ et un réel positif K, l'ensemble des points M tel que $MF_1 + MF_2 = K$ décrit une ellipse. Le milieu du segment $F_1 F_2$ est appelé centre de l'ellipse.
* Représentation polaire (__fondamentale__): Soit un point F centre d'un repère polaire. L'ensemble des points M dont les coordonnées du vecteur position $\overrightarrow{FM}$ sont tels que $r = \frac{p}{1 + e \cos{\theta - \theta_0}}$ avec $p > 0$ et $0 \leq e < 1$ décrit une ellipse. __Le point F est un des foyers de l'ellipse__. On dit que p est le __paramètre de l'ellipse__ et que __e__ est l'excentricité de l'ellipse.
* Représentation cartésienne (très utile). L'ensemble des M dont les coordonnées $(x,y)$ sont telles que: ${(\frac{x}{a})}^2 + {(\frac{y}{b})}^2 = 1$ décrit une ellipse dont le centre est le centre du repère.
* Représentation paramétrique (utile): L'ensemble des M dont les coordonnées $(x(t) = a \cos t ; y(t) = b \sin(t))$ décrit une ellipse dont le centre est le centre du repère.

```{figure} ./images/mathematiques_ellipse.jpg
:name: fig_222
:align: center

```

````

````{attention}

On fera attention au fait que le centre du repère ne définit pas le même point particulier de l'ellipse suivant qu'on utilise les coordonnées cartésiennes ou polaires.

````

````{important} __Fondamental : Caractéristiques d'une ellipse.__

Les caractéristiques importantes sont:

* le demi-grand axe a (=OA)
* le demi-petit axe b (=OB)
* la distance focale c (=OF)

On démontrera en exercice les relations suivantes:

\begin{align*}
a = \frac{p}{1 - e^{2}}\\
c^{2} = a^{2} - b^{2}\\
e = c / a
\end{align*}
````
### Trajectoire parabolique

````{important} __Définition : Parabole__

Une parabole est une courbe non fermée qu'on peut caractériser/reconnaître de plusieurs manières:

* Représentation polaire (__fondamentale__): Soit un point F centre d'un repère polaire. L'ensemble des points M dont les coordonnées du vecteur position $\overrightarrow{FM}$ sont tels que $r = \frac{p}{1 + e \cos{\theta - \theta_0}}$ avec $p > 0$ et $e = 1$ décrit une parabole. __Le point F est appelé foyer de la parabole__. On dit que p est le __paramètre de la parabole__ et que __e__ est l'excentricité de la parabole.
* Représentation cartésienne (très utile). L'ensemble des M dont les coordonnées $(x,y)$ sont telles que: $y = ax^2 + bx + c$ décrit une parabole d'axe de symétrie parallèle à Oy.

```{figure} ./images/mathematiques_paraboleb.jpg
:name: fig_223
:align: center

```

````

````{attention}

Dans le cas polaire, si $\theta_0 = 0$ (cas fréquent) l'axe de symétrie de la parabole est l'axe qui sert d'origine des angles, soit en général l'axe Ox. Ce qui est différent du cas cartésien présenté ici.

````

### Coniques

````{important} __Définition : Coniques__

Les coniques correspondent à l'ensemble des courbes qu'on peut obtenir par l'intersection d'un cône et d'un plan. Il en résulte trois types de conique:

* l'ellipse
* la parabole
* l'hyperbole

```{figure} ./images/conique.png
:name: fig_224
:align: center

```

````

````{important} __Fondamental : Equation polaire d'une conique__

En choisissant correctement l'origine du repère polaire, on peut exprimer l'équation polaire d'une conique sous la forme:

\begin{equation}
r(\theta) = \frac{p}{1 \pm e \cos \left(\theta - \theta_0\right)}
\end{equation}
Le centre du repère est alors appelée foyer de la conique. A noter que l'ellipse et la parabole possède deux foyers symétriques par rapport au centre de la conique (centre de symétrie de la conique).

p est appelée paramètre de l'ellipse et e excentricité. En changeant l'origine des angles, on peut faire en sorte de $\theta_0 = 0$.
````


De nombreuses propriétés seront vues sur les coniques lors du cours sur les potentiels newtoniens. On retiendra déjà que la valeur de l'excentricité déterminer le type de conique:

* ellipse: $0 \leq e < 1$
* parabole: $e = 1$
* hyperbole: $e > 1$. Attention, en coordonnées polaires, les asymptotes sont en général obliques.


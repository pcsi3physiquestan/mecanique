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

# Cinématique du point
## Référentiel

````{important} __Référentiel__

Un référentiel $\mathfrak{R}$ est un ensemble de points rigides - c'est-à-dire fixes les uns par rapports aux autres - auquel on associe une horloge. Comme le temps est absolu en mécanique classique, l'horloge est la même quelque soit le référentiel.
````

````{margin}
Repère et référentiel sont deux objets physiques distincts qu'il ne faut pas confondre. On peut associer à un référentiel une multitude de repères.
````
````{important} __Repère associé à un référentiel__

En physique, on  associe à un référentiel, un(des) repère(s) $(O, \overrightarrow{e_x}, \overrightarrow{e_y}, \overrightarrow{e_z})$ soit la donnée d'un point (O)  dans le référentiel (c'est-à-dire  par rapport aux points rigides définit précédemment) et une base de 3 vecteurs  dans ce même référentiel.
````

## Position et trajectoire

### Vecteur position: Définition

````{important} __Vecteur position__

On définit la position d'un point matériel M dans un référentiel $\mathfrak{R}$ à l'aide du vecteur position $\overrightarrow{OM}$ où O est un __point fixe__ du référentiel.
````

````{sidebar} Type de représentation
On peut être amené à tracer des trajectoires en utilisant la représentation paramétrique (coordonnées en fonction d'un même paramètre, le temps) ou cartésienne (une coordonnée cartésienne en fonction d'un autre) ou polaire (une coordonnée polaire en fonction d'une autre).
````
````{important} __Equation horaire et trajectoire__

L'évolution du mouvement du point matériel $\overrightarrow{OM}(t)$ est appelée __équation horaire__. Elle est aussi définie par les composantes du vecteur position dans la base de projection. La courbe paramètrée (ou trace) ainsi définie est appelée __trajectoire__.
````

### Expression du vecteur position

```{margin}
On trouvera très souvent la notation $r$ au lieu de $\rho$ pour désigner la variable radiale en coordonnées cylindriques ou polaires. Attention, elle ne représente pas la même grandeur qu'en sphérique.
```

````{sidebar} Bases locales
On rappelle que les bases cylindriques et sphériques sont des bases __locales__ dont les vecteurs vont varier lorsque le point M se déplace. Il faudra donc tenir compte de leur dérivées temporelles :

* Coordonnées cylindrique: $\overrightarrow{OM}(t) = \rho_M(t) \overrightarrow{e_r}(\theta(t)) + z_M(t) \overrightarrow{e_z}$.
* Coordonnées sphériques: $\overrightarrow{OM}(t) = r_M(t) \overrightarrow{e_r}(\theta(t), \phi(t))$.

````
````{important} __Expressions__

On peut exprimer le vecteur position dans les différents repères. Les vecteurs des bases locales sont exprimées au point M mobile:

* Coordonnées cartésiennes: $\overrightarrow{OM}(t) = x_M(t) \overrightarrow{e_x} + y_M(t) \overrightarrow{e_y} + z_M(t) \overrightarrow{e_z}$.
* Coordonnées cylindrique: $\overrightarrow{OM}(t) = \rho_M(t) \overrightarrow{e_r}(t) + z_M(t) \overrightarrow{e_z}$.
* Coordonnées sphériques: $\overrightarrow{OM}(t) = r_M(t) \overrightarrow{e_r}(t)$.
````

## Vecteur vitesse
### Vecteur vitesse: Définition

````{margin}
Il est important de préciser le référentiel d'étude: il définit les vecteurs qu'on considère fixe. Dans un premier temps, il n'y aura qu'un seul référentiel.
````
````{important} __Vecteur vitesse__

Soit O un point fixe du référentiel R et M un point mobile. La vitesse du point M dans le référentiel R est définit comme la dérivée temporelle du vecteur position dans le référentiel R.

$$
\overrightarrow{V_{M/R}} = {(\frac{d \overrightarrow{OM}}{dt})}_{R}
$$
````

### Expression du vecteur vitesse

````{important} __Expressions du vecteur vitesse__
```{figure} ./images/qr_code/qr_cinema_demo_vitesse.png
:name: qr_cinema_demo_vitesse
:width: 150px
:align: right
:target: cinema_point.html#expression-du-vecteur-vitesse
```
Le vecteur vitesse s'exprime.
* En coordonnées cartésiennes:

$$
\overrightarrow{v_{M/\mathfrak{R}}} = \dot x \overrightarrow{e_x} + \dot y \overrightarrow{e_y} + \dot z \overrightarrow{e_z}
$$

* En coordonnées cyindriques:

$$
\overrightarrow{v_{M/\mathfrak{R}}} = \dot r \overrightarrow{e_r} +r \dot \theta \overrightarrow{e_\theta} + \dot z \overrightarrow{e_z}
$$

* En coordonnées spheriques:

$$
\overrightarrow{v_{M/\mathfrak{R}}} = \dot r \overrightarrow{e_r} + r \dot \theta \overrightarrow{e_\theta} + r \sin{\theta} \dot \varphi \overrightarrow{e_\varphi}
$$
````

````{topic} Démonstration
> On peut démontrer ces expressions de deux manières: soit en dérivant le vecteur position (il faut tenir compte des dérivées des vecteurs des bases locales, nous le verrons en traitant le cas du vecteur accélération) ou en utilisant l'expression du vecteur déplacement élémentaire. Nous présentons ce dernier cas. On rappelle que le déplacement élémentaire s'exprime (respectivement en coordonnées cartésiennes, cylindriques, sphériques):
> 
> \begin{equation}
\overrightarrow{dOM} = dx \overrightarrow{e_x} + dy \overrightarrow{e_y} + dz \overrightarrow{e_z}
\end{equation}
> \begin{equation}
\overrightarrow{dOM} = dr \overrightarrow{e_r} + r d \theta \overrightarrow{e_{\theta}} + dz \overrightarrow{e_z}
\end{equation}
> \begin{equation}
\overrightarrow{dOM} = dr \overrightarrow{e_r} + r d \theta \overrightarrow{e_{\theta}} + r \sin \theta d\varphi \overrightarrow{e_{\varphi}}
\end{equation}
> Ici, on rapport le déplacement élémentaire à la variation temporelle dt pendant lequel le déplacement se fait, ce qui revient à rapporter chaque différentielle ($dx, dy, d\theta, dr...$) par dt, c'est-à-dire les remplacer par les dérivées. On obtient bien les expressions données.
````

## Vecteur accélération

### Vectreur accélération: Définition

````{margin}
Comme le vecteur vitesse, le vecteur accélération dépend du référentel dans lequel il est calculé.
````
````{important} __Vecteur accélération__

On définit l'accélération d'un point M dans un un référentiel R comme la dérivée du vecteur vitesse dans le référentiel R.

$$
\overrightarrow{a_{M/R}} = {(\frac{d \overrightarrow{v_{M/R}}}{dt})}_{R}= {(\frac{d^2 \overrightarrow{OM}}{dt^2})}_{R}
$$
````


## Vecteur accélération: Expressions

````{important} __Vecteur accélération en coordonnées cartésiennes.__

En coordonnées cartésiennes, le vecteur accélération s'écrit:

$$
\overrightarrow{a_{M/R}} = \ddot x \overrightarrow{e_x} + \ddot y \overrightarrow{e_{y}} + \ddot z \overrightarrow{e_z}
$$
````

````{important} __Vecteur accélération en coordonnées cylindriques.__
```{figure} ./images/qr_code/qr_cinema_demo_acc_cy.png
:name: qr_cinema_demo_acc_cy
:width: 150px
:align: right
:target: cinema_point.html#vecteur-acceleration-expressions
```
En coordonnées cylindriques, le vecteur accélération s'écrit:

$$
\overrightarrow{a_{M/R}} = (\ddot r - r \dot \theta^2) \overrightarrow{e_r} + (2 \dot r \dot \theta + r \ddot \theta) \overrightarrow{e_{\theta}} + \ddot z \overrightarrow{e_z}
$$
````

````{topic} Démonstration dans le cas cylindrique
>On va partir de l'expresson du vecteur vitesse et le dériver.
>
>\begin{align*}
\overrightarrow{v_{M/R}}& = \frac{\rm{d\overrightarrow{v_{M/R}}}}{\rm{dt}}\\
& = \frac{\rm{d}}{\rm{dt}}\left(\dot r\overrightarrow{e_r} + r \dot \theta \overrightarrow{e_{\theta}} + \dot z \overrightarrow{e_z}\right)\\
& = \ddot r \overrightarrow{e_r} + \dot r \underbrace{\frac{\rm{d}\overrightarrow{e_r}}{\rm{dt}}_{\mathfrak{R}}}_{= \dot \theta \overrightarrow{e_{\theta}}} + \left(\dot r \dot \theta + r \ddot \Theta\right)\overrightarrow{e_{\theta}} + r \dot \theta \underbrace{\frac{\rm{d}\overrightarrow{e_{\theta}}}{\rm{dt}}_{\mathfrak{R}}}_{= - \dot \theta \overrightarrow{e_r}} + \ddot z \overrightarrow{e_z}\\
& = (\ddot r - r \dot \theta^2) \overrightarrow{e_r} + (2 \dot r \dot \theta + r \ddot \theta) \overrightarrow{e_{\theta}} + \ddot z \overrightarrow{e_z}
\end{align*}
````

## Relation géométrique entre vitesse et accélération

````{margin}
Un mouvement uniforme n'est pas forcément rectiligne, le vecteur vitesse peut changer de direction.
````
````{important} __Mouvement uniforme, accélérié et décéléré__

* Un mouvement est dit __uniforme__ si la __norme__ de la vitesse est constante au cours du mouvement.
* Si la norme diminue, on dit que le mouvement est décéléré. Si la norme augmente, il est accéléré.
````


````{important} __Relation vitesse et accélération__

```{figure} ./images/qr_code/qr_cinema_demo_acc_vit.png
:name: qr_cinema_demo_acc_vit
:width: 150px
:align: right
:target: cinema_point.html#relation-geometrique-entre-vitesse-et-acceleration
```
* Dans un mouvement uniforme, le vecteur accélération est soit nul, soit perpendiculaire au vecteur vitesse.
* Dans un mouvement accéléré, le vecteur accélération forme avec le vecteur vitesse un angle en valeur absolue inféreure à $\pi / 2$
* Dans un mouvement décéléré, le vecteur accélération forme avec le vecteur vitesse un angle en valeur absolue supérieure à $\pi / 2$
````

````{topic} Démonstration
>Soit $\theta = (\overrightarrow{v};\overrightarrow{a})$. Remarquons que: 
>
>\begin{align*}
\overrightarrow{v} \cdot \overrightarrow{a} &= \overrightarrow{v} \cdot \frac{d\overrightarrow{v}}{dt}\\
\left \| v \right \| \left \| a \right \| \cos \theta &= \frac{d}{dt}(\frac{1}{2} v^2)
\end{align*}
>La vitesse est donc constante si: $\left \| v \right \| \left \| a \right \| cos \theta = 0$ soit si $\left \| a\right \|=0$ ou si $\theta = \pm \pi/2$.
>
>Sinon, $\textrm{sign}(\frac{dv}{dt}) = \textrm{sign}(\theta)$ donc la vitesse est décroissante si $|\theta| > \pi/2$ et croissante si $|\theta| < \pi/2$.
````



## Vecteur accélération: Base de Frenet
````{margin}
Le vecteur vitesse étant par définition tangent à la trajectoire, il est colinéaire à $\overrightarrow{u_T} $ (et dans le même sens).

On remarquera donc la relation utile: $\overrightarrow{u_T} = \frac{\overrightarrow{v}}{\left \| \overrightarrow{v}\right \|} $.
````
````{important} __Base de Frenet__

La base de Frenet est une __base locale__ définie __pour une trajectoire plane__. Elle est définit par deux vecteurs unitaires:

* Un vecteur tangeant à la trajectoire $\overrightarrow{u_T} $ et dirigé dans le sens du mouvement
* Un vecteur normale à la trajectoire $\overrightarrow{u_N} $ et dirigé de manière à ce que l'angle $(\overrightarrow{u_T}, \overrightarrow{u_N}) = + \frac{\pi}{2} $.
````


``````{important} __Composantes de l'accélération.__

Pour un mouvement plan, on peut décomposer l'accélération en deux composantes:
* l'accélération tangentielle $\overrightarrow{a_T} $ suivant $\overrightarrow{u_T}$
Cette composante de l'accélération est réponsable de la variation de vitesse (en norme: accélération et décélération)
* l'accélération normale $\overrightarrow{a_N} $ suivant $\overrightarrow{u_N} $
Cette composante de l'accélération est responsable de la déviation du mobile (changement de direction et donc courbure de la trajectoire.


Une étude des composantes de l'accélération montre qu'on a les relations suivantes:

\begin{align*}
\left\vert \overrightarrow{a_T} \right\vert &= \left\vert \frac{\rm{d}v}{\rm{dt}} \right\vert\\
\left\vert \overrightarrow{a_N} \right\vert &= \frac{v^2}{\left\vert R \right\vert}
\end{align*}
où $R$ est appelé rayon de courbure. Il peut varier dans le temps et reflète... la courbure de la trajectoire en un point.

````{list-table} Interprêter et visualiser la base de Frenet
:header-rows: 1

* - __Visualiser__
  - __Interpréter__
* - ```{image} ./images/qr_code/qr_cinema_frenet_visualiser.png
    :name: qr_cinema_frenet_visualiser
    :width: 150px
    :align: right
    :target: https://www.geogebra.org/m/BzmtMzUq
    ```
  - ```{image} ./images/qr_code/qr_cinema_frenet_interp.png
    :name: qr_cinema_frenet_interp
    :width: 150px
    :align: right
    :target: cinema_point.html#vecteur-acceleration-base-de-frenet
    ```
````
``````

````{topic} Interprétation
>Le [rayon de courbure](https://www.geogebra.org/m/BzmtMzUq) est algébrique: son signe dépend de la concavité de la trajectoire. Dans le cadre du programme, on se contentera de sa valeur absolue dans l'expression de l'accélération normale. Il suffit alors d'orienter l'accélération normale par la physique: est est toujours vers l'intérieur de la courbure de la trajectoire.
>
> On peut interpréter ces expressions.
>
>*  plus l'accélération normale est grande, plus la trajectoire va être courbée soit un faible rayon. De plus, plus la vitesse est grande, plus il faut une forte accélération pour courber la trajectoire.
>* l'accélération tangentielle étant directement reliée au caractère accéléré ou décéléré, il est logique d'avoir cette relation. La démonstration de l'expression de l'accélération tangentielle se fait d'ailleurs à partir du calcul du produit scalaire $\overrightarrow{a}\cdot\overrightarrow{v} $ comme on l'a fait précédemment.
>
>Quelques cas particuliers pour le rayon de courbure:
>* Cas d'une trajectoire circulaire (cf. suite): le rayon de courbure est le rayon du cercle.
>* Cas d'une trajectoire rectiligne: l'accélération normale étant alors nulle, le rayon de courbue est infini.
````





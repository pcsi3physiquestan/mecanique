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
# Vecteur accélération

## Vectreur accélération: Définition

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


## Vectreur accélération: Base de Frenet

````{margin}
Le vecteur vitesse étant par définition tangent à la trajectoire, il est colinéaire à $\overrightarrow{u_T} $ (et dans le même sens).

On remarquera donc la relation utile: $\overrightarrow{u_T} = \frac{\overrightarrow{v}}{\left \| \overrightarrow{v}\right \|} $.
````
````{important} __Base de Frenet__

La base de Frenet est une __base locale__ définie __pour une trajectoire plane__. Elle est définit par deux vecteurs unitaires:

* Un vecteur tangeant à la trajectoire $\overrightarrow{u_T} $ et dirigé dans le sens du mouvement
* Un vecteur normale à la trajectoire $\overrightarrow{u_N} $ et dirigé de manière à ce que l'angle $(\overrightarrow{u_T}, \overrightarrow{u_N}) = + \frac{\pi}{2} $.

````


````{important} __Composantes de l'accélération.__

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
````

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




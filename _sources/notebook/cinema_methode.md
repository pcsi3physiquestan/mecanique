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
# Méthodes

## Cinématique

````{admonition} Calcul d'une accélération en coordonnées sphériques.
:class: attention

On considère un point M contraint à se déplacer sur une sphère fixe de rayon $R_0$. Il part du pôle Nord de la sphère en direction du pôle Sud à une vitesse $v_0$ constante. Déterminer le vecteur accélération et l'évolution des coordonnées sphériques du point M dans un repère sphérique associé au référentiel de la boule.

````

````{topic} Résolution
>Cet exercice présente deux points importants: la traduction de contrainte cinématique en terme d'expression des coordonnées et des vecteurs et la détermination d'une accélération en sphérique par dérivation du vecteur vitesse.
>
> * Coordonnées et vecteur vitesse.
> Ici, les contraintes sont: $\rho = R_0= Cste; \theta = \frac{v_0}{R_0} t; \varphi = \varphi_0 = Cste$. On choisi l'origine des angles de tels sorte que $\varphi_0 = 0$. Il est important de comprendre l'expression de $\theta(t)$ qui traduit la relation en vitesse linéaire et vitesse angulaire.
>
> Il vient que le vecteur vitesse s'écrit:
>
>\begin{equation}
\overrightarrow{v_{M/Boule}} = R_0 \frac{v_0}{R_0} \overrightarrow{e_{\theta}}
\end{equation}
> * Dérivation du vecteur vitesse.
> Il vient par dérivation:
>
>\begin{align*}
\overrightarrow{a_{M/Boule}} &= \frac{\rm{d}v_0}{\rm{dt}} \overrightarrow{e_{\theta}} + v_0 \frac{\rm{d}\overrightarrow{e_{\theta}}}{\rm{dt}}\\
&= v_0 \left(\dot \theta  \frac{\partial \overrightarrow{e_{\theta}}}{\partial \theta} + \dot \varphi \frac{\partial \overrightarrow{e_{\theta}}}{\partial \varphi}\right)\\
&= - \frac{v_{0}^2}{R_0} \overrightarrow{e_\rho}
\end{align*}
````

````{admonition} Cas d'un satellite géostationnaire. 
:class: attention

Un satellite géostationnaire est un satellite en orbite circulaire autour de la terre à une altitude $h=r-R_T$ où $R_T$ est le rayon de la Terre (r est le rayon de l'orbite). L'orbite est équatoriale et il reste fixe par rapport à un point de la Terre. Il est soumis à une accélération dans le référentiel géocentrique:

$$
\overrightarrow{a} = - g_0 {(\frac{R_T}{r})}^2 \overrightarrow{e_\rho}
$$
Calculer r avec $g_0 = 9,8 \rm{m.s^{-1}}$ et $R_T = 6400 \rm{km}$.
````

````{topic} Résolution
>On peut utilise directement le fait que l'accélération radiale s'écrit $- \rho \dot \theta^2 \overrightarrow{e_\rho}$ (ici $r= \rho$)
>
>Un satellite géostationnaire doit tourner autour de la terre en 24h, soit une vitesse angulaire $\dot \theta = \frac{2 \pi}{T_0}$ avec $T_0 = 24 \rm{h} = 86400 \rm{s}$.
>
>Il vient:
>
>\begin{align*}
r &= {\left(\frac{g_0 R_T^2T_0^2}{4 \pi^2 }\right)}^{\left(1/3\right)}\\
&= 42 \times 10^3 \rm{km}
\end{align*}
````

````{admonition} Mouvement uniformément accéléré 
:class: attention

On considère un point M donc le vecteur accélération est constant. Déterminer l'équation horaire du point M pour une vitesse initiale $\overrightarrow{v_0}$ et une position initiale $M_0$ à $t = 0$.

````
````{topic} Résolution

>La direction du vecteur accélération étant constante, on va particulariser cet axe en le choisissant comme axe Ox. On pose le point O confondu avec $M_0$ et on choisit un système de coordonnées cartésiennes dont l'axe Oy est tel que le vecteur vitesse initiale soit plan xOy. On peut donc écrire  que:
>
>\begin{align*}
\overrightarrow{a} &= a_0 \overrightarrow{e_x}\\
\overrightarrow{v} &= v_{0x} \overrightarrow{e_x} + v_{0y} \overrightarrow{e_y}
\end{align*}
>
>Par projection, on trouve que:
>
>\begin{align*}
\frac{\rm{d}v_x}{\rm{dt}} &= a_0\\
\frac{\rm{d}v_y}{\rm{dt}} &= 0\\
\frac{\rm{d}v_z}{\rm{dt}} &= 0
\end{align*}
>soit par intégration:
>
>\begin{align*}
v_x &= v_{0x} + a_0 t \Longrightarrow x(t) = \frac{a_0}{2}t^2 + v_{0x} t + x_0\\
v_x &= v_{0x} \Longrightarrow x(t) = v_{0x} t + y_0\\
v_x &= 0 \Longrightarrow x(t) = z_0
\end{align*}
>Comme nous le verrons, on peut montrer qu'une telle équation est celle d'une parabole.

````

## Cinétique
### Calcul de moment cinétique

````{admonition} Exercice 
:class: attention

Soit un repère cartésien de centre O associé à un référentiel $\mathfrak{R}$.

On considère un point matériel M de masse M en mouvement rectiligne sur un axe Oz à une vitesse $v(t)$.

1. Exprimer la quantité de mouvement de M dans le référentiel $\mathfrak{R}$.
1. Exprimer le moment cinétique du point M par rapport au point O dans le référentiel $\mathfrak{R}$. Commenter sa valeur.
1. Exprimer le moment cinétique du point M par rapport à l'axe Ox dans le référentiel $\mathfrak{R}$. Commenter sa valeur.
1. Exprimer le moment cinétique du point M par rapport à l'axe Bx dans le référentuel $\mathfrak{R}$. On donne les coordonnées de $B(a,b,0)$. Commenter.

````
````{topic} Résolution
>__Quantité de mouvement__
>\begin{equation}
\overrightarrow{p_{M/R}} = m \overrightarrow{v_{M/R}}
\end{equation}
>
>
>__Moment cinétique__
>\begin{align*}
\overrightarrow{L_{O/\mathfrak{R}}(M)} &= \overrightarrow{OM} \wedge \overrightarrow{p_{M/R}}\\
&= z \overrightarrow{e_z} \wedge m v(t) \overrightarrow{e_z}\\
&= 0\\
L_{Ox/\mathfrak{R}}(M) &= \overrightarrow{e_x} \cdot \overrightarrow{L_{O/\mathfrak{R}}(M)} = 0\\
\overrightarrow{L_{B/\mathfrak{R}}(M)} &= \overrightarrow{BM} \wedge \overrightarrow{p_{M/R}}\\
&= (-a \overrightarrow{e_x} - b \overrightarrow{e_y} + z \overrightarrow{e_z}) \wedge m v(t) \overrightarrow{e_z}\\
&= mav(t) \overrightarrow{e_y} - mv(t)b \overrightarrow{e_x}\\
L_{Ox/\mathfrak{R}}(M) &= \overrightarrow{e_x} \cdot \overrightarrow{L_{B/\mathfrak{R}}(M)} = - mv(t)b
\end{align*}
>Les moments par rapport à O et Ox sont évidemment nuls car le point M ne tourne pas autour de O (il s'en éloigne ou s'en rapproche en ligne droite) ni autour de Ox.
>
>Le moment autour de Bx est non nul car si l'on se place sur l'axe Bx, on voit effectivement le point M tourner autour de l'axe. Si v(t) et b sont positifs, le moment est négatif. En effet, la rotation à effectuer pour suivre le point M quand on est sur l'axe Bx ne se fait effectivement pas en cohérence avec l'orientation de l'axe Bx.

````

````{admonition} Exercice 
:class: attention

On considère un point M sur une trajectoire circulaire de centre O et d'axe Oz. Exprimer la quantité de mouvement dans une base cylindrique ainsi que le moment cinétique de M sur l'axe Oz.

````
````{topic} Résolution
>__Quantité de mouvement__
>
>\begin{align*}
\overrightarrow{p_{M/R}} &= m \rho \dot \theta \overrightarrow{e_{\theta}}\\
\overrightarrow{L_{O/\mathfrak{R}}(M)} &= \overrightarrow{OM} \wedge \overrightarrow{p_{M/R}}\\
&= \rho \overrightarrow{e_\rho} \wedge m \rho \dot \theta \overrightarrow{e_{\theta}}\\
&= m \rho^2 \dot \theta \overrightarrow{e_z} \\
\end{align*}
````

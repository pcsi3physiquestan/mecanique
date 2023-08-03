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
# Applications

## Actions mécaniques

````{admonition} Interaction électromagnétique
:class: attention
On considère un champ électromagnétique dont les deux parties électriques et magnétiques ont la même origine. Dans ces conditions, on montre qu'en norme $B \sim \frac{E}{c}$ avec $c$ la vitesse de la lumière dans le vide.
1. Dans le cadre de la mécanique relativiste $v \ll c$, montrer que la partie magnétique de l'interaction de Lorentz est toujours négligeable en norme devant la partie électique.
````
_Point utile pour cet exercice_
* _$\Longrightarrow$ Interactions usuelles._

````{admonition} Variation du champ de gravitation
:class: attention
1. Déterminer l'altitude à laquelle le champ de gravitation a diminué de 1% par rapport à son intensité au niveau de la mer.
2. Sachant que le champ de pesanteur est constitué à plus de 90% par l'action de la gravité, commenter l'hypothèse d'un champ de pesanteur uniforme et ses possibles limites.
````
_Point utile pour cet exercice_
* _$\Longrightarrow$ Interactions usuelles._


````{admonition} Mouvement d'une planète 
:class: attention

Le mouvement d'une planète du système solaire, dans les hypothèses des lois de Kepler est une ellipse dont l'un des foyers des le Soleil. Dans ce cadre d'hypothèses, la seule action subit par la planète est l'action gravitationnelle exercée par le Soleil. La planète et le Soleil sont assimilés à des points matériels.

1. Représenter qualitativement la trajectoire de la planète dans le référentiel héliocentrique. En quel point de l'ellipse la force gravitationnelle est-elle la plus forte ? la plus faible ?
1. Représenter deux points où la planète est accéléré, deux points où la planète est ralentie et deux points où l'accélération est normale à la vitesse. Que se passe-t-il en ces points ?
1. Que vaut le moment de la force gravitationnelle calculée au Soleil ? On remarquera que malgré sa valeur, le mouvement de rotation de la planète autour du Soleil évolue.
````
_Point utile pour cet exercice_
* _$\Longrightarrow$ Interactions usuelles._
* _$\Longrightarrow$ Cinématique du point._
* _$\Longrightarrow$ Moment d'un force._

````{topic} Éléments de réponse (sans justification)
1. La force est (en norme) la plus forte au point le plus proche du Soleil (appelé périhélie) et elle est la plus faible au point le plus éloigné du Soleil (appelé aphélie).
1. Accéléré quand l'angle entre la vitesse et l'accélération est aigu, ralenti quand il est obtu. L'accélération est normale à la vitesse à l'aphélie et au pérhélie : en ces points, la vitesse atteint un extremum.
1. Il est nul (vecteur $\overrightarrow{SP}$ parallèle à la force gravitationnelle).


```{dropdown} _Conservation du moment cinétique_

Comme on le verra par la suite, la nullité du moment résultant des forces extérieures conduit à la conservation du moment cinétique. Cette propriété aura de nombreuse conséquences sur l'étude du mouvement des planètes.

```
````



## Théorèmes

````{admonition} Expérience de Milikan
:class: attention

On place des goutellettes d'huile chargée de masse m et de charge q entre deux plaques et on maintient les deux plaques distantes d'une distance d à une différence de potentiel U orienté de la plaque du haut vers la plaque vers le bas. Il règne alors entre les plaque un chaque électrique $\overrightarrow{E} = \frac{U}{d}\overrightarrow{e_z}$ avec $\overrightarrow{e_z}$ un vecteur unitaire vertical orienté vers le haut. On suppose le champ de pesanteur uniforme.

Exprimer la charge q en fonction des autres grandeurs introduites et de l'intensité du champ de pesanteur.
````
_Point utile pour cet exercice_
* _$\Longrightarrow$ Interactions usuelles._
* _$\Longrightarrow$ PFD._

````{admonition} Jeux aquatiques 
:class: attention

Un baigneur (masse $m=80\rm{kg}$) saute d'un plongeoir situé à une hauteur $h=10\rm{m}$ au-dessus de la surface d'eau. On considère qu'il se laisse chuter sans vitesse initiale et qu'il est uniquement soumis à la force de pesanteur (on prendra $g = 10 \rm{m.s^{-2}}$) durant la chute. On note Oz l'axe vertical descendant, O étant le point de saut.

1. Déterminer la vitesse $v_e$ d'entrée dans l'eau ainsi que le temps de chute $t_e$. Faire l'application numérique. 

Lorsqu'il est dans l'eau, le baigneur ne fait aucun mouvement. Il subit en plus de la pesanteur:

* une force de frottement: $\overrightarrow{f_v} = - k \overrightarrow{v}$ (où $\overrightarrow{v}$ est la vitesse dans le référentiel terrestre et $k = 250 \rm{kg/s}$).
* la poussée d'Archimède: $\overrightarrow{\Pi_A} = - \frac{m}{d_h} \overrightarrow{g}$ ($d_h = 0,9$ est la densité du corps humain).

2. Etablir l'équation différentielle du mouvement à laquelle obéit la vitesse en projection sur Oz, notée $v_z$. On posera $\tau = m/k$.
2. Intégrer cette équation.
2. Déterminer la vitesse limite $v_L$ en fonction de $m, k, g$ et $d_h$. Faire l'application numérique. 
2. Exprimer la vitesse $v(t)$ en fonction de $v_e, v_L, \tau$ et $t$. Déterminer à quelle instant le baigneur commence à remonter. Faire l'application numérique.
2. En prenant la surface de l'eau comme nouvelle origine, exprimer $z(t)$. En déduire la profondeur maximale pouvant être atteinte.
2. En fait il suffit que le baigneur arrive au fond de la piscine avec une vitesse de l'ordre de 1m/s pour pouvoir se repousser avec ses pieds: à quel instant $t_2$ atteint-il cette vitesse et quelle est la profondeur minimale du bassin?

Le même baigneur décide maintenant d'effectuer un plongeon. On suppose qu'il entre dans l'eau avec un angle $\alpha = 60^{\circ}$ par rapport à l'horizontale et une vitesse $v_e = 8 \rm{m.s^{-1}}$. Les forces qui s'exercent sur lui sont les mêmes que précédemment mais le coefficient k est divisé par deux en raison d'une meilleure pénétration dans l'eau. On repère le mouvement par les axes Ox (axe horizontal de même sens que $\overrightarrow{v_0}$) et Oz (vertical descendant comme précédemment); le point O est le point de pénétration dans l'eau.

8. Déterminer les projections des équations du mouvement sur Ox et Oz. 
3. En déduire les composantes de la vitesse dans l'eau en fonction du temps. Existe-t-il une vitesse limite?
3. Le plongeur peut-il atteindre le fond de la piscine situé à 4m?

````
_Point utile pour cet exercice_
* _$\Longrightarrow$ Pesanteur._
* _$\Longrightarrow$ PFD._
* _$\Longrightarrow$ Méthodes de résolution du PFD (ordre 1)._

````{topic} Eléments de réponse (sans justification)

L'équation à vérifier est:

\begin{align*}
\frac{\rm{d}v_z}{\rm{dt}} + \frac{1}{\tau} v_z = -m \left(\frac{1}{d_h} - 1\right)g
\end{align*}
$v_e = -\sqrt{2gh}$ et $t_e = \sqrt{\frac{2h}{g}}$.

\begin{align*}
v_z(t) = v_L + (v_e - v_L)e^{-\frac{\left(t-t_e\right)}{\tau}}
\end{align*}
où $v_L = \frac{m (\frac{1}{d_h} - 1) g}{k}$.

Temps de remontée: $t_{rem} = \tau \ln \frac{v_L}{v_L - v_e} = $

\begin{align*}
z(t) = v_L \left(t - t_e\right) - \tau (v_e - v_L)e^{-\frac{\left(t-t_e\right)}{\tau}} -h + \tau (v_e - v_L)
\end{align*}
````



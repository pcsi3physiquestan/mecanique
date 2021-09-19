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
# Exercices d'application

## Jeux aquatiques

````{admonition} Exercice 
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
````{dropdown} Eléments de réponse (sans justification)

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
````

## Volant freiné

````{admonition} Exercice 
:class: attention

On considère un volant qui tourne autour d'un axe fixe horizontal. Son moment d'inertie autour de cet axe vaut J. Son barycentre est sur l'axe et le champ de pesanteur est uniforme et constant. Au cours du mouvement, le volant subit des frottements solides qu'on modélise comme un couple constant dont le moment par rapport à l'axe de rotation est $\vert M_f \vert = \alpha J$ avec $\alpha$ constant. On lance le volant à une vitesse angulaire $\omega_0$ et celui-ci s'immobilise après N tours.


1. Exprimer le coefficient $\alpha$ en fonction de $\omega_0$ et N.

````
````{dropdown} Eléments de réponse (sans justification)

$\alpha = \frac{\omega_0^2}{4 \pi N}$
```
````


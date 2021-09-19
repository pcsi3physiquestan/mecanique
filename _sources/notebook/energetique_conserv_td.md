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
# Travaux dirigés

## Mouvement d'un anneau sur une piste

````{admonition} Exercice 
:class: attention

On considère le dispositif suivant où un objet assimilable à un point matériel M de masse m se déplace solidairement à une piste de deux parties circulaires de rayons $R_1$ et $R_2$ et de centres $C_1$ et $C_2$ dans un plan vertical. On repère la position de M par l'angle $\theta$ dont le centre de référence est soit $C_1$ (partie (1)), soit $C_2$ (partie (2)). On prend les angles croissants dans le sens trigonométrique et $\theta_A=- \pi/2$. Il n'y a pas de frottements et on note g l'accélération de la pesanteur.

```{figure} ./images/energetique_piste_anneau.jpeg
:name: fig_247
:align: center

```

1. Exprimer l'énergie potentielle de pesanteur $E_p(\theta)$ de M en supposant $E_p = 0$ au point $B(\theta = \pi)$. On distinguera les cas (1) et (2). 
1. Tracer l'allure de $E_p(\theta)$
1. Déterminer les positions angulaires d'équilibre et leur stabilité. 
1. L'anneau est initialement en A. Il est lancé avec une vitesse $V_0$ (dans le sens trigonométrique). 
    1. Montrer graphiquement qu'on doit imposer une condition sur la vitesse $V_0$ pour que le mobile M atteignent le point F. 
    1. Exprimer cette condition en fonction des données du problème. 
    1. En déduire la vitesse du mobile en F (notée $V_F$) quand cette condition est remplie. 
    1. La condition précédente remplie, l'anneau sort-il de la piste en S? A quelle vitesse (notée $V_S$)? 
1. Déterminer à chaque instant la valeur de l'accélération normale en fonction de V la vitesse du mobile et des rayons $R_1$ et $R_2$ pour chaque partie (1) et (2). 
1. Dans la partie (1), déterminer la réaction de la piste sur l'anneau. S'il était remplacé par une bille roulant à l'intérieur de la piste, quelle serait la condition sur formule pour que la bille reste sur la piste. 
1. Même question pour la partie (2).

````
````{dropdown} Eléments de réponse (sans justification)

\begin{align*}
&\begin{cases}
E_p( \theta \leq \pi) &= -mgR_1 (\cos \theta + 1)\\
E_p( \theta \geq \pi) &= -mgR_2 (\cos \theta + 1)
\end{cases}
& V_0 \geq \sqrt{2 g R_1}\\
& V_S = \sqrt{V_{0}^2 - mgR_1 + mgR_2}
& N = \frac{mV_0^2}{R_{1}} + 3mg \cos \theta > 0
\end{align*}
\begin{align*}
````

## Equilibre de charges et petits mouvements

````{admonition} Exercice 
:class: attention

Tous les mouvements ont lieu suivant l'axe Ox et on néglige l'effet du poids. La force électrostatique exercée par un point $M_1$ de charge $q_1$ sur un point $M_2$ de charge $q_2$ est: $\overrightarrow{f} = \frac{q_1 q_2}{4 \pi \epsilon_0 M_1 M_2^2} \overrightarrow{u}$ où $\overrightarrow{u}$ est un vecteur unitaire dirigé de $M_1$ vers $M_2$. On travaille dans un référentiel R supposé galiléen.

1. Un point matériel de charge $q$ est fixé en O, origine du repère. Un autre point matériel M de charge identique $q$, initialement à droit de O, à la distance $a$ de O, est abandonné sans vitesse initiale.
    1. Déterminer en fonction de $x=OM>0$, l'énergie potentielle associée à la force électrostatique subie par M. On la prendra par     convention nulle pour M à l'infini. 
    1. Le point M est-il dans un état lié ou de diffusion? 
    1. Déterminer la vitesse du point M lorsqu'il est à l'infini. 
1. Un autre point matériel fixe O' de charge 4q est ajouté à une distante 2a à droite de O. Le point M est placé entre O et O'.
    1. Déterminer vectoriellement la résultante des forces qui s'exerce sur M en fonction de x=OM ($0<x<2a$). En déduire la position d'équilibre. On la notera par la suite $x_0$.
    1. Déterminer l'expression de l'énergie potentielle $E_p(x)$ du point et étudier la stabilité de la position d'équilibre $x_0$ pour 0 < x < 2a. 
    1. Représenter l'allure de $E_p(x)$ pour la particule de charge q pour $x \in [0; 2a]$. Calculer la valeur de l'extremum $E_p(x_0)$.
1. On lâche sans vitesse initiale la particule M (de charge q, masse m) au voisinage du point d'équilibre.
    1. Justifier qu'on puisse faire l'approximation $(x - x_0) \ll 1$ pour tout le mouvement. 
    1. Etablir l'équation différentielle du mouvement au voisinage de cette position 
    1. En déduire la pulsation des petites oscillations et la forme de $x(t)$.

````
````{dropdown} Eléments de réponse (sans justification)

Cas à une charge: $E_p(x) = \frac{q^2}{4\pi \epsilon_0 x}$

$v_{\infty}^2 = \frac{q^2}{2\pi \epsilon_0 m a}$

Cas à deux charges: $E_p(x) = \frac{q^2}{4 \pi \epsilon_0} \left ( \frac{1}{x} + \frac{4}{2a - x}\right)$

Position d'équilibre (stable): $x_{eq} = \frac{2a}{3}$

$\omega_0 = \sqrt{\frac{\frac{q^2}{4 \pi \epsilon_0}\frac{27}{4a^2}}{m}}$
````

## Bille accrochée à deux ressorts

````{admonition} Exercice 
:class: attention

On considère le mouvement d'une bille M de masse m pouvant coulisser sans frottement sur un cerceau de plan vertical, de centre O et de rayon R. On note AB le diamètre horizontale du cerceau, Ox l'axe horizontal, Oy l'axe vertical et $\theta$ l'angle entre Ox et OM. Le sens trigonométrique est pris positif (on suppose que $\theta_B = 0$). On suppose que le cerceau est fixe dans le référentiel du laboratoire supposé galiléen. Dans tout le problème, on prendra comme origine des potentiels le point le plus bas du cerceau.

1. Dans un premier temps, la bille est attachée à un ressort de longueur à vide nulle et de raideur k dont la seconde extrémité est fixée en B.
    1. Faire un bilan des forces qui s'appliquent sur la bille M. Quelles sont les forces qui travaillent?
    1. Déterminer l'expression de la longueur du ressort en fonction de R et $\theta$. En déduire l'expression de l'énergie potentielle élastique pour le point M.
    1. Déduire du théorème de l'énergie mécanique l'équation différentielle du mouvement.
    1. Déterminer à partir de l'équation différentielle les position d'équilibre et étudier leur stabilité par linéarisation de l'équation. On note $\theta_d$ la position d'équilibre pour $\theta \in [- \pi; 0]$.
    1. Retrouver les conclusions précédentes par une étude de l'énergie potentielle.
1. Dans la suite, en plus du ressort précédent, on attache la bille à un deuxième ressort identique au premier mais dont la seconde extrémité est fixée en A.
    1. Faire un bilan des forces qui s'appliquent sur la bille M. Quelles sont les forces qui travaillent?
    1. Déterminer l'expression de la longueur du second ressort en fonction de R et $\theta$. En déduire l'expression de l'énergie potentielle élastique du le point M pour le second ressort.
    1. Exprimer le théorème de l'énergie cinétique (forme locale) pour le point M. En déduire l'équation différentielle du mouvement. Qu'observe-t-on?
    1. Déterminer la résultante des forces de rappel élastique et justifier l'observation précédente.
    1. Déterminer les positions d'équilibre et étudier leur stabilité.
    1. Déterminer l'expression de la réaction $\overrightarrow{N}$ du cerceau en fonction de $\theta$ sachant qu'on abandonne la bille depuis $\theta = \theta_0$ sans vitesse initiale. (On supposera $\vert \theta_0 \vert \approx \pi/2$).
    1. En déduire la condition à vérifier pour que la bille quitte le cerceau.
    1. Quelle est la condition nécessaire sur $k, R, m, g$ pour que la bille reste sur le cerceau lorsqu'elle est à l'équilibre.

````
````{dropdown} Eléments de réponse (sans justification)

Un ressort: 

$E_p = -k R^2 {(\cos{\theta})} - mgR\sin \theta + mgR$

Positions d'équilibre: $\tan \theta = \frac{mgR}{kR^2}$, il n'y a qu'une position stable: $\theta_{eq} = \arctan \frac{mgR}{kR^2}$

Deux ressorts:

$E_p = -mgR \sin\theta + mgR$, la seule position d'équilibre est en $\pi/2$
````



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

# Méthodes numériques

L'application de ces méthodes numériques nécessitent d'avoir d'abord travailler sur la résolution numérique d'équations différentielles d'[ordre 1](https://pcsi3physiquestan.github.io/capacites_numeriques/elec_reponse_o1.html) et [d'ordre 2](https://pcsi3physiquestan.github.io/capacites_numeriques/elec_reponse_o2.html). Une fois que vous aurez traité ces parties, vous pourrez faire les exercices suivant. Les méthodes écrites devront être modifiées pour le deuxième exercice.

## Période d'un pendule simple

__Attention, les angles sous Python sont en radians.__

On considère un pendule simple de longueur $l = 1 \rm{m}$ dans un champ de pesanteur $g = 9.81 \rm{m.s^{-2}}$. On néglige tout frottement.

> 1. Ecrire l'équation différentielle que doit vérifier l'angle $\theta$ que fait la tige avec la verticale descendante puis mettre ce problème sous la forme d'un problème d'Euler $\frac{\rm{d}Y}{\rm{dt}}(t) = F(Y(t), t)$ en précisant les expressions de $Y(t)$ et $F(Y(t), t)$. Quelle est la taille de $Y(t)$.
> 2. En utilisant la fonction native `odeint` de `scipy.integrate` obtenir l'évolution de l'angle $\theta$ sur $30 \rm{s}$ pour une pendule lâché d'un angle $120 ^{\circ}$ sans vitesse initiale.
> 3. Ecrire une `periode(alph:float) -> float` qui, après avoir résolution le problème d'Euler précédent pour un pendule lâché sans vitesse initiale d'un angle `alph` sur une durée de $100 s\rm{s}$, déterminer la période du signal. Pour cela, vous devrez :
>     * Déterminer N le nombre de changement de signe de $\theta(t)$ (dont le nombre d'annulations).
>     * La durée $\delta t$ entre la première et la dernière annulation.
>     * La période $T = \frac{2\delta t}{N-1}$
> 4. Tracer la période des oscillations du pendule pour des angles entre $alph = 10 ^{\circ}$ et $alph = 150 ^{\circ}$ par pas de $10 ^{\circ}$. Analyser.

## Portée d'un tir de badminton

La trajectoire d'un volant de badminton (masse $m = 5.3 \rm{g}$) nécessite de prendre en compte les frottements de l'air. La forme du volant et sa vitesse impose un régime d'écoulement d'air turbulent et la force de frottement de l'air sur le volant est alors modélisée par:

$$
\overrightarrow{f}_v = - \frac{1}{2} \rho \pi R^2 C_x \left \| \overrightarrow{v}\right \| \overrightarrow{v}
$$

```{margin}
_La physique du sport_, Caroline Cohen, 2014
```
avec $\rho = 1.29 \times 10^{-3} \rm{kg.m^{-3}}$  la masse volumique de l'air, $R = 3.4 \rm{cm}$ le rayon du volant de badminton (face au flux d'air), $C_x = 0.65$ le coefficient de trainée du volant dans l'air et $\overrightarrow{v}$ la vitesse du volant dans l'air.

Soumis de plus à la pesanteur $g = 9.81 \rm{m.s^{-2}}$, l'étude théorique de la trajectoire du volant est délicate. On se propose de l'étude de manière numérique pour une vitesse initiale $V_0 = 60 \rm{m.s^{-1}}$ et un angle de départ $alph$ variable. L'altitude initiale du volant est $h_0 = 2\rm{m}$.

> 1. Ecrire l'équation différentielle qui régit l'évolution du volant de badmintion et mettre ce problème sous la forme d'un problème d'Euler $\frac{\rm{d}Y}{\rm{dt}}(t) = F(Y(t), t)$ en précisant les expressions de $Y(t)$ et $F(Y(t), t)$. Quelle est la taille de $Y(t)$.
> 2. Ecrire une fonction `euler(f:callable, v0:float, alph:float, pas:float) -> (numpy.ndarray, numpy.ndarray)` qui réalise le schéma d'intégration d'Euler explicite et renvoie l'évolution des coordonnées de position et de vitesse pour une vitesse initiale `v0` et un angle `alph` initial. __L'intégration ne devra pas s'arrêter pour un temps défini mais lorsque l'altitude du volant devient négative.__
> 3. Tracer la trajectoire du volant pour un angle de $45 ^{\circ}$ en choisissant un pas d'intégration correct.
> 4. Ecrire une fonction `portee(alph:float)` qui renvoie la portée estimée du tir pour un angle `alph`.
> 5. Tracer la portée du tir en fonction de l'angle $alph$ et déterminer la gamme d'angle acceptable pour un retour de fond de court où la portée doit être entre 9m et 12m.

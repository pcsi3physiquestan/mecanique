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

## Pendule simple modifié

````{admonition} Exercice 
:class: attention

On considère un pendule simple modifié. Un mobile ponctuel M de masse m est accroché à l'extrémité d'un fil inextensible de longueur L et de masse négligeable, dont l'autre extrémité est fixe en O. On néglige tout frottement. On repère la position du pendule par l'angle $\theta$ qu'il fait avec la verticale. Lorsque $\theta>0$, le système se comporte comme un pendule simple de centre O et de longueur de fil L. A la verticale et en dessous de O, un clou planté en O' avec OO'=L/3, qui bloquera la partie haute du fil vers la gauche. Quand $\theta < 0$, le système se comporte donc comme un pendule simple de centre O' et de longueur de fil 2L/3.

A la date t=0, le mobile est lâché sans vitesse initiale avec une inclinaison $\theta(0) = \theta_0 > 0$. On note $t_1$ la date de première rencontre du fil avec le clou et $t_2$ la date de la première annulation de la vitesse du mobile pour formule. L'intervalle $[0; t_1[$ est nommé première phase du mouvement, l'intervalle $]t_1;t_2[$ est nommé deuxième phase du mouvement. A la date $t_1^{-}$, le fil n'a pas encore rencontré le clou et à la date $t_1^{+}$, le fil vient de toucher le clou.

1. Par le théorème de la puissance mécanique (dérivée du théorème de l'énergie mécanique), établir l'équation différentielle vérifiée par $\theta$ pour la première phase du mouvement. 
1. En utilisant le théorème de l'énergie mécanique, déterminer la vitesse $v_1^{-}$ de M à la date $t_1^{-}$. En déduire la vitesse angulaire $\omega_1^{-}$ à cette date. 
1. Dans l'hypothèse des petites oscillations (pour cette question uniquement), déterminer la durée $\delta t_I$ de la première phase. 
1. Le blocage de la partie supérieure du fil par le clou ne s'accompagne d'aucun transfert énergétique. Déterminer la vitesse $v_1^{+}$ de M à la date $t_1^{+}$. En déduire la vitesse angulaire $\omega_1^{+}$ à cette date. 
1. Déterminer l'angle $\theta_2$ atteint à l'instant $t_2$. 
1. On se place à nouveau dans le cadre des petites oscillations. En utilisant les résultats des questions 1 et 2, donner sans calcul la durée $\delta t_{II}$ de la deuxième phase. 
1. Décrire brièvement la suite du mouvement de ce système et donner l'expression de sa période T. 

````



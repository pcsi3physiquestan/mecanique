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
# Méthodes : Applications des théorèmes
Les exercices seront corrigés en cours. Une version dui corrigé est disponible en ligne (Connexion Moodle nécessaire).
```{image} ./images/qr_code/qr_theoremes_methodes.png
:name: qr_theoremes_methodes
:width: 150px
:align: right
:target: https://moodlecpge.stanislas.fr/mod/resource/view.php?id=174
```



## Mouvement dans un champ de pesanteur

Cet exercice présente plusieurs points de méthodes extrêment importants :
* la méthode générale d'étude d'un système mécanique
* l'application du principe fondamental de la dynamique
* l'utilisation de différentes d'intégration: primitivation, équation différentielle linéaire et __séparation des variables__.


````{admonition} Exercice 
:class: attention

On considère un point matériel M de masse $m$ se déplaçant dans un champ de pesanteur uniforme $\overrightarrow{g}$. On oriente l'axe Oz tel que $\overrightarrow{g} = - g \overrightarrow{e_z}$.

1. Cas d'une chute libre. On suppose que le mobile est initialement immobile à une altitude $h$.
    1. Cas sans frottements: Exprimer $z(t)$ et en déduire le temps que met le mobile pour atteindre l'altitude $z=0$. Déterminer la vitesse à cet instant.
    1. Cas avec frottements linéaires: On suppose que le solide est soumis à une force de frottements du type $\overrightarrow{F} = - \lambda \overrightarrow{v}$
        1. Etablir l'équation différentielle qui régit l'évolution de $v(t)$
        1. En déduire l'existence d'une vitesse limite $v_{l}$
        1. Déterminer $v(t)$ puis $z(t)$.
        1. Exprimer un temps caractéristique au bout duquel on peut considérer que le mobile a atteint sa vitesse limite.

    1. Cas de frottements quadratiques: On suppose que le solide est soumis à une force de frottements du type $\overrightarrow{F} = - k \left \| \overrightarrow{v} \right \| \overrightarrow{v}$. On note $v(t)$ telle que $\overrightarrow{v} = v(t) \overrightarrow{e_z}$.
        1. Sachant que le mobile a toujours du déplacement vers le bas, expliciter $\overrightarrow{F}$.
        1. En déduire l'équation différentielle qui régit l'évolution de $v(t)$
        1. Déterminer la vitesse $v_l$ (en norme) telle que le mouvement soit rectiligne uniforme.
        1. Réécrire l'équation différentielle sous la forme: $m \dot v - k v^2 = - k v_l^2$.
        1. En déduire $v(t)$ puis $z(t)$.
        1. Exprimer $z(v)$. Montrer qu'on peut déterminer une distance $H$ caractéristique sur laquelle la vitesse limite $v_l$ est atteinte.
1. Tir balistique: On suppose que le mobile est tiré du point O avec une vitesse $\overrightarrow{v_0} = v_0 \cos \alpha \overrightarrow{e_x} + v_0 \sin \alpha \overrightarrow{e_z}$.
    1. On néglige à nouveau les frottements.
        1. Déterminer, par une intégration vectorielle, le vecteur position $\overrightarrow{OM}(t)$.
        1. Déterminer l'altitude la plus haute atteinte et la portée $x_{\max}$, c'est-à-dire la distance à laquelle retombe le mobile à l'altitude $z=0$. En déduire l'angle $\alpha$ pour lequel la portée est la plus grande à $v_0$ fixée.
        1. Pour atteindre une distance $x_1 < x_{\max}$ à $v_0$ fixé, montrer qu'on peut choisir deux angles de tir possible. Qualifier ces deux tirs.
        1. On veut déterminer l'ensemble des points qui ne peuvent pas être atteinte par le mobile si l'on fixe $v_0$ Montrer que ces points sont situé dans une portion du plan délimitée par une parabole dont on déterminera l'équation.
    1. On considère maintenant des frottements fluides linéaires: $\overrightarrow{F} = - \lambda \overrightarrow{v}$
        1. Intégrer vectoriellement l'équation en $\overrightarrow{v}(t)$ obtenue. En déduire $\overrightarrow{OM}(t)$
        1. Exprimer l'équation cartésienne $z(x)$ de la trajectoire.
        1. Montrer que, même si l'on permet au mobile de descendre jusqu'à $z = - \infty$, il ne pourra pas dépasser une portée limite $x_{\lim}$
````

## Système masse-ressort
Outre les points évoquées précédemment, nous étudier le cas où l'équation différentielle linéaire est du second ordre. On verra ici le cas d'un oscillateur harmonique.

````{admonition} Exercice 
:class: attention

On considère un ressort de raideur k et de longueur à vide $l_0$ dont l'une des extrémités est accrochée en un point fixe A et l'autre extrémité en un point matériel M de masse m. Le ressort est maintenu vertical et le point M glisse sans frottements (A est toujours au dessus de M).

On repère la position de M sur un axe Ox vertical vers le haut où l'origine O est telle que la coordonnées x de M est nulle quand le système est au repos.

1. Déterminer la longueur du ressort à l'équilibre.
1. Déterminer l'équation qui régit l'évolution de $x(t)$.
1. En déduire l'expression de $x(t)$ si le point M est initialement immobile et que la longueur initialement du ressort est $l_1$.
````

## Perle sur un cerceau

Cet exercice va montrer comment appliquer le théorème du moment cinétique à un point matériel.

````{admonition} Exercice 
:class: attention

On considère une perle assimilable à un point matériel M de masse m considère à glisser sans frottements sur un cerceau de rayon R et de centre O dans le plan est vertical.

Etablir l'équation d'évolution de l'angle entre la verticale descendante et $\overrightarrow{OM}$ au moyen du théorème du moment cinétique puis simplifier l'équation obtenue si l'on suppose le mouvement de la perle de faible amplitude autour de sa position d'équilibre stable.
````

## Atome de Bohr


On va utiliser ici les différents théorèmes, non pas pour déterminer le mouvement (qui sera connu) mais pour déterminer certaines caractéristiques du système (ici le moment cinétique).


````{admonition} Exercice 
:class: attention

Soit un proton O de charge +e fixe et un électron M de charge -e (et de masse me) en mouvement circulaire uniforme (rayon R) autour du proton (supposé fixe). L'expérience montre que l'énergie totale du système est quantifiée sous la forme: $E_n = -\frac{K}{n^2}$ (on prend l'origine des énergies potentielles nulle à l'infini). Montrer que le moment cinétique de l'électron par rapport à O est quantifié.

On donne l'expression de l'énergie potentielle de l'électron sous l'action seule du proton: $E_p = \frac{-e^2}{4 \pi \epsilon_0 r}$ où r est la distance proton-électron.

````

## Mouvement d'un traineau

````{admonition} Exercice 
:class: attention

On considère un traineau assimilable à un point matériel de masse $m$ glissant sur un sol horizontal avec une vitesse $v$ constante. Le contact avec le sol suit les lois de Coulomb avec un coefficient de frottements dynamique $f_d$. L'existence des frottements impose, pour maintenir une vitesse constante $\overrightarrow{v}$ une traction $\overrightarrow{T}$par un utilisateur. Celle-ci se fait au moyen d'une corde avec un angle $\alpha$ avec l'horizontale.

1. Déterminer la norme $T$ de la traction en fonction de $\alpha, f, m$ et $g$.
````
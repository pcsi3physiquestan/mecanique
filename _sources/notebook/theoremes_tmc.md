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
# Théorème du moment cinétique

## Théorème du moment cinétique: Enoncé

````{important} __Fondamental : Théorème du moment cinétique. Enoncé par rapport à un point.__

Soit un point matériel M. Dans un référentiel galiléen $\mathfrak{R}$, la dérivée du moment cinétique du point M en un point A fixe dans $\mathfrak{R}$ par rapport au temps est égale à la somme des moments des forces appliquées en M par rapport au même point A.

\begin{equation}
{(\frac{d \overrightarrow{L_{O/\mathfrak{R}}}(M)}{dt})}_{\mathfrak{R}} = \overrightarrow{M_O}(\overrightarrow{F})
\end{equation}
````

>__Démonstration__
>\begin{align*}
\frac{\rm{d}\overrightarrow{L_{A/\mathfrak{R}}}(M)}{\rm{dt}}_{\mathfrak{R}} &= {\frac{\rm{d}}{\rm{dt}}\left(\overrightarrow{AM} \wedge \overrightarrow{p_{M/\mathfrak{R}}}\right)}_{\mathfrak{R}} \\
&= {\frac{\rm{d}}{\rm{dt}}\left(\overrightarrow{AM}\right)}_{\mathfrak{R}}  \wedge \overrightarrow{p_{M/\mathfrak{R}}} + \overrightarrow{AM} \wedge {\frac{\rm{d}}{\rm{dt}}\left(\overrightarrow{p_{M/\mathfrak{R}}}\right)}_{\mathfrak{R}}\\
&= \underbrace{\overrightarrow{V_{M/\mathfrak{R}}}  \wedge \overrightarrow{p_{M/\mathfrak{R}}}}_{= 0} + \overrightarrow{AM} \wedge \left(\sum \overrightarrow{F_{\to M}}\right)\\
&= \sum \overrightarrow{M_{A}\left(\overrightarrow{F_{\to M}}\right)}
\end{align*}
````{important} __Fondamental : Théorème du moment cinétique. Enoncé par rapport à un axe.__

Soit un point matériel M. Dans un référentiel galiléen $\mathfrak{R}$, la dérivée du moment cinétique du point M sur un axe $\Delta$ orienté fixe dans $\mathfrak{R}$ par rapport au temps est égale à la somme des moments des forces appliquées en M par rapport au même axe $\Delta$.
````


>__Démonstration__
>Il suffit d'appliquer le TMC en un point de l'axe et de projeter l'équation sur un vecteur directeur de l'axe.



__Interprétation__
On retrouve "l'intuition" qui a été utilisée dans le chapitre précédent pour prévoir l'évolution du moment. Le moment résultant sur le point M va influencer la rotation du point M autour de l'axe de calcul.


## Théorème du moment cinétique: Application au solide.

````{important} __Fondamental : TMC appliqué à un solide.__

La dérivée temporelle du moment cinétique d'un système de points matériel par rapport à un point/un axe fixe dans un référentel $\mathfrak{R}$ est égal à la somme du moment des actions extérieures calculé au point point/axe.
````


>__Démonstration__
>On va démontrer le cas du TMC par rapport à un point A. Le cas sur une axe étant similaire. Comme pour le cas du TRC, on peut appliquer le théorème du moment cinétique à chaque point $M_i$ du système. On distingue encore les actions extérieures et les actions intérieures. On rappelle que pour deux points $M_i$ et $M_j$ du système. Les forces de $M_i$ sur $M_j$ et de $M_i$ sur $M_j$ sont opposées et portées par la droite $M_i M_j$.
>
>On somme l'ensemble des théorèmes du moment cinétique ponctuels et on s'intéresse aux actions intérieures. On va particulariser les moments des actions de $M_i$ sur $M_j$ et de $M_j$ sur $M_i$. La somme donne:
>
>\begin{align*}
\overrightarrow{M_{A/\mathfrak{R}}\left(\overrightarrow{F_{M_j\to M_i}}\right)} + \overrightarrow{M_{A/\mathfrak{R}}\left(\overrightarrow{F_{M_i\to M_j}}\right)} &= \overrightarrow{AM_i} \wedge \overrightarrow{F_{M_j\to M_i}} + \overrightarrow{AM_j} \wedge \overrightarrow{F_{M_i\to M_j}}\\
&= \left(\overrightarrow{AM_i} - \overrightarrow{AM_j}\right) \wedge \overrightarrow{F_{M_j\to M_i}}\\
&= \overrightarrow{M_j M_i} \wedge \overrightarrow{F_{M_j\to M_i}}\\
&= 0
\end{align*}
>Le dernier produit vectoriel est nul car la troisième loi de Newton donne que la force de $M_j$ sur $M_i$ est portée par la droite $M_j M_i$. Il vient que le moment résultant des actions intérieures est nul.



__Interprétation__
Le moment cinétique d'un solide contient deux termes: l'information sur la rotation du centre d'inertie autour de l'axe d'étude et l'information sur la rotation du solide sur lui-même. Dans le cadre du programme, le moment cinétique se ramènera directement à l'information sur la rotation su solide complet autour de l'axe fixe considéré.

Dans ce cadre, l'interprétation du moment cinétique reste la même: on relie le mouvement de rotation sur l'axe à l'influence des actions extérieures sur ce mouvement (par le moment résultant de ces actions).


````{attention}
__TMC et TRC__


Pour un système de points matériels, le TMC __ne se déduit pas__ du théorème de la résulante cinétique.

Les deux théorèmes vont être complémentaires: le premier donne le mouvement du centre d'inertie et le second le mouvement de rotation autour de l'axe considéré.

````


Ces théorèmes ne servent pas uniquement à déterminer les mouvements. Ils peuvent aussi servir à déterminer les composantes de force/moment résultant d'une action inconnue (cas des actions de contacts). Comme on l'a fait "intuitivement" dans le chapitre précédent, on appliquera ces théorèmes en __statique__, c'est-à-dire que les termes inertiels (dérivée quantité de mouvement ou du moment cinétique) seront nuls.



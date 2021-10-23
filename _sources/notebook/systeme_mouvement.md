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
# Mouvements particuliers

## Translation

_On rappelle que dans une translation, tous les points du système ont la même vitesse dans un référentiel donné. Cette vitesse correspond donc aussi à la vitesse du centre d'inertie._

````{admonition} Fondamental : Eléments cinétiques
:class: attention

L'énergie cinétique du système S dans un référentiel peut alors s'écrire:

\begin{align*}
E_{c/R} &= \sum\limits_{i=1}^{n} \frac{1}{2} m_i v_i^2\\
&= \sum\limits_{i=1}^{n} \frac{1}{2} m_i v_{G/R}^2\\
&= \frac{1}{2} M v_{G/R}^2
\end{align*}
Le moment cinétique du système S par rapport à un point A dans un référentiel donné s'écrit donc:

\begin{align*}
\overrightarrow{L_{A/\mathfrak{R}}} &= \sum\limits_{i} \overrightarrow{AM_i} \wedge m_i \overrightarrow{v_{i/\mathfrak{R}}}\\
&= \left(\sum\limits_{i} m_i \overrightarrow{AM_i}\right) \wedge \overrightarrow{v_{G/\mathfrak{R}}}\\
&= \overrightarrow{AG} \wedge \overrightarrow{v_{G/\mathfrak{R}}}
\end{align*}
````
````{attention}

Ces expressions ne sont valables que pour un mouvement de translation.

````

## Solide en rotation autour d'un axe fixe

### Moment d'inertie

>_On rappelle que le champ de vitesse d'un solide en rotation autour d'un axe fixe s'exprime:_
>
>\begin{equation}
\overrightarrow{v_{P/R}} = \overrightarrow{\Omega} \wedge \overrightarrow{AP}
\end{equation}
>avec A un point de l'axe de rotation.


Nous allons d'abord introduire une grandeur très important pour décrire la rotation d'un solide. Nous verrons par la suite qu'elle intervient dans l'expression de l'énergie cinétique et du moment cinétique.


````{admonition} Définition : Moment d'inertie
:class: tip

Lorsqu'un solide S est en rotation autour d'un axe fixe, on définit son moment d'inertie $J_{S/\Delta}$ par rapport à l'axe  par la grandeur:

* Cas discret: $J_{S/\Delta} = \sum\limits_{i=1}^{n} m_i d_i^2$ où $d_i$ est la distance entre le point $P_i$ et l'axe.
* Cas continu: $J_{S/\Delta} = \iiint_{P \in S} \rho(P) {d(P)}^2 d \tau(P)$ où $d(P)$ est la distance entre le point P et l'axe.

````


__Analyse__
On remarquera que cette grandeur dépend à la fois de la masse (inertie) et de la distance à l'axe de rotation. On rappelle que plus la masse est loin de l'axe, plus il est difficile de modifier sa rotation depuis l'axe. On a donc bien une grandeur qui reflètre l'inertie du système.

Il est important de pouvoir analyser qualitativement le moment d'inertie d'un solide en fonction de sa répartition de masse. On observe en effet qu'à masse totale égale, __le moment d'inertie sera d'autant plus grand que la répartition de masse est éloignée de l'axe.__


### Solide en rotation autour d'un axe fixe: grandeurs cinétiques

_L'expression de la quantité de mouvement peut toujours s'obtenir par sommation et/ou en utilisant la position du centre d'inertie. Attention, la quantité de mouvement n'est pas nécessairement nulle (cas d'un centre d'inertie qui n'est pas sur l'axe de rotation)._

````{admonition} Fondamental : Moment cinétique sur l'axe de rotation
:class: attention

Pour un solide S en rotation autour d'un axe fixe  dans R, le moment cinétique $\sigma_{S/\Delta}$ du solide S dans le référentiel R s'exprime comme le produit du moment d'inertie $J_{S/\Delta}$ du même système multiplié par la vitesse de rotation $\omega$ __comptée algébriquement en cohérence avec l'orientation de l'axe__ (règle du tire-bouchon par exemple):

\begin{equation}
\sigma_{S/\Delta} = J_{S/\Delta} \omega
\end{equation}
````


__Démonstration__
\begin{align*}
\sigma_{S/\Delta} &= \iiint_{P \in S} \rho(P)(\overrightarrow{OP} \wedge \overrightarrow{v(P)})\cdot \overrightarrow{u_{\Delta}} d \tau(P)\\
&= \iiint_{P \in S} \rho(P)(\overrightarrow{OP} \wedge (\overrightarrow{\Omega} \wedge \overrightarrow{OP})) \cdot \overrightarrow{u_{\Delta}} d \tau(P)\\
\intertext{En utilisant des coordonnées cylindriques d'axe $\Delta$:}
&= \iiint_{P \in S} \rho(P)((r(P) \overrightarrow{e_r} + z(P) \overrightarrow{e_z}) \wedge (r(P) \omega \overrightarrow{e_{\theta}})) \cdot \overrightarrow{e_{z}} d \tau(P)\\
&= \iiint_{P \in S} \rho(P) r^2(P) \omega d \tau(P)\\
&= J_{S/\Delta} \omega
\end{align*}
````{admonition} Fondamental : Energie cinétique d'un solide en rotation autour d'un axe fixe.
:class: attention

Dans le cas d'une rotation autour d'un axe fixe $\Delta$, l'énergie cinétique du solide peut s'écrire sous la forme:

\begin{equation}
E_c = \frac{1}{2} J_{S/\Delta} \omega^2
\end{equation}
où $J_{S/\Delta}$ est le moment cinétique de S par rapport à l'axe $\Delta$ et $\omega$ la vitesse angulaire de rotation du solide sur le même axe.
````


__Démonstration__
\begin{align*}
E_{c/R} &= \sum\limits_{i=1}^{n} \frac{1}{2} m_i v_i^2\\
&= \sum\limits_{i=1}^{n} \frac{1}{2} m_i {(r_i \omega)}^2\\
&= \frac{1}{2} J_{S/\Delta} \omega^2
\end{align*}
````{dropdown} Remarque

On peut remarquer que le moment d'inertie par rapport à l'axe est d'autant plus grand que la plus grande partie de la masse du solide est éloignée de l'axe. Puisque ce sont les points les plus éloignés de l'axe qui auront la plus grande vitesse, il est logique que l'énergie cinétique soit d'autant plus grande que le moment d'inertie est grand.

On pourra faire le parallèle entre la forme de l'énergie cinétique de translation et celle de l'énergie cinétique de rotation. La masse inertielle, couplé à la vitesse de translation, joue le même rôle que le moment d'inertie, couplé à la vitesse angulaire de rotation.

````

````{attention}

Attention, ces expressions ne sont valables que si l'ensemble du solide tourne à la même vitesse angulaire, c'est-à-dire que le solide est indéformable.

````

### Moment d'inertie et moment cinétique

````{admonition} Exercice 
:class: attention

1. On considère un solide S constitué de deux tiges de longueurs L pouvant coulisser l'une sur l'autre. La tige placée en dessous est accrochée par une extrémité à un axe fixe dans un référentiel $\mathfrak{R}$. Préciser sans calcul pour quelles positions de la tige supérieure le moment d'inertie est maximal ou minimal.
1. Déterminer le moment d'inertie d'un point matériel de masse m sur un axe$\Delta$ situé à une distance d.
1. On considère deux cylindriques concentriques de moment d'inertie respectifs $J_1$ et $J_2$ sur leur axe de symétrie et tournant chacun à des vitesses angulaires $\omega_1$ et $\omega_2$ autour de cet axe. Déterminer le moment cinétique et l'énergie cinétique de l'ensemble constitué des deux cylindres.

````



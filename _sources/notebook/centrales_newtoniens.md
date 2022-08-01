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
# Potentiels newtoniens


````{important} __Interaction newtonienne__

Une interaction newtonienne est une force (ou un champ de force) dont l'intensité est inversement proportionnelle au carré de la distance entre les deux particules qui interagissent soit une force de la forme: $\overrightarrow{F} = - \frac{K}{r^2} \overrightarrow{e_r}$ en coordonnées cylindriques ou sphériques.

````

````{important} __Interaction électrostatique ou de Coulomb__

Soit deux particules chargées de charges $q_1$ et $q_2$ située aux points $M_1$ et $M_2$. La charge en $M_1$ exerce sur la charge en $M_2$ une force appelée force électrostatique de Coulomb dont l'expression est:

$$
\overrightarrow{F_{1 \rightarrow 2}} = \frac{q_1 q_2}{4 \pi \epsilon_0} \frac{\overrightarrow{M_1 M_2}}{M_1 M_2^3}
$$
où $\epsilon_0$ est appelée permittivité du vide: $\epsilon_0 = 8,85 \times 10^{-12} \rm{m^{-3}.kg^{-1}.A^{2}.s^{4}}$

````

````{important} __Interaction gravitationnelle ou de Newton__

Soit deux points matériels situées en $M_1$ et $M_2$ qui possèdent des masses gravitationnelles $m_{1}$ et $m_{2}$. Le point en $M_1$ exerce sur le point en $M_2$ une force gravitationnelle ou force de Newton dont l'expression est:

$$
\overrightarrow{F_{1 \rightarrow 2}} = -G m_{1} m_{2} \frac{\overrightarrow{M_1 M_2}}{M_1 M_2^3}
$$
où G est appelé constante de gravitation universelle: $G = 6,67 \times 10^{-11} \rm{m^{3}.kg^{-1}.s^{-2}}$

````

```{margin}
En général (mais ce n'est pas obligatoire), on choisit de fixer l'énergie potentielle nulle à l'infini.
```
````{important} __Energie potentielle__
Une interaction newtonienne dérive d'une énergie potentielle dont l'expression est $E_p = - \frac{K}{r} + cste$.
````

````{important} __Analogie__

On peut remarquer que la forme mathématique des deux forces est très semblables. Il vient que le traitement mathématique du mouvement d'un point matériel dans un champ gravitationnel sera identique au traitement du mouvement d'un point dans un champ électrostatique. Il suffira de transformer correctement les grandeurs comme dans l'analogie oscillateur mécanique-oscillateur électrique. Les correspondances sont les suivantes:

|Grandeur/Interaction | Electrostatique | Gravitationnel |
|:-:|:-:|:-:|
|Constante K | $- \frac{q_1 q_2}{4 \pi \epsilon_0}$ | $Gm_1 m_1$ |
|Causes | $q_1, q_2$ | $m_1, m_2$ |
````

Cf. [l'activite sur les ordre de grandeur](newt_odg).

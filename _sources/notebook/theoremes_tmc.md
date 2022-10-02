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

## Enoncé

````{important} __Théorème du moment cinétique. Enoncé par rapport à un point.__

Soit un point matériel M. Dans un référentiel galiléen $\mathfrak{R}$, la dérivée du moment cinétique du point M en un point A fixe dans $\mathfrak{R}$ par rapport au temps est égale à la somme des moments des forces appliquées en M par rapport au même point A.

$$
{(\frac{d \overrightarrow{L_{O/\mathfrak{R}}}(M)}{dt})}_{\mathfrak{R}} = \overrightarrow{M_O}(\overrightarrow{F})
$$
````

>__Démonstration__
>\begin{align*}
\frac{\rm{d}\overrightarrow{L_{A/\mathfrak{R}}}(M)}{\rm{dt}}_{\mathfrak{R}} &= {\frac{\rm{d}}{\rm{dt}}\left(\overrightarrow{AM} \wedge \overrightarrow{p_{M/\mathfrak{R}}}\right)}_{\mathfrak{R}} \\
&= {\frac{\rm{d}}{\rm{dt}}\left(\overrightarrow{AM}\right)}_{\mathfrak{R}}  \wedge \overrightarrow{p_{M/\mathfrak{R}}} + \overrightarrow{AM} \wedge {\frac{\rm{d}}{\rm{dt}}\left(\overrightarrow{p_{M/\mathfrak{R}}}\right)}_{\mathfrak{R}}\\
&= \underbrace{\overrightarrow{V_{M/\mathfrak{R}}}  \wedge \overrightarrow{p_{M/\mathfrak{R}}}}_{= 0} + \overrightarrow{AM} \wedge \left(\sum \overrightarrow{F_{\to M}}\right)\\
&= \sum \overrightarrow{M_{A}\left(\overrightarrow{F_{\to M}}\right)}
\end{align*}

````{important} __Théorème du moment cinétique. Enoncé par rapport à un axe.__

Soit un point matériel M. Dans un référentiel galiléen $\mathfrak{R}$, la dérivée du moment cinétique du point M sur un axe $\Delta$ orienté fixe dans $\mathfrak{R}$ par rapport au temps est égale à la somme des moments des forces appliquées en M par rapport au même axe $\Delta$.
````

>__Démonstration__
>Il suffit d'appliquer le TMC en un point de l'axe et de projeter l'équation sur un vecteur directeur de l'axe.


````{topic} Interprétation
On retrouve "l'intuition" qui a été utilisée dans le chapitre précédent pour prévoir l'évolution du moment. Le moment résultant sur le point M va influencer la rotation du point M autour de l'axe de calcul.
````



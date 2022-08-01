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

# Théorèmes énergétiques
````{admonition} Compétences
:class: tip
* Calculer la puissance et le travail d'une force
* Reconnaître le caractère moteur ou résistant d'une force.
* Savoir que la puissance dépend du référentiel
* Utiliser le théorème de l'énergie cinétique ou le théorème de la puissance cinétique de manière appropriée en fonction des contextes
* Utiliser le théorème de l'énergie mécanique ou le théorème de la puissance mécanique de manière appropriée en fonction des contextes
* Établir et connaître l'expression de l'énergie potentielle de pesanteur, gravitationnelle, élastique, de torsion et électrostatique.
* Distinguer forces conservatives et non conservatives. Reconnaître les cas de conservation de l'énergie mécanique.
````

````{topic} Rappels
_Soit un point matériel M de masse m animé d'une vitesse $\overrightarrow{v_{M/\mathfrak{R}}}$ dans un référentiel $\mathfrak{R}$. L'énergie cinétique du point matériel dans le référentiel $\mathfrak{R}$ est définie comme $E_{c/\mathfrak{R}}(M) = \frac{1}{2}m v_{M/\mathfrak{R}}^2$_

* Considérons un système mécanique évoluant d'un état A (vitesse et position donnée) à un état B (vitesse et position donnée). On peut définir l'énergie cinétique à chaque état A et B indépendamment des états précédents ou succédants aux états A et B et la __variation__ d'énergie cinétique de A à B ne dépend pas du chemin parcouru pour passer de l'état A à l'état B. On dit que l'énergie cinétique est une fonction d'état.
    * pour une variation finie, c'est-à-dire un déplacement sur une distance qui ne tend pas vers 0, on note la variation d'énergie cinétique $\Delta E_c$. (L'important c'est le $\Delta$).
    * pour une variation infinitésimale, c'est-à-dire un déplacement sur une distance qui tend vers 0, on note la variation d'énergie cinétique $dE_c$. (L'important, c'est le $d$ qui représente une différentielle).
````

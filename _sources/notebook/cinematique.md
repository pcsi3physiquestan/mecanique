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
# Cinématique et cinétique du point

````{admonition} Compétences
:class: tip
* Etablir les expressions du vecteur vitesse, du vecteur accélération et du vecteur position dans le cas des coordonnées cartésiennes et cylindriques.
* Etablir les expressions du vecteur position et du vecteur vitesse dans le cas des coordonnées sphériques. Savoir établir l'expression du vecteur accélération dans des cas simples.
* Etablir, à partir d'un schéma, le déplacement élémentaire dans les différents systèmes de coordonnées. Construire le tridère local associé à chaque système de coordonnées et en déduire les composantes du vecteur vitesse.
* Choisir un système de coordonnées adapté au problème posé.
* Cas du mouvement circulaire: Exprimer les composantes du vecteur position, du vecteur vitesse et du vecteur accélération en coordonnées polaires.
* Cas du mouvement circulaire: Identifier le lien entre le vecteur accélération, la courbure de la trajectoire, la norme du vecteur vitesse et sa variation temporelle.
* Situer qualitativement le vecteur accélération dans la concavité d'une trajectoire plane.
* Connaître les caractéristiques cinétiques d'un point matériel et pouvoir les calculer dans différentes systèmes de coordonnées pour des mouvements usuels.
* Relier la direction et le sens du vecteur moment cinétique aux caractéristiques du mouvement.
````

Nous allons commencer par étudier les mouvements de points matériels. Les mouvements d'un tel système sont décrits uniquement par ses mouvements de translation (rectiligne ou non). Il n'y a pas de _rotation_ d'un point sur lui même.  
Nous allons présenté ses éléments _cinématiques_ (décrivant le mouvement sans matérialité du point) et _cinétiques_ (décrivant le mouvement du point avec son inertie : on tient compte de sa masse.)
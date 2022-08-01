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
# Oscillations forcées

On se place maintenant dans le cas d'un oscillateurs amorti soumis à une force sinusoïdale. On s'intéresse uniquement au cas du régime sinusoïdal forcé. Comme étudié précédemment, on réalise le changement de variable nécessaire pour annuler second membre constant. On va étudier deux types de réponses: la réponse en élongation et la réponse en vitesse.


## Oscillations forcées: Equation

````{topic} Mise en équation
Comme on l'a vu, l'équation d'évolution devient:

\begin{align*}
\frac{\rm{d^2}X}{\rm{dt^2}} + 2 \xi \omega_0 \frac{\rm{d}X}{\rm{dt}} + \omega_0^2 X = F_m \cos \omega t
\end{align*}
````

````{admonition} Réponse en position 
:class: attention

1. Déterminer la réponse en position en régime forcé. On déterminera l'amplitude complexe puis l'amplitude réelle et la phase. Quel type de filtrage est réalisé.
1. Etudier l'existence d'une résonance en fonction du coefficient d'amortissement.
1. Pour $\xi = 1$, déterminer la fréquence de coupure.
1. Etudier l'allure du diagramme de Bode.

````

````{admonition} Réponse en vitesse 
:class: attention

1. Déterminer la réponse en vitesse en régime forcé. On déterminera l'amplitude complexe puis l'amplitude réelle et la phase. Quel type de filtrage est réalisé.
1. Déterminer la pulsation de résonance et étudier la largeur de la bande passante.
1. Etudier l'allure du diagramme de Bode.

````

````{admonition} Réponse en puissance 
:class: attention

1. En appliquant le théorème de l'énergie mécanique, montrer que la puissance moyenne fournie par la force excitatrice est proportionnelle à l'amplitude de la vitesse au carré du système.
1. En déduire la réponse fréquentielle en puissance et son allure. Pour quelle pulsation la puissance absorbée par l'oscillateur est-elle maximale ?

````


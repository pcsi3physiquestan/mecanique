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
# Eléments cinétiques
## Quantité de mouvement

````{sidebar} Intérêt
La quantité de mouvement est fondamentale car c'est elle qui est directement modifiée par l'action du milieu extérieur au point matériel M par l'intermédiaire des forces comme nous le verrons par la suite.
````
````{important} __Quantité de mouvement d'un point matériel__

Soit M un point matériel de masse inertielle m. On définit la quantité de mouvement d'un point M dans le référentiel R par la grandeur:

$$
\overrightarrow{p_{M/R}} = m \overrightarrow{v_{M/R}}
$$
````

## Moment cinétique d'un point matériel

````{topic} Introduction
Au niveau du point matériel, le moment cinétique se déduit de la quantité de mouvement. Il permet d'étudier plus simplement certains types de mouvement (mouvement de rotation) car il donne directement des informations sur...  la rotation du point.

Lorsque nous travaillerons à des systèmes de points matériels, nous verrons que ce moment ne se déduit plus directement de la quantité de mouvement et devient alors une source d'information __complémentaire__ à la quantité de mouvement.
````

### Moment cinétique: Définition

````{sidebar} Dépendance du point considéré

Un moment cinétique se calcule par rapport à un A de l'espace (pas nécessairement le centre du repère). Il est important de le préciser car l'expression du moment cinétique __dépend du point considéré__. Celà devient évident lorsqu'on donne un sens (cf. suite) au moment cinétique.

On peut calculerun moment cinétique par rapport à un point fixe ou non fixe dans le référentiel considéré. En physique, on se limitera à l'utilisation d'un point fixe de manière à pouvoir appliquer les théorème fondamentaux.
````
````{important} __Moment cinétique par rapport à un point.__

Soit un point M de masse m, de vitesse $\overrightarrow{v_{M/R}}$, de quantité de mouvement $\overrightarrow{p_{M/R}}$ rapport au référentiel R et A un point. Le moment cinétique d'un point M par rapport à un point A dans le référentiel R est défini par le vecteur:

$$
\overrightarrow{L_{A/R}(M)} = \overrightarrow{AM} \wedge \overrightarrow{p_{M/R}}
$$
````

```{margin}
L'expression précédente ne dépend pas du point B __tant que B est sur l'axe.__ C'est pourquoi on peut parler de moment cinétique sur un axe sans précision.
```
````{important} __Moment cinétique par rapport à un axe.__

Soit un axe $\Delta$ orienté. On note B un point de cet axe et $\overrightarrow{u_{\Delta}}$ un vecteur unitaire directeur de l'axe. On définit un moment cinétique rapport à l'axe $\Delta$:

$$
L_{\Delta/R} = \overrightarrow{u_{\Delta}} \cdot \overrightarrow{L_{B/R}}(M)
$$
````



````{attention}
__Scalaire et vecteur__

Le moment cinétique par rapport à un point est un __vecteur__ et le moment cinétique par rapport à un axe est un __scalaire__. Il est important de faire cette différence.
````

### Moment cinétique: Interprétation

````{topic} Interprétation du moment cinétique par rapport à un axe
>Dans toute la suite on travaillera implicitement dans un référentiel $\mathfrak{R}$.
>
>Pour interprêter le moment cinétique par rapport à un axe orienté $\Delta$, on va se placer dans un repère cylindrique d'axe $\Delta$ centré en un point O de l'axe.
>
>On peut donc écrire:
>
>\begin{align*}
\overrightarrow{OM} = r \overrightarrow{e_r} + z \overrightarrow{e_z}\\
\overrightarrow{v_{M/\mathfrak{R}}} = \dot r \overrightarrow{e_r} + r \dot \theta \overrightarrow{e_{\theta}} + \dot z \overrightarrow{e_z}
\end{align*}
>On peut donc calculer le moment cinétique de M sur $\Delta$ dans $\mathfrak{R}$:
>
>\begin{align*}
L_{\Delta/R} &= \overrightarrow{u_{\Delta}} \cdot \overrightarrow{L_{O/R}}(M)\\
&= m\overrightarrow{e_z} \cdot ((r \overrightarrow{e_r} + z \overrightarrow{e_z}) \wedge (\dot r \overrightarrow{e_r} + r \dot \theta \overrightarrow{e_{\theta}} + \dot z \overrightarrow{e_z}))\\
&= m r^2 \dot \theta
\end{align*}
>On observe que:
>
>* Le moment cinétique de M sur l'axe $\Delta$ n'est pas nul que le point M tourne autour de l'axe $\Delta$ __à l'instant t__. C'est fondamental pour comprendre l'utilisation du moment cinétique: il est principalement utilisée pour étudier des rotations. Attention, ça ne signifie pas que la trajectoire est courbe: un point M qui va en ligne droite semble tourne quand on se place sur un axe B non parallèle à la trajectoire ! Le moment est non nul si M semble tourner __par rapport à l'axe__.
>* Il dépend aussi de la distance à l'axe. L'introduction du moment cinétique est d'avoir une grandeur similaire à la quantité de mouvement mais pour la rotation, c'est-à-dire qui va être la grandeur modifiée par les actions du milieux extérieures __sur la rotation de M autour de l'axe__. D'un point de vue inertiel, on comprend qu'il est plus difficile de modifier la rotation d'un point matériel situé loin de l'axe si on se trouve sur l'axe.
>* Il est __algébrique__ et le moment cinétique est positif si le point M tourne dans le sens des $\theta$ croissant (angles orientés __en cohérence avec l'axe orienté__ $\Delta$) et le moment cinétique est négatif si le point M tourne dans le sens des $\theta$ décroissant (angles orientés __en cohérence avec l'axe orienté__ $\Delta$).
>
>On observe donc que le moment cinétique, à l'image de la quantité de mouvement contient des information
>
>*  sur le mouvement: sa vitesse de rotation et son sens de rotation autour de l'axe.
>* sur la facilité qu'on aura à modifier cette rotation depuis l'axe: sa masse et sa distance à l'axe.
>
>Il faut noter néanmoins que l'on ne garde __que des informations sur la rotation relative à l'axe.__. Comme montré précédemment un mouvement peut avoir des caractéristiques qui n'apparaissent plus directement (comme une trajectoire rectiligne non parallèle à l'axe $\Delta$).
````

````{topic} Interprétation du moment cinétique par rapport à un point.
>En remarquant que la projection du moment cinétique par rapport à un point Bsur différents axes passante par B, on trouve la tendance qu'a le point M à tourner autour de chaque axe. Il apparaît donc que le moment cinétique du point M par rapport à un point B correspond à la tendance que possède le point M à tourner autour de B (avec toutes les précautions précédentes sur le fait de tourner).
>
>On pourra noter aussi que cette tendance est maximale dans une direction. Il s'agit de la direction du vecteur moment cinétique: cette direction portant le moment cinétique par rapport à un point  donne l'axe perpendiculaire au plan dans lequel M est entrain de se déplacer autour de B à l'instant t.
````

# Energie cinétique

````{important} __Energie cinétique d'un point matériel__

On appelle énergie cinétique d'un point matériel M de masse m dans le référentiel R, la quantité scalaire:

$$
E_c = \frac{1}{2} m v_{M/R}^2
$$
````

````{topic} Variation d'énergie cinétique
* La variation d'énergie cinétique entre deux points A et B ne dépend que des états du système au point A et B (de la vitesse au point A et B) mais pas du chemin parcouru entre les deux. C'est pourquoi, on note cette variation $\Delta E_c$ (l'important, c'est le signe $\Delta$).
* Sur un déplacement infinitésimal, cette variation est infinitésimale et se note $dE_c$ (l'important, c'est le "d" appelé "d droit").
````




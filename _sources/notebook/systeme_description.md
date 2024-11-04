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
# Description d'un système de points

## Masse et centre d'inertie

````{important} __Masse totale__

On définit la masse totale M du système S comme la somme de toutes les masses des points matériels composant le solide.
````

````{topic} Expression mathématique
Dans le cadre d'une description discrète, la masse totale est simplement $M = \sum\limits_{i=1}^{n} m_i$.

Dans le cadre d'une description continu, la masse totale devient une intégrale: $M = \iiint_{P \in S} \rho(P) d \tau(P)$. A l'heure actuelle, il n'est pas demandé de savoir calculer une telle intégrale. Il suffit de comprendre qu'on somme des petits volumes infinitésimaux $d\tau(M)$ coefficientés (ici par la masse volumique).
````


```{margin} Interprétation qualitative
On remarquera que le centre d'inertie est décalé vers les zones plus massiques et que sa position respecte les symétries de masse du système.
```
````{important} __Centre d'inertie__

On définit le centre d'inertie G du système S comme le barycentre des points du solide affectés de leur masse.

* Cas d'un système discret:

$$
\overrightarrow{OG} = \frac{1}{M}\sum\limits_{i=1}^{n} m_i \overrightarrow{OP_i}
$$

* Cas continu:

$$
\overrightarrow{OG} = \frac{1}{M}\iiint_{P \int S} \rho(P) \overrightarrow{OP} d \tau(P)
$$
````

## Description d'un mouvement

### Description d'un mouvement: généralités (en ligne)
```{image} ./images/qr_code/qr_systemes_mouvement.png
:name: qr_systemes_mouvement
:width: 150px
:align: center
:target: systeme_description.html#description-d-un-mouvement-generalites-en-ligne
```


````{topic} Champ de vitesse
Le champ des vitesses d'un solide dans un référentiel R est la description de la vitesse de l'ensemble des points qui composent le solide. Il s'agit soit d'un ensemble discret de vecteurs vitesse affectés à chaque point, soit d'un champ vectoriel qui associe à chaque point P une vitesse correspondant à la vitesse du petit élément de matière autour du point P.
````

````{topic} Description générale - Cas d'un solide indéformable
Puisque tous les points du solide indéformable sont contraints à se déplacer ensemble, il vient que les mouvements des points du solide sont reliés les uns aux autres. Il suffit en réalité de connaître deux paramètres du mouvement global du solide pour pouvoir déterminer la vitesse de n'importe quel point du solide. Pour s'en convaincre - ce n'est pas une preuve - on peut remarquer que le mouvement d'un solide, à un instant t peut se décomposer en deux parties:

* un mouvement de translation globale du solide.
* un mouvement de rotation autour d'un axe (différent à chaque instant) appelé axe instantané de rotation.

Selon cette image, le mouvement d'un solide peut être décrit entièrement au moyen:

* De la vitesse en un point du solide.
* De la vitesse angulaire de rotation du solide autour de l'axe instantané de rotation. Celle-ci sera décrite par un vecteur rotation: $\overrightarrow{\Omega}$ contenant à la fois l'information sur la direction de l'axe et sur la vitesse angulaire.

__L'ensemble des deux données constitue le torseur cinématique introduit en sciences de l'ingénieur:__

$$
\mathcal{T}_{\Sigma,A} =
\begin{cases}
  &\Omega\\
  &\overrightarrow{v}_{A/R}
\end{cases}
$$

Pour comprendre l'utilisation des relations à venir ainsi que la descriptions des actions mécaniques. Nous conserverons ces notations bien qu'il ne soit pas nécessaire en physique de toujours écrire les grandeurs sus la forme de torseur. Cela simplifie surtout la compréhension des méthodes.
````

En physique nous n'utiliserons que deux cas particuliers: la translation seule et la rotation autour d'un axe fixe.

````{topic} Complément : Composition des vitesse (HP)
Soit un solide donc le vecteur taux de rotation à un instant t est $\overrightarrow{\Omega}$ et donc la vitesse en un point A du solide est connue par: $\overrightarrow{v_{A/R}}(t)$. Alors la vitesse en tout point B du solide est connue et donnée par la relation (de Varignon):

$$
\overrightarrow{v_{B/R}} = \overrightarrow{v_{A/R}} + \overrightarrow{\Omega} \wedge \overrightarrow{AB}
$$
Cette formule est valable quelque soit le mouvement du solide. Néanmoins, elle n'est pas à connaître et ne peut être appliquée directement en physique. Elle est par contre probablement à connaître et à savoir utiliser en SI. Les conséquences et définitions associées qui auront pu être vues en SI (centre instantanée de rotation, détermination graphique d'une vitesse... ) ne sont pas à connaître en physique. Par contre, les cas particuliers qui vont être présentés ensuite sont à connaître.

On dit qu'on réexprime le torseur cinématique en un autre point:

$$
\mathcal{T}_{\Sigma,A} =
\begin{cases}
  &\Omega\\
  &\overrightarrow{v}_A
\end{cases}
\Longrightarrow
\mathcal{T}_{\Sigma,B} =
\begin{cases}
  &\Omega\\
  &\overrightarrow{v_{B/R}} = \overrightarrow{v_{A/R}} + \overrightarrow{\Omega} \wedge \overrightarrow{AB}
\end{cases}
$$
````

## Mouvement de translation
```{margin}
Une translation ne signifie pas que le solide va forcément tout droit (ne pas confondre mouvement de translation et mouvement rectiligne). Ainsi, un solide peut avoir un mouvement de translation circulaire: c'est le cas des nacelles de grande roue.
```

````{important} __Translation__
Un solide est en translation si pour tout point P du solide, la vitesse $\overrightarrow{v_{P/R}}$ est identique.

```{topic} __Ecriture en terme de torseur(HP)__

Du point de vue torseur, on décrit donc un solide en translation avec un vecteur rotation nul:

$$
\mathcal{T}_{\Sigma,B} =
\begin{cases}
  &\Omega = 0\\
  &\overrightarrow{v_{B/R}}
\end{cases}
$$
Et il ne dépend pas du point considéré.
```
````




## Mouvement de rotation autour d'un axe fixe

````{important} __Rotation autour d'un axe fixe__

On peut définir le concept de rotation en rapport avec les composantes du torseur cinématique (cf SI). Pour nous, la description d'un solide en rotation autour d'un axe fixe est visuelle: il tourne sur lui-même.

````

````{important} __Champ de vitesse d'un solide en rotation__

Soit un solide en rotation autour d'un axe fixe, à un instant t, tous les points du solide ont la même vitesse angulaire $\omega(t)$. On peut alors définir un vecteur $\overrightarrow{\Omega}(t)$ appelé vecteur rotation du solide tel que pour tout point P du solide, la vitesse $\overrightarrow{v_{P/R}}$ s'écrit:

$$
\overrightarrow{v_{P/R}} = \overrightarrow{\Omega} \wedge \overrightarrow{AP}
$$
où A est un point de l'axe de rotation.
```{topic} __Ecriture en terme de torseur(HP)__

Du point de vue torseur, on décrit donc un solide en rotation par un torseur en un point de l'axe de rotation où sa vitesse est nulle:

$$
\mathcal{T}_{\Sigma,A \in axe} =
\begin{cases}
  &\Omega\\
  &\overrightarrow{v_{A/R}} = 0
\end{cases}
$$
La formule de Varignon redonne la relation du champ de vitesse précédent.
```
````

````{admonition} Démonstration
:class: note
>La vitesse angulaire est la même pour tout point du solide (sinon il se déformerait). On se place dans un système de coordonnées cylindriques d'axe $Az$ l'axe de rotation et de centre A. Pour un point P à un distance $r$ de l'axe:
>
>\begin{align*}
\overrightarrow{\Omega} \wedge \overrightarrow{AP} &= \omega \overrightarrow{e_z} \wedge (r \overrightarrow{e_r} + z \overrightarrow{e_z}) \\
&= r \omega \overrightarrow{e_{\theta}} \\
&= \overrightarrow{v_{P/R}}
\end{align*}
````

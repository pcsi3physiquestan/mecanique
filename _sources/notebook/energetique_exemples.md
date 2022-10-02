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
# Méthodes

## Calcul du travail d'une force.


Nous allons voir ici la méthode permettant de calculer le travail d'une force. Dans le cadre du programme, le point centrale est le paramétrage. Il permet d'obtenir une expression simple de l'intégrale à calculer.


````{admonition} Exercice 
:class: attention

On considère un point M sur une trajectoire circulaire dans un plan vertical. On repère l'angle $\theta$ que fait le vecteur position $\overrightarrow{OM}$ (O est le centre du cercle) par rapport au point le plus bas du cercle. Déterminer le travail du poids sur M lorsqu'il passe du point $\theta = 0$ au point $\theta = \theta_1$.

````
````{topic} Résolution
>__Plan du calcul__  
>
>On va détailler le calcul en deux étapes: on calcule le travail infinitésimal sur un déplacement élémentaire le long du cercle pour une position d'angle $\theta$ quelconque. On va alors trouver une expression de la forme $f(\theta)d\theta$. Il suffira alors de l'intégrer en choisissant correctement les bornes d'intégration en fonction du chemin choisi.
>
>
>
>__Travail infinitésimal__
>Le déplacement élémentaire __sur le cercle__ s'écrit $\overrightarrow{dOM} = R d\theta \overrightarrow{e_\theta}$. Quant à la force, elle s'écrit $\overrightarrow{P} = mg \cos \theta \overrightarrow{e_r} - mg \sin \theta \overrightarrow{e_\theta}$. Le travail élémentaire s'écrit donc: $\delta W = -mgR \sin \theta d \theta$
>
>
>
>__Intégration__
>L'expression du travail infinitésimal fait apparaître que l'intégration sera suivant $\theta$ (en effet, c'est en faisant varier cet angle qu'on décrit entièrement la trajectoire de M sur le cercle). Les bornes d'intégration sous le point de départ et d'arrivée soit $\theta = 0$ et $\theta = \theta_1$. Il vient:
>
>\begin{align*}
W &= \int_{\theta=0}^{\theta=\theta_1} - mgR \sin \theta d\theta \\
&= mgR \left(\cos \theta_1 - 1\right)
\end{align*}

```{admonition} Analyse du résultat
:class: hint, dropdown
On pourra vérifier ici l'homogénéité en utilisant le fait que mgz est homogène à une énergie (potentiel de pesanteur). Donc l'expression précédente est bien homogène à un terme énergétique comme doit l'être un transfert d'énergie mécanique (un travail).

On remarquera aussi que ce travail est __négatif__. Ce qui veut dire que le système a perdu de l'énergie sous l'effet du poids. En effet, en montant, il est ralenti: le poids a alors un effet __résistant__. Si le mouvement s'était effectué dans l'autre sens, le travail (transfert d'énergie mécanique) aurait été positif: le système aurait gagné de l'énergie. Le poids aura alors eu un effet __moteur__.
```
````

## Application du TEM/TEC

````{admonition} Toboggan circulaire 
:class: attention

On considère une masse m ponctuelle qui se déplace sans frottements sur une demie-sphère de centre O et de rayon R. Elle est soumise à un champ de pesanteur g et est lâchée du sommet avec une vitesse très faible vers la droite. La masse décolle-t-elle de la sphère? On utilisera deux méthodes différentes (utilisant respectivement le TEC puis le TEM) pour répondre à la question.

````
````{topic} Correction 
>__Condition de décollement et paramétrage__
>
>La condition de décollement est on le rappelle l'annulation de la composante normale de la réaction du toboggan sur la masse. Remarquons déjà que le TEC/TEM n'apporterons pas d'information sur cette composante. Elle est en effet perpendiculaire au moins (donc elle ne travaille pas) et dirigée vers le centre du cercle formé par le toboggan (donc de moment nul en ce centre). Il faut donc commencer par appliquer un PFD au point matériel M dans le référentiel du toboggan supposé galiléen.
>
>On utilise un système de coordonnées cylindriques d'axe Oz perpendiculaire au plan du mouvement (le mouvement est plan puisque les deux forces sont dans un même plan et la vitesse initiale dans le même plan) où O est le centre de la sphère. La vitesse s'écrit alors $\overrightarrow{v} = R \dot \theta \overrightarrow{e_\theta}$ et l'accélération $\overrightarrow{a} = - R \dot \theta^2 \overrightarrow{e_r} + R \ddot \theta \overrightarrow{e_\theta}$.
>
>Les deux forces qui s'appliquent sont le poids $\overrightarrow{P} = -mg \cos \theta \overrightarrow{e_r} + mg \sin \theta \overrightarrow{e_\theta}$ et la réaction du toboggan supposée normale par l'absence des frottements $\overrightarrow{R} = R \overrightarrow{e_r}$. La condition de contact s'écrit $R > 0$. L'annulation coïncidera avec le décollage.
>
>On applique donc le PFD.
>
>\begin{align*}
-m R \dot \theta^2 &= -mg \cos \theta + R\\
m R \ddot \theta &= mg \sin \theta
\end{align*}
>L'équation suivant $\overrightarrow{e_r}$ permet de déterminer R en fonction de la vitesse angulaire. Il reste donc à déterminer cette vitesse angulaire en fonction de l'angle pour répondre à la question. On va utiliser le TEC ou le TEM pour déterminer cette relation. Remarquons qu'on aurait pu utiliser à la place la seconde équation en la multipliant par $\dot \theta$.
>
>__Application du TEC__
>
>Il est important de savoir quel théorème on applique (puissance ou énergie) et de préciser sur quoi on applique le théorème. Ici, on va appliquerle théorème de l'énergie cinétique entre l'instant 0 et un instant t où le mobile est à un angle $\theta$. On considèrera la vitesse initiale négligeable devant la vitesse à l'instant t.
>
>L'énergie cinétique s'écrit: $E_c =\frac{1}{2} m R^2 \dot  \theta^2$. Sa variation vaut: $\Delta E_c = \frac{1}{2} m R^2 \dot  \theta(t)^2 - 0$
>
>La réaction du support est __perpendiculaire à la vitesse__ donc son travail est nulle sur tout le trajet. Le poids travaille est l'expression du travail élémentaire est $\delta W = mg \sin \theta d\theta$. En intégrant entre $\theta(t=0) = 0$ et $\theta(t=t) = \theta$, il vient: $W = mgR (1 - \cos \theta)$.
>
>On peut donc appliquer le théorème de l'énergie mécanique:
>
>
>\begin{align*}
\frac{1}{2} m R^2 \dot \theta^2 &= mgR \left(1 - \cos \theta\right)\\
m R \dot \theta^2 &= 2 mg \left(1 - \cos \theta\right)
\end{align*}
>Il vient en remplçant dans la première équation: $ R = 3 mg \cos \theta - 2mg$. La condition de décollement s'obtient pour $\theta = \arccos 2/3$.
>
>__Application du théorème de l'énergie mécanique__
>
>On applique à nouveau le théorème de l'énergie mécanique entre t=0 et t=t. Remarquons que la réaction du toboggan ne travaille pas et que le poids dérive d'une énergie potentielle donc il n'y a pas de force non-conservative: l'énergie mécanique est une constante. La variation d'énergie potentielle de pesanteur s'écrit $\Delta E_p = mg x(t) - mg x(0) = mg (\cos\theta - 1)$. Il vient:
>
>\begin{align*}
\Delta E_c + \Delta E_p &= 0\\
\left(\frac{1}{2} m R^2 \dot \theta^2 - 0\right) + mgR \left(\cos \theta - 1\right)&= 0\\
m R \dot \theta^2 &= 2 mg \left(1 - \cos \theta\right)
\end{align*}
>La suite de la résolution est identique au cas précédent. On remarquera l'équivalence logique de l'écriture du TEC et du TEM.

````

## Systèmes conservatifs

````{admonition} Propriétés états liés (en ligne).
:class: attention
Démontrer les propriétés suivantes spour un état lié d'un système conservatif.
* Les points extrêmes atteints par un état liés sont les points où $E_p = E_m$.
* Un état lié est nécessairement périodique
* L'évolution de la vitesse est symétrique à l'aller et au retour. 
````

````{topic} Démonstration
>__Démonstration__
>Commençons par rappeler que le PFD implique pour un système conservatif que l'accélération est une donnée de la position et de la vitesse seule (les forces ne peuvent varier explicitement en fonction du temps où le système ne serait pas conservatif). Cela signifie qu'en un état donné, la connaissance de la position et de la vitesse défini entièrement le mouvement ultérieur (on connaît l'équation différentielle et on a les deux conditions initiales, c'est un problème de Cauchy).
>
>Cela signifie aussi que si un système repasse par le même point  $(x(t);v(t))$ alors il va reproduire la même trajectoire de phase, c'est-à-dire le même mouvement.
>
>Points extrêmes: En un point où $E_p < E_m$, la vitesse du mobile est non nulle. S'il rebrousse chemin en ce point, alors il y aurait discontinuité de la vitesse (changement de signe nécessaire), ce qui est impossible. Il ne peut donc rebrousser chemin qu'en un point de vitesse nulle. (La réciproque est directe).
>
>Périodicité et symétrie: Supposons que le mobile passe par un point A entre les deux points extrêmes E et D. Une fois passé par E et D, il va revenir en A dans le même sens de parcours qu'initialement. Et en ce point, il aura la même vitesse (avec le même sens). On est donc revenu dans le même état. La remarque précédente assure que le mouvement ultérieur sera identique au mouvement précédent: le mouvement sera périodique.
>
>De même, on peut remarquer qu'à chaque position x, la vitesse sera la même, que le mouvement se fasse de E vers D ou de D vers E: le mouvement est donc symétrique.
````

````{admonition} Saut à l'elastique
:class: attention

On prend l'exercice du [saut à l'élasique](saut_elas). L'élastique est toujours modélisé par un ressort de raideur $k$ et de longueur à vide $l_0$ lorsqu'il est tendu et n'exerce aucune force lorsqu'il est détendu.

On veut savoir à quelle hauteur remonterait une masse test M de masse minimale (ici $m=65\rm{kg}$) si elle est lâchée sans vitesse initiale, l'élastique tendu au maximum : le point d'attache est à la hauteur $h=18\rm{m}$ au dessus du point de départ.

1. Déterminer l'altitude atteinte en utilisant l'énergie potentielle.
````
```{margin}
Attention au raccordement de $E_p$ pour la force de rappel : $E_p$ doit être __continue__.

```
````{topic} Correction
>On paramètre un axe vertical descendant où $z=0$ lorsque la loongueur de l'élastique est $l_0$.  
>Les seules actions qui s'appliquent sur le système \{masse-test\} sont:
>* le poids
>* l'action de l'élastique lorsqu'il est tendu.
>Ces deux forces étant conservatives, le système est conservatif et l'énergie mécanique est conservée.
>
>* L'énergie potentielle de rappel élastique est $E_{p,el} = \frac{1}{2}k z^2$ si $z > 0$ et nulle sinon.
>* L'énergie potentielle de pesanteur est $E_{p,pes} = -mgz$
>
> L'énergie potentielle totale est donc:
> \begin{equation}
\begin{cases}
E_ p &= \frac{1}{2}k z^2 - mgz \textrm{ si } z > 0\\
E_ p &= -mgz \textrm{ si } z < 0
\end{cases}
\end{equation}
>
> __Positions extrèmes :__ Le système étant conservatif, le TEM appliqué entre la position de départ et la hauteur maximale ($z_m$) s'écrit $E_m(z_m) - E_m(z_0) = 0$ avec $z_0 = h$. Soit (on fait l'hypothèse que z_m < 0) :
\begin{align*}
  0 &= -mgz_m - \left(\frac{1}{2}k h^2 - mgh \right)\\
  z_m &= h -\frac{k}{2mg} h^2
\end{align*}
````
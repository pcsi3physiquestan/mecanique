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
# Système à 1 degré de liberté

_Il est délicat de visualiser les propriétés précédentes et d'autres que nous allons voir pour des systèmes à multiples degrés de liberté car on ne peut avoir de représentation graphique simple de l'énergie potentielle. Par contre, pour un système à 1 degré de liberté, les représentations sont possibles. Nous allons travailler sur un tel système qui sera très présent en physique._

_Plusieurs éléments d'explications graphiques et d'exemples sont disponibles en ligne._

```{image} ./images/qr_code/qr_energie_conservatif.png
:name: qr_energie_conservatif
:width: 150px
:align: center
:target: energetique_conserv_1d.html
```

## Système à 1 degré de liberté et profil

````{sidebar} Illustration
Pour la suite, on considèrera que les grandeurs dépendent de la variable x. On notera ainsi $E_p(x), E_c(x)...$.

```{figure} ./images/meca_ep_1d_profil.jpg
:name: fig_profil_d_energie_potentielle239
:align: center
Profil d'énergie potentielle
```
````
````{important} __Système à 1 degré de liberté__

Un système à degré de liberté est un système où toutes les grandeurs peuvent être décrites comme des fonctions d'une seule coordonnée de l'espace ($x, \theta...$). Il s'agit en général dun mouvement rectiligne ou d'un mouvement de rotation.
````

````{topic} Analogie avec un profil d'altitude
Dans le cas d'une bille roulant sur un profil d'altitude à 1 dimension, l'altitude z dépend uniquement de x. On peut alors représenter $z(x)$ mais aussi $E_p(x)$ qui est proportionnelle à z.

Si les propriétés établies par la suite sont très générales et s'appliquent à des cas où l'énergie potentielle n'a pas pour origine la pesanteur, on pourra garder à l'esprit cet exemple pour visualiser les propriétés d'équilibre, de stabilité, d'état lié et de diffusion établies par la suite.

```{figure} ./images/meca_ep_1d_pes.jpg
:name: fig_240
:align: center
```
````

````{topic} Position et vitesse
On remarquera que l'énergie cinétique est aussi une fonction de la position __dans le cas d'un système conservatif__. En effet, on a :

$$E_c = E_m - E_p(x)$$

On retrouve ce principe sur le graphique suivant. On observe ici bien l'échange d'énergie entre l'énergie cinétique et l'énergie potentielle et on peut prévoir les caractéristique du mouvement:

* quand l'énergie potentielle augmente, la vitesse diminue
* quand l'énergie potentielle diminue, la vitesse augmente
* quand l'énergie potentielle atteint la valeur de l'énergie mécanique, la vitesse est nécessairement nulle
* en un point x, la vitesse sera la même quelque soit le sens de déplacement.
* en un point x où l'énergie potentielle est minimale, la vitesse sera maximale.

```{figure} ./images/meca_ep_1d_force_ec.jpg
:name: fig_profil_d_energie_potentielle_et_energie_cinetique241
:align: center
Profil d'énergie potentielle et énergie cinétique
```

Cette propriété permet de calculer la vitesse (en norme), en tout point d'une trajectoire d'un système conservatif et de prévoir les point où la vitesse est nulle ou maximale.
````

````{topic} _Energie potentielle et force_
On a aussi donné la direction de la force qui, on le rappelle, peut être déterminée en fonction de la __monotonie__ de l'énergie potentielle. Sa valeur ne se lit pas directement par contre (il faudrait la pente).
````

## Etats et barrière de potentiel

### Zonnes accessibles et barrière de potentiel

````{important} __Zones accessibles__

On va s'intéresse ici au cas des systèmes conservatifs : l'énergie mécanique est une constante.

On rappelle la positivité de l'énergie cinétique qui permet d'écrire la condition suivante: un point de coordonnées x est accessible par le système si $E_p(x) \leq E_m$: l'énergie potentielle est bornée. Cela définit des zones interdites et des zones accessibles.

```{figure} ./images/meca_ep_1d_zones.jpg
:name: fig_zones_accessibles_et_inaccessibles242
:align: center
Zones accessibles et inaccessibles
```

Dans l'exemple ci-dessus, si le système possède une énergie mécanique égale à $E_{m4}$, toutes les positions de $x_D$ à $x_E$ et les positions de $x_F$ à l'infini sont accessibles et les autres sont inaccessibles.
````

````{important} __Barrière de potentiel__

Remarquons que le mobile ne peut passer de la zone DE à la après F. En effet, pour passer de la première zone à la seconde, il faudrait passer par des points entre E et F qui sont inaccessibles par leur trop forte énergie potentielle. On dit qu'il y a une __barrière d'énergie potentielle__.

Suivant ses conditions initiales, le système sera soit "bloqué" entre D et E, soit entre F et l'infini.
````

````{margin}
Une fois qu'on a fourni de l'énergie au système, il n'est pas dans l'état "supérieur à F" défini précédemment (son énergie mécanique a changé). Il est dans un état qu'on pourrait pour l'instant appelé "supérieur à C" en utilisant les notations du graphique.
````
````{topic} Franchissement d'une barrière de potentiel

Sans apport d'énergie extérieure supplémentaire, le système ne peut passer de l'état "entre DE" à l'état "supérieur à F".

Par contre, si l'on apporte suffisamment d'énergie à un système bloqué "entre DE", il pourra se libérer.

```{figure} ./images/meca_ep_1d_barriere.jpg
:name: fig_barriere_d_energie_potentielle243
:align: center
Barrière d'énergie potentielle
```

Dans l'exemple ci-dessus, on apporte de l'énergie pour faire passer l'énergie mécanique à $E_{m3}$. Le système peut alors franchir la barrière d'énergie potentielle.

On peut chercher à calculer l'énergie minimale à apporter pour "libérer" le système. Il s'agit ici de la différence $E_{m5} - E_{m4}$soit la hauteur de la barrière de potentiel.
````

### Etats liés et de diffusion

````{important} __Etats liés et de diffusion__

On remarque sur les états précédents deux types d'états très particuliers: des états où le système est __confiné__ dans une portion d'espace (état "entre DE"). On parle d'état __lié__.

Des états où le système peut s'éloigner indéfiniment (état "supérieur à F"), on parle __d'état de diffusion__.

````

````{topic} Etats possibles

```{figure} ./images/meca_ep_1d_general.jpg
:name: fig_244
:align: center
```

Nous allons, au moyen du graphique précédent étudier les différentes états et leurs caractéristiques.
* $E_m = E_{m0}$: Cas où il n'y a aucun point accessible, c'est un état impossible.
* $E_m = E_m{1}$: Cas où il n'y a qu'un seul point accessible, c'est un __état d'équilibre.__ Nous verrons par la suite qu'il s'agit d'un état d'équilibre stable.
* $E_m = E_{m2}$: Cas où le seul état possible est un __état lié.__
* $E_m = E_{m3}$: Cas où le seul état possible est un __état de diffusion.__
* $E_m = E_{m4}$: Cas où deux états possibles existent, un état lié et un état de diffusion. L'état dans lequel se trouvera le système dépendra de ses conditions initiales. Une fois dans un état, le système ne peut passer de l'un à l'autre à cause de la __barrière de potentiel__.
* $E_m = E_{m5}$: Cas limite (inaccessible en pratique). Le système est soit dans un état lié (entre F et $O_1$), soit dans un état de diffusion (entre $O_1$ et l'infini) soit dans un état d'équilibre au point $O_1$. Comme nous le verrons par la suite, cet état d'équilibre est instable.
Le système ne peut pas passer d'un état à l'autre car il mettra un temps infini à atteindre le point $O_1$ (cette propriété est affirmée est non démontrée, elle ne peut se déduire du seul graphique proposé ici et aucune démonstration ne sera proposée).
````

## Equilibre et stabilité

### Condition d'équilibre

````{sidebar} Equilibre et stabilité
On retrouve l'assertion donnée précedemment selon laquelle $x_0$ et $x_1$ dont des positions d'équilibres.

Néanmoins, si l'on fait l'analogie avec une bille sur un profil d'altitude, on peut deviner que la nature de ces positions d'équilibre n'est pas la même, c'est là qu'intervient la notion de stabilité.

__Equilibre et stabilité sont donc deux concepts différents.__
````
````{important} __Condition d'équilibre__

Les positions d'équilibre d'un système conservatif sont nécessairement des positions où l'énergie potentielle possède un extremum (ou plus généralement un point d'annulation de la dérivée).
````

````{margin}
Si l'on travaille dans un autre système de coordonnées (cylindriques par exemple), l'expression du gradient doit être modifiée. La conclusion sera néanmoins identique.
````
````{topic} Démonstration
>On a déjà démontré cette propriété dans le cas général, mais nous allons à nouveau la présenter ici dans le cas à une dimension.
>
>On rappelle que la résultante des forces conservatives (ici la seule) est donnée par:
>
>\begin{align*}
\overrightarrow{F} &= - \overrightarrow{grad} E_p\\
&= - \frac{\rm{d}E_p}{\rm{dx}}(x) \overrightarrow{e_x}
\end{align*}
>A l'équilibre, la résultante des forces est nulle donc la dérivée de l'énergie potentielle est nulle.
````

### Stabilité des positions des d'équilibre

````{sidebar} Remarque

Il peut très bien y avoir plusieurs positions d'équilibre stable. On parle alors de bifurcation, car lorsque le système perd de l'énergie, il va naturellement aller vers une position d'équilibre (ou vers l'infini s'il était en état de diffusion). S'il y a deux positions d'équilibre, il va "bifurquer" vers l'une ou l'autre.

````
````{important} __Stabilité__

Une position d'équilibre est dite stable si, en écartant légèrement le mobile de cette position d'équilibre, il reviendra de lui-même vers la position d'équilibre.

Si la position n'est pas stable, elle est dite instable.
````


````{topic} __Preuve d'une stabilité__

On rappelle qu'il a été étudié précédemment deux méthodes possibles de stabilité d'une position d'équilibre: 
* on réalise l'écart cité précédemment et on étudie le signe de l'accélération
* on réalise l'écart cité précédemment et on linéarise l'équation différentielle du mouvement pour en étudier la stabilité.

Nous allons compléter ces deux méthodes par une troisième portant sur l'énergie potentielle.
````

````{important} __Energie potentielle et stabilité__

Si en une position d'équilibre, la dérivée seconde est strictement positive, alors c'est une position d'équilibre stable.

Si en une position d'équilibre, la dérivée seconde est strictement négative, alors c'est une position d'équilibre instable.

Si elle est nulle, on ne peut conclure.
````

````{admonition} Démonstration
:class: important
>On peut utiliser l'une des deux méthodes énoncées précédemment pour prouver cette propriété. Nous allons ici utiliser la propriété de stabilité des équation différentielle linéaires mais on pourrait très bien utiliser l'analyse du signe de l'accélération (s'entraîner à le faire).
>
>On rappelle que la force s'écrit $\overrightarrow{F} = - \frac{\rm{d}E_p}{\rm{dx}}(x) \overrightarrow{e_x}$. Pour linéairise le PFD, nous allons développer l'énergie potentielle à l'ordre 2. Il vient:
>
>\begin{align*}
E_p(x) &\approx_{x \approx x_{eq}} E_p(x_{eq}) + \underbrace{\frac{\rm{d}E_p}{\rm{dx}}(x_{eq})}_{=0} (x - x_{eq}) + \frac{1}{2} \frac{\rm{d^2}E_p}{\rm{dx^2}}(x_{eq}) {\left(x - x_{eq}\right)}^2\\
F(x) = - \frac{\rm{d}E_p}{\rm{dx}} &\approx_{x \approx x_{eq}} - 0 -  0 -  \frac{\rm{d^2}E_p}{\rm{dx^2}}(x_{eq}) {\left(x - x_{eq}\right)}\\
m \ddot x &= F(x) \approx - \frac{\rm{d^2}E_p}{\rm{dx^2}}(x_{eq}) {\left(x - x_{eq}\right)}\\
\frac{\rm{d^2}E_p}{\rm{dx^2}}(x_{eq}) x_{eq} &= m \ddot x + \frac{\rm{d^2}E_p}{\rm{dx^2}}(x_{eq}) x
\end{align*}
>La dernière équation est stable si la dérivée seconde est positive et instable si la dérivée seconde négative. Si elle est nulle, il faut faire un développement limité à un ordre supérieur. Mais l'équation obtenue n'est pas linéaire, la seule méthode utilisable sera de vérifier le signe de l'accélération.
````


### Petits mouvements autour d'une position d'équilibre stable

````{important} __Petits mouvements autour d'une position d'équilibre stable__

Autour d'une position d'équilibre stable, le système va rester confiné et se comporte comme un oscillateur harmonique de pulsation propre $\sqrt{\frac{\frac{\rm{d^2}E_p}{\rm{dt^2}}(x_{eq})}{m}}$.

La preuve est directe à partir de l'équation obtenue précédemment:

\begin{align*}
m \ddot x + \frac{\rm{d^2}E_p}{\rm{dx^2}}(x_{eq}) x &= \frac{\rm{d^2}E_p}{\rm{dx^2}}(x_{eq}) x_{eq}
\end{align*}
````
````{topic} Importance de ces études

L'étude aux petits mouvements est fondamentale, notamment pour les systèmes microscopiques. Elle permet une étude souvent fine des systèmes chimiques où les déplacements des atomes dans les liaisons intramoléculaires sont souvent des déplacements faibles autour de leur position d'équilibre. De la, on peut, comme nous le verrons par la suite, déduire des comportements en spectroscopie.

Cette caractéristiques a elle seule justifie l'importance des oscillateurs harmoniques et des oscillateurs amortis (cas où s'ajoute une force de frottements fluides au système, cf. suite).

On remarquera que cela revient à approximer localement l'énergie potentielle par une parabole, c'est-à-dire par un système masse-ressort de raideur $k = \frac{\rm{d^2}E_p}{\rm{dt^2}}(x_{eq})$. Cela explique pourquoi on modélise souvent les liaison moléculaires par des ressorts. La "raideur" de la liaison tend à modéliser la force avec laquelle le système sera ramené vers son état d'équilibre.

````

## Effet des frottements

````{topic} Effets des frottements fluides
Si le système est soumis à des forces de frottements, son énergie mécanique ne sera plus conservé. S'il s'agit de la seule force non conservatives, alors l'énergie mécanique va diminuer. Le système va alors tendre vers une des positions d'équilibre stable.

Dans le cas de frottements fluides, la condition d'équilibre n'est pas changée (puisque les frottements fluides dépendent de la vitesse, à l'équilibre, ils sont nuls). Les positions d'équilibre seront les mêmes que celles étudiées dans le cas conservatifs.

Suivant l'importance de la force frottements, le système va soit tendre directement vers la position d'équilibre, soit osciller autour de cette position en s'y approchant.

```{figure} ./images/meca_ep_1d_aperio.jpg
:name: fig_245
:align: center
```

```{figure} ./images/meca_ep_1d_pseudoper.jpg
:name: fig_246
:align: center
```
````

````{topic} Effets des frottements solides
Les frottements solides vont aussi faire diminuer l'énergie mécanique et rapprocher le système des positions d'équilibre stable. Néanmoins, comme nous le verrons dans le cas des oscillateurs, la valeur atteintes ne sera pas nécessairement la position d'équilibre déterminée dans le cadre des systèmes conservatifs (puisque la force de frottements solides peut être non nuls à l'équilibre).
````

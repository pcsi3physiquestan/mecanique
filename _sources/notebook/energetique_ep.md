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
# Forces/actions conservatives et énergie potentielle

Nous avons vu précédemment que le travail d'une action dépendant a priori du chemin parcouru entre 2 points. Il existe néanmoins une classe de forces où ce n'est plus le cas. Le travail ne dépendra plus que des positions A et B. Ces actions ont en physique un rôle extrêment important au point qu'on va les particulariser: ce sont les actions conservatives.


## Forces/actions conservatives: définition

````{admonition} Définition : Actions ponctuelle conservatives
:class: tip

Il existe des actions dont le travail sur un trajet entre deux points A et B __ne dépend que des positions des points A et B__ mais pas du chemin parcouru entre les deux.

````

````{admonition} Définition : Energie potentielle
:class: tip

Puisque le travail de l'action du point A au point B ne dépend pas du chemin parcouru mais uniquement des positions A et B, il existe une fonction __de la seule position__ notée $E_p$ dont la variation $E_p(B) - E_p(A)$ permet de déterminer le travail de l'action de A à B. On appelle cette fonction __énergie potentielle__ et elle est définit de telle sorte que le travail de l'action du point A au point B vaut:

\begin{equation}
W_{A \to B} = - \left(E_p(B) - E_p(A)\right) = - \Delta E_{p,A \to B}
\end{equation}
Remarque: On dit que la force dérive d'une énergie potentielle.

````

````{admonition} Fondamental : Energie potentielle et constante
:class: attention

L'énergie potentielle de pesanteur est __définie à une constante près__. Le point où l'énergie potentielle est nulle peut-être choisi arbitrairement, ce qui signifie qu'une valeur d'énergie potentielle __n'a pas de sens__. Ce n'est qu'une __variation__ d'énergie potentielle qui possède un sens.
````

````{dropdown} Remarque

__Dépendance de l'énergie potentielle__
L'énergie potentielle d'une action ponctuelle conservative (on parle de __force conservative__) dépend de la force en question et uniquement de la position où l'on calcule l'énergie potentielle. C'est donc une fonction de la position seulement (pas de la vitesse).

````

````{admonition} Attention : Signe -
:class: note

Il faut bien faire attention à la présence du signe - entre le travail et la variation d'énergie potentielle. Une telle définition permettra de "passer" l'énergie potentielle du "côté" de l'énergie cinétique pour faire apparaître l'énergie mécanique. Nous pourrons alors fournir une interprétation plus complète de l'intérêt des forces conservatives.

````

````{admonition} Fondamental : Variation infinitésimale de l'énergie potentielle.
:class: attention

L'énergie potentielle est alors une grandeur d'état puisqu'elle s'exprime en fonction du seul état du système à l'instant considéré. Lors d'une transformation, on va donc calculer une __variation__ de l'énergie potentielle. Si la variation est finie, on la notera $\Delta E_p$, si elle est infinitésimale, on la notera $dE_p$. Ces notations sont à mettre en rapport avec celle pour l'énergie cinétique: ce sera une généralité pour les grandeurs dites "d'état", c'est-à-dire qui ne dépendent que de l'état du système à un instant donné et pas de la façon avec laquelle il est arrivé dans cet état.
````

## Energie potentielle et force


__Variation infinitésimale de l'énergie potentielle.__
Dans le cadre d'un déplacement infinitésimale $\overrightarrow{dOM}$, la variation d'énergie potentielle d'une action ponctuelle s'écrit:

\begin{align*}
dE_p &= - \delta W(\overrightarrow{F}) \\
&= - \overrightarrow{F} \cdot \overrightarrow{dOM}\\
&= - P_{/\mathfrak{R}}(\overrightarrow{F}) dt
\end{align*}
````{admonition} Fondamental : Relation force et énergie potentielle
:class: attention

L'expression précédennte démontre immédiatement la relation suivante:

\begin{align*}
dE_p = - \overrightarrow{F} \cdot \overrightarrow{dOM}\\
\overrightarrow{F} = - \overrightarrow{grad} E_p
\end{align*}
La dernière expression permet de déduire de l'énergie potentielle l'expression de la force dans tous les types de repères.
````

## Forces conservatives usuelles

### Méthode de détermination d'une énergie potentielle


__Méthodes__
Il existe deux méthodes de détermination de l'expression d'une énergie potentielle:

* si on ne sait pas si l'action dérive d'une énergie potentielle (ou qu'on doit le prouver), alors il faut calculer le travail infinitésimale et le mettre sous la forme d'une différentielle $\delta W = - d(f(M))$. On idenitifie alors f(M) à l'énergie potentielle (à une constante près).
Remarque: on peut aussi calculer la puissance transmise et l'écrire sous la forme: $P = \frac{\rm{d}}{\rm{dt}}(f(M))$. De la même manière f(M) s'identifie à l'énergie potentielle.

Attention, la fonction f ne doit dépendre __que de la position de M (coordonnées), pas des dérivées de la position__.

* si on sait que l'action dérive d'une énergie potentielle, on peut utiliser l'expression du gradient et intégrer (dans le cadre du programme, uniquement si la force ne dépend que d'une seule coordonnée).

On utilisera ici la première méthode puisque le but est de __prouver__ que les forces ci-après dérivent d'une énergie potentielle.


### Energie potentielle de pesanteur

````{admonition} Fondamental : Cas d'un point matériel
:class: attention

L'action du poids sur un point matériel M dérive d'une énergie potentielle dont l'expression est:

\begin{equation}
E_{p,pes} = mg h + K
\end{equation}
où h est l'altitude et K une constante - on rappelle que l'énergie potentielle est définie à une constant près.
````


__Démonstration__
On utilise un système de coordonnées cartésiennes où z est la coordonnée verticale vers le haut (donc h)

\begin{align*}
\delta W &= -mg \overrightarrow{e_z} \wedge \left(dx \overrightarrow{e_x} + dy \overrightarrow{e_y} + dz \overrightarrow{e_z}\right)\\
&= -mg dz\\
&= -d \left(mgz\right)
\end{align*}
````{attention}

Dans l'expression précédente, l'axe Oz est orienté __vers le haut__. Si l'axe est orienté vers le bas, il apparaît un signe -dans l'expression de l'énergie potentielle.

````

````{admonition} Fondamental : Cas d'une action sur un solide
:class: attention

L'énergie potentielle de l'action de la pesanteur uniforme sur un solide peut s'écrire $E_p = M g h_G + K$ où M est la masse totale du solide et $h_G$ l'altitude du centre d'inertie.

La démonstration se fait sommation des énergies potentielles de chaque point du solide.
````

### Force de Lorentz


__Partie magnétique__
Sur un point matériel, la partie magnétique de la force de Lorentez __ne travaille pas__, c'est-à-dire que le travail de cette force est nul (et la puissance aussi).



__Démonstration__
La force magnétique est par définition perpendiculaire à la vitesse, donc la puissance transmise est nulle.


````{admonition} Fondamental : Partie électrique
:class: attention

L'action sur un point matériel du champ électrique indépendant du temps $\overrightarrow{E}$ dérive d'une énergie potentielle appelée énergie potentielle électrostatique. Elle s'écrit sous la forme $E_p(M) = qV(M)$ où q est la charge du point matériel et V(M) est le potentiel électrique dépendant du seul champ électrique (et pas du point matériel sur lequel il agit). On a la relation $\overrightarrow{E} = - \overrightarrow{grad} V$.

Remarque: Le potentiel électrique est celui introduit en électrocinétique. Cette expression ne sera utilisée qu'en fin d'année.
````

### Forces newtoniennes

````{admonition} Fondamental : Potentiel newtonien
:class: attention

Soit un point O de masse $m_O$ et/ou de charge$q_O$ agissant sur un point M de masse $m$ et/ou de charge $q$. Les forces gravitationnelles et coulombiennes dont les expressions sont de la forme $\overrightarrow{F} = - \frac{K}{r^2} \overrightarrow{e_r}$dans un système de coordonnées de sphérique centrée au point O dérivent d'une énergie potentielle appelées respectivement énergie potentielle de gravitation et énergie potentielle électrostatique et dont l'expression est: $E_p = -\frac{K}{r} + Cste$.
````

````{dropdown} Remarque

On s'entraînera à expliciter K suivant que la force soit gravitationnelle ou coulombienne.

````


__Démonstration__
Comme dit dans la propriété, on va se placer en coordonnées sphériques centrées au point O.

\begin{align*}
\delta W &= - \frac{K}{r^2}\overrightarrow{e_r} \wedge \left(dr \overrightarrow{e_r} + r d\theta \overrightarrow{e_\theta} + r \sin\theta d\varphi \overrightarrow{e_\varphi}\right)\\
&= -\frac{K}{r^2} dr\\
&= -d \left(- \frac{K}{r}\right)
\end{align*}

__Interprétation__
On remarquera que suivant le signe de K, l'énergie potentielle est croissante ou décroissante. Or la relation force-énergie potentielle, permet de déduire de la monotonie de l'énergie potentielle son sens (ici suivant $\overrightarrow{e_r}$, soit son caractère attractif ou répulsif).

Ainsi, si $K < 0$, l'énergie potentielle est décroissante en r, donc la force est dirigée vers les r croissants: la force est répulsive.

Ainsi, si $K > 0$, l'énergie potentielle est croissant en r, donc la force est dirigée vers les r décroissants: la force est attractive.


### Actions de rappel

````{admonition} Fondamental : Action de rappel d'un ressort
:class: attention

L'action de rappel d'un ressort dérive d'une énergie potentielle dont l'expression est:

\begin{equation}
E_p = \frac{1}{2} k \Delta l ^2 = \frac{1}{2} k \left(l - l_0\right)^2
\end{equation}
````


__Démonstration__
On travaille dans un système de coordonées cartésiennes d'axe Ox le long du ressort et le point O est à l'autre extrémité du ressort tel que$l = x$. On trouve alors que $\overrightarrow{u_{ext}} = \overrightarrow{e_x}$ et donc:

\begin{align*}
\delta W &= -k\left(x - l_0\right) \overrightarrow{e_x} \wedge \left(dx \overrightarrow{e_x} + dy \overrightarrow{e_y} + dz \overrightarrow{e_z}\right)\\
&= -k \left(x - l_0\right) dx\\
&= -d \left(\frac{1}{2} k {\left(x - l_0\right)}^2\right)
\end{align*}
On retrouve l'expression en remplaçant x par l.


````{admonition} Fondamental : Energie potentielle de torsion
:class: attention

L'action de rappel d'un couple de torsion dérive d'une énergie potentielle dont l'expression est:

\begin{equation}
E_p = \frac{1}{2} C \Delta \theta ^2 = \frac{1}{2} C \left(\theta - \theta_0\right)^2
\end{equation}
````


__Démonstration__
On ne peut ici justifier cette propriété par les actions ponctuelles. On va donc calculer directement le travail infinitésimal pour l'action globale. On est ici dans le cadre d'un solide en rotation, donc le travail infintésimal s'écrit $M_{axe/torsion}d\theta$ où $M_{axe/torsion}$ est le moment résultant de l'action sur l'axe de rotation et $\theta$ une coordonnées angulaire repérant la rotation du solide dans le plan perpendiculaire à l'axe de torsion. On rappelle que le moment résultant s'écrit $- C(\theta - \theta_0)$:

\begin{align*}
\delta W &= -C\left(\theta - \theta_0\right) d \theta \\
&= -d \left(\frac{1}{2} C {\left(\theta - \theta_0\right)}^2\right)
\end{align*}
````{dropdown} Remarque

__Interprétation__
On remarque que l'énergie potentielle est minimale pour un allongement nul ou pour une torsion nulle: cela correspond bien à la configuration ou le ressort/fil de torsion n'exerce pas d'action sur le système accroché.

L'énergie potentielle augment quand l'allongement du ressort augmente: la force est donc dirigée vers l'intérieur du ressort, elle tend à comprimer le ressort. A l'inverse, quand l'allongement du ressort diminue, l'énergie potentielle augmente aussi, donc la force est dirigée vers l'extérieur du ressort, elle tend à étendre le ressort. On retrouve le principe de la force de rappel.

On pourra s'entraîner à observer ce phénomène graphiquement en traçant l'énergie potentielle de rappel élastique.

````


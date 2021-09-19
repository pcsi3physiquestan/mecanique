# Exemples

## Toboggan circulaire

````{admonition} Exercice 
:class: attention

On considère une masse m ponctuelle qui se déplace sans frottements sur une demie-sphère de centre O et de rayon R. Elle est soumise à un champ de pesanteur g et est lâchée du sommet avec une vitesse très faible vers la droite. La masse décolle-t-elle de la sphère? On utilisera deux méthodes différentes (utilisant respectivement le TEC puis le TEM) pour répondre à la question.

````
````{dropdown}
 

__Condition de décollement et paramétrage__

La condition de décollement est on le rappelle l'annulation de la composante normale de la réaction du toboggan sur la masse. Remarquons déjà que le TEC/TEM n'apporterons pas d'information sur cette composante. Elle est en effet perpendiculaire au moins (donc elle ne travaille pas) et dirigée vers le centre du cercle formé par le toboggan (donc de moment nul en ce centre). Il faut donc commencer par appliquer un PFD au point matériel M dans le référentiel du toboggan supposé galiléen.

On utilise un système de coordonnées cylindriques d'axe Oz perpendiculaire au plan du mouvement (le mouvement est plan puisque les deux forces sont dans un même plan et la vitesse initiale dans le même plan) où O est le centre de la sphère. La vitesse s'écrit alors $\overrightarrow{v} = R \dot \theta \overrightarrow{e_\theta}$ et l'accélération $\overrightarrow{a} = - R \dot \theta^2 \overrightarrow{e_r} + R \ddot \theta \overrightarrow{e_\theta}$.

Les deux forces qui s'appliquent sont le poids $\overrightarrow{P} = -mg \cos \theta \overrightarrow{e_r} + mg \sin \theta \overrightarrow{e_\theta}$ et la réaction du toboggan supposée normale par l'absence des frottements $\overrightarrow{R} = R \overrightarrow{e_r}$. La condition de contact s'écrit $R > 0$. L'annulation coïncidera avec le décollage.

On applique donc le PFD.

\begin{align*}
- m R \dot \theta^2 &= -mg \cos \theta + R\\
m R \ddot \theta &= mg \sin \theta
\end{align*}
L'équation suivant $\overrightarrow{e_r}$ permet de déterminer R en fonction de la vitesse angulaire. Il reste donc à déterminer cette vitesse angulaire en fonction de l'angle pour répondre à la question. On va utiliser le TEC ou le TEM pour déterminer cette relation. Remarquons qu'on aurait pu utiliser à la place la seconde équation en la multipliant par $\dot \theta$.


__Application du TEC__

Il est important de savoir quel théorème on applique (puissance ou énergie) et de préciser sur quoi on applique le théorème. Ici, on va appliquerle théorème de l'énergie cinétique entre l'instant 0 et un instant t où le mobile est à un angle $\theta$. On considèrera la vitesse initiale négligeable devant la vitesse à l'instant t.

L'énergie cinétique s'écrit: $E_c =\frac{1}{2} m R^2 \dot  \theta^2$. Sa variation vaut: $\Delta E_c = \frac{1}{2} m R^2 \dot  \theta(t)^2 - 0$

La réaction du support est __perpendiculaire à la vitesse__ donc son travail est nulle sur tout le trajet. Le poids travaille est l'expression du travail élémentaire est $\delta W = mg \sin \theta d\theta$. En intégrant entre $\theta(t=0) = 0$ et $\theta(t=t) = \theta$, il vient: $W = mgR (1 - \cos \theta)$.

On peut donc appliquer le théorème de l'énergie mécanique:

\begin{align*}
\frac{1}{2} m R^2 \dot \theta^2 &= mgR \left(1 - \cos \theta\right)\\
m R \dot \theta^2 &= 2 mg \left(1 - \cos \theta\right)
\end{align*}
Il vient en remplçant dans la première équation: $ R = 3 mg \cos \theta - 2mg$. La condition de décollement s'obtient pour $\theta = \arccos 2/3$.


__Application du théorème de l'énergie mécanique__

On applique à nouveau le théorème de l'énergie mécanique entre t=0 et t=t. Remarquons que la réaction du toboggan ne travaille pas et que le poids dérive d'une énergie potentielle donc il n'y a pas de force non-conservative: l'énergie mécanique est une constante. La variation d'énergie potentielle de pesanteur s'écrit $\Delta E_p = mg x(t) - mg x(0) = mg (\cos\theta - 1)$. Il vient:

\begin{align*}
\Delta E_c + \Delta E_p &= 0\\
\left(\frac{1}{2} m R^2 \dot \theta^2 - 0\right) + mgR \left(\cos \theta - 1\right)&= 0\\
m R \dot \theta^2 &= 2 mg \left(1 - \cos \theta\right)
\end{align*}
La suite de la résolution est identique au cas précédent. On remarquera l'équivalence logique de l'écriture du TEC et du TEM.

````


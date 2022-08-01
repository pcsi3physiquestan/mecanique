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

# Applications

## Forces centrales
````{admonition} Effet centrifuge
:class: important
1. Montrer que dans un mouvement à force centrale conservative.

\begin{equation}
m \frac{\rm{d^2}r}{\rm{dt^2}} = - \frac{\rm{d}E_{p,eff}}{\rm{dr}}
\end{equation}

Grâce à cette relation et en analysant les différents termes de $E_{p,eff}$, retrouver l'effet centrifuge de la rotation et les effets possibles (centrifuge/centripète) de la force centrale.
````

````{admonition} Mouvement circulaire uniforme
:class: important

Justifier que le mouvement circulaire correspondant à $E_m = E_{p,eff,min}$ est un mouvement uniforme.
````

## Forces newtoniennes

````{admonition} Mouvement circulaire
:class: attention
On considère le mouvement d'une planète autour du Soleil et on suppose sa trajectoire circulaire de rayon R.
1. Etablir sa vitesse en fonction de R. En déduire la troisième loi de Kepler
2. Déterminer l'expression de l'énergie mécanique, cinétique et potentielle et montrer que $E_m = - E_c = \frac{E_p}{2}$.
````

````{admonition} Satellite Hipparcos 
:class: attention

Le satellite Hipparcos lancé le 8 août 1987 était constitué principalement d'un télescope de 30cm de diamètre. Celui-ci a permis d'établir un catalogue des positions, distances et éclats de plus de 118000 étoiles avec une précision jamais atteinte. Ce satellite devait être placé sur une orbite géostationnaire à une altitude H=36000km. Un problème de mise à feu du moteur d'apogée a laissé Hipparcos sur son orbite de transfert son altitude variant entre h et H. Après utilisation des moteurs de positionnement, l'altitude minimale a été porté à h=500km. 

Une programmation du satellite a permis de s'affranchir des problèmes liés à cette orbite. Au cours d'une révolution, il passe dans la ceinture de Van Allen. On supposera que cette ceinture comprise entre 2 sphères de rayon $r_1 = 8400 \rm{km}$ et $r_2 = 28000 \rm{km}$ et de centre celui de la Terre. La ceinture de Van Allen est constituée de particule piégées dans le champ magnétique terrestre. Ces particules aveuglent les détecteurs d'Hipparcos interrompant les mesures des positions des étoiles. Il est cependant utilisable à $65\%$. On assimile la terre à une sphère de centre O, de rayon R=6400km et de masse M et le satellite à un point matériel (S,m). On suppose le référentiel géocentrique R galiléen. La période de rotation de la terre dans ce référentiel appelée jour sidéral vaut T=86164s.

1. Quelle la nature de la trajectoire d'Hipparcos?
1. Déterminer les expressions de l'excentricité e et du paramètre de l'ellipse p en fonction de h,H et R. A.N.
1. Exprimer et calculer le demi-grand axe a de la trajectoire.
1. Rappeler la troisième loi de Kepler.
1. Déduire de la question précédente, la relation entre la période de rotation de la Terre T et l'altitude de l'orbite géostationnaire H.
1. Exprimer la période $T_h$ de révolution d'Hipparcos en fonction de T,R,H et h. Calculer $T_h$ en heure.
1. Déterminer les valeurs numériques de angles $\theta_1$ et $\theta_2$ d'entrée et de sortie de la ceinture de Van Allen du satellite. On donnera les valeurs comprises entre $0 ^{\circ}$ et $180 ^{\circ}$.
1. Représenter sur un schéma clair la trajectoire du satellite et l'aire balayée par $\overrightarrow{OS}$ lors d'un passage dans la ceinture de Van Allen. Pour la question suivante, on prendre une valeur approché de $S_b = 200 \times 10^{6} \rm{km}$.
1. Déterminer le rapport $\rho = t_0/T_h$ en fonction de $S_b$ et $S_e$ (surface de l'ellipse) où $t_0$ est la durée totale d'inactivité d'Hipparcos sur une période.

````

````{admonition} Satellite artificiel 
:class: attention

On étudie le lancement d'un satellite artificiel à partir d'un point O de la surface terrestre.

1. Établir l'expression de la vitesse du point O dans le référentiel géocentrique $R_T$ assimilé à un référentiel galiléen en fonction de la vitesse de rotation de la Terre autour de l'axe de ses pôles $\omega$, du rayon terrestre $R_T$ et de la latitude du lieu $\lambda$.
1. En déduire les conditions les plus favorables pour le lancement d'un satellite. Parmi les champs de tirs suivants, lequel choisir de préférence?
    * Baïkonour au Kazakhstan: $\lambda = 46 ^{\circ}$
    * Cap Canaveral aux USA: $\lambda = 28,5 ^{\circ}$
    * Kourou en Guyane française: $\lambda = 5,23 ^{\circ}$

3. Etablir l'expression de l'énergie potentielle de gravitation du système Terre-satellite en fonction de l'altitude z du satellite par rapport au sol. On prend pour référence une énergie potentielle nulle à l'infini. En déduire l'expression de l'énergie mécanique du satellite sur sa base de lancement dans le référentiel géocentrique.
3. On appelle ici vitesse de libération $v_l$, la vitesse verticale minimale qu'il faut communiquer initialement au satellite par rapport au sol, pour qu'il puisse se libérer de l'attraction terrestre. Donner l'expression de $v_l$. Calculer sa valeur numérique dans le cas où le satellite est lancé de la base de Kourou. On supposera que la vitesse du point O attaché au sol est horizontale et la vitesse communiquée au satellite verticale.

On considère un satellite artificiel m en mouvement circulaire autour de la Terre.
1. Montrer que le mouvement du satellite est uniforme. Etablir l'expression de la vitesse du satellite en fonction de son altitude ainsi que la troisième loi de Kepler liant la période de rotation T du satellite au rayon r de sa trajectoire.
2. Calculer le rayon de l'orbite d'un satellite géostationnaire et définir son plan de révolution.
3. Quelle énergie cinétique minimale faut-il communiquer au satellite pour qu'il échappe à l'attraction terrestre s'il est initialement en orbite circulaire autour de la Terre à l'altitude z?  A.N. z = 36000 km; m=6 tonnes.
4. Soit un satellite d'énergie initiale $E_{m0}$. Son orbite est relativement basse et il subit donc les frottements des couches hautes de l'atmosphère. Il s'ensuit que l'énergie mécanique du satellite varie suivant la loi $E_m = E_{m0} (1+ bt)$, b étant un coefficient constant positif. On suppose que la trajectoire reste approximativement circulaire. Préciser le signe de $E_{m0}$. Etablir l'expression du rayon r et de la vitesse v du satellite en fonction du temps. Comparer les évolutions de r et de v ainsi que celles des énergies potentielle et cinétique. Que devient l'énergie perdue?
````

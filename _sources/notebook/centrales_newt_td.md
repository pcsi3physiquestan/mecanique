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
# Travaux dirigés: Potentiels newtoniens

## Etude du mouvement d'une planète par la méthode du vecteur excentricité

````{admonition} Exercice 
:class: attention

On veut étudier le mouvement d'une planète P, assimilée à un point matériel dans le champ de gravitation d'une étoile de masse $M_e$, de centre O considérée comme ponctuelle et fixe. La planète de masse $M_P$ est située à une distance $r=OP$ de O. On considère le référentiel lié à l'étoile comme galiléen.

1. Exprimer la force exercée par l'étoile sur la planète en fonction de $M_p, M_e, r, G$ la constante de gravitation universelle et $\overrightarrow{u_r} = \frac{\overrightarrow{OP}}{r}$.
1. Justifier que le mouvement est plan. Préciser ce plan.

On rappelle que l'équation polaire d'une ellipse est $r(\theta) = \frac{p}{1+ e \cos \theta}$. On définit le vecteur excentricité: $\overrightarrow{e} = - \frac{L}{GM_e M_P} \overrightarrow{v} + \overrightarrow{u_{\theta}}$ où $\overrightarrow{v}$ est la vitesse de la planète.

3. Montrer que le vecteur excentricité est un vecteur constant. En fait, ce vecteur est orthogonal au grand axe de l'ellipse.
3. En calculant le produit scalaire $\overrightarrow{e} \cdot \overrightarrow{u_{\theta}}$, montrer que l'on retrouve bien l'équation d'une ellipse.
3. Que vaut le module de $\overrightarrow{e}$? Préciser p en fonction de G, $M_p$, $M_e$ et L.
3. Préciser la valeur de l'excentricité dans le cas d'un mouvement circulaire.
3. Dans le cas d'un mouvement circulaire, préciser la valeur de L en fonction de R (rayon du cercle), $v_c$ (vitesse circulaire) et $M_p$. Déterminer l'expression de la vitesse $V_c$ en fonction de R, G et $M_e$ à l'aide du vecteur excentricité.

````

## Explosion d'une comète

````{admonition} Exercice 
:class: attention

Une comète de période T=770 ans s'est approchée du soleil à $d = 7,75 \times 10^{-3} \rm{u.a.}$

1. On suppose que la trajectoire est elliptique. Déterminer le demi-grand axe a, l'excentricité e, le paramètre p de l'ellipse et les vitesses à l'aphélie ($v_A$) et au périhélie ($v_P$). A-t-on eu raison de faire l'hypothèse d'une trajectoire elliptique?
1. A son périhélie, elle a explosé en deux morceaux de masse $m_1$ et $m_2$, partis respectivement avec la vitesse $v_1$ et $v_2$ dans deux directions faisant des angles respectifs $\alpha_1 = -20 ^{\circ}$ et $\alpha_2 = 50 ^{\circ}$ avec la direction initiale de $v_P$. La quantité de mouvement totale se conserve durant l'explosion et l'on observe que: $\left \| v_1\right \| \sim \left \| v_2 \right \|$.
    1. En utilisant la conservation de la quantité de mouvement, déterminer le rapport des masses $m_1/m_2$ puis la norme des vitesses des fragments.
    1. Calculer l'énergie mécanique par unité de masse pour chaque fragment. En déduire le type de la nouvelle trajectoire.

````

## Mise en orbite d'une sonde spatiale

````{admonition} Exercice 
:class: attention

On souhaite mettre en orbite une sonde spatiale(s) autour de Mars. Ce véhicule possède au point A la vitesse $v_A$ et présente un "paramètre d’impact" b (cf. Figure). On donne:

* $v_A = 2,5 \rm{km/s}$
* rayon de Mars: $r_M = 3397 \rm{km}$
* masse de Mars: $M_M = 6,39 \times 10^{23} \rm{kg}$

```{figure} ./images/Mecanique_TD7_EX1_1.jpg
:name: fig_262
:align: center

```

Remarque: Le point B n'est pas placé correctement sur le schéma. Cela n'a pas d'influence sur les raisonnements.

1. Au point A, on suppose que le véhicule est assez éloigné de Mars pour pouvoir négliger l'énergie gravitationnelle. En déduire l'expression de l'énergie mécanique et la nature de la trajectoire de(s). Le justifier sur un graphique.
1. Montrer que le moment cinétique se conserve et définir la constante des aires C. Calculer C en fonction de $v_A$ et b.
1. Sachant que ma trajectoire d'approche est tangente au cercle de rayon $\alpha r_M$ en B, calculer $v_B$ (vitesse en B) en fonction de $v_A, r_M, \alpha$ et $b$.
1. Exprimer le paramètre d'impact b, en fonction de $r_M, v_A, M_M$ et $\alpha$. A.N.: $\alpha = 3$.
1. Déterminer la distance minimale $b_m$ pour que le véhicule évite la surface de Mars.
1. Déterminer la vitesse $v_c$ d'un objet sur l'orbite circulaire de rayon $3 r_m$ ainsi que sa période de révolution en fonction des données.
1. Au point B (avec $\alpha = 3$), on veut que le véhicule passe sur l'orbite circulaire de rayon $3 r_M$. Déterminer la variation de vitesse $\Delta v_c$ à communiquer au véhicule en fonction des données.

````

## Comète à trajectoire parabolique

````{admonition} Exercice 
:class: attention

La comète Arend-Roland est une comète à trajectoire d'excentricité e estimée à 1,0002. On assimilera la trajectoire à une parabole d'excentricité e=1. La comète est passée à son périhélie, le 8 avril 1857, à $r_P = 0,316 \rm{u.a.}$ du soleil.

1. Calculer le paramètre de la trajectoire.
1. Exprimer le paramètre p de la conique en fonction de la constante des aires C, de G et la masse du soleil $M_S$. En déduire la vitesse de la comète au périhélie.
1. Montrer que l'on peut exprimer la vitesse angulaire $\dot \theta$ en fonction de la constante des aires C et du paramètres p de la parabole par: $\dot \theta = C\frac{{(1+ \cos \theta)}^2}{p^2}$. En quel point est prise l'origine $\theta=0$?
1. On note $t_0$ l'instant de passage au périhélie P. Montrer alors que l'on obtient le temps de passage pour le point d'angle $\alpha$ avec:

$$t(\alpha) = t_0 + \int_0^{\alpha} \frac{p^2}{C} \frac{d \theta}{{(1+ cos \theta)}^2}$$

5. Pour calculer cette intégrale, on effectue le changement de variable $x = \tan \frac{\theta}{2}$. En déduire l'expression: $t = t_0 + \frac{p^2}{C} (X + \frac{X^3}{3})$ où $X = \tan \frac{\alpha}{2}$.
1. (Analyse numérique) La comète a été découverte par les astronomes belges Sylvain Arend et Georges Roland le 8 novembre 1856. A quelle distance se trouvait-elle du Soleil?

````

## Satellite Hipparcos

````{admonition} Exercice 
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

## Satellite artificiel

````{admonition} Exercice 
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

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
# Forces newtoniennes

## Echelle microscopique


__Position du problème.__
Le but de cet exercice est d'estimer à l'échelle microscopique l'intensité des interactions coulombiennes et gravitationnelles de manière à les comparer.

On va considère un atome d'hydrogène et estimer l'intensité des deux interactions dans le cas proton-électron. On note r la distance proton-électron


__Ordres de grandeur__

On note $F_g$ l'intensité de la force gravitationnelle et $F_e$ l'intensité de la force électrostatique.

\begin{align*}
F_g &\sim \frac{G m_P m_e}{r^2} \sim \frac{10^{-10}\times 10^{-27} \times 10^{-30}}{r^2} \sim \frac{10^{-67}}{r^2}\\
F_e &\sim \frac{e^2}{4 \pi \epsilon_0} \frac{1}{r^2} \sim \frac{10^{-38}}{10 \times 10^{-11} r^2} \sim \frac{10^{-28}}{r^2}
\end{align*}
Il vient un rapport $\frac{F_g}{ F_e} = 10^{-39} \Longrightarrow F_g \ll F_e$.


````{important} __Fondamental : Conclusion__

D'un point de vue "analytique", cela signifie que pour une étude des phénomènes microscopiques, on aura tendance à négliger l'action de la gravitation.

D'un point de vue physique, on peut remarquer que contrairement à l'interaction gravitationnelle, l'interaction électrostatique peut être répulsive ou attractive. Elle va donc favoriser l'association de charges de signes différents créant ainsi de la matière globalement neutre: les atomes et molécules. L'interaction électrostatique assure la cohésion de la matière à l'échelle microscopique.
````

## Cohésion de la matière à l'échelle macroscopique


__Du microscopique au macroscopique__
L'approche microscopique de la matière que nous venons de faire implique une question: comment, alors qu'elle est négligeable à l'échelle microscopique, l'interaction gravitationnelle peut-elle avoir une influence aussi importante à l'échelle macroscopique au point de gouverner le mouvement des planètes?

Pour répondre à cette question, nous allons considérer deux approche: l'une purement qualitative va permettre de comprendre quelles interactions doivent être prises en compte à l'échelle macroscopique, l'autre semi-qualitative essaiera de déterminer sur quelle échelle l'interaction gravitationnelle devient prépondérante pour assurer la cohésion de la matière.

Nous venons donc de voir que les interactions coulombiennes et newtoniennes ont tendance à attirer des éléments de matière neutre les uns vers les autres formant ainsi des agrégats de matière et assurant ainsi sa cohésion. D'un point de vue qualitative, cela signifie que la matière tend à se neutraliser, ce qui va diminuer l'intensité des actions électrostatiques à grande distance. A l'inverse, un agrégat de matière tend à augmenter les masses et donc augmenter l'interaction gravitationnelle. Donc l'une augmente et l'autre diminue avec la taille des systèmes. Reste à déterminer à partir de quelle taille la cohésion commence à être assurée de manière prépondérante par l'interaction gravitationnelle.



__Position du problème__
Essayons de voir quelles forces entrent en ligne de compte pour assurer cette cohésion. Nous allons ici effectuer une analyse purement basée sur des ordres de grandeurs et pas sur des calculs précis. Soit un corps $\Sigma$ dont la longueur caractéristique est L. Son volume et sa section sont alors de l'ordre de $V \sim L^3$ et $S \sim L^2$.

En notant $a = 10^{-10} \rm{m}$ la taille caractéristique d'un atome du ce corps (plus exactement on considère que la taille caractéristique du volume occupé par un atome), il vient que le nombre d'atome qui compose ce corps est $N \sim {(L/a)}^3$. Un atome possède en moyenne une cinquantaine d'électron de sorte que la masse d'une atome, principalement ramenée à la masse du noyau est de l'ordre de $m_a = 1000 \times 50 \times m_e \sim 10^{-25} \rm{kg}$. La masse M du corps est donc $M \sim N m_a \sim 10^5 L^3 \rm{kg}$.

Divisons le corps en deux parties à peu près de même taille. Leur taille caractéristique est donc $L/2 \sim L$ et leur masse caractéristique est $M/2 \sim M$. Comme nous l'avons dit précédemment la cohésion du corps correspond à la force d'interaction entre les deux parties du corps. Ces interactions correspondent à l'interaction gravitationnelle et à l'interaction électrostatique.



__Interaction gravitationnelle__
Pour l'interaction gravitationnelle, on peut considérer globalement les deux sous-corps. Le point d'influence est associé au centre des graves. Pour une répartition de matière pas trop déséquilibrée, on peut considérer que la distance entre les deux centres des graves est de l'ordre de L. Il vient:

$F_g \sim \frac{GM^2}{L^2} \sim \frac{10^{-10}\times10^{10}\times L^6}{L^2} \sim L^4$



__Interaction électrostatique__
Pour l'interaction électrostatique, la matière étant neutre, on peut considérer que les interactions à distance entre les deux sous-corps sont nulles. Les seules interactions ont lieu entre les atomes proches et sont du type Van der Waals. Cette interaction a donc pour ordre de grandeur: $f_e \sim \frac{p^2}{3 \epsilon_0 a^4}$ où $p$ est le moment dipolaire de la molécule, on a: $4p \sim 10^{-29} \rm{C.m}$. Ces interactions ont lieu entre des atomes proches: ils ne peuvent donc avoir lieu qu'à la surface de contact entre les deux. L'interaction aura donc lieu entre atomes. Il vient que l'interaction électrostatique a pour expression:

$F_e \sim \frac{L^2}{a^2} \frac{4 p^2}{3 \epsilon_0 a^4} \sim \frac{10^{-58}}{10^{-10}\times 10^{-60}}L^2 \sim 10^{12} L^2$



__Comparaison__
Le rapport des deux interactions est donc: $\frac{F_e}{F_g} \sim \frac{10^{12}}{L^2}$.

On voit que pour des distances bien inférieures à 1000km la cohésion de la matière est assurée par les forces de cohésion électrostatiques. Ainsi la cohésion du corps humain ainsi que de la plupart des objets que nous utilisons est assurée par les interactions électrostatiques entre électrons proches.

Au contraire, pour des distances supérieures à 1000km, la force de gravitation prend le dessus et assure la cohésion de la matière: c'est elle qui responsable de la cohésion des planètes ou assure la stabilité des étoiles (c'est d'ailleurs un jeu entre la force de gravitation et la pression du gaz composant les étoiles qui détermine la stabilité de l'étoile (pas d'effondrement ni d'expulsion de matière vers l'extérieur)).



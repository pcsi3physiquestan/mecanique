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

## Forces centrales

````{admonition} Forces centrales particulières 
:class: attention

On considère une force centrale dont l'énergie potentielle s'écrit comme $E_p = - \frac{K}{r^n}$ avec K réel et n réel.

1. Préciser suivant que K soit positif ou négatif le caractère attractif ou répulsif de la force associée.
1. Représenter l'énergie potentielle effective suivant le signe de K et suivant les valeurs de n ($n \in \mathbb{Z}$) et préciser s'il est possible:
1. d'atteindre l'infini
1. d'atteindre le centre de force
1. d'observer une trajectoire circulaire (on ne demande pas une expression du rayon)

1. Préciser quelles valeurs de K et n correspondent à des cas physiques usuels.

````

_On ne justifiera pas ici les tracés. Il est __vivement conseillé__ d'essayer de les tracer seul (croissances comparées)._
````{topic} Eléments de réponse

```{figure} ./images/meca_force_centrale_Krn.png
:name: fig_258
:align: center
```

Les réponses ne sont pas justifiés.

* Si K est positif et n négatif ou K est négatif et n est positif, la force est répulsive. Sinon la force est répulsive. (S'intéresser à la monotonie de l'énergie potentielle __seule__).

On distingue différents cas:
* Atteindre l'infini: ce n'est possible que s'il n'y a pas de barrière de potentiel infini en $r=+\infty$. C'est toujours réalisé pour n positif ou pour n négatif et K négatif.
    * On distinguera le cas répulsif où quelque soit l'énergie mécanique, le système sera dans un état de diffusion des cas attractif où suivant la valeur de l'énergie mécanique, le système sera dans un état lié ou de diffusion.
    * Si K est positif et n négatif, alors l'énergie potentielle tendant vers l'infini aux grands rayons, le mobile est nécessairement dans un état lié.
* Atteindre le centre de force: ce n'est possible que s'il n'y a pas de barrière de potentiel infini en $r=0$. Le seul cas permettant de compenser l'effet centrifuge du terme d'énergie cinétique orthoradiale est le cas où K et positif et $n > 2$. Le tracé montre qu'il faut alors une énergie mécanique suffisante car il existe une barrière d'énergie potentielle.
    * Le cas $n = 2$ est un cas limite permettant les deux possibilités suivantes les valeurs de K et$L_O$.
* L'existence d'une trajectoire circulaire nécessite un extremum d'énergie potentielle. Ce n'est possible que pour une force attractive. Si n est supérieur à 2, cet état a peu de chance d'être observé car un léger écart va l'éloigner de la trajectoire circulaire.
* Cas usuels : 
    * Cas newtonien (coulombien ou gravitationnelle): $n=1$ (force en $1/r^2$)
    * Cas de Van der Waals: $n=6$ (force en $1/r^7$) en tenant compte des aspects statistiques.

````

````{admonition} Cas d'une force de rappel élastique 
:class: attention

On s'intéresse au cas d'un point matériel M relié à un ressort de raideur k et de longueur à vide nulle. Il est libre de se mouvoir dans toutes les directions de l'espace. On néglige l'action de la pesanteur. On pose un repère cylindrique de sorte que les conditions initiales soient:

\begin{align*}
\overrightarrow{OM}(t=0) = r_0 \overrightarrow{e_r}\\
\overrightarrow{v_M}(t=0) = v_1 \overrightarrow{e_r} + v_0 \overrightarrow{e_{\theta}}
\end{align*}
1. Justifier la conservation du moment cinétique et de l'énergie mécanique.
1. Déterminer l'expression de ces deux grandeurs en fonction des conditions initiales.
1. Montrer que l'énergie mécanique se ramène à la dépendance du rayon r seul en introduisant une énergie potentielle effective. Discuter de la nature du mouvement. Que se passe-t-il si  $v_0=0$?
1. Déterminer les rayons extrêmaux ainsi que la vitesse maximale du mobile.
1. Déterminer la relation entre $v_0$ et $r_0$ pour observer un mouvement circulaire. Commenter le caractère uniforme/accéléré/décéléré d'un tel mouvement.

````

```{margin}
En pratique, on traite le cas de l'oscillateur spatial étudié ici différemment en utilisant un système de coordonnées cartésien. Cela permet de montrer que la trajectoire est elliptique.
```
````{topic} Elément de réponss
On ne donne pas ici les réponses complètes:

1. Appliquer le théorème du moment cinétique puis le théorème de l'énergie cinétique.
1. $L_O = mr_0 v_0$ et $E_m = \frac{1}{2}m (v_1^2 +v_0^2)+ \frac{1}{2}k r_0^2$
1. On montrera que le système est toujours dans un état lié. Si la vitesse orthoradiale est nulle initialement, elle le restera et le moment cinétique est nul. Le mouvement est alors rectiligne et symétrique en O le centre de force (pas de barrière de potentiel en r=0).
1. L'équation $E_m =E_{p,eff}$ aboutit à la résolution d'un trinôme du second degré.
1. La conservation du moment cinétique implique que le mouvement est uniforme. $v_0 = \sqrt{\frac{k}{m}}r_0$


````

## Potentiels newtoniens

````{margin}
Cette relation ne __peut PAS être utilisée directement.__
````
```{admonition} Relation énergie - excentricité
:class: attention
Montrer que : 

$$
E_m = \frac{1}{2} \frac{K^2}{mC^2} (e^2 - 1)
$$
et retrouver la relation entre le signe de $E_m$ et le type de trajectoire.
```

````{topic} Correction
>On utilise l'expression trouvée précédemment:
>
>$E_m = \frac{1}{2} mC^2 ({(\frac{du}{d \theta})}^2 + u^2 - \frac{2K}{mC^2} u)$
>
>or $u(\theta) = \frac{1 + e \cos \theta}{p}$ soit $\frac{du}{d \theta} = \frac{-e \sin \theta}{p}$. Donc:
>
>\begin{align*}
E_m &= \frac{1}{2} mC^2 ({(\frac{e \sin \theta}{p})}^2 + {(\frac{1 + e \cos \theta}{p})}^2 - \frac{2K}{mC^2} \frac{1 + e \cos \theta}{p})\\
&= \frac{1}{2} mC^2 (\frac{e^2}{p^2} \sin^2 \theta + \frac{e^2}{p^2} \cos^2 \theta + \frac{1}{p^2} + \frac{2e}{p^2} \cos \theta - \frac{2 + 2e \cos \theta}{p^2})\\
&= \frac{1}{2} \frac{K^2}{mC^2} (e^2 - 1)
\end{align*}
>D'où le lien entre énergie mécanique et type de trajectoire en utilisant les valeurs particulières de l'excentricité.
````

````{admonition} Relation Em et a
:class: attention
Démontrer la relation entre l'énergie mécanique et le demi-grand axe dans le cas d'une trajectoire elliptique. Pour cela:
1. Exprimer une relation entre vitesse et rayon au périhélie et à l'aphélie.
2. Exprimer l'énergie mécanique au périhélie et à l'aphélie
3. En déduire la relation demandée
````
````{topic} Correction
>1. A l'aphélie et au périhélie, la vitesse est purement orthoradial de sorte que le moment cinétique s'écrit (indice A pour l'aphélie et P pour le périhélie): $L_A = m v_A r_A$ et $L_P = m v_P r_P$. Le TMC conduit à la conservation du moment cinétique soit:
>\begin{equation}
r_A v_A = r_P v_P
\end{equation}
>2. Il vient:
>\begin{equation}
\begin{cases}
E_{m,A} &= \frac{1}{2}m v_A^2 - \frac{Gm M}{r_A}\\
E_{m,P} &= \frac{1}{2}m v_P^2 - \frac{Gm M}{r_P}
\end{cases}
\end{equation}
>3. Le TEM montre que l'énergie mécanique est conservée. En multipliant les deux équations précédentes par $r_A^2$ et $r_P^2$ et en utilisant $r_A V_A = r_P v_P$, il vient:
>
>$$
(r_A^2 - r_P^2) E_m = - G m M (r_A - r_P)
$$
d'où la relation demandée avec $a = r_P + r_A$
````


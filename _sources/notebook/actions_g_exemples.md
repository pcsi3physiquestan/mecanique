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
# Exemples d'analyse

## Cube sur plan incliné

````{admonition} Exercice 
:class: attention

On étudie un cube (de masse uniformément répartie) sur un plan incliné. On admet qu'à l'équilibre, la somme des forces résultats est nulle et la somme des moments résultants en un même point est nulle.

1. Représenter la force résultante de l'action du poids en un point judicieusement choisi.
1. Le cube est immobile. Par une analyse du bilan des actions, représenter la force résultante de l'action du plan incliné sur le cube en un point judicieusement choisi.
1. Que se passe-t-il si l'on incline trop le plan ?

````

>__Résolution__
>
>__1.Force résultante du poids.__
>Le poids estune action globale qui n'a pas de point d'application. MAIS, on a vu qu'une action globale était _mathématiquement_ équivalente à une action ponctuelle en un point de moment résultant nul. Un tel point est donc un bon endroit pour "représenter" une action globale.  
>Dans le cas du poids, on sait que le moment résultant est nul au centre d'inertie (champ de pesanteur uniforme) donc on va représenter le poids en G, le centre du cube.
>_Note : On pourrait remarquer que le moment résultant du poids est aussi nul en tout point à la verticale de G. Le choix de le représenter en G plutôt qu'en un autre point à sa verticale reste arbitraire._
>
>__2.Force résultante de la réaction.__
>Deux forces s'appliquent sur le cube : son poids et l'action du support. La somme des force est nulle à l'équilibre, donc la force résultante de l'action du support est un vecteur force opposé : $\overrightarrow{R} = - \overrightarrow{P}$.  
>On va de même chercher un point de moment résultant nul. A l'équilibre, la somme des moments résultants en un même point. Donc si le moment du poids en un point B est nul, le moment de l'action du support est aussi nul en B. Il vient que le moment de  de l'action du support est nul en tout point à la verticale de G.  
>Pour garder le sens physique de l'action de contact, on aura tendance à représenter $\overrightarrow{R}$ au point d'intersection entre cette verticale et le plan incliné. _Mais mathématiquement, on pourrait le représenter en G._
>
>__3.Inclinaison du plan__  
>Si l'on incline trop le cube, on observe que l'intersection (notée B) entre la verticale en G etle plan incliné se retrouve hors du cube (angle supérieur à 45 degré).  
>Commençons par remarquer que chaque action ponctuelle entre le plan incliné et le cube est toujours dirigée vers l'extérieur du plan (condition de non pénétration sur la composante normale). Ce qui signifie que _le moment en B de toutes ces actions ponctuelles aura le même sens_ (soit positif suivant $\overrightarrow{e_z}$ sur le [schéma](cube_incline)). Il vient que le moment résultant est nécessairement non nul en B : le cube ne peut être en équilibre aux fortes pentes, il va basculer.

```{figure} ./images/meca_actions_cube.png
:name: cube_incline
:align: center
Actions sur le cube
```
## Cylindre sur plan incliné

````{admonition} Exercice 
:class: attention

On considère un cylindre de rayon R, de hauteur h et de masse M uniformément répartie placé sur un plan incliné d'angle $\alpha$.

1. Sur un plan de coupe, représenter les forces résultantes associées à chaque action extérieure sur le cylindre. On distinguera deux cas suivant le comportement de l'action de contact.
1. Le cylindre peut-il rester immobile ? Peut-il glisser sans rouler ? Peut-il rouler sans glisser ? On expliquera ceci au moyen d'un bilan des actions.

````
>Le raisonnement sur le cube peut-être refait ici et montre que le même résultant de l'action du plan sur le cylindre ne peut-être nul que sur l'arête de contact entre le cylindre et le plan incliné. Le poids est lui toujours de moment nul en G. 
>On observe, une fois le schéma réalisé (s'entraîner à le faire), que la somme des moments est nécessairement non nulle donc le cylindre ne peut rester immobile et va forcément tourner (rouler). Il n'y a par contre pas _a priori_ de contradiction à un roulement sans glissement.

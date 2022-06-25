Au 19e siècle, l'anglais George Boole cherche une façon d'utiliser la rigueur mathématique pour résoudre des problèmes logiques. Il développe un système où les seules valeurs possibles sont vrai et faux.

Au milieu des années 1930, Claude Shannon prouve qu'il serait possible d'implémenter toutes expressions algébriques booléennes à l'aide de l'électronique. Cette découverte devint la fondation mathématique de l'informatique.

# Opérateurs

...

## Priorités

|Priorité|Opérateur|
|:------:|:-------:|
|1       |Négation |
|2       |Et       |
|3       |Ou       |

## Négation

Permet d'inverser la valeur, donc vrai devient faux, et faux devient vrai:

| A | ¬A |
|:-:|:--:|
| Faux | Vrai  |
| Vrai | Faux  |

## Et

Vrai si, et seulement si, les deux valeurs sont vraies:

| A | B |A ^ B|
|:-:|:-:|:---:|
| Faux | Faux |  Faux  |
| Faux | Vrai |  Faux  |
| Vrai | Faux |  Faux  |
| Vrai | Vrai |  Vrai  |

## Ou

Vrai si au moins une des deux valeurs est vraie:

| A | B |A v B|
|:-:|:-:|:---:|
| Faux | Faux |  Faux  |
| Faux | Vrai |  Vrai  |
| Vrai | Faux |  Vrai  |
| Vrai | Vrai |  Vrai  |

## Ou exclusif

Vrai si seulement l'une des deux valeurs est vraie:

| A | B |A ⊕ B|
|:-:|:-:|:----:|
| Faux | Faux |  Faux   |
| Faux | Vrai |  Vrai   |
| Vrai | Faux |  Vrai   |
| Vrai | Vrai |  Faux   |

# Propriétés

...

## Loi de Morgan

...
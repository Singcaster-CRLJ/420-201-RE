Au 19e siècle, l'anglais George Boole cherche une façon d'utiliser la rigueur mathématique pour résoudre des problèmes logiques. Il développe un système où les seules valeurs possibles sont vrai et faux.

Au milieu des années 1930, Claude Shannon prouve qu'il serait possible d'implémenter toutes expressions algébriques booléennes à l'aide de l'électronique. Cette découverte devint la fondation mathématique de l'informatique.

# Opérations

Les principales opérations de l'algèbre booléenne sont la négation, la conjonction, et la disjonction.

## Priorités

|Priorité|Opération  |
|:------:|:----------|
|1       |Négation   |
|2       |Conjonction|
|3       |Disjonction|

## Négation

Inverse la valeur, donc vrai devient faux, et faux devient vrai:

|X   |¬X  |
|:--:|:--:|
|Faux|Vrai|
|Vrai|Faux|

## Conjonction

Vrai si, et seulement si, les deux valeurs sont vraies:

| X | Y |X ^ Y|
|:-:|:-:|:---:|
| Faux | Faux |  Faux  |
| Faux | Vrai |  Faux  |
| Vrai | Faux |  Faux  |
| Vrai | Vrai |  Vrai  |

## Disjonction

Vrai si au moins une des deux valeurs est vraie:

| X | Y |X v Y|
|:-:|:-:|:---:|
| Faux | Faux |  Faux  |
| Faux | Vrai |  Vrai  |
| Vrai | Faux |  Vrai  |
| Vrai | Vrai |  Vrai  |

## Disjonction exclusive

Vrai si seulement l'une des deux valeurs est vraie:

| X | Y |X ⊕ Y|
|:-:|:-:|:----:|
| Faux | Faux |  Faux   |
| Faux | Vrai |  Vrai   |
| Vrai | Faux |  Vrai   |
| Vrai | Vrai |  Faux   |

# Expression

...

## Associativité

X ^ (Y ^ Z) = (X ^ Y) ^ Z<br>
X v (Y v Z) = (X v Y) v Z

## Commutativité

X ^ Y = Y ^ X<br>
Y v X = Y v X

## Distributivité

...

## Loi de Morgan

¬(X ^ Y) = ¬X v ¬Y<br>
¬(X v Y) = ¬X ^ ¬Y

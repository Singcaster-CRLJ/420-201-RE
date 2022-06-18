Logique classique utilisée en programmation pour les propositions et l'algèbre booléenne.

# Négation

Permet d'inverser la valeur, donc vrai devient faux, et faux devient vrai:

| A | ¬A |
|:-:|:--:|
| Faux | Vrai  |
| Vrai | Faux  |

# Et

Vrai si, et seulement si, les deux valeurs sont vraies:

| A | B |A ^ B|
|:-:|:-:|:---:|
| Faux | Faux |  Faux  |
| Faux | Vrai |  Faux  |
| Vrai | Faux |  Faux  |
| Vrai | Vrai |  Vrai  |

# Ou

Vrai si au moins une des deux valeurs est vraie:

| A | B |A v B|
|:-:|:-:|:---:|
| Faux | Faux |  Faux  |
| Faux | Vrai |  Vrai  |
| Vrai | Faux |  Vrai  |
| Vrai | Vrai |  Vrai  |

# Ou exclusif

Vrai si, et seulement si, l'une des deux valeurs est vraie:

| A | B |A ⊕ B|
|:-:|:-:|:----:|
| Faux | Faux |  Faux   |
| Faux | Vrai |  Vrai   |
| Vrai | Faux |  Vrai   |
| Vrai | Vrai |  Faux   |

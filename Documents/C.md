Langage de programmation structuré, mais de bas niveaux, permettant de manipuler dynamiquement les espaces mémoire avec des pointeurs, offrant des types primitifs, et très performant grâce à une implémentation de ses compilateurs près du processeur.

# Historique

En 1969, dans les laboratoires de Bell, Ken Thompson développe un système d'exploitation qui deviendra le très célèbre UNIX.

Développé en Assembleur, le système d'exploitation devient difficile à maintenir et à faire évoluer. Thompson, ne trouvant pas d'alternatives existantes viables, conçut, avec l'aide de Denis Ritchie, le langage B. Mais celui-ci n'aboutit pas convenablement pour la réécriture du système UNIX. En 1971, Denis Ritchie entreprit donc de faire évoluer le langage B, pour devenir le langage C.

![Denis Ritchie et Ken Thompson](Images/CHistory.png)

AT\&T, principal commanditaire des laboratoires Bell, oeuvrait dans le domaine des systèmes téléphoniques et, à l'époque, une loi lui interdisait de commercialiser autre chose. Ainsi, en 1975, le système d'exploitation UNIX complet, incluant son code source, fut distribué dans les universités à des fins éducatives.

C'est ainsi que le langage C devint l'un des plus utilisés dans le domaine des technologies de l'information.

# Compilation

Le code source, écrit avec un langage de programmation, n'est pas compréhensible par une machine. Celui-ci doit être traduit, ce que l'on nomme « compilation », afin de créer un programme pouvant être exécuté par un ordinateur:

![Compilation](Images/CCompilation.png)

# Sources

Le code source d'un programme en langage C est stocké dans des fichiers textes ayant, habituellement, « .c » comme extension.

## Commentaires

Tout ce qui suit les caractères « // » sur une ligne est ignoré lors de la compilation:

![Commentaire](Images/CComment.png)

Tout ce qui est encadré des balises « /* » et « */ » est aussi ignoré lors de la compilation:

![Commentaire](Images/CTagComment.png)

## Blocs

Un bloc de code est initié par une accolade ouvrante et terminé par une accolade fermante:

![Bloc](Images/CCodeBlock.png)

# Données

En informatique, c'est le système binaire qui est utilisé pour représenter toutes les données. Il est donc difficile de différencier les valeurs, puisque tout est un amas de 0 et de 1.

## Types

Le langage C offre quelques types primitifs pour représenter les valeurs:

|Type  |Langage C|Taille  |Littéral           |
|:-----|:--------|:-------|:------------------|
|Entier|char     |1 octet |42 ou '*'          |
|      |short    |2 octets|32767              |
|      |int      |4 octets|2147483647         |
|      |long     |8 octets|9223372036854775807|
|Réel  |float    |4 octets|3.1415926          |
|      |double   |8 octets|3.141592653589793  |

Il est possible de préciser, pour les types entiers, que les valeurs peuvent qu'être positives, permettant de représenter de plus grandes valeurs:

|Langage C     |Taille  |Litéral             |
|:-------------|:-------|:-------------------|
|unsigned char |1 octet |255                 |
|unsigned short|2 octets|65534               |
|unsigned int  |4 octets|4294967294          |
|unsigned long |8 octets|18446744073709551614|

### Définitions de type

L'identificateur de certains types n'est parfois pas assez révélateur au niveau du type de donnée et de sa taille. Il est possible de créer des alias de ces types:

![Définition de type](Images/CTypeDef.png)

*Même s'il s'agit du même type de données, la taille est plus claire, et il est plus simple de différencier les valeurs entières (en utilisant « byte ») des valeurs caractères (en utilisant « char »).*

# Variables #

Les variables représentent des espaces, en mémoire centrale, afin de pouvoir y stocker et y consulter des données.

## Identificateurs

Plutôt que d'utiliser les adresses physiques de la mémoire centrale d'un ordinateur pour accéder aux données, il est possible de « nommer » les variables à l'aide d'un identificateur. Mais quelques contraintes s'appliquent à la composition de ceux-ci:

- Doivent débuter par une lettre ou le caractère '_'.
- Doivent contenir que des lettres, des chiffres, et des caractères '_'.
- Doivent être différents des mots-clés du langage C.

## Déclarations

Le diagramme ci-dessous expose toutes les possibilités de syntaxe afin de déclarer et initialiser des variables de même type:

![Diagramme syntaxique](Images/CVariableRailroad.png)

# Point d'entré

La procédure, ou fonction, identifiée « main » est le point d'entré d'un programme en langage C:

![Procédure principale](Images/CMain.png)

La fonction principale permet de retourner une valeur entière au système d'exploitation:

![Fonction principale](Images/CMainRet.png)

La fonction principale peut aussi avoir des paramètre afin de reçevoir des arguments:

![Fonction principale](Images/CMainArgv.png)

# Macros

Ces instructions sont toutes précédées du caractère « # » et sont exécutées avant la compilation.

## Définitions

Sert régulièrement à déclarer des constantes, et agit comme un « rechercher-remplacer »:

![Booléens](Images/CBoolTypeDef.png)

Ainsi, tous les termes « false » seront remplacés par 0 et tous les termes « true » seront remplacés par 1, avant la compilation.

## Inclusions

Agit comme un « copier-coller »:

![Inclusion](Images/CInclude.png)

Ainsi, le code nécessaire sera copié du fichier « stdbool.h » et collé à l'endroit du « #include » avant la compilation.

*Par exemple, pour utiliser des variables booléennes dans un projet, il faut définir le type (typedef) « bool », et définir (#define) les constantes « false » et « true ». Ces définitions ont plutôt été placées dans un fichier d'en-tête « stdbool.h », permettant ainsi de seulement l'inclure (#include) dans les projets nécessitant l'utilisation de booléens.*

# Opérateurs

...

## Priorités

Liste, non exhaustive, des opérateurs du langage C:

|Priorité|Opérateur|Description                     |Évaluation                               |
|:------:|:-------:|:-------------------------------|:---------------------------------------:|
|1       |()       |Parenthèses                     |![Gauche à droite](Images/RightArrow.png)|
|        |[]       |Crochets                        |![Gauche à droite](Images/RightArrow.png)|
|        |.        |Membre de structure             |![Gauche à droite](Images/RightArrow.png)|
|        |->       |Membre de pointeur de structure |![Gauche à droite](Images/RightArrow.png)|
|2       |*        |Indirection                     |![Droite à gauche](Images/LeftArrow.png) |
|        |&        |Déréférencement                 |![Droite à gauche](Images/LeftArrow.png) |
|        |~        |Négation bit à bit              |![Droite à gauche](Images/LeftArrow.png) |
|        |!        |Négation logique                |![Droite à gauche](Images/LeftArrow.png) |
|        |-        |Négation arithmétique           |![Droite à gauche](Images/LeftArrow.png) |
|        |--       |Décrémentation                  |![Droite à gauche](Images/LeftArrow.png) |
|        |++       |Incrémentation                  |![Droite à gauche](Images/LeftArrow.png) |
|3       |*        |Multiplication                  |![Gauche à droite](Images/RightArrow.png)|
|        |/        |Division                        |![Gauche à droite](Images/RightArrow.png)|
|        |%        |Modulo                          |![Gauche à droite](Images/RightArrow.png)|
|4       |+        |Addition                        |![Gauche à droite](Images/RightArrow.png)|
|        |-        |Soustraction                    |![Gauche à droite](Images/RightArrow.png)|
|5       |<<       |Décalage de bit à gauche        |![Gauche à droite](Images/RightArrow.png)|
|        |>>       |Décalage de bit à droite        |![Gauche à droite](Images/RightArrow.png)|
|6       |<        |Plus petit                      |![Gauche à droite](Images/RightArrow.png)|
|        |<=       |Plus petit ou égal              |![Gauche à droite](Images/RightArrow.png)|
|        |>        |Plus grand                      |![Gauche à droite](Images/RightArrow.png)|
|        |>=       |Plus grand ou égal              |![Gauche à droite](Images/RightArrow.png)|
|7       |==       |Égal                            |![Gauche à droite](Images/RightArrow.png)|
|8       |&        |Et bit à bit                    |![Gauche à droite](Images/RightArrow.png)|
|9       |^        |Ou exclusif bit à bit           |![Gauche à droite](Images/RightArrow.png)|
|10      |\|       |Ou bit à bit                    |![Gauche à droite](Images/RightArrow.png)|
|11      |&&       |Et logique                      |![Gauche à droite](Images/RightArrow.png)|
|12      |\|\|     |Ou logique                      |![Gauche à droite](Images/RightArrow.png)|
|13      |?:       |Opérateur conditionnel          |![Droite à gauche](Images/LeftArrow.png) |
|14      |=        |Affectation                     |![Droite à gauche](Images/LeftArrow.png) |
|15      |,        |Séquence                        |![Gauche à droite](Images/RightArrow.png)|

*Les opérateurs de priorité 2 sont unaires.*

## Arithmétiques

Les opérateurs arithmétiques ...

### Type

...

### Modulo

...

### Incrémentation et Décrémentation

...

## Relationnels

Les opérateurs relationnels ...

## Logiques

Les opérateurs logiques ...

### Bit à bit

...

# Structures de contrôle

Elles permettent de contrôler le flot d'exécution d'un programme.

## Si

Si une proposition, toujours interprétée comme étant booléenne, est vraie, une ou plusieurs instructions sont exécutées:

![Si](Images/ControlStructure.png)

### Sinon

Une ou plusieurs instructions peuvent aussi être exécutées dans le cas ou la proposition est fausse:

![Sinon](Images/CompleteControlStructure.png)

Le diagramme ci-dessous expose toutes les possibilités de syntaxe afin de déclarer cette structure de contrôle:

![Commutateur](Images/CElseRailroad.png)

## Commutateur

...

![Commutateur](Images/SwitchStructure.png)

### Défaut

...

![Défaut](Images/SwitchDefault.png)

Le diagramme ci-dessous expose toutes les possibilités de syntaxe afin de déclarer cette structure de contrôle en langage C:

![Commutateur](Images/CSwitchRailroad.png)

# Structures de répétition

Elles permettent d'exécuter des instructions à plusieurs reprises.

## Tant que

Une ou plusieurs instructions sont exécutées tant que la proposition est vraie:

![Tant que](Images/LoopStructure.png)

Le diagramme ci-dessous expose toutes les possibilités de syntaxe afin de déclarer cette structure de répétition en langage C:

![While](Images/CWhileRailroad.png)

## Pour

...

# Entrées et Sorties

...

## Affichage

...

## Saisi

...

## Fichier

...

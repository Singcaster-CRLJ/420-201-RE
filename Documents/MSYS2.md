# MSYS2

Système de distribution d'outils de développement.

## Téléchargement

Téléchargez et exécutez le [programme d'installation](https://www.msys2.org/).

## Installation

![1](Images/MSYS201.png)

Cliquez sur le bouton « Suivant »:

![2](Images/MSYS202.png)

Cliquez sur le bouton « Suivant »:

![3](Images/MSYS203.png)

Cliquez sur le bouton « Suivant »:

![4](Images/MSYS204.png)

Veuillez patienter:

![5](Images/MSYS205.png)

Cliquez sur le bouton « Terminer »:

![6](Images/MSYS206.png)

### Mise à jour

Pour s'assurer que le système est à jour, saisissez l'instruction suivante:

```
pacman -Suy
```

![7](Images/MSYS207.png)

Appuyez sur la touche « Entrée (Enter) »:

![8](Images/MSYS208.png)

### Outils de développement

Pour installer les outils de développement, saisissez l'instruction suivante:

```
pacman -S --needed base-devel mingw-w64-x86_64-toolchain
```

![9](Images/MSYS209.png)

Appuyez sur la touche « Entrée (Enter) »:

![10](Images/MSYS210.png)

Appuyez sur la touche « Entrée (Enter) »:

![11](Images/MSYS211.png)

Appuyez sur la touche « Entrée (Enter) »:

![12](Images/MSYS212.png)

### Librairie graphique

Pour installer la librairie graphique « SDL2 », saisissez l'instruction suivante:

```
pacman -S mingw-w64-x86_64-SDL2 mingw-w64-x86_64-SDL2_image mingw-w64-x86_64-SDL2_ttf
```

![13](Images/MSYS213.png)

Appuyez sur la touche « Entrée (Enter) »:

![14](Images/MSYS214.png)

Appuyez sur la touche « Entrée (Enter) »:

![15](Images/MSYS215.png)

### Configuration

Pour que Windows connaisse les outils de développement, ouvrez le « Menu Démarrer »:

![16](Images/MSYS216.png)

Saisissez « variable » dans le champ de recherche:

![17](Images/MSYS217.png)

Cliquez sur le meilleur résultat « Modifier les variables d'environnement système »:

![18](Images/MSYS218.png)

Cliquez sur le bouton « Variables d'environnement ... »:

![19](Images/MSYS219.png)

Double-cliquez sur la ligne « Path » des variables système:

![20](Images/MSYS220.png)

Cliquez sur le bouton « Nouveau », saisissez « C:\msys64\mingw64\bin », et cliquez sur tous les boutons « Ok » jusqu'à fermer toutes les fenêtres, puis redémarrez l'ordinateur.
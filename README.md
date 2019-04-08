# Jeu des 6 couleurs

Ce KATA est un sujet intéressant pour mettre en pratique les différentes méthodes/pratiques vues au cours de la formation proposée par LCDLV.
<br>
Le but est de créer un jeu de stratégie au tour par tour.
<br><br>
Vous trouverez dans ce README toutes les informations nécessaires pour réaliser le jeu. Le README est divisé en plusieurs parties:<br><br>
**-Règles du jeu<br><br>
-Exemples<br><br>
-Extensions possibles**
<br><br><br>
***

## Règles du jeu

- Le jeu des 6 couleurs est un jeu relativement simple qui peut se jouer de 2 à 4 joueurs (*plus de joueurs peuvent être ajoutés mais il faudra toujours qu'il y ait au moins 2 couleurs de plus que le nombre de joueurs*)<br><br>
- Le jeu prend place sur une grille composée de cellules colorées de manière aléatoire (parmi les 6 couleurs possibles)<br><br>
- Chaque joueur commence avec une seule cellule située à une des extrémités de la grille, cette cellule sera à l'initialisation sans couleur ou d'une couleur non présente dans les 6 couleurs (*voir WARNING ci-dessous*)<br><br>
- Couleurs des cellules: Bleu / Vert / Rouge / Magenta / Jaune / Orange<br><br>
- Le but de chaque joueur est de récupérer le plus de cellules possibles sur le plateau avant que l'ensemble des cellules soient prises.<br><br>

#### Capture de cellule
Pour capturer une cellule il faut respecter 2 conditions:<br>
- la cellule qu'on veut récupérer doit être adjacente à au moins une de nos cellules.<br>
- la cellule doit avoir la même couleur que celle choisie par le joueur.<br><br>

#### Tour de jeu pour un joueur
Comme mentionné précédemment, c'est un jeu au tour par tour.<br>
**A chaque tour un joueur choisit une couleur parmi celles qui lui sont proposées pour changer la couleur de toutes ses cellules par cette nouvelle couleur.**<br>
Les couleurs proposées sont celles qui ne sont possedées par aucun joueur.<br>
**Le joueur ne pourra donc jamais choisir la même couleur que celle qu'il a choisi au tour précédent ou une couleur possedée par un adversaire.**<br>
Une fois la couleur choisie toutes ses cellules deviennent de cette couleur et les cellules adjacentes aux siennes et de la même couleur deviennent ses cellules.

#### Warning
**⚠La couleur de chaque cellule est choisie aléatoirement parmi les 6 couleurs cependant les cellules de chaque joueur doivent être à l'initialisation de la grille d'une couleur non présente ou d'aucune couleur pour éviter tout avantage d'un joueur au début de la partie**<br>
**⚠ Deux cellules (ou plus) qui ont la même couleur et sont adjacentes forment un groupe de cellules: si une des cellules du groupe est prise par un joueur l'ensemble des cellules de ce groupe seront prises**<br><br>

Le jeu termine lorsque toutes les cellules sont prises ou lorsqu'un joueur possède plus de la moitié des cellules du jeu (ou encore s'il a assez de cellules pour avoir plus de cellules que les autres joueurs même si ceux-ci  récuperaient les cellules restantes).
<br><br><br>
***

## Exemples

Imaginons que le tableau ci-dessous représente la grille où les cellules indiquent leur couleur par l'initiale de celle-ci et que le joueur possède la première cellule (initiale de la couleur en majuscule):

| R   | b   | v   |
| --- | --- | --- |
| j   | v   |  b  |

En choisissant **bleu** le joueur récupère la cellule bleu qui est collée à sa cellule mais pas d'autres cellules car aucune autre ne remplit la condition pour être obtenue.

| B   | B   | g   |
| --- | --- | --- |
| y   | g   |  b  |

***
Dans cet exemple on va considerer que le joueur possède les 2 premières cellules (en majuscule) et il y a un groupe de cellules bleues:

| R   | R   | b   |
| --- | --- | --- |
| j   | v   |  b  |

Si le joueur choisit le **bleu** alors il obtiendra 2 cellules car celles-ci sont dans le même groupe et une des cellules touche une cellule du joueur.

| B   | B   | B   |
| --- | --- | --- |
| j   | v   |  B  |
<br><br><br>
***

## Extensions possibles

On peut ajouter au jeu des améliorations au jeu en proposant d'autres règles:<br>

### Interface graphique
Donner au jeu un meilleur aspect qu'un simple affichage console en proposant une interface graphique.

### Sauvegarde d'une partie
Pouvoir sauvegarder l'état d'une partie pour ensuite pouvoir la reprendre plus tard.

### Capture de cellules entourées
Ajouter une règle permettant la capture automatique de cellules (ou groupes de cellules) qui sont entourées par les cellules d'un joueur.

### Brouillard de guerre
Proposer un brouillard de guerre qui bloque la visibilité du jeu pour chaque joueur permettant à celui-ci de ne voir que les cellules adjacentes aux siennes.

### Changer la forme des cellules ou la taille de la grille
Changer la forme des cellules pour proposer par exemple des cellules triangulaires ou hexagonales.<br>
Proposer aux joueurs de choisir la taille de la grille à l'initialisation de la partie.
<br><br><br>*Jeu proposé par Vincent Rojo*

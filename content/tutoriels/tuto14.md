+++
title = ""
description = "Theme 1 Architecture des ordinateurs : modèle de von Neumann"
weight = 0
+++

<h1>INTRODUCTION</h1>

## <u>I Contexte</u><br>
En 1946 le premier ordinateur entièrement électronique est enfin opérationnel. Il s’agit de ***l’ENIAC
(Electronic Numerical Integrator And Computer)***. Il pouvait en principe être reprogrammé pour
résoudre tous les problèmes calculatoires (il est dit Turing-complet).

Il s’agit d’une machine imposante (17 468 tubes à vide, 7 200 diodes à cristal, 1 500 relais, 70 000 résistances, 10 000 condensateurs et environ 5millions de soudures faites à la main) occupant une surface de 167 m².
6 femmes ont été les premières personnes à programmer l’ENIAC pour le calcul de tirs balistiques.
Pour programmer un calcul il fallait faire un plan des connexions nécessaires, puis procéder au câblage physique. Le travail était long et les erreurs dures à détecter.

![Photo Eniac](https://external-content.duckduckgo.com/iu/?u=http%3A%2F%2Fpbs.twimg.com%2Fmedia%2FDV6fBIEVwAMw7Md.jpg&f=1&nofb=1&ipt=3007cdc3cd390aa514ed693198468d14ca2303346465008af72aa526e6ef535b&ipo=images)

## <u>II von Neumann</u><br>
Le mathématicien/physicien/… américano-hongrois John von Neumann (1903 - 1957), qui a participé à l’élaboration du projet ENIAC, propose alors un nouveau modèle pour simplifier le
fonctionnement d’un ordinateur. Il décide de séparer physiquement la partie contrôle/calculs de la
partie mémoire, tout en affirmant qu’une instruction n’est qu’une donnée de mémoire comme une
autre (on peut donc stocker des programmes en mémoire).
C’est le modèle d’architecture de von Neumann, qui est encore utilisé de nos jours !

Voici un schéma de l’architecture de von Neumann
![ schéma de l’architecture de von Neumann](https://commons.wikimedia.org/w/index.php?search=architecture+de+von+Neumann&title=Special%3AMediaSearch&go=Go&type=image)


## <u>III les différentes parties</u><br>

L’architecture de von Neumann est donc composée de 4 principales parties.

### La memoire 

Elle permet de stocker des informations sous forme de bits. La mémoire ne peut pas
stocker un seul bit à la fois, elle stocke des mots de 8 bits (ou 16/32/64 bits) appelés un
octet. Le processeur accède à différents mots de la mémoire grâce à leur adresse.

### Le Processeur (CPU)

C’est le cœur de tout ordinateur. Il est lui même composé de 2 parties indépendantes,
d’une part l’Unité de Contrôle (UC) et d’autre part l’Unité Arithmétique et Logique
(UAL ou ALU en anglais).

Uc : C'est elle qui donne des ordres , elle cherche la prochiane instruction en memoire et le fait executer par AUL

UAL : C'est l'organe de l'ordinateur changé d'affecte les calcules et de changer ou de savoir les info en memoire 

Les discpositifs entrée et sortie  (E/O)

### Quels que dispositif d'entrée : <br>
clavier , souris , camera , micro , tablette graphique , scanner , ecran tactile
### Quels que dispositif de sortie : <br>
enceinte , ecran , imprimante , projecteur , ecran tactil

### le bus 
C’est la partie physique qui permet aux autres composants de communiquer entre-eux.

## <u>IV Le processeur et ses instructions</u><br>

Les UC et UAL d’un processeur ne connaissent qu’un nombre réduit d’instructions. Celles-ci
dépendent du modèle et de la marque du processeur mais la plupart des processeurs récents ont une
partie de leur jeu d’instructions commune.
Afin de pouvoir travailler avec des informations, un processeur possède un petit espace mémoire
propre pour stocker des données. Il y a généralement au moins 8 registres permettant de stocker un mot
de 8 bits chacun (voir 32 ou même 64 bits pour les plus récents).
Il n’est pas demandé en 1ère NSI de connaître par cœur le langage assembleur (qui permet de donner
presque directement des instructions au processeur) mais vous devez en comprendre le
fonctionnement.
Voici quelques instructions classiques mais simplifiées pour un microprocesseur ARM moderne :

Instruction | 	Operandes (exemple) | Commentaires
 --- | --- | --- 
LDR | R0, 102  | Charge le mot à l’adresse 102 en mémoire dans le registre R0.
STR | R1, 63 | Écrit le contenu du registre R1 dans la mémoire à l’adresse 63.
MOV | R0, R2 | Copie la valeur de R2 dans R0. MOV ne peut accéder à la mémoire. 
ADD | R0, R3, #13 | Ajoute le contenu de R3 et le nombre 13 (opérande immédiat grâce au #, sinon c’est une adresse mémoire) et écrit le résultat dans leregistre R0.														
SUB | R1, R2, R0 | Soustrait le contenu de R0 à R2 et écrit le résultat dans R1.
B 	| 18  | La prochaine instruction se trouve à l’adresse mémoire 18 (saut). 
CMP | R0,R1 | CoMPare les valeurs des registres R0 et R1. Commande suivie d’une instruction de saut conditionnel 
BEQ | 13 | En cas d’égalité (Equal) du CMP, l’instruction suivante est à l’adresse 13 
BNE | 13 | En cas d’inégalité (Not Equal) du CMP
BGT | 13 | Si le premier opérande du CMP est supérieur au second (GreaterThan)
BLT | 13 | Si le premier opérande du CMP est inférieur au second (LessThan)
HALT | 13 | Fin de l’exécution. Important sinon le programme continue ! 


Exemples : 

1) Que font les instructions suivantes ?
MOV R1, #33 : Copie la valeur de 33 dans R1
ADD R0, R1, #12 : Ajoute le conteneur R1 et le nombre 12 dans R0
STR R0, 100 : Ecrit le contenue de R0 dans la cellue 100

2) Que fait le programme suivant si l’adresse mémoire 102 contient le nombre 42 ?
LDR R0, 102
MOV R1, R0
ADD R0, R0, R1
STR R0, 102
Remarque : l’assembleur permet aussi d’utiliser des étiquettes pour les adresses mémoires (ce qui est
pratique pour les sauts) et se charge de convertir l’étiquette par l’adresse mémoire correspondante :
3) LDR R0, 30
LDR R1, 31
CMP R0, R1
BGT saut
SUB R0, R1, R0
STR R0, 30
HALT
saut:
SUB R0, R0, R1
STR R0, 32
HALT
Que contient l’adresse mémoire 30 à la fin du programme si :
Adresse mémoire 30 au début  | Adresse mémoire 31 | Adresse mémoire 32 à la fin 
 --- | --- | --- 
24  | 18 | 6
15 | 45 | -
12 | 12 | 0 

Que fait donc le programme précédent ? Écrire un programme en Python faisant la même chose (on
considérera que l’adresse mémoire 30 sera une variable x et l’adresse 31 une variable y).


Pour aller plus loin :
Êtes-vous capable d’écrire un programme en assembleur utilisant au maximum 4 registres pour
multiplier un nombre entier positif écrit à l’adresse mémoire 100 par un nombre entier positif écrit à
l’adresse mémoire 101 et enregistrer le résultat à l’adresse mémoire 102 ?


Sources : https://fr.wikipedia.org/wiki/Architecture_de_von_Neumann
https://pixees.fr/informatiquelycee/n_site/nsi_prem_von_neu.html
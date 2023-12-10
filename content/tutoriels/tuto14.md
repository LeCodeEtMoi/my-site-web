+++
title = ""
description = "Theme 1 Architecture des ordinateurs : modèle de von Neumann"
weight = 0
+++

<h1>INTRODUCTION</h1>

<u>I Contexte</u><br>
En 1946 le premier ordinateur entièrement électronique est enfin opérationnel. Il s’agit de ***l’ENIAC
(Electronic Numerical Integrator And Computer)***. Il pouvait en principe être reprogrammé pour
résoudre tous les problèmes calculatoires (il est dit Turing-complet).

Il s’agit d’une machine imposante (17 468 tubes à vide, 7 200 diodes à cristal, 1 500 relais, 70 000 résistances, 10 000 condensateurs et environ 5millions de soudures faites à la main) occupant une surface de 167 m².
6 femmes ont été les premières personnes à programmer l’ENIAC pour le calcul de tirs balistiques.
Pour programmer un calcul il fallait faire un plan des connexions nécessaires, puis procéder au câblage physique. Le travail était long et les erreurs dures à détecter.

![Photo Eniac](https://external-content.duckduckgo.com/iu/?u=http%3A%2F%2Fpbs.twimg.com%2Fmedia%2FDV6fBIEVwAMw7Md.jpg&f=1&nofb=1&ipt=3007cdc3cd390aa514ed693198468d14ca2303346465008af72aa526e6ef535b&ipo=images)

<u>II von Neumann</u><br>
Le mathématicien/physicien/… américano-hongrois John von Neumann (1903 - 1957), qui a participé à l’élaboration du projet ENIAC, propose alors un nouveau modèle pour simplifier le
fonctionnement d’un ordinateur. Il décide de séparer physiquement la partie contrôle/calculs de la
partie mémoire, tout en affirmant qu’une instruction n’est qu’une donnée de mémoire comme une
autre (on peut donc stocker des programmes en mémoire).
C’est le modèle d’architecture de von Neumann, qui est encore utilisé de nos jours !

Voici un schéma de l’architecture de von Neumann
![ schéma de l’architecture de von Neumann](https://commons.wikimedia.org/w/index.php?search=architecture+de+von+Neumann&title=Special%3AMediaSearch&go=Go&type=image)


<u>III les différentes parties</u><br>

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
clavier , souris , camera , micro , tablette graphique , scanner , ecran tactil 
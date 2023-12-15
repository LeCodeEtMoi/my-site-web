+++
title = ""
description = "Theme 3 Tuples et liste"
weight = 0
+++

En programmation , un objet peut être simple ( un nombre une chaine de caractère , un booléen) ou construit ( conposé de plusieure "objet")

Exemple : Un objet 'train' peut être composé de deux objets 'trains' (accroché entre eux ) est composé d'un locomotive , de vagon etc..

Ici nous allons étudiée deux structure de trype contruits : les tuples et les listes 

## <u>I Les tuples</u><br>

Un uplet (tuple en anglais) est une séquence d'éléments non modifiables . Pour créer un tuple on utilise des parentèse . L'acces aux élément se fait avec leur indices ( prmier indice : 0)


Exemple d'utilisation avec python

t =() # tuple vide

t = (4) # initier un tuple avec seul valeur 

t = t+(2,5,7,8) # concaténation t vaut ( 4,2,5,7,8)

t[2] = #affiche 5

t[2]=3 # Va provoquer une erreur car les tuples sont non modifiable 

t =(4,1,5,2,3,9,7,2,8)

t[2:5] # résultat (5,2,3)
t[:5] # résultat retournée ( 4,1,3,2,3)
t[3:] #résultat retourn ( 2,3,9,7,2,8)
t[:3]+(10,)+t(4:) #résultat (4,1,5,10,3,9,2,8)
len(t) # résultat retourné 9

## <u>II Les tableaux ( ou listes )</u><br>

Un tableau ( list en python) est une séquence d'élément modifiabls . Pour créer un tableau on utilise des crochet . L'acces au élément se fait avec les indices , le premier indice est 0

Exemple d'utulisation avec python 

Le tableauvide est noté []

l = [4,1,6,11,12] # initialisation du tableau

l[2] #affiche 6

l[1]=10 #erreur
len(l) # affiche 5
l[2:] # afiche [6,11,12]
l[3:6] # affiche [11,12]
[6,3,1] + [4,8] # affiche [6,3,1,4,8]


Il est possible de rajouter un élément a une liste il se place alors en fin liste :

l.append(15) #ajoute 15 en dernier position
l.append(0)

Il est possible de siuprimer le dernièer élément de tableaux :

l =['a','c','yo','deux','d']
l.pop # suprimme et renvoie la dernière element

Les tableaux sont des itéralbe , il est possible de les parcourir de deux façon : 

i = ['a','c','yo','deux']

for element in l :
	print(element)



i = ['a','c','yo','deux']

for i in range(len(l))
	print(l[i])

Les affichages serront identiques : Il affiche un par un les élément de la liste 'a','c','yo','deux'
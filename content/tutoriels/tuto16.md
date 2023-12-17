+++
title = ""
description = "Theme 3 Tuples et liste"
weight = 0
+++

En programmation , un objet peut être simple ( un nombre une chaine de caractère , un booléen) ou construit ( conposé de plusieure "objet")

Exemple : Un objet 'train' peut être composé de deux objets 'trains' (accroché entre eux ) est composé d'un locomotive , de vagon etc..

Ici nous allons étudiée deux structure de trype contruits : les tuples et les listes 

# <u>I Les tuples</u><br>

Un uplet (tuple en anglais) est une séquence d'éléments non modifiables . Pour créer un tuple on utilise des parentèse . L'acces aux élément se fait avec leur indices ( prmier indice : 0)


<u>Exemples d'utilisation avec python</u> : 

t =() # tuple vide<br>

t = (4) # initier un tuple avec seul valeur <br>

t = t+(2,5,7,8) # concaténation t vaut ( 4,2,5,7,8)<br>

t[2] = #affiche 5<br>

t[2]=3 # Va provoquer une erreur car les tuples sont non modifiable <br>

t =(4,1,5,2,3,9,7,2,8)<br>

t[2:5] # résultat (5,2,3)
t[:5] # résultat retournée ( 4,1,3,2,3)
t[3:] #résultat retourn ( 2,3,9,7,2,8)
t[:3]+(10,)+t(4:) #résultat (4,1,5,10,3,9,2,8)
len(t) # résultat retourné 9

# <u>II Les tableaux ( ou listes )</u><br>

Un tableau ( list en python) est une séquence d'élément modifiabls . Pour créer un tableau on utilise des crochet . L'acces au élément se fait avec les indices , le premier indice est 0

<u>Exemples d'utilisation avec python</u> : 

Le tableauvide est noté []

l = [4,1,6,11,12] <b># initialisation du tableau</b><br>

l[2] <b># affiche 6</b><br>

l[1]=10 <b># erreur</b><br>
len(l) <b># affiche 5</b><br>
l[2:] <b># afiche [6,11,12]</b><br>
l[3:6] <b># affiche [11,12]</b><br>
[6,3,1] + [4,8] <b># affiche [6,3,1,4,8]</b><br>


<b>Il est possible de rajouter un élément a une liste il se place alors en fin liste :</b>

l.append(15) #ajoute 15 en dernier position
l.append(0)

Il est possible de siuprimer le dernièer élément de tableaux :

l =['a','c','yo','deux','d']<br>
l.pop # suprimme et renvoie la dernière element

Les tableaux sont des itéralbe , il est possible de les parcourir de deux façon : 

i = ['a','c','yo','deux']<br>

for element in l :
	print(element)



i = ['a','c','yo','deux']

for i in range(len(l))<br>
	print(l[i])<br>

Les affichages serront identiques : Il affiche un par un les élément de la liste 'a','c','yo','deux'
+++
title = ""
description = "Theme 1 Architecture des ordinateurs : modèle de von Neumann"
weight = 0
+++

## <u>I Origine</u><br>

L'algebre de Bool est du au logicien mathematicien et philosophe britanique George Bool (1815-1864) En 1847 , puis 1854 , ce scientifique publie les bases de ce qu'on appelle aujourd'hui l'alegbre de Boole . Son interet dst de tarduire des idées en concepts en équation , leur appliquer certaines lois et retraduire le résulatat en terme logiques , n'acceptant pas que des valeur numerique : 0 et 1 (Faux ou Vrais) . L'importance de son travail est dans de nombreux travail est dans de nombreux domaines ( théorie des probabilités, circuits téléphonique , hdroliques ..) Dont l'informatique .

 ## <u>II Définition</u><br>

 <b>Un booleen est un type de variable a 2 étape : Vrais (True)(1) et Faux (False)(0)</b>

 Un booléen peut être le résultat d'un comparaison , il s'agit alors d'un test. Si le test est valide , le résultat est alors Vrai ( True sous Python). Dans le cas contraire , le résulat est Faux . (False sous Python)<br>

 <u>Exemple</u>

 N = 13 
 print(N > 12)
 L'interpreteur affiche <b>True</b>

 N = 13 
 print(N < 12)
 L'interpreteur affiche <b>False</b>

 Les operateurs de comparaisons que nous utiliserons sont : 

 Operateur | Signification
 --- | --- 
 < | strictemment inferieur
 <= | inferieur ou égal
 > | strictement superieur
 => | superieur ou égal
 == | égal
 != | different


 ## <u>III Operateur et tables de vérités</u><br>

 Operateur "et" : L'operateur "and" permet de tester si deux booleens sont vrais : "a and b " a pour résultat True si et seulement si o est vrais et b est vrai. Sa table de vérité est la suivante : 

  a | b | a and b 
 --- | --- |
 0 | 0 | 0
 0 | 1 | 0
 1 | 0| 0
 1 | 1 | 1

Remarques : 

- matématiquement le résultat est donné par intersaction 
- cette operation booléenne est appelée "conjonction"

Exemple : La variable booléenne AmpouleOK représente le fait qu'une ampoule est en état de fonctionnement , la variable booléenne InterrupeteurOn est vrais si l'interupteur  controlant cette ampoule est en position "on" La varialble booléene LUmièreAllumée represente le fait que la lumière est allumée.

Alors : LumièreAllumée = AmpouleOk and InterupteurON

Operateur "ou" : L'operateur "or" permet de tester si l'un des deux booléens est au moins vrai : "a or b" a pour résultat True et si seulement si au moins un des deux booléens a ou b est vrai . Sa table de vérité est la suivante : 

  a | b | a or b 
 --- | --- |
 0 | 0 | 0
 0 | 1 | 1
 1 | 0| 1
 1 | 1 | 1

 Remarque : 

 - Cette operation booléenne est appelée "disjonction"

 Exemple : La variable booléenne AmpoleHS represente le fait qu'une ampoule n'est pas en état de fonctionnement , la variable booléenne InterupteurOff est vrais si l'interupteur controlant est en position "off" La variable booléenne LumièreEteinte represente le fait que la lumière est éteinte .

 Alors Lumière Eteinte = InterupteurOff or AmpouleHS

 Operateur "non" : L'operateur "not" retourne le booléen opposé . Sa talbe de vérité est la suivante 

   a | not a 
 --- | --- |
 0 | 1 | 
 1 | 0 |

 Remarque : 

 - cette operateur boooléenne est appelée "négation"

 Exemple :

 La variable booléenne EauSolide represente le fait que l'eau est sous forme de glace , la variable TemperaturePositive est vrai si la temprature de l'eau est positive .

 Alors : Temperature Positive : not EauSolide 
 		 Eau Solide  : not TemperaturePositive


 Operateur "ou exclusif" l'operateur "xor" permet de tester si et seulement l'un des deux booléens est vrai : "a xor b " a pour résultat True si et seulement l'un des deux des booléens est vrai: "a xor b" a pour résultat True si et seulement si un des des booléens a ou b est vrais et l'autre faux . Sa table de vérité la suivante : 


  a | b | a xor b 
 --- | --- | ---
 0 | 0 | 0
 0 | 1 | 1
 1 | 0| 1
 1 | 1 | 0

 Exemple : 

 Deux interupteur va et viens controle la lumière d'un pice , pour qu'elle soit alumée . La variable booléenne VaEtViens1_ON represente le fait que l'interupteur va et vient n°1 est en position "on".La variable booléenne VaEtVient2_ON represente le fait que l'interupteur va et viens n°2 est en position "on" EtatLumière est vraie si la lumière est alumée

 Alors : ÉtatLumière = VaEtVient1 xor VaEtVient2 





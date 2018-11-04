# zFraction
## Définition de classe, surcharge d'opérateurs

### Introduction
En C++, vous pouvez représenter différents types de données. Les entiers, les nombres réels, les nombres complexes,... Mais il n'existe pas de type représentant une notion que l'on retrouve souvent en mathématique, les fractions.  
Vous l'avez sûrement deviné, je vous propose donc de créer une classe pour palier à ce "manque".  
Cet exercice est également un grand classique de la programmation.

### Objectif
Le but de cet exercice est de réaliser une classe Fraction qui permettera de représenter la notion de fraction.  
Pour rappel, une fraction est un nombre donné par le rapport de deux nombres entiers. Par exemple 22/7 ou 355/113. 

### Contraintes

Votre classe devra fournir les services suivants:

1. Construction à partir d'un nombre entier.  
	Construction à partir d'un couple d'entier "Numérateur-Dénominateur".

2. Construction à partir d'un nombre à virgule (double).

3. Construction à partir d'une chaine de caractère de la forme "35/8".

4. Surcharge des opérateurs arithmétiques usuels (+,-,\*,/) et pourquoi pas puissance via l'opérateur ^. Attention aux divisions par 0. Pensez également à implémenter les versions +=,-=, \*=,/= et ^= des opérateurs. Vous pouvez également réfléchir à la question des opérateurs du type "Fraction + Entier" ou "Reel + Fraction".

5. Surcharger l'opérateur << pour l'affichage dans un flux. (Pensez au cas particulier des fractions comme 2/1 par exemple !)

6. Surcharger les opérateurs de comparaison (==,!=,<,>,<=,>=).

7. Proposer une fonction "toDouble" qui convertit la fraction en nombre à virgule.

8. Proposer un moyen de connaître le dénominateur et le numérateur.

Votre fraction devra toujours être exprimée sous forme irréductible. C'est-à-dire que 3/9 devra être converti en 1/3

### Références
Pour implémenter les opérateurs, les règles qui s'appliquent aux fractions sont disponibles sur [wikipedia](https://fr.wikipedia.org/wiki/Fraction_\(math%C3%A9matiques\)#Op%C3%A9rations_sur_les_fractions)

Pour simplifier les fractions, il est utile de connaitre le plus grand dénominateur commun (PGCD). Pour le calculer, vous pouvez vous référer à [l'algorithme d'Euclide](https://fr.wikipedia.org/wiki/Algorithme_d'Euclide)

### Crédits
Cet exercice est une réécriture de l'exercice proposé par Nanoc sur [OpenClassroom](https://openclassrooms.com/forum/sujet/exercices-venez-vous-entrainer-41065?page=24#message-3053616)
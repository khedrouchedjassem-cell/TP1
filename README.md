TP1 — Tests Unitaires avec JUnit 5
Bugs détectés et corrections
Exercice 1 — Classe Palindrome
Bug détecté

Une erreur était présente dans la boucle while : les indices i et j étaient mal mis à jour.

Code incorrect :

i--;
j++;

Correction :

i++;
j--;

Le problème a été corrigé dans Exo1Correction.java.

Remarque

Dans cet exercice, les tests de couverture de branches et de couverture de conditions sont pratiquement identiques.

Exercice 2 — Anagram
Bug détecté

Une erreur de condition était présente dans la boucle for de la méthode isAnagram :

Code incorrect :

for (int i = 0; i <= s1.length(); i++)

Correction :

for (int i = 0; i < s1.length(); i++)

Cette erreur provoquait un dépassement d’indice (IndexOutOfBoundsException).

Exercice 3 — BinarySearch
Bugs détectés
La condition de la boucle ne permettait pas de comparer le dernier élément lorsque low == high.

Code incorrect :

while (low < high)

Correction :

while (low <= high)
Une condition incorrecte était utilisée dans la comparaison :

Code incorrect :

array[mid] <= element

Si array[mid] == element, la méthode doit directement retourner mid.

Exercice 4 — QuadraticEquation
Cas de tests réalisés
a = 0 → lève une IllegalArgumentException
delta < 0 → retourne null (aucune solution réelle)
delta == 0 → retourne une seule racine réelle
delta > 0 → retourne deux racines réelles
Exercice 5 — RomanNumeral
Bug détecté

Une erreur était présente dans la condition de la boucle for.

Code incorrect :

for (int i = 0; i <= symbols.length; i++)

Correction :

for (int i = 0; i < symbols.length; i++)
Cas de tests réalisés
Vérification des bornes (1 et 3999)
Cas utilisant la notation soustractive (IV, IX, XL, etc.)
Cas avec répétitions autorisées (III, XXX)
Vérification des exceptions lorsque :
n < 1
n > 3999

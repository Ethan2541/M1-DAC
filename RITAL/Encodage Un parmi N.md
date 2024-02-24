

## Généralités

<hr>

L'encodage One-Hot est régulièrement utilisé dans les problèmes de classification afin de convertir une catégorie en entrée numérique. On utilise pour cela un vecteur où le bit correspondant à la catégorie concernée est à 1, et où les autres bits sont à 0.

L'avantage de cette représentation est l'absence de biais (toutes les valeurs sont traitées également) et la possibilité de considérer un grand nombre de catégories (susceptible d'induire le [[Fléau de la Dimension]]).


## Traitement du Langage

<hr>

En traitement du langage, il consiste à représenter un document sous la forme d'un vecteur de présence de la taille du vocabulaire V. Parfois, on retire de ce vocabulaire une liste de stopwords : des mots très fréquemment utilisés et pauvres en signification.

Alternativement, pour un document de taille N, on peut utiliser une matrice de présence (similaire à une bitmap) comportant N lignes et $|V|$ colonnes.

Cette méthode présente plusieurs désavantages :
- Données pauvres : dans le cas de la matrice notamment, on a beaucoup de 0
- Pas de taille fixe dans le cas de la matrice
- Sémantique non conservée

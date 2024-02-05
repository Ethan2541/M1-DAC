

L'algorithme KNN est un algorithme d'apprentissage automatique supervisé.
- *Optical Character Recognizer : détection de l'écriture manuscrite*
- *Notations de crédit*

Si l'on se donne une entrée $x$, alors il s'agit de trouver les $K$ plus proches voisins au sens de la distance $||\cdot||$. En régression, on attribue à $x$ la moyenne ou la médiane des variables. En classification, on prédit la classe de $x$ selon la classe majoritaire parmi ces $K$ points.

![[knn.jpg]]

Le choix de $K$ est primordial mais dépend avant tout du jeu de données. De manière générale, des petites valeurs de $K$ conduisent à des frontières de décision instables. De plus, choisir $K$ impair permet d'éviter les égalités dans les problèmes de classification empêchant de définir clairement la classe de $x$.

La [[Validation croisée]] peut aider à choisir $K$ optimal. Alternativement, on peut itérer l'algorithme pour plusieurs valeurs de $K$ et tracer le taux d'erreur en fonction de $K$.

Si cet algorithme est facile à implémenter et polyvalent, il devient plus lent à mesure que la quantité d'observations augmente. Il est de plus fortement sujet au [[Fléau de la Dimension]] puisque la distance perd son sens dans les espaces à haute dimension.



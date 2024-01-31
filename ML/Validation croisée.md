

## Définition

<hr>

La validation croisée est une méthode permettant d'évaluer la fiabilité d'un modèle. 

Cependant, cette méthode est sensible au déséquilibre de classes (cf. [[Équilibrage des classes]]). Il peut être intéressant d'utiliser des [[Courbes ROC]], des [[Courbes Précision-Rappel]], ou la métrique de [[F1 Score]] afin d'évaluer les performances d'un classifieur sur la classe minoritaire.


## K-Folds

<hr>

Dans cette variante de validation croisée, on a un paramètre $K$ généralement compris entre 5 et 10. Le principe est de découper le jeu de données en $K$ paquets, puis de réaliser l'apprentissage sur $K-1$ de ces paquets avant d'évaluer le modèle sur le dernier paque.

Il s'agit ensuite de répéter jusqu'à ce que chaque paquet ait servi à l'évaluation des performances du modèle.


## Leave-One-Out

<hr>

Cette variante est un cas extrême des K-Folds avec $K = n$ où $n$ est la taille du jeu de données. Elle est également plus appropriée dans les cas où $n$ est petit.
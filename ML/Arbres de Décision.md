

## Principe

<hr>

![[binary_decision_tree.png]]

Un arbre de décision est un outil d'aide à la décision permettant de représenter l'ensemble des résultats possibles d'une série de choix sous la forme d'un arbre.

Chaque nœud représente un test sur une dimension de notre observation $x$. L'arité d'un nœud détermine le nombre de choix possibles, et sa profondeur le nombre de choix restants. En conséquence, une feuille est un label de $\mathcal{Y}$. Ces feuilles doivent être aussi pures que possible.

En modélisant une série de tests logiques très simples, on parvient ainsi à prédire un résultat ou classifier une observation. Ces arbres sont généralement calculés automatiquement à partir d'algorithmes d'apprentissage supervisé, et sélectionnent les caractéristiques discriminantes de sorte à minimiser l'entropie (degré d'aléatoire).

Plus un arbre de décision est profond, plus le risque de [[Surapprentissage]] est élevé. En effet, en augmentant le nombre de tests statistiques, on enrichit l'ensemble de fonctions.

Les arbres de décision sont notamment utilisés lorsque les données ne sont pas linéaires, et lorsque l'interprétabilité compte plus que la performance du modèle. Pour garder des arbres intéressants, on privilégie généralement les arbres équilibrés aux peignes.
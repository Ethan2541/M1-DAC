

![[binary_decision_tree.png]]

Un arbre de décision (Random Forest) est un outil d'aide à la décision permettant de représenter l'ensemble des résultats possibles d'une série de choix sous la forme d'un arbre.

Chaque noeud représente un test sur une dimension de notre observation $x$. L'arité d'un nœud détermine le nombre de choix possibles, et sa profondeur le nombre de choix restants. En conséquence, une feuille est un label de $\mathcal{Y}$.

En modélisant une série de tests logiques très simples, on parvient ainsi à prédire un résultat ou classifier une observation. Ces arbres sont généralement calculés automatiquement à partir d'algorithmes d'apprentissage supervisé, et sélectionnent les caractéristiques discriminantes.

Les arbres de décision sont notamment utilisés lorsque les données ne sont pas linéaires, et lorsque l'interprétabilité compte plus que la performance du modèle.
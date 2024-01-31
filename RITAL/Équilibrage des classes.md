

## Définition

<hr>

L'équilibre des classes est un critère important. En règle générale, on a beaucoup plus d'exemples négatifs que positifs. Pour maximiser ses performances, le modèle va donc systématiquement rendre la classe négative.

Le modèle ainsi obtenu sera très performant mais n'aura rien appris. Pour le vérifier, on utilise d'autres outils comme les [[Courbes ROC]].


## Rééquilibrage des données

<hr>

Pour équilibrer les classes, on peut s'assurer de suréchantillonner la classe minoritaire et/ou supprimer des données de la classe majoritaire.


## Repondération de la fonction de coût

<hr>

Alternativement, on peut repondérer la fonction de coût $\Delta$ :
$$C = \sum_i \alpha_i \Delta(f(x_i), y_i)$$
où $\alpha_i = 1$ si la classe est majoritaire et $\alpha_i = \beta > 1$ si la classe est minoritaire.
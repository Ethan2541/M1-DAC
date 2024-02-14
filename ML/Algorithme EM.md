

L'algorithme Expectation-Maximization est utilisé lorsque l'on a des valeurs incomplètes MCAR (Missing Completely At Random) et que l'on souhaite maximiser une log-vraisemblance. Il repose notamment sur le cas d'égalité de l'inégalité de Jensen.

On distingue les observations $x^o$ des valeurs incomplètes ou manquantes $x^h$.

Il faut dans un premier temps initialiser les paramètres de l'algorithme : $\Theta = \Theta^0$.


## Étape Expectation

<hr>

Pour satisfaire le cas d'égalité de Jensen, on pose :
$$Q_i^{t+1} = P(x_i^h|x_i^o,\Theta)$$

On calcule ensuite :
$$\log\mathcal{L}^{t+1}(x^o,\Theta) = \sum_{i=1}^n\sum_{x_i^h\in x^h}Q_i^{t+1}(x_i^h)\log(\frac{P(x_i^o,x_i^h|\Theta)}{Q_i^{t+1}(x_i^h)})$$

En pratique, les $Q_i^t$ sont les poids des lignes du tableau auquel sont rajoutées toutes les lignes possibles vis-à-vis des valeurs de $x^h$.


## Étape Maximization

<hr>

On met ensuite à jour les paramètres :
$$\Theta^{t+1} = argmax_\Theta\log\mathcal{L}^{t+1}(x^o,\Theta)$$

Et on répète l'algorithme tant que l'on a pas convergé.

**NB :** ne pas oublier que l'on peut oublier les $Q_i^t$ dans le cas où ces derniers ne dépendent pas de $\Theta$.
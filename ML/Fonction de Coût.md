

## Définition et Propriétés

<hr>

Une fonction de coût / de perte est une mesure de la performance d'un modèle, permettant de quantifier les différences entre la réalité et ses prédictions.

De telles fonctions sont généralement choisies :
- Convexes : pour garantir l'existence d'un minimum global
- Régulières (différentiables) : même si ce n'est pas grave qu'elles ne soient pas différentiables en tout point


## Types de Fonctions de Coût

<hr>

Plusieurs fonctions de perte sont utilisées en apprentissage automatique car certaines conviennent mieux que d'autre selon les algorithmes appliqués.

### 0-1 Loss

La fonction 0-1 loss détermine binairement si la prédiction est correcte ou non :
$$l(y,\hat{y}) = [y = \hat{y}]$$
Cette fonction permet ainsi de compter le nombre de classifications correctes.

### Hinge Loss

Cette fonction est communément utilisée pour les modèles du type [[Support Vector Machine]] ou [[Perceptron]].
$$l(y,w) = \max \{0, \alpha + 1 - yw^tx\}$$
où $\alpha$ est une marge permettant de mieux séparer les valeurs nulles des valeurs non nulles.

### Cross Entropy

Soit $p$ est la distribution de référence, et $q$ la distribution des prédictions d'un modèle. L'entropie croisée se définit comme :
$$H(p,q) = -\sum_y p(x) \log(q(x))$$

### Binary Cross Entropy

Plus particulièrement, l'entropie croisée binaire, se calcule comme la vraisemblance négative en régression logistique de $y|x$.
$$l(y,w) = -y\log(\sigma(f_w(x))) - (1-y)\log(1-\sigma(f_w(x)))$$

Dans ce cas, $p$ est la probabilité (paramètre d'une binomiale) que $x$ appartienne à la région correspondant à la classe $y$, et $q$ la prédiction de $x$ : $\sigma(f_w(x))$.

### Mean Squared Error

La MSE est une fonction de coût très couramment utilisé dans les problèmes de régression, mais aussi dans les problèmes de classification normalisés entre $0$ et $1$.
$$l(y,\hat{y}) = \sum_{i=1}^N(y_i-\hat{y})^2$$
Elle n'est cependant pas adaptée dans le cas où les valeurs prédites sont très éloignées des valeurs à atteindre, ce qui est régulièrement le cas en classification. Elle n'est également pas utilisé en apprentissage profond en classification multi-classes car elle lisse plus les sorties qu'elle ne maximise la sortie correspondante à la classe à prédire.
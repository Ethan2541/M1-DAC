

## Principe

<hr>

On se donne une sortie prédite $\hat{y}$ et la sortie attendue $y$. La [[Fonction de Coût]] en sortie du réseau nous permet de déterminer l'importance d'augmenter / diminuer plus ou moins intensément chaque sortie.

Le gradient de la [[Fonction de Coût]] par rapport aux poids $\nabla_wC$ donne une information sur l'impact de chaque dimension de $w$ sur la fonction de coût.

Comme une sortie est une combinaison linéaire pondérée par une matrice de poids $W$, on peut ainsi mettre à jour les dimensions les plus importantes, notamment, dans le calcul de la fonction de coût grâce au gradient. Comme on connaît le résultat que l'on souhaite obtenir pour chaque neurone de la couche précédente, on procède récursivement, d'où l'idée de rétropropagation.

Sur un ensemble d'exemples, il s'agit finalement de moyenner les mises à jour obtenues.


## Propriétés utiles

<hr>

**Règle de la chaîne :** $\frac{\partial x}{\partial z} = \frac{\partial x}{\partial y}\frac{\partial y}{\partial z}$

**Théorème de Schwarz :** $\frac{\partial}{\partial x}\left(\frac{\partial f}{\partial y}\right) = \frac{\partial}{\partial y}\left(\frac{\partial f}{\partial x}\right)$
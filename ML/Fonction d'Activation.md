

## Définition

<hr>

Une fonction d'activation est une fonction différentiable non linéaire appliquée sur la sortie d'un nœud dans un réseau de neurones, ce qui permet de rajouter de l'expressivité et ainsi obtenir des modèles plus complexes.


## Fonctions d'Activation usuelles

<hr>

### Tangente Hyberbolique

La tangente hyperbolique $\tanh:\mathbb{R}\rightarrow[-1,1]$ est généralement préférée à la fonction sigmoïde.
$$\tanh(x) = \frac{e^x-e^{-x}}{e^x+e^{-x}}$$
Elle souffre cependant du problème de [[Disparition du Gradient]], contrairement à la fonction ReLU.

### Fonction Sigmoïde

La fonction sigmoïde $\sigma:\mathbb{R}\rightarrow[0,1]$ est un cas particulier très répandu de la fonction logistique.
$$\sigma(x) = \frac{1}{1 + e^{-x}}$$
Sa sortie peut être interprétée comme une probabilité. A l'instar de la tangente hyperbolique, elle souffre du problème de [[Disparition du Gradient]].

### Rectified Linear Unit

La fonction ReLU est très utilisée car elle permet notamment de résoudre le problème de [[Disparition du Gradient]].
$$f(x) = \max(0,x) = \frac{x+\left|x\right|}{2}$$
Elle n'est cependant pas différentiable en 0. On fixe généralement sa dérivée en 0 à 0 ou 1.

### Softmax

Cette fonction est généralement utilisée comme la dernière fonction d'activation d'un neurone. Il s'agit d'une généralisation de la fonction sigmoïde.
$$\sigma(x)_k = \frac{e^{x_k}}{\sum_{i=1}^Ke^{z_i}}$$
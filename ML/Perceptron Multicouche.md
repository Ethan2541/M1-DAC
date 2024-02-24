

## Structure

<hr>

![[1651263246889.png]]

Un perceptron multicouche est l'architecture la plus répandue de réseau de neurones :
- Couche d'entrée de dimension identique aux données
- Couches cachées dont chaque neurone est un perceptron suivi d'une [[Fonction d'Activation]]
- Couche de sortie de dimension identique aux étiquettes

Plus le réseau est profond (couches cachées nombreuses), plus le modèle sera expressif, mais aussi complexe, augmentant le risque de [[Surapprentissage]].


## Passe Avant

<hr>

Une passe avant consiste à parcourir itérativement le réseau, couche par couche. Pour une couche donnée, on calcule la sortie de chaque perceptron, combinaison linéaire des entrées pondérées par les poids associés, à laquelle on applique la fonction d'activation choisie. On poursuit ensuite jusqu'à ce qu'on arrive à la couche de sortie.

La [[Fonction de Coût]] permet de calculer l'erreur entre la vraie étiquette et celle prédite. C'est une étape importante de l'apprentissage car elle est nécessaire à la [[Rétropropagation du Gradient]].


## Vision Modulaire

<hr>

On peut voir le perceptron multicouche comme un assemblage de modules :
- **Linéaires :** combinaison linéaire des entrées pondérées par les poids
- **D'activation :** application d'une [[Fonction d'Activation]]
- **De coût :** calcul de la [[Fonction de Coût]]

Dans le cadre de la [[Rétropropagation du Gradient]], il faut calculer le gradient de la [[Fonction de Coût]] pour chaque module.

## Implémentation PyTorch

<hr>

Dans PyTorch, lorsque l'on spécifie vouloir garder les informations sur les gradients, on construit un graphe de calcul (cher en mémoire et en temps). Puis, les méthodes `forward()` et `backward()` implémentent les briques de base du perceptron multicouche.
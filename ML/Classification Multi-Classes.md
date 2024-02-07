

## Définition

<hr>

La classification multi-classes vise à déterminer l'appartenance d'une observation à une classe parmi $K > 2$ classes. Elle est dite multi-labels lorsque plusieurs étiquettes sont attendues.


## One vs Rest

<hr>

La stratégie One vs All vise à entraîner un classifieur par classe en considérant les exemples positifs comme ceux appartenant à la classe en question, et le reste des observations en exemples négatifs.

Cette méthode peut cependant conduire à un déséquilibre dans les données (cf. [[Équilibrage des classes]]).


## Cas des Réseaux de Neurones

<hr>

Dans le cas des réseaux de neurones, on retrouve $K$ neurones avant la sortie, lissés grâce à la fonction Softmax pour pouvoir comparer leurs valeurs. 

On préfère également utiliser l'entropie croisée plutôt que les moindres carrés qui ont tendance à minimiser globalement les valeurs du vecteur au lieu de se concentrer sur la maximisation de la classe attendue.

**NB :** avec PyTorch, il n'est généralement pas nécessaire d'ajouter la couche d'activation avant la sortie puisque celle-ci est directement calculée lors de l'appel multi-classes.


La régularisation est une méthode pour lutter contre le [[Fléau de la Dimension]]. Elle consiste à ajouter un coefficient à la fonction de coût $\Delta$ :
$$C = \Delta \pm \lambda ||w||_\alpha$$
Dans le cas de la maximisation de la vraisemblance, le signe est positif. Pour les moindres carrés, le signe est positif.

On distingue plusieurs types de régularisation :

- Lasso Regression $(\alpha = 1)$ : favorise les solutions "sparse" en supprimant des dimensions du vecteur d'entrée (certains coefficients sont mis à 0)

- Ridge Regression $(\alpha = 2)$ : diminue tous les poids, mais ces derniers sont rarement mis à 0 contrairement à $||\cdot||_1$. Très compatible avec les problèmes de type moindres carrés

- $\alpha = \infty$ : minimise la valeur absolue maximale des paramètres du modèle
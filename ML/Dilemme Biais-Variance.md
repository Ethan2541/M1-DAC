

## Définitions

<hr>

**Biais :** erreur due aux hypothèses simplifiées du modèle lors de la phase d'apprentissage. Plus la complexité du modèle augmente, moins ce dernier tend à être biaisé.
$$B = \mathbb{E}[\hat{f}(x) - f(x)]$$

**Variance :** erreur due à la sensibilité aux fluctuations de l'ensemble d'apprentissage. C'est la variabilité du modèle lorsqu'il est confronté à de nouvelles données. Une variance élevée peut caractériser le [[Surapprentissage]].
$$V = \mathbb{E}[(\hat{f}(x) - \mathbb{E}[\hat{f}(x)])^2]$$


## Corrélation

<hr>

Considérons que les données sont bruitées : $y_i = f(x_i) + \epsilon_i$ om $\epsilon_i$ a une moyenne nulle et une variance $\sigma^2$ (c'est l'erreur irréductible). On définit l'erreur comme :
$$\mathbb{E}[(y - \hat{f}(x))^2] = \sqrt{B^2 + V} + \sigma^2$$

Par ailleurs, la variance tend à diminuer lorsque la taille de l'ensemble d'apprentissage augmente.

Il est aussi possible d'appliquer une [[Réduction de Dimension]] ou de sélectionner des variables (features) afin de diminuer la variance tout en simplifiant le modèle.


## Notion de [[Risque]]

<hr>

En reprenant les notions de [[Risque]], on peut écrire :

- **Erreur d'estimation (biais) :** $\hat{R}^*_{n,\mathcal{F}} - R^*_\mathcal{F}$
- **Erreur d'approximation (variance) :** $R^*_\mathcal{F} - R^*$

Le biais correspond à l'erreur due à l'échantillonnage du risque sur les données observées, alors que la variance correspond au biais introduit lors du choix de l'ensemble des fonctions possibles, comparé au risque optimal.
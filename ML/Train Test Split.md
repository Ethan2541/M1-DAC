

## Procédé

<hr>

Le procédé de validation Train-Test Split permet d'évaluer les performances d'un modèle sur l'inférence de nouvelles données. Si l'on se donne un jeu de données, $q_{train}$ et $q_{test}$, le principe est de diviser le jeu de données selon les proportions respectives.

Typiquement, on retrouve couramment les proportions suivantes :
- $q_{train}\simeq 70-80\%$ 
- $q_{test}\simeq 20-30\%$

On obtient ainsi deux sous-ensembles :
- Disjoints pour diminuer le risque de surapprentissage
- Constitués aléatoirement ([[Randomisation]]) afin de représenter correctement les données initiales
qui forment une partition de l'ensemble de départ $X_{train}$ et $X_{test}$ sur lesquelles entraîner et tester le modèle.


## Cas pratiques

<hr>

Afin d'obtenir des estimations plus robustes et moins biaisées des performances du modèle, il est conseillé de répéter le processus plusieurs fois.

On découpe parfois le jeu de données en 3 pour introduire un jeu de validation avec lequel choisir le modèle parmi les candidats entraînés sur le jeu d'apprentissage (hyperparamètres, ...). Dans ce cas, le jeu de validation est formé à partir d'environ $10\%$ du jeu de données, à hauteur égale avec le jeu de test.


## Random Shuffling

<hr>

Il faut également bien prendre conscience qu'il est important de mélanger les exemples (shuffle) pour ne pas introduire de biais, à moins que le jeu de données ne soit trop grand (ce qui ralentirait la pipeline), déjà mélangé, ou arrangé de la bonne façon.

Le cas des séries temporelles est différent. On souhaite préserver la continuité des données (prédire le futur à partir du passé). On ne peut pas non plus prendre un morceau d'exemples successifs (et donc une seule période de temps) pour éviter de biaiser notre modèle.



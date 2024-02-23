

Le risque associé à une [[Fonction de Coût]] correspond à son espérance.
$$R(y_i|x) = \sum_j l(y_i,y_j)p(y_i|x)$$
Dans le cas de la 0-1 loss, le risque associé vaut $1 - p(y_i|x)$.

Le risque complet est l'intégrale de ce risque sur l'ensemble des observations.
$$R(f) = \int_\mathcal{X} R(f(x)|x)p(x)dx$$
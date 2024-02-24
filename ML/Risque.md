

Le risque associé à point, pour une [[Fonction de Coût]] $l$ correspond à son espérance.
$$R(y_i|x) = \sum_j l(y_i,y_j)p(y_i|x)$$
Dans le cas de la 0-1 loss, le risque associé vaut $1 - p(y_i|x)$.

Le risque correspond à l'espérance de la [[Fonction de Coût]] $l$ associée suivant la distribution des données observées :
$$R(f) = \int_\mathcal{X} R(f(x)|x)p(x)dx$$
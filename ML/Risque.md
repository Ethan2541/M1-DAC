

Le risque associé à point, pour une [[Fonction de Coût]] $l$, correspond à son espérance.
$$R(y_i|x) = \sum_j l(y_i,y_j)p(y_j|x)$$
Dans le cas de la 0-1 loss, le risque associé vaut $1 - p(y_i|x)$.


Le risque complet est l'espérance de la [[Fonction de Coût]] $l$ associée suivant la distribution des données observées :
$$R(f) = \int_\mathcal{X} R(f(x)|x)p(x)dx$$


Le risque correspond à l'espérance de la [[Fonction de Coût]] $l$ associée suivant la distribution des données observées $p$ :
$$R_{l,p}(f) = \int_{\mathcal{X}\times\mathcal{Y}}l(f(x),y)p(x,y)dx$$


Le risque bayésien est le risque minimum :
$$R^*_{l,p}(f) = \min_{f:\mathcal{X}\mapsto\mathcal{Y}}\int_\mathcal{X} R(f(x)|x)p(x)dx$$


Pour mesurer le risque, on calcule le risque empirique sur $n$ échantillons :
$$\hat{R}_{n,l,p}(f) = \frac{1}{n}\sum_{i=1}^n l(f(x),y)$$
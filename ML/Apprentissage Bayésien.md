

## Principe

<hr>

L'apprentissage bayésien est un ensemble d'approches notamment utilisées en classification (certaines variantes peuvent être utilisées en régression). 

L'objectif principal est de déterminer la classe d'un objet en trouvant un classifieur $f: \mathcal{X}\rightarrow\mathcal{Y}$. Ainsi, une prédiction est notée $\hat{y} = f(x)$. 

Dans le cas de la classification binaire, $\mathcal{Y} = \{y_+, y_-\}$, on peut inférer la classe d'une observation à partir de la formule de Bayes :
$$p(y|x) = \frac{p(x,y)}{p(x)} = \frac{p(x|y)p(y)}{p(x|y_+)p(y_+) + p(x|y_-)p(y_-)}$$
où $p(y|x)$ est la probabilité *a posteriori*, $p(x|y)$ est la vraisemblance de $x$ par rapport à $y$, et $p(y)$ la probabilité *a priori*.

La décision bayésienne consiste à étudier le rapport $\frac{p(y_+|x)}{p(y_-|x)}$, donc $f(x) = argmax_y \frac{p(x|y)p(y)}{p(x)}$.C'est le meilleur classifieur possible. Il est cependant limité car $p(x|y)$ est en pratique très difficile à calculer (cf. [[Estimation de densité]]).

**NB :** le dénominateur $p(x)$ n'est pas important dans le contexte de maximisation puisque $x$ est fixé.


## Naive Bayes

<hr>

Le modèle Naive Bayes est un [[Modèle Génératif]] (car il se concentre sur le calcul de la loi jointe pour déterminer la conditionnelle) dans lequel on considère qu'une observation $x\in\mathbb{R}^d$ a toutes ses dimensions indépendantes conditionnellement à la classe $y$ :
$$p(x|y) = \prod_{i=1}^dp(x_i|y)$$
On peut ensuite procéder à la résolution de la maximisation par [[Maximum de Vraisemblance]] pour un vecteur donné $x$.
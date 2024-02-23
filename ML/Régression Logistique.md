

## Principe

<hr>

Le [[Modèle Discriminatif]] de régression logistique (ou logit) est couramment utilisé pour les problèmes de classification binaire. L'objectif est de déterminer la probabilité d'une classe par rapport à un échantillon $p(y|x)$.

La régression logistique est un [[Modèle Linéaire]]. On commence tout d'abord par déterminer un classifieur linéaire $f_w$ dont l'image détermine la classe attribuée. Pour se ramener à une probabilité entre 0 et 1, on applique la fonction sigmoïde plutôt que la fonction signe qui a le désavantage d'avoir une dérivée peu informative.

La prise de décision se fait sur le critère : $p(y|x) > 0,5$.


## Fonction de Coût

<hr>

Dans le cadre de la régression logistique, on ne peut pas directement utiliser la MSE comme [[Fonction de Coût]] : avant sigmoïde, les erreurs seraient trop élevées, et après sigmoïde les erreurs seraient trop petites car on comparerait des probabilités à des labels 0 ou 1.

On préfère donc le [[Maximum de Vraisemblance]] sur la distribution conditionnelle $y|x$ (en prenant comme paramètres du modèle les poids $w$). Dans le cas de classes -1/1 :
$$p(y|x) = \sigma(f_w(x))^{\frac{1+y}{2}}(1-\sigma(f_w(x)))^{\frac{y-1}{2}}$$
$$-\log(\mathcal{L}(Y|X,w)) = -\frac{1}{N}\sum_{i=1}^N\left[\frac{1+y^{(i)}}{2}\log\left(\sigma\left(f_w\left(x^{(i)}\right)\right)\right) + \frac{y^{(i)}-1}{2}\log\left(1-\sigma\left(f_w\left(x^{(i)}\right)\right)\right)\right]$$
Cette fonction de coût, l'entropie croisée, est convexe et souvent minimisée par [[Descente de Gradient]].
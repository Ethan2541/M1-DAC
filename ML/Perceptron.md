

## Principe

<hr>

Un perceptron a pour objectif de tracer une frontière de décision entre deux classes -1/1 en déterminant une fonction linéaire $f_w(x) = \langle w,x\rangle$ non unique. La décision se base sur $\text{sgn}(f_w(x))$. Il s'agit d'un [[Modèle Linéaire]].

La correction, identique à la descente de gradient, n'a lieu que lorsque le perceptron se trompe, c'est-à-dire $yf(x) < 0$ (de façon similaire au perceptron de Rosenblatt).

La [[Fonction de Coût]] utilisée est la Hinge Loss :
$$l(f_w(x),y) = \max(0,\alpha-y\langle w,x\rangle)$$
$$\nabla_wl(f_w(x),y) = \begin{cases}0 & \text{si }y\langle w,x\rangle < 0\\-yx & \text{sinon}\end{cases}$$
$\alpha$ permet de garder une petite marge pour éviter d'être trop proche de 0, car si les données sont bruitées, on peut rapidement dépasser la frontière.

Dans le cas où les données ne sont pas linéairement séparables, on peut envisager d'ajouter une dimension supplémentaire en espérant se ramener à des données linéairement séparables. Attention toutefois au phénomène du [[Fléau de la Dimension]].


## Algorithme

<hr>

```python
w = np.random.random()
while True:
	wtmp = w
	for xi, yi in data:
		if yi*f(xi) < 0:
			w = w + alpha*yi*xi
	if (w - wtmp) < eps:
		break
```


## Convergence

<hr>

D'après le théorème de Novikoff, si les hypothèses suivantes sont vérifiées :
- $\exists R,\forall x, \|x\|\leq R$
- Les données sont linéairement séparables avec une marge $\rho$
- L'ensemble d'apprentissage est présenté au perceptron un nombre suffisant de fois

Alors l'algorithme converge après au plus $R^2/\rho^2$ itérations.
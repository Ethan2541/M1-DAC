

## Présentation

<hr>

L'algorithme de descente de gradient est utilisé pour minimiser des fonctions convexes et différentiables.

Les paramètres de cet algorithme sont :
- Le point initial $x_0$ : généralement, l'hypothèse de convexité n'est pas vérifiée globalement. Selon le point initial, on peut donc tomber sur un minimum local. Il est ainsi important d'en essayer plusieurs
- Le pas d'apprentissage $\alpha$ : s'il est trop grand on peut ne jamais converger, s'il est trop petit la convergence peut être longue ou l'on peut passer en-dessous du seuil de convergence en étant loin du minimum
- Le seuil de convergence $\epsilon$ permettant de mettre déterminer si l'algorithme a convergé


## Intuition

<hr>

D'après le développement de Taylor, pour une fonction $f$ différentiable en $w_0$ :
$$f(w) = f(w_0) + \nabla_wf(w_0)(w-w_0) + O(\|w-w_0\|^2)$$
On en déduit qu'en bougeant de $h$ dans la direction $u$, on a :
$$f(w_0 + \alpha u) - f(w_0) = \alpha\nabla_wf(w_0)u + \alpha^2O(1)$$
Pour faire décroître $f$, il faut donc minimiser $\nabla_wf(w_0)u$.

On choisit de bouger dans la direction du gradient d'où $u = - \frac{\nabla_wf(w_0)}{\|\nabla_wf(w_0)\|}$.


## Algorithme

<hr>

```python
w = np.random.random()
while True:
	wtmp = w
	# Choisir les x, y selon la variante batch / stochastique / mini-batch
	grad_f = gradient(f, x, y)
	w = w - alpha*grad_f
	if (w - wtmp) < eps:
		break
```


## Variantes

<hr>

- **Hors-ligne (batch) :** pour chaque époque, la correction se fait à partir de l'ensemble des points, assurant stabilité et rapidité

- **En ligne (stochastique) :** une époque correspond à une correction à partir d'un exemple tiré au hasard. Cela permet une meilleure tolérance au bruit

- **Hybride (mini-batch) :** une correction est faite à partir d'un sous-ensemble d'exemples
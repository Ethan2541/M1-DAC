

## Loi Faible des Grands Nombres

<hr>

Soit une suite de variables aléatoires indépendantes et identiquement distribuées $(X_i)_{i\in\mathbb{N}}$ d'espérance finie $\mu$. Alors la moyenne empirique converge en probabilité vers l'espérance :
$$\forall\epsilon\gt 0, \lim_{n\rightarrow +\infty}\mathbb{P}(|\bar{X_n} - \mu|\gt\epsilon) = 0$$
Autrement dit,  la probabilité que la moyenne empirique s'éloigne de l'espérance d'un petit montant $\epsilon$ devient de plus en plus faible à mesure que la taille de l'échantillon $n$ augmente. C'est donc un estimateur convergent de l'espérance.


## Loi Forte des Grands Nombres

<hr>

Soit une suite de variables aléatoires indépendantes et identiquement distribuées $(X_i)_{i\in\mathbb{N}}$ d'espérance finie. Alors la moyenne empirique converge presque sûrement vers l'espérance :
$$\mathbb{P}(\lim_{n\rightarrow +\infty} \bar{X_n} = \mathbb{E}[X]) = 1$$
Autrement dit, la probabilité que la moyenne empirique converge vers l'espérance théorique est égale à 1. C'est un estimateur fortement convergent de l'espérance.

La loi des grands nombres justifie ainsi l'utilisation de la moyenne empirique comme estimateur de l'espérance dans les algorithmes d'apprentissage.
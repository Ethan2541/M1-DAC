

## Test d'Hypothèse

<hr>

On suppose la taille de l'échantillon connue égale à $n > 30$, et on se donne deux hypothèses $H_0$ et $H_1$ portant sur un paramètre du modèle. Pour faciliter les calculs, on s'efforce de choisir $H_0$ simple (condition d'égalité).

1. On possède $n$ variables aléatoires d'espérance $\mu$ et de variance $\sigma^2$. Par le [[Théorème Central Limite]], la moyenne empirique $\bar{X}$ suit une loi normale de paramètres $(\mu,(\frac{\sigma}{\sqrt{n}})^2)$.
2. Le risque est $\alpha = p(\text{rejet } H_0|H_0) = p(\bar{X}>c|\bar{X}\sim\mathcal{N}(\mu, (\frac{\sigma}{\sqrt{n}})^2)$
3. Avec la table de la loi normale, on détermine la valeur de $c$ puis on établit une règle de décision basée sur $c$ et les paramètres de l'échantillon.
4. En spécialisant notre hypothèse $H_1$ (se ramener à une condition d'égalité) sur plusieurs valeurs de paramètres, on peut établir la courbe de puissance $1-\beta = p(\text{accepter} H_1 | H_1)$

**NB :** ce n'est pas tant affirmer qu'une hypothèse est vérifiée, mais plutôt qu'on ne peut la rejeter.


## Test d'Ajustement

<hr>

Les tests d'ajustement permettent de vérifier à partir d'un échantillon si une distribution suit une certaine loi.

1. On établit le tableau de contingence attendu si la distribution suivait la loi
2. On compare les effectifs théoriques $\nu_i$ des effectifs réels $n_i$ en calculant $A = \sum_{i=1}^n\frac{(n_i-\nu_i)^2}{\nu_i}$
3. On se réfère à la loi du $\chi_2^{d}$ où $d$ est le nombre de degrés de liberté du problème. Si $A > \chi_2^{DDL}$, on rejette l'hypothèse.


## Test d'Indépendance

<hr>

Les tests d'indépendance permettent de déterminer, lorsque la taille de l'échantillon est très élevée, si deux variables aléatoires sont indépendantes.

1. À partir du tableau de contingence de la loi jointe $(n_{i,j})$, calculer la somme $L_i$ sur chaque ligne $i$, et la somme $C_j$ sur chaque colonne $j$. Notons $N$ la somme totale de la loi jointe.
2. Établir le tableau de contingence $(\nu_{i,j})$ où $\nu_{i,j} = \frac{L_i\times C_j}{N}$
3. Calculer $A = \sum_{i=1}^n\frac{(n_i-\nu_i)^2}{\nu_i}$ et le comparer à $\chi_2^{d}$ où $d = (n_{lignes} - 1)\times(n_{cols} - 1)$
4. Si $A > \chi_2^{d}$, on rejette l'hypothèse d'indépendance.


Soit une suite de variables aléatoires $(X_i)_{i\in\{1,...,n\}}$ admettant un moment d'ordre 2. Le théorème central limite établit la convergence de la somme $S_n = \sum_{i=1}^{n}X_i$ vers une loi normale.

En particulier, si les variables sont indépendantes et identiquement distribuées, de moyenne $\mu$ et de variance $\sigma^2$, on a :
$$Y_n = \frac{S_n - \mu}{\sigma\sqrt{n}} \sim \mathcal{N}(0,1)$$
En pratique, ce théorème est vérifié pour $n\gt 30$. À noter cependant que l'écart entre $Y_n$ et $\mathcal{N}(0,1)$ diminue à mesure que $n$ augmente.
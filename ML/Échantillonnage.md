

L’échantillonnage (méthodes de Monte Carlo) propose une simulation stochastique pour le calcul d’intégrales (ou d’équations différentielles). Soient $N$ variables aléatoires $X_i$ indépendantes et identiquement distribuées :
$$
E_P(f) = \int f(x)\cdot P(x)dx\approx\frac{1}{N}\sum_{i\leq N}f(X_i)
$$

Le Rejection Sampling est une technique d'échantillonnage qui consiste en tirer un point $x_0$ aléatoirement selon une loi $Q$ vérifiant $\forall x, cQ(x)\geq P(x)$. Selon la valeur du ratio $\frac{P(x_0)}{cQ(x_0)}$, on accepte ou on rejette le point $x_0$.

C'est une technique très utile lorsque l'échantillonnage direct est impossible. Elle est cependant limitée par son efficacité : beaucoup d'échantillons sont susceptibles d'être rejetés si $cQ(x)$ est beaucoup plus grand que $P(x)$. Il est de plus difficile d'estimer $c$ lorsque les données ont une dimension élevée.
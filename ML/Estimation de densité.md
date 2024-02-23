

## Principe

<hr>

L'estimation de densité est une technique utilisée pour modéliser une distribution de probabilité. Elle peut ainsi être utile pour estimer des distributions difficilement obtenables (cf. [[Apprentissage Bayésien]]).


## Première approche

<hr>

Une première méthode pour estimer la densité de probabilité $p_\mathcal{B}$ d'une région $\mathcal{B}$ de volume $V$ en fonction de $k$ échantillons observés dans cette zone parmi $n$ est de construire une variable aléatoire $X$ comptant le nombre de points dans $\mathcal{B}$. Dans la suite, on suppose $p_\mathcal{B}$ constante.

Cette variable aléatoire suit une loi binomiale de paramètres $(N, \mathbb{P}(x\in\mathcal{B}))$ et d'espérance $\mathbb{E}\left[X\right] = N\times\mathbb{P}(x\in\mathcal{B})$.

On a donc $\mathbb{P}(x\in\mathcal{B}) = \int_\mathcal{B}p_\mathcal{B}(x)dx = p_\mathcal{B}\times V = \frac{\mathbb{E}\left[X\right]}{N}\Rightarrow p_\mathcal{B} = \frac{k}{NV}$.

**NB :** on considère souvent $\mathcal{B}$ comme un hypercube de côté $\sigma$ et de dimension $d$. Dans ce cas, le volume est $V = \sigma^d$.


## Estimation par histogramme

<hr>

En discrétisant l'espace des observations (par exemple sous forme d'une grille 2D si $x\in\mathbb{R}^2$), on peut calculer les fréquences des points observés et les utiliser pour estimer $\mathbb{P}(x\in\mathcal{D})$. Comme l'appartenance d'un point est très sensible aux effets de bords, les résultats de cette méthode peuvent varier drastiquement en changeant la façon dont est discrétisé l'espace.

Cette méthode n'est pas adaptée pour les espaces de haute dimension car la discrétisation est trop coûteuse.


## Estimation par noyau

<hr>

La méthode de Parzen-Rosenblatt propose une implémentation de l'estimation par noyau. Elle repose sur la création de fenêtres de taille $\sigma$ autour des points observés. On perd ainsi les effets de bord.
$$\hat{f_\sigma}(x) = \frac{1}{NV}\sum_{i=1}^N\phi\left(\frac{x-x_i}{\sigma}\right)$$
où $\phi$ est un [[Noyau]] qui correspond à un genre de lissage permettant de tenir davantage compte des données proches que des données éloignées. En particulier, $\lim_{x\rightarrow +\infty} = 0$. Un exemple très courant est le noyau gaussien :
$$\phi(x) = \frac{1}{\sqrt{2\pi}}e^{-\frac{1}{2}x^2}$$
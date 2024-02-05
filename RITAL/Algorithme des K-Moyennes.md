

## Principe

<hr>

![[kmoyennes.png]]

L'algorithme des K-Moyennes est un algorithme d'apprentissage automatique non supervisé dont l'objectif est de diviser l'ensemble des observations en $K$ partitions.

L'étape initiale est d'assigner aléatoirement $K$ centroïdes dans l'espace :
- **Méthode de Forgy :** choisir aléatoirement $K$ observations du jeu de données
- **Partitionnement aléatoire :** assigner aléatoirement un cluster à chaque observation avant de calculer les centroïdes

Il s'agit ensuite de déterminer l'appartenance des observations selon leur proximité (au sens de la distance $||\cdot||$) par rapport à chacun de ces centroïdes. Après avoir obtenu nos $K$ partitions, on redétermine les centroïdes de chaque cluster (moyenne des observations du cluster), puis on répète jusqu'à convergence de l'algorithme (les centroïdes sont identiques d'un tour à l'autre).

L'avantage de cet algorithme est qu'il converge souvent très rapidement (souvent $\leq 10$ itérations) mais les résultats peuvent être très différents selon le choix initial des centroïdes. Il nécessite également d'avoir une idée du nombre $K$ de partitions.


## Choix de $K$

<hr>

**Méthode du coude :** choisir $K$ comme le point d'inflexion de la courbe $\sum_{i=1}^N ||x - \mu(x)||^2$ où $\mu(x)$ est le barycentre du cluster de $x$

**Score de silhouette :** à utiliser dans les cas où la méthode du coude produit des résultats ambigus. Le but est de maximiser le score, donc être le plus proche possible de $+1$. Pour un point donné $i$ :
$$
\begin{equation}
  s(i) =
    \begin{cases}
      \frac{b(i) - a(i)}{\max{\{a(i), b(i)\}}} & \text{si $|C_i| > 1$}\\
      0 & \text{sinon}
    \end{cases}       
\end{equation}
$$
où $a(i) = \frac{1}{|C_i|-1}\sum_{j\in C_i\setminus\{i\}} d(i,j)$, et $b(i) = \min_{j\neq i}\frac{1}{|C_j|}\sum_{k\in C_j}d(i,k)$ sont respectivement la mesure de similarité de $i$ par rapport à sa propre classe, et la mesure de dissimilarité de $i$ par rapport aux points des autres clusters. En particulier, si $i$ a été correctement assigné, $a(i) < b(i)$.


La divergence de Kullback-Leibler est une mesure de dissimilarité positive, non symétrique, entre deux distributions de probabilités, qu'elles soient continues ou discrètes.
$$D_{KL}(P||Q) = 
\begin{cases}
	\sum_{x\in\mathcal{X}}P(x)\log\frac{P(x)}{Q(x)} & \text{si P, Q discretes}\\
	\int_{\mathcal{X}}p(x)\log\frac{p(x)}{q(x)}dx & \text{si P, Q continues}
\end{cases}$$

La divergence de Kullback-Leibler est souvent apparentée à une distance sans en être une (il manque les axiomes de symétrie et d'inégalité triangulaire). En particulier, plus elle est élevée, plus les distributions $P$ et $Q$ sont différentes.

Elle est notamment utilisée pour :
- **La détection de changements :** comparaison d'une distribution avant et après un évènement donné
- **La comparaison de documents :** en choisissant $P$ comme la distribution des mots au sein d'un document $d_i$ et $Q$ celle d'un document $d_j\neq d_i$
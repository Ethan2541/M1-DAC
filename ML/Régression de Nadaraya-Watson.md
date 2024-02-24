

Intuitivement, on cherche à compter les distributions $p(X|Y=y)$ pour toutes les valeurs possibles de $y$ avant de les comparer entre eux. On termine en normalisant par le nombre de points dans l'ensemble des données.

On définit le classifieur $m$ comme l'espérance conditionnelle de $Y$ pour $X=x$ donné.
$$m(x) = \int_\mathcal{Y}yp(y|x)dy = \frac{\int_{\mathcal{Y}}yp(x,y)dy}{p(x)}$$

A partir des propriétés des noyaux multivariés, on a :
$$m(x) = \frac{\int_\mathcal{Y}y\frac{1}{N}\sum_{i=1}^NK_{\sigma_1}(x-x_i)K_{\sigma_2}(y-y_i)}{p(x)}$$

Par linéarité de l'intégrale et en posant $\int_\mathcal{Y}yK_{\sigma_2}(y-y_i) = y_i$ (car la fenêtre du noyau est centrée sur $y_i$), on retrouve l'estimateur de Nadaraya-Watson.
$$m(x) = \frac{\sum_{i=1}^Ny_iK(x_i-x)}{\sum_{i=1}^NK(x_i-x)}$$
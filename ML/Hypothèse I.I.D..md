

Des variables $X_i$ sont indépendantes et identiquement distribuées si elles sont indépendantes deux-à-deux, et si elles suivent la même loi :
$$
\begin{equation}
    \begin{cases}
        \forall i\neq j, X_i\perp X_j \\
        \forall i, X_i\thicksim \mathcal{L}(\theta)
    \end{cases}
\end{equation}
$$


Cette hypothèse permet de simplifier de nombreux calculs (construction de modèles, échantillonnage, ...).

Cependant, elle est invalide dans certains cas, notamment :
- Séries temporelles : les données sont souvent dépendantes de celles antérieures et/ou postérieures
- Clusters : dans ces groupes, les données tendent à partager des similarités
- [[Biais de Sélection]] : les données ne sont pas choisies aléatoirement et sont implicitement corrélées

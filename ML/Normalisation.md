

## Objectif

<hr>

La normalisation est une technique dont le but est de transformer les caractéristiques sur une échelle similaire, et ainsi améliorer les performances et la stabilité du modèle.


## Techniques de normalisation

<hr>

### Min-Max Scaling

Le scaling permet de convertir une plage de valeurs, dont le minimum et le maximum sont connus, en une plage standard entre 0 et 1 :
$$x' = \frac{x - x_{min}}{x_{max} - x_{min}}$$
Les données sont alors réparties plus ou moins uniformément.

### Clipping

Le clipping consiste à seuiller les données selon des bornes $s_{min}$ et $s_{max}$ ingénieusement choisies. Cela permet notamment d'éliminer des outliers.

### Log Scaling

Le Log Scaling est utilisé lorsque la distribution est asymétrique (skewness) : de nombreuses valeurs sont présentes d'un côté par opposition à l'autre côté.

### Standardisation / Normalisation Z Score

La standardisation permet de centrer une distribution (de préférence supposée normale) autour de 0 et de fixer sa variance à 1, facilitant ainsi la visualisation et les calculs.
$$Z = \frac{X - \mu}{\sigma}$$
En particulier, le Z Score (cote Z) est une métrique indiquant de combien d'écarts-types $\sigma$, une donnée est éloignée de la moyenne $\mu$ de sa distribution.

Cette technique est utile lorsque la distribution est connue (moyenne et variance), et lorsque le modèle (notamment [[Méthode des K-plus-proches-voisins]], [[Algorithme des K-Moyennes]], ...) comporte plusieurs caractéristiques (pour la mise à l'échelle).
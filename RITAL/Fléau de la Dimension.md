

## Généralités

<hr>

![[hughes.png]]

Le fléau de la dimension, également appelé Phénomène de Hughes, désigne les phénomènes liés aux études portant sur des données de dimension élevée.

Pour atténuer ce fléau, un moyen efficace est la [[Régularisation Laplacienne]].


## Conséquences

<hr>

**[[Data Sparsity]] :** dans des espaces à haute dimension, le nombre d'exemples nécessaire pour couvrir l'espace augmente, ce qui rend difficile la reconnaissance de patterns.

**Difficultés à visualiser :** visualiser des espaces à haute dimension est complexe, et projeter les données sur des espaces de dimension moins élevée peut induire une perte d'informations.

**Distorsion des métriques de distance :** dans les espaces de haute dimension, les écarts de distance sont négligeables. Des algorithmes comme la [[Algorithme des K-plus-proches-voisins]] sont ainsi susceptibles de mal fonctionner.

**[[Surapprentissage]] :** le modèle a des difficultés à généraliser, en partie à cause de la misère de données.
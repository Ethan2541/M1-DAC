
## Généralités

<hr>

On parle de données parcimonieuses lorsque l'on manque de données ou que la plupart des valeurs sont absentes.

Cela se produit notamment lorsque la dimension du problème est très élevée (cf. [[Fléau de la Dimension]]).


## Conséquences

<hr>

**Complexité :** les complexités spatiale et temporelle augmentent car on doit stocker les valeurs nulles / manquantes qui n'apportent aucune information, et l'entraînement sera plus long

**Problème du Cold Start :** dans les systèmes de recommandations, lorsqu'un nouvel utilisateur s'inscrit ou qu'un nouveau produit est mis en ligne, le manque d'informations peut gêner le bon fonctionnement du système de recommandations.

**[[Surapprentissage]] :** il est difficile d'inférer des propriétés sur le modèle lorsque les données sont insuffisantes car le modèle est plus susceptible de prendre en compte le bruit.
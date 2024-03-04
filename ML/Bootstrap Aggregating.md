

Le bagging est une méthode d'[[Apprentissage Ensembliste]] permettant d'apprendre $N$ modèles différents sur plusieurs régions d'un ensemble d'apprentissage $E$ de taille $N$. Contrairement au [[Boosting]], le bagging est utilisé lorsque la variance est élevée, et que le biais est faible.

Le principe est de constituer $N$ ensembles [[Bootstrap]] $E_i$ et d'apprendre 1 classifieur sur chacun de ces nouveaux ensembles d'apprentissage. La prédiction finale est une moyenne des prédictions de chaque classifieur.
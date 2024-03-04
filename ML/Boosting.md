

En [[Apprentissage Ensembliste]], l'intuition derrière le boosting est de partir d'un classifieur faible (peu expressif, ses performances sont à peine meilleures que le modèle aléatoire), et de corriger progressivement les erreurs que l'on remarque. Les algorithmes les plus utilisés de boosting sont AdaBoost, XGboost et Light GBM.

Les erreurs de chaque classifieur sont déterminées à partir d'ensembles d'exemples différents. En agrégeant tous les classifieurs faibles avec une somme pondérée, on obtient un classifieur fort performant.

Comparées au [[Bootstrap Aggregating]], les méthodes de boosting sont utilisées lorsque la variance est faible et le biais élevé.
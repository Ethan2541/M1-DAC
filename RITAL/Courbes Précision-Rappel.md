

## Notations

<hr>

**Précision :** taux de prédictions correctes parmi les prédictions positives
$$P = \frac{TP}{TP + FP}$$

**Rappel (Sensibilité) :** taux de détection, taux d'individus positifs détectés
$$R = \frac{TP}{TP + FN}$$


## Courbes Précision-Rappel et AUC

<hr>

Les courbes de précision-rappel permettent d'évaluer le compromis entre la précision du modèle et sa capacité de détection pour différents seuils de classification. L'AUC, l'aire sous la courbe, mesure ce compromis. Plus l'AUC est proche de 1, plus le modèle détecte un grand nombre de cas positifs sans se tromper.

Pour comparer avec les [[Courbes ROC]], si ces deux modèles de courbes permettent d'évaluer les performances d'un modèle, les courbes de Précision-Rappel sont plus adaptés lorsque les classes sont déséquilibrées.
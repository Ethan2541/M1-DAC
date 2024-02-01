

## Notations

<hr>

**Taux de vrais positifs (Sensibilité) :** capacité à détecter les cas positifs
$$TPR = \frac{TP}{TP + FN}$$

**Taux de faux positifs (Antispécificité) :** échec de reconnaissance des cas négatifs
$$FPR = \frac{FP}{FP + TN}$$


## Courbes ROC et AUC

<hr>

Le principe de la courbe ROC est de déterminer le taux de vrais positifs et le taux de faux positifs pour différentes valeurs de seuils.

![[courbesroc.png]]

L'AUC (Area Under Curve) représente l'aire sous la courbe (inférieure à 1). Plus elle est proche de 1, plus le modèle est capable de distinguer les classes positives des classes négatives.

Attention, cependant, cette métrique peut être sujette à confusion dans le cas où les classes sont fortement déséquilibrées (cf. [[Équilibrage des classes]]).
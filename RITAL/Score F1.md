

Le Score F1 est une métrique permettant d'évaluer la performance des modèles de classification (2 classes ou plus), notamment lorsque les données sont fortement déséquilibrées.

Le Score F1 est défini comme la moyenne harmonique de la précision et du rappel (cf. [[Courbes Précision-Rappel]]). Il compare donc les prédictions positives correctes aux erreurs faites par le modèle :
$$F1Score = 2\frac{PR}{P + R} = \frac{TP}{TP + \frac{1}{2}(FN + FP)}$$

En particulier, un Score F1 peu élevé indique que le modèle manque beaucoup de positifs (rappel faible) ou identifie des négatifs comme positifs (précision faible).
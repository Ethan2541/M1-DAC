

Un modèle linéaire est un modèle qui fait l'hypothèse que les labels $Y$ sont linéaires par rapport aux observations $X$. Dans ce cas, le classifieur $f_w$ peut s'écrire sous la forme :
$$f_w(x) = \langle w,x\rangle + w_0$$
où $w_0$ est le biais du modèle. Il est parfois inclus dans le vecteur $w$ quitte à enrichir la structure des observations (en ajoutant une dimension à 1).
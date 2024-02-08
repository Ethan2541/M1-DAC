

## Maximum de Vraisemblance

<hr>

Soit un échantillon d'observations $x\in\mathbb{R}^{N\times d}$, et $\theta$ les paramètres du modèle considéré. On note $\mathcal{L}(x,\theta) = p(x|\theta)$ la vraisemblance.

En faisant l'hypothèse que les échantillons de $x$ sont mutuellement indépendantes (cf. [[Hypothèse I.I.D.]]), on a :
$$\mathcal{L}(x,\theta) = \prod_{i=1}^Np(x_i|\theta)$$
Et en passant au logarithme, la log-vraisemblance (parfois multipliée par $-1$) vérifie :
$$\mathcal{LL}(x,\theta) = \sum_{i=1}^N\log(p(x_i|\theta))$$
En déterminant le point critique (à supposer que la fonction soit convexe), on peut maximiser la log-vraisemblance, et donc la vraisemblance.

**NB :** les constantes multiplicatives ne sont donc d'aucune aide dans le calcul de l'argmax.


## Maximum A Posteriori

<hr>

On suppose de connaître également la probabilité *a priori* $p(\theta)$. Dans ce cas :
$$p(\theta|x) = p(x|\theta)p(\theta)$$
Et on peut procéder comme pour le maximum de vraisemblance.


## Lois a priori usuelles

<hr>

**Loi Gamma $\Gamma(\alpha,\beta)$ :** $f(x;\alpha;\beta) = x^{\alpha-1}\frac{\beta^\alpha e^{-\beta x}}{\Gamma(\alpha)}$

**Loi Beta :** $B(\alpha, \beta) = \frac{\Gamma(\alpha)\Gamma(\beta)}{\Gamma(\alpha+\beta)}$ et $f(x;\alpha;\beta) = Cx^{\alpha-1}(1-x)^{\beta-1}$
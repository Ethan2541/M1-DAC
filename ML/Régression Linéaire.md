

## Présentation

<hr>

L'objectif de ce [[Modèle Discriminatif]] (pas d'hypothèses sur les distributions de $X$ et $Y$) est de déterminer une application linéaire $f_w$ en faisant l'hypothèse :
$$Y\sim X + \epsilon$$
où $\epsilon$ est une variable aléatoire représentant du bruit gaussien d'espérance nulle et de variance $\sigma^2$.

En moyenne, les sorties sont linéaires par rapport aux entrées :
$$\mathbb{E}[y|x] = w_0 + \sum_{i=1}^dw_ix_i$$
La loi $y|x$ suit donc une loi gaussienne $\mathcal{N}(f_w(x),\sigma^2)$.


## Application

<hr>

En pratique, on cherche à minimiser l'espérance d'une [[Fonction de Coût]] (souvent la MSE). Comme les échantillons sont généralement supposés indépendants et identiquement distribués, par [[Échantillonnage]], cela revient à minimiser la moyenne empirique sur notre échantillon.
$$\arg\min_w\mathbb{E}[l(f_w(x),y)] = \int_{x,y}l\left(f_w(x),y\right)p(x,y)dxdy$$
$$\Leftrightarrow\arg\min_w\frac{1}{N}\sum_{i=1}^Nl\left(f_w\left(x^{(i)}\right),y^{(i)}\right)$$
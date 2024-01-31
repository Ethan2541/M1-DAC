
## Généralités

<hr>

Le modèle Sac de Mots est utile pour la classification de documents, mais peut aussi être appliqué à la classification d'images.

Avantages :
* Facile à implémenter
* Léger et rapide
* Opportunité d'enrichir le modèle

Inconvénients :
- Perte de la structure de la phrase
- Certaines tâches sont impossibles : génération de textes, ...
- Écart sémantique : tous les mots sont orthogonaux deux-à-deux


## Fonctionnement

<hr>

![[sacdemots.png]]

### Tokenisation

La tokenisation est une étape de pré-traitement qui consiste à découper les données textuelles en une série de tokens (lettres, mots, [[N-Grams]], ...)

### Encodage

Un document est représenté par l'histogramme des occurrences des mots qui le composent, sous la forme d'un vecteur de comptage, de taille fixe $|V|$.

Dans certains cas, il est plus intéressant d'utiliser un vecteur binaire et ainsi ignorer la fréquence des termes en se ramenant à l'[[Encodage One-Hot]].

### Normalisations

Première normalisation par rapport à la fréquence des termes :
$$\forall i, \sum_{k}d_{ik}^{(tf)} = 1$$

Seconde normalisation pour diminuer l'attention portée sur les stopwords en multipliant par l'inverse de la fréquence d'apparition des termes dans l'ensemble des documents :
$$d_{ik}^{tfidf} = d_{ik}^{tf}\log\frac{|C|}{|\{d | t_k\in d|\}}$$
### Algorithmes

Outre l'apprentissage bayésien, on peut utiliser un classifieur linéaire bi-classe (que l'on peut étendre avec la méthode Un-Contre-Tous).

Dans ce cas, il faut définir une fonction de décision linéaire :
- Simple : $f(x_i) = \sum_j x_{ij}w_j$
- Régression logistique : $f(x_i) = \frac{1}{1 + e^{-(x_iw+b)}}$

Formulation de la fonction de coût :
- Maximisation de la vraisemblance : $L_{log} = \sum_{i=1}^{N}y_i\log(f(x_i)) + (1-y_i)\log(1-f(x_i))$
- Moindres carrés : $C = \sum_{i=1}^{N}(f(x_i)-y_i)^2$
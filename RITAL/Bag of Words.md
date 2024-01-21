
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

### Algorithmes

Naive Bayes

Décision linéaire simple

Régression logistique

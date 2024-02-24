

La disparition du gradient est un problème que l'on rencontre fréquemment dans les méthodes utilisant la [[Rétropropagation du Gradient]]. Lorsque le gradient devient trop petit, la phase d'apprentissage ralentit voire s'arrête.

La cause principale de ce problème est l'utilisation d'une [[Fonction d'Activation]] dont la dérivée s'annule rapidement. Ce phénomène est le plus visible dans les réseaux les plus profonds, où la règle de chaînage fait que l'on multiplie les dérivées entre elles, ce qui diminue davantage le gradient.
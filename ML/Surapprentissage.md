

## Définition

<hr>

Le surapprentissage / sur-ajustement / surinterprétation est un phénomène qui se produit en apprentissage automatique lorsqu'un modèle apprend trop en détails les données d'entraînement et s'adapte au bruit du jeu d'apprentissage.

Dans cette éventualité, le modèle perd sa capacité à généraliser et inférer sur de nouvelles données de test, ce qui se traduit par de mauvaises performances lorsqu'il est confronté à de nouvelles observations.

![[surapprentissage.png]]

*Prenons un étudiant qui révise pour son examen. S'il est attentif et s'il comprend bien les concepts étudiés, il sera capable de répondre aux questions de l'examen avec succès. Mais s'il se contente de mémoriser par cœur les réponses aux annales, il aura du mal à répondre à des questions légèrement différentes.*

Il s'oppose conceptuellement au sous-apprentissage qui se produit lorsque le modèle est trop simpliste ou pas suffisamment entraîné. Dans ce cas, le modèle présente de mauvaises performances durant la phase d'apprentissage.


## Causes du surapprentissage

<hr>

**Complexité du modèle :** un modèle avec de nombreux paramètres (haute dimension) est plus susceptible de souffrir de surapprentissage
- *Des polynômes de degré élevés pourront par exemple passer par chaque point du jeu d'entraînement alors qu'une droite pourrait constituer une meilleure approximation du modèle*

**[[Données Parcimonieuses]] :** le manque de données conduit le modèle à porter davantage son attention sur le bruit de l'ensemble d'entraînement

**[[Fonction de Coût]] :** un mauvais choix de la fonction de coût pour mesurer l'erreur peut inciter le modèle à sur-ajuster les données d'entraînement


## Solutions

<hr>

Pour détecter le surapprentissage, on utilise souvent la [[Validation croisée]].

Les solutions les plus courantes pour l'éviter sont d'augmenter la taille de l'ensemble d'apprentissage, diminuer les paramètres du modèle, ou encore la [[Régularisation Laplacienne]]. 


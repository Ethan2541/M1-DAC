
## Qu'est-ce que la Data Science ?

<hr>

![[DALAS/Images/Relations-entre-donnee-information-et-connaissance.png]]

* **Donnée :** mesure brute $\rightarrow$ *Un thermomètre mesure la valeur 40*
* **Information :** donnée remise en contexte $\rightarrow$ *Température de 40°C*
* **Connaissance :** information assimilée $\rightarrow$ *40°C correspond à de la fièvre pour un humain*

$\Rightarrow$ L'objectif de la Data Science est de mettre une connaissance sur une donnée


## Procédé global

<hr>

![[DALAS/Images/Data-Science-Process.svg]]
### Identification du problème

* Données existantes (attention à la législation)
* Applications possibles et leurs difficultés / délais
* Objectifs SMART (Spécifiques Mesurables Atteignables Réalistes Temporels)


### Acquisition des données

* [[Web Scrapping]]
* Données dispersées sur plusieurs fichiers
* Formats hétérogènes


### Préparation des données

* Unifier les labels
* Fusionner les données
* Supprimer les doublons
* Traiter les valeurs manquantes

**Il faut aussi faire attention aux biais !**
- *ChatGPT s'étant entraîné sur des données américaines, les lettres de recommandation qu'il produit ont un style distinct de celui propre aux locuteurs français.*


### Planification et construction du modèle

* Comprendre les données et identifier un modèle adéquat
* Split les jeux de données entraînement / test, et annoter les données si besoin
* Évaluation des performances
	* Comparaison de modèles
	* Exemples sur lesquels le modèle échoue
* Construction du modèle
	* Entraînement
	* Paramétrage : hyperparamètres, ...
	* Fine Tuning : entraînement sur d'autres jeux de données)

Le but n'est pas de tester tous les modèles possibles car cela peut demander du temps et des ressources de calcul : une intuition scientifique est nécessaire.

Il est nécessaire de comprendre parfaitement le fonctionnement d'un modèle.
- *ChatGPT est entraîné à compléter des phrases saisies par l'utilisateur :*
	- *Quel âge a Barack Obama ?* $\leftarrow$ *NON*
	- *L'âge de Barack Obama est* $\leftarrow$ *OUI*


### Visualisation et communication

- Dashboards
- Storytelling à adapter selon les compétences du client
- Utiliser le vocabulaire du problème


### Déploiement et maintenance

- Docker, Cloud, MLOps
- Déploiement $\Rightarrow$ Nouvelles données et retours $\Rightarrow$ Nouveau modèle plus performant
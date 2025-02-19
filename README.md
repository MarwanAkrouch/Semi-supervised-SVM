L’objectif de cette étude est de reproduire l’approche continue de la méthode S3VM introduite par Chapelle, Chi et Zien dans leur article “A Continuation Method for Semi-Supervised SVMs”. 
Cette méthode s’applique aux jeux de données comprenant à la fois des données labellisées et des données non labellisées. 
L’approche continue est justifiée par le fait que, dans le problème d’optimisation, la fonction à minimiser n’est pas convexe et possède plusieurs minima locaux.

Après avoir implémenté la méthode, nous avons décidé de l’appliquer aux données MNIST afin d’évaluer ses performances.

## Résultats

Les résultats obtenus en classification à deux classes sont très satisfaisants, même pour de faibles pourcentages de données labellisées, que ce soit avec la version linéaire ou avec un k-PCA. 
Par exemple, avec 25 % de données labellisées, nous avons obtenu une précision d’environ 98 % sur le jeu de test et d’environ 99 % sur les données non labellisées du jeu d’entraînement. 
La performance du modèle sur l’ensemble des données non labellisées présente un intérêt particulier dans le cadre de l’apprentissage transductif.

D’autre part, la classification multiclasses avec une approche One vs Rest donne également de bons résultats. 
De plus, l’utilisation d’un k-PCA avec un noyau RBF améliore l’accuracy du modèle tout en réduisant sa complexité : 
la précision sur le jeu de test est d’environ 54 % dans le cas linéaire et atteint environ 68 % en appliquant un k-PCA avec un noyau gaussien.

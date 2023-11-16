# Synthèse du projet

## Contexte
Dans le cadre de l'analyse des données de segmentation client, l'objectif était de déterminer le segment *(variable Var_1)* pour chaque client en utilisant un ensemble restreint de variables explicatives. La problématique étant orientée marketing, l'accent a été mis sur la livraison de résultats explicatifs et facilement interprétables par les équipes métier.

## Méthodologie
1. **Exploration des données :** Les données ont été chargées et inspectées, identifiant des variables telles que le genre, le statut matrimonial, le niveau d'éducation, la profession, etc.


2. **Prétraitement des données :** Un ensemble de prétraitements a été appliqué aux données, incluant le remplacement des valeurs manquantes avec l'imputation k-NN et la gestion des variables catégorielles avec des labelEncoder. La technique SMOTE a été utilisée pour traiter les données déséquilibrées.

3. **Choix du modèle :** Initialement, un arbre de décision simple a été envisagé, mais en raison du faible lien entre les variables et la variable cible, une forêt aléatoire a été choisie pour améliorer la précision tout en maintenant l'interprétabilité.

4. **Optimisation du modèle :** Une recherche sur grille avec validation croisée a été utilisée pour optimiser les hyperparamètres de la forêt aléatoire, en mettant l'accent sur la métrique de F1-pondérée.

5. **Évaluation du modèle :** Le modèle final a été évalué à l'aide de la matrice de confusion, montrant de bons résultats dans la prédiction des différentes catégories.

6. **Interprétation des résultats :** La méthode Shapley a été utilisée pour interpréter les prédictions du modèle, permettant de comprendre l'impact de chaque variable sur les prédictions pour chaque catégorie.

## Résultats et Conclusions
- Le modèle optimisé a démontré de bonnes performances sur l'ensemble de test malgré la nature déséquilibrée des données.
- L'utilisation de Shapley a permis d'interpréter les résultats du modèle en identifiant les variables qui ont le plus d'impact sur chaque catégorie.
- L'interprétation des segments reste assez difficile du fait du peu de variables à disposition. 

Cette approche a permis de développer un modèle prédictif robuste tout en fournissant des informations explicites sur les variables qui influencent la segmentation client. Ces résultats peuvent être utilisés pour guider les décisions marketing de manière plus informée.

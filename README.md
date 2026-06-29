# FedHealth
Prédiction du diabète à partir de données distribuées

Ce projet implémente une approche de prédiction du diabète basée sur l’apprentissage automatique et l’apprentissage fédéré. L’objectif est de classifier les patients comme diabétiques ou non diabétiques à partir de variables cliniques, tout en tenant compte du fait que les données médicales peuvent être réparties entre plusieurs établissements et ne peuvent pas toujours être centralisées pour des raisons de confidentialité.

L’approche proposée repose sur l’utilisation de forêts aléatoires entraînées localement sur plusieurs clients simulant différents sites de collecte de données. Les prédictions produites par ces modèles locaux sont ensuite combinées au niveau d’un serveur à l’aide d’un mécanisme d’agrégation par vote souple. Cette stratégie permet de comparer les performances d’un modèle centralisé classique avec celles d’une approche fédérée, dans des scénarios IID et non-IID.

Le projet comprend les étapes principales suivantes : préparation et harmonisation de jeux de données publics, formulation du problème comme une classification binaire, entraînement d’un modèle Random Forest centralisé, simulation d’un cadre fédéré à cinq clients, agrégation des prédictions par soft voting, puis évaluation des performances à l’aide de métriques telles que l’accuracy, la précision, le rappel, le F1-score et l’AUC.

Ce travail s’inscrit dans le contexte de l’intelligence artificielle appliquée à la santé, avec un accent particulier sur la confidentialité des données, la robustesse face à l’hétérogénéité des données distribuées et la comparaison entre apprentissage centralisé et apprentissage fédéré.

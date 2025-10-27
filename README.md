## Description du projet
Ce projet comprend deux exercices principaux :

### Exercice 1 : Implémentation d’un modèle Word2Vec Skip-Gram avec Negative Sampling à partir de zéro en utilisant TensorFlow, entraîné sur le corpus text8 (extrait de Wikipédia).

### Exercice 2 : Utilisation d’un embedding pré-entraîné (Google News Word2Vec) pour construire un classifieur de sentiments sur le jeu de données Yelp Review Polarity.

##  Exercice 1 : Word2Vec from Scratch
### Objectif
Implémenter et entraîner un modèle Word2Vec Skip-Gram en utilisant :

Negative Sampling pour accélérer l’entraînement

Des embeddings de taille 200

Un vocabulaire limité aux 50 000 mots les plus fréquents (hors mots rares remplacés par UNK)

### Étapes clés :
Téléchargement et prétraitement du corpus text8

Construction du vocabulaire et remplacement des mots rares par UNK

Génération de paires (mot central, mot contexte) via next_batch

Définition des fonctions de perte (nce_loss) et d’évaluation (similarité cosinus)

Entraînement avec affichage des mots les plus proches à intervalles réguliers

### Fonctionnalités supplémentaires :
afficher_contextes() : visualise les contextes d’un mot donné dans le corpus

## Exercice 2 : Classification de sentiments Yelp avec Word Embeddings
### Objectif
Construire un modèle de classification binaire (positif/négatif) pour des avis Yelp en utilisant :

Des word embeddings pré-entraînés (Google News Word2Vec, 300 dimensions)

Une architecture simple avec GlobalAveragePooling et couches denses

### Étapes clés :
Chargement des embeddings Google News via gensim

Chargement et équilibrage des données Yelp

Tokenization et padding des séquences

Création d’une matrice d’embedding initialisée avec les vecteurs pré-entraînés

Construction et entraînement d’un modèle séquentiel Keras

Évaluation sur un jeu de test

### Dépendances
tensorflow
numpy
gensim
scikit-learn
pandas
urllib
zipfile
collections

## Résultats attendus
  ### Word2Vec : Diminution de la perte et similarités sémantiques plausibles (ex: five → four, six, three)
  
  ### Classification Yelp : Précision > 90% sur le jeu de test avec les embeddings pré-entraînés



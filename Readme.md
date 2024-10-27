# README - Projet d'Apprentissage Non Supervisé : Segmentation des Clients

## Description du projet
Ce projet a été réalisé dans le cadre du Nanodegree en Machine Learning d'Udacity. L'objectif principal est d'explorer et de segmenter un jeu de données contenant des informations sur les dépenses annuelles de divers clients dans différentes catégories de produits. En utilisant des méthodes d'apprentissage non supervisé, nous cherchons à identifier des segments de clients distincts et à mieux comprendre leurs comportements d'achat. Cela permettrait à un distributeur en gros de mieux structurer ses services de livraison et de personnaliser son offre en fonction des besoins spécifiques de chaque segment.

## Jeu de données
Le jeu de données utilisé pour ce projet provient du UCI Machine Learning Repository. Il contient les montants annuels dépensés par les clients dans six catégories de produits :

- **Fresh** (Produits frais)
- **Milk** (Produits laitiers)
- **Grocery** (Épicerie)
- **Frozen** (Produits congelés)
- **Detergents_Paper** (Détergents et papier)
- **Delicatessen** (Charcuterie)

Pour les besoins de ce projet, les caractéristiques 'Channel' (type de client) et 'Region' (région géographique) ont été exclues de l'analyse afin de se concentrer sur les six catégories de produits.

## Étapes d'analyse
### 1. Exploration des données
Dans cette première section, les données sont visualisées et des résumés statistiques sont générés pour chaque catégorie de produits. Cela permet de mieux comprendre la distribution des dépenses pour chaque type de produit et de détecter des valeurs extrêmes (outliers).

Un exemple d'observation est que les catégories "Fresh" et "Grocery" sont les plus dépensées par la majorité des clients, tandis que les dépenses pour "Delicatessen" sont généralement plus faibles.

### 2. Analyse des clients échantillons
Trois clients ont été sélectionnés comme échantillons pour une analyse plus approfondie. En observant les dépenses de ces clients et en les comparant aux médianes des distributions des dépenses pour chaque catégorie, nous avons formulé des hypothèses sur le type d'établissement qu'ils pourraient représenter :

- **Client 1 (Index 0)** : Probablement un **restaurant**, avec des achats importants de produits congelés, des produits frais proches de la médiane, et des achats de charcuterie.
- **Client 2 (Index 1)** : Probablement un **supermarché**, avec des achats élevés pour toutes les catégories sauf la charcuterie, suggérant l'absence de cette section dans l'établissement.
- **Client 3 (Index 2)** : Probablement un **café**, avec des achats importants de lait, des dépenses modérées en épicerie et charcuterie, mais des achats faibles en produits frais et congelés.

## Méthodologie
### 1. Prétraitement des données
Les données ont été nettoyées et normalisées pour s'assurer que chaque caractéristique contribue de manière égale à l'analyse. Les valeurs aberrantes ont été identifiées et, le cas échéant, supprimées ou traitées pour ne pas fausser les résultats.

### 2. Segmentation des clients
En utilisant des méthodes d'apprentissage non supervisé, telles que l'algorithme K-means, nous avons segmenté les clients en groupes distincts en fonction de leurs comportements d'achat. Ces segments permettent de mieux comprendre les besoins spécifiques des différents types de clients et d'adapter les stratégies de vente et de marketing en conséquence.

### 3. Analyse des résultats
Les segments identifiés ont été interprétés et visualisés pour comprendre les comportements dominants dans chaque groupe. L'objectif était de créer des profils de clients et d'optimiser la personnalisation des services de livraison et des offres promotionnelles pour chaque segment.

## Conclusion
L'analyse de ce jeu de données a permis d'identifier différents segments de clients en fonction de leurs habitudes de dépenses. Ces informations sont précieuses pour les grossistes, car elles leur permettent d'optimiser leurs services et de personnaliser leurs offres en fonction des besoins spécifiques de chaque type de client.

Ce projet a démontré l'importance de l'apprentissage non supervisé dans l'analyse des comportements d'achat et la segmentation de la clientèle.

## Requis pour l'exécution du projet
Pour exécuter ce projet, vous aurez besoin des outils et bibliothèques suivants :

- Python 3.x
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn
- Jupyter Notebook

## Instructions d'exécution
1. Clonez ce dépôt ou téléchargez les fichiers.
2. Installez les dépendances nécessaires via pip : `pip install -r requirements.txt`
3. Ouvrez le fichier Jupyter Notebook : `jupyter notebook customer_segments.ipynb`
4. Suivez les étapes du notebook pour exécuter le projet et afficher les résultats.

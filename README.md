 StackOverFlow Tags :

------------------------------------------------------------------------------------------------------------------------------------------------

Projet_5 : Catégorisez_automatiquement_des_questions

Pour notre analyse sur stackoverflow, nous avons dû créer une requête SQL comme celle ci :

------------------------------------------------------------------------------------------------------------------------------------------------

SELECT TOP(50000) Id, CreationDate, Score, ViewCount, Title , Tags , Body, AnswerCount,

FROM Posts

WHERE CreationDate BETWEEN CONVERT(datetime, '2022-01-01') AND CONVERT(datetime, '2022-02-01')

AND Score > 5

AND ViewCount > 1

AND AnswerCount > 1

ORDER BY CreationDate

------------------------------------------------------------------------------------------------------------------------------------------------

On a juste dû changer la date de création pour garder les données de Janvier à Juillet.

A partir de là, on fait une bréve analyse des données pour faire des visualisations succintes.

Ensuite à partir de cette bréve analyse, on va commencer à nettoyer les données textuelles.

------------------------------------------------------------------------------------------------------------------------------------------------

On va faire comme suit :

- Nettoyage HTML via Beautiful Soup
- Nettoyage du texte pour supprimer les chiffres fin de phrase etc etc ..
- Suppression des verbes contractées
- Suppression des stopwords
- Tokennisation
- P.O.S. Tagging
- Lemmatisation

------------------------------------------------------------------------------------------------------------------------------------------------

Ensuite on fera du Features Engineering pour créer differentes colonnes :


La colonne tags sera coupé comme suit :

- 1 colonne avec 1 tag affiché le plus pertinent 
- 1 colonne avec une liste de tags
- 1 colonne avec un array des tags 

La colonne corpus sera coupé comme suit :

- 1 colonne corpus avec le corpus sous forme de liste
- 1 colonne corpus avec le corpus sous forme de array

------------------------------------------------------------------------------------------------------------------------------------------------

Ensuite une fois faite :

Nous allons faire des algorithmes non supervisés :

- Le Bag of Words 
- Le tf-idf 
- la LDA via bow et tf-idf 
- le nmf 
- le word2cv
- le BERT
- le USE

------------------------------------------------------------------------------------------------------------------------------------------------

Nous allons également faire des algorithmes supervisés :

- La Régression Logistique
- Le K.N.N
- Le Random Forest
- Le decision Tree Classifier 
- Le Xgboost
- Le gradient Classifier
- L'adaboost

Ci-joint le lien pour l'API :
https://github.com/Aurelien07/API_Stackoverflow

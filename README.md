# Rapport d'analyse de données

Ce rapport présente une analyse de données concernant les temps de trajet entre différentes villes en France, ainsi que la génération d'un dictionnaire réduisant les vecteurs de ces trajets à une échelle donnée.

## Préparation des données

Les données utilisées dans cette analyse sont stockées dans un dataframe `df_regularite` contenant les informations suivantes :

- "Gare de départ" : la gare de départ du trajet
- "Gare d'arrivée" : la gare d'arrivée du trajet
- "Date" : la date du trajet
- "Durée moyenne du trajet" : la durée moyenne du trajet en minutes

Un dictionnaire `cities` a également été créé pour associer chaque ville à ses coordonnées géographiques.

## Calcul des temps de trajet

La fonction `haversine` a été utilisée pour calculer la distance géographique entre deux villes, en se basant sur leurs coordonnées géographiques. Cette distance a ensuite été utilisée pour estimer le temps de trajet moyen en utilisant les données de `df_regularite`.

## Réduction des vecteurs de trajet

La fonction `reduction_vect_trajet` a été créée pour réduire les vecteurs de trajet entre deux villes à une échelle donnée. Cette fonction prend en entrée l'échelle de réduction, ainsi que les noms des villes de départ et d'arrivée, et utilise les coordonnées géographiques de ces villes, ainsi que le temps de trajet moyen entre ces villes, pour calculer un vecteur de temps.

La fonction `generate_reducted_dico` a été utilisée pour créer un dictionnaire réduisant tous les vecteurs de trajet à une échelle donnée par rapport à une ville de référence donnée. Cette fonction prend en entrée l'échelle de réduction et le nom de la ville de référence, et utilise la fonction `reduction_vect_trajet` pour calculer les vecteurs de trajet réduits pour toutes les autres villes.

## Conclusion

Ce rapport a présenté une analyse de données concernant les temps de trajet entre différentes villes en France, ainsi que la génération d'un dictionnaire réduisant les vecteurs de ces trajets à une échelle donnée. Ces résultats pourraient être utilisés pour visualiser les déplacements entre différentes villes en France à différentes échelles, ou pour créer des modèles prédictifs de temps de trajet entre différentes villes.

# Simulateur de système énergétique français


## Utilisation:
La feuille "bilan" permet de définir les capacités de production de nucléaire, éolien et solaire avec un facteur par rapport aux capacités historiques

Elle permet aussi de définir la capacité de stockage du système

La feuille "graphes bilan" montre la consommation, le bilan instantanée production-consommation, l'énergie stockée et l'apport d'énergie supplémentaire nécessaire pour assurer l'équilibre production/consommation

La feuille "stockage vs apport pilotable" synthétise les besoins en apport supplémentaire (potentiellement en énergie fossile) en fonction du stockage disponible, pour différents scénarios de production

Le stockage coutant très cher, un zoom est fait sur les scénarios à stockage limité (<0.5TWh)


Les données de production et de consommation au pas de 30 minutes viennent de https://opendata.reseaux-energies.fr/pages/accueil/

Les chiffres moyens pour 2018 viennent de https://bilan-electrique-2018.rte-france.com/#


## Limitations: 
Pas de modélisation de l'apport net de l'hydraulique, parce que pas de séparation dans les données RTE de la part fatale (hydrolien au court de l'eau) et de la part pilotable (retenues)

Le scénario commence au 1er Mars 2018: hypothèse que le pic hivernal qui vient de passer et qu'il a consommé tout le stockage->stockage à 0 au premier Mars

Les énergies pilotables sont mal modélisées puisque qu'on prend juste un coef sur les données historiques, alors que pour chaque scénario elle devraient s'adapter différemment. Du coup il faut mieux mettre le coef fossile à 0, et représenter le fossile par l'apport pilotable

Néanmoins pour tenir compte des constantes de temps de mise en marche du nucléaire, et des diminutions temporaire de capacités dues aux arrêts techniques, c'est plus réaliste que juste prendre une production constante

Il n'y a qu'un seul niveau de stockage de modélisé, alors qu'on pourrait utiliser deux niveau: un de faible capacité mais rapide et efficace pour les variations journalières, et un de forte capacité mais plus lent et moins efficace pour les variations saisonnières

Le modèle de couts du réseau est très approximatif vu qu'il se base uniquement sur les longueurs moyennes des lignes estimées au doigt mouillé


## Version:
3

## Contact:
/u/gosnold
# Kickstarter prediction

## Introduction

Kickstarter est une plateforme américaine de crowd lending. Les porteurs de projet en tout genre lancent leurs campagnes sur kickstarter. Une campagne a une durée limitée durant laquelle les investisseurs (potentiellement le commun des mortels) peut décider d'investir de l'argent dans le projet.

Il existe des projets dans des domaines tout à fait varié et évidemment les succès des campagnes sont variables. On dit qu'une campagne sur kickstarter est réussie lorsque la somme demandée par les porteurs de projets a été apportée par les investisseurs.

Ainsi, il peut être intéressant pour les porteurs de projet d'avoir une connaissance assez fines des critères de réussite d'une campagne sur kickstarter (travail de visualisation des données et de data analyst). Mais il est d'autant plus intéressant pour les investisseurs de savoir si les projets dans lesquels ils investissent verront le jour ou non. Personne n'a envie de jeter d'argent par les fenêtres 💸

_In fine_, nous avons tenté de prédire la réussite ou l'échec d'une campagne kickstarter (problème de classification binaire).

## Avant-propos

Avant de foncer tête baissée dans le machine learning pur, nous avons pris le temps de visualiser nos données, de regarder sur internet ce qui avait déjà été fait (nous sommes partis d'un notebook trouvé en ligne et avons tenté de prolonger la réflexion).

Nous avons travaillé plusieurs sur ce projet, sans nous servir de git. La collaboration a été maladroite, vous pourrez donc observer de multiples notebooks à ouvrir avec Jupyter.

## Pipeline

### Data visualization

Nous avons commencé par visualiser les données. L'idée était de faire apparaitre des "motifs" lors de la visualisation, des corrélations évidentes, en vain. Je me suis chargé de cette partie.

### Preprocessing

Il s'agissait de ne garder que les features les plus intéressantes et éventuellement de réduire la dimension pour parvenir à une meilleure séparabilité.

### Classification simple

Nous avons tous testé pléthore de modèles de classification : naïve bayésienne, random forest, adaboost, réseaux de neurones, etc. Le but était d'identifier les modèles les plus performants, les uns indépendemment des autres.

### Stacking

L'idée la plus avancée que nous ayons eu a été de mettre en place des algorithmes de stacking. Il s'agit d'entrainer plusieurs modèles sur nos données, de récupérer les plus performants, et de donner les sorties de ces modèles en entrée d'un nouvel algorithme de classification. L'idée est d'avoir des classifieurs plus ou moins faibles et de les combiner pour en faire un classifieur bien plus performant. Notre critère d'évaluation a été le score F1.

Je me suis chargé de cette partie aussi.

## Démarrage

Comme tout le code est réparti dans des notebooks indépendants les uns des autres, je vous conseille de les ouvrir aléatoirement en vous fiant aux noms qui leur ont été donnés, après avoir cloné le dépôt localement.

Je n'ai pas uploadé les datasets que nous avions trouvé en ligne car ils sont excessivement lourds et inutiles pour visualiser le travail que nous avons effectué.

## Conclusion

Nous avons finalement atteint un score F1 de 76% avec le stacking. C'est un résultat décevant car à peine plus élevé que celui des classifieurs seuls sans stacking. Nous avons travaillé en temps limité et aurions pu aller plus loin avec plus de temps.

## Authors

- **Bastien Velitchkine** - _Student @ CentraleSupélec_ - [Bassvelitchkine](https://github.com/Bassvelitchkine)
- **Merlin Egalité** - _Student @ CentraleSupélec_ - [MerlinEgalite](https://github.com/MerlinEgalite)
- **Maïwenn Danno** - _Student @ CentraleSupélec_
- **Mickaël De La Roque** - _Student @ CentraleSupélec_

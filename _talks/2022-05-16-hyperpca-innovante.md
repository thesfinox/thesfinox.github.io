---
title: "HyperPCA. Une méthode d’analyse innovante pour l’imagerie hyperspectrale"
collection: posters
type: "Poster"
permalink: /talks/2022-05-16-hyperpca-innovante
venue: "Journées Scientifiques de l’ISAS"
date: 2022-05-16
location: "Saclay, France"
---

### Contexte
Le projet CAMELIA (CArtographie Multi-Élémentaire par LIBS et Intelligence Artificielle, PTC-ID 2021-2022) porte sur la cartographie multi-élémentaire à l’échelle micrométrique d’échantillons par spectroscopie de plasma induit par laser (« Laser-Induced Breakdown Spectroscopy », ou LIBS, en anglais). Cette technique utilise un faisceau laser focalisé sur la surface d’un échantillon pour créer un plasma dont l’émission est caractéristique des éléments présents. Des cartographies en deux dimensions de la surface sont obtenues en déplaçant l’échantillon à chaque tir du laser : chaque pixel de la cartographie correspond à un spectre, qui contient l’information sur les éléments présents dans le plasma d’ablation. Cependant, cette technique a un rapport signal/bruit intrinsèquement faible, dû à l’utilisation d’un seul tir laser par cratère pour augmenter la résolution latérale. Elle présente également une dimensionnalité très élevée, liée au nombre de cratères nécessaires pour cartographier une surface donnée. Par conséquent, l’extraction de l’information physico-chimique de ces données fortement bruitées et de grande dimension, est un enjeu majeur.
### Objectifs
Dans CAMELIA, on développe des techniques basées sur l’apprentissage automatique et l’intelligence artificielle, pour exploiter efficacement le signal. L’objectif est de mettre au point une méthode pour s’affranchir au maximum du bruit des données et pour extraire le signal spectroscopique. Cette technique doit permettre la reconstruction de la distribution des éléments chimiques sur la surface de l’échantillon. Par ailleurs, la méthodologie doit être interprétable sur le plan spectroscopique et physico-chimique, et non supervisée, car aucune connaissance a priori des échantillons ne doit être requise.
### Méthodologie
Dans le domaine de la cartographie LIBS, outre la méthode usuelle d’exploitation des spectres à partir l’intensité de raies prédéfinies, l’Analyse en Composantes Principales (ACP) a été proposée par plusieurs auteurs car elle permet de fournir des résultats interprétables et de façon non supervisée [1]. Cette méthode permet de cartographier en deux dimensions la distribution des éléments chimiques. La méthodologie proposée est basée sur des développements récents de l’ACP [2], qui ont montré des résultats prometteurs pour la réduction du bruit et la reconstruction du signal. Pour résoudre les problèmes soulevés par la spécificité des données de cartographie LIBS, nous avons proposé dans CAMELIA la technique HyperPCA [3, 4], basée sur le couplage d’une transformée en ondelettes pour la création d’une représentation parcimonieuse des données et la résolution des interférences spectrales, et d’une approche basée sur une fonction noyau pour la réduction du bruit. Cette procédure permet de s’affranchir de la présence d’une distribution du bruit aléatoire pour des jeux de données de grande dimensionnalité : cette configuration est typique de la cartographie LIBS et de l’imagerie hyperspectrale, ce qui permet l’exploitation de cette méthode. Notre démarche a donc consisté à comparer les résultats obtenus par l’approche univariée usuelle, par l’ACP et par l’HyperPCA, sur des jeux de données simulées et expérimentales.
### Résultats
L’HyperPCA fournit une plus grande quantité d’information, avec une meilleure qualité, par rapport à la méthode usuelle et par rapport à l’ACP : on obtient un grand nombre de composantes lisibles même en présence d’un rapport signal/bruit très faible. De plus, l’utilisation d’une transformée en ondelettes permet de capturer les propriétés physiques des profils des raies d’émission. On observe enfin que les composantes calculées par HyperPCA sont souvent mono-élémentaires, ce qui permet d’obtenir des cartographies plus facilement interprétables. 
### Conclusion et perspectives
L’HyperPCA a été introduite dans le projet CAMELIA pour l’analyse des données hyperspectrales (LIBS en particulier). L’algorithme proposé montre des améliorations significatives par rapport aux méthodes de l’état de l’art, pour l’extraction de l’information physico-chimique, puisqu’il peut être employé en présence d’un rapport signal/bruit très faible. La quantité d’information récupérée et la qualité des composantes principales sont les avantages les plus évidents de cette technique. L’HyperPCA permet de grouper les raies d’émission dans les composantes par élément chimique, ce qui donne des cartographies facilement interprétables en termes de contributions mono-élémentaires. En perspective, on peut envisager d’appliquer cette approche à l’analyse quantitative par LIBS, car elle offre une méthode de réduction de dimensionnalité et d’extraction de composantes de très bonne qualité. Il serait également intéressant d’explorer d’autres applications de l’HyperPCA pour des tâches de segmentation d’image, ou encore d’étudier des méthodes plus avancées, comme l’ACP tensorielle, pour tenir compte de la distribution spatiale des données dans les cartographies.
### Références
- [a] R. Finotello, M. Tamaazousti and J.-B. Sirven, « Méthodes d’analyse en composantes principales innovantes pour l’imagerie hyperspectrale », Séminaire des 60 ans de la CETAMA, 19 – 21 octobre 2021, Nîmes, France
- [b] R. Finotello, M. Tamaazousti and J.-B. Sirven, « HyperPCA: An Advanced Framework of Principal Components Analysis for Hyperspectral Images », Séminaire annuel PE-PTC, 22 – 24 novembre 2021, Grenoble, France
- [c] R. Finotello, M. Tamaazousti and J.-B. Sirven, « Sparse Representations and Kernel-based PCA », EMSLIBS 2021, 29 novembre – 2 décembre 2021, Gijón, Espagne
- [1] L. Jolivet et al., “Review of the recent advances and applications of LIBS-based imaging,” Spectrochimica Acta Part B: Atomic Spectroscopy 151 (2019) 41–53. doi:10.1016/j.sab.2018.11.008.
- [2] M. E. A. Seddik, M. Tamaazousti, and R. Couillet, “A kernel random matrix-based approach for sparse PCA,” 2019. https://openreview.net/forum?id=rkgBHoCqYX
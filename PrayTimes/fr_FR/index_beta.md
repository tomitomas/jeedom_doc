# Plugin Prières (PrayTimes) - BETA

Ce plugin permet de connaitre les différentes heures de prières de la journée sur une ville donnée.

Les calculs sont réalisés selon la méthode définie par l'organisation des Musulmans de France (MF), anciennement Union des organisations islamiques en France.

<img src="..\img\praytimes_icon.png" width="20%" />

# DISCLAIMER  

Le plugin se base sur une API, proposée par un service externe, et peut par conséquent cesser de fonctionner à tout moment.

# Configuration des Villes

La configuration des équipements Prières est accessible à partir du menu `Plugins`, sous la catégorie `Organisation`.  

Ni dépendances, ni démon, le plugin s'active et s'utilise directement simplement.  

L'ajout d'un nouvel équipement se fait comme sur n'importe quel autre plugin, simplement en cliquant sur `Ajouter`.  

Pour fonctionner, vous aurez besoin de définir la ville pour laquelle vous souhaitez obtenir les heures de prières. Par défaut la ville configurée dans les paramètres de votre Jeedom est pré-définie.
<br/>
<img src="..\img\all.png" width="50%" />  

<br/>
De façon standard, deux onglets de configuration sont disponibles :

1. Equipement
2. Commandes
<br/><br/>

# Equipement  

<img src="..\img\equipement.png" width="80%" />  
<br/><br/>
Vous retrouvez ici toute la configuration standard de votre équipement :  

* Nom de l’équipement : définit nom de votre équipement Pense-Bête,
* Objet parent : indique l’objet parent auquel appartient l’équipement,
* Catégorie : catégorise l’équipement (il peut appartenir à plusieurs catégories)
* Activer : permet de rendre votre équipement actif,
* Visible : rend votre équipement visible sur le dashboard
  
La seconde partie gère différentes options.

* Afficher J+1 : permet de créer des commandes afin d'obtenir également les heures de prières de J+1.
* Nom de la ville : ville pour laquelle vous souhaitez obtenir les informations
* Pays : pays de la ville indiqué au dessus

La dernière partie permet de personnaliser le widget visible sur le dashboard :

* Template de widget : si coché, alors vous obtiendrez

<img src="..\img\widget.png" width="80%" />  

La prochaine prière est indiquée en verte, et un décompte vous indique combien de temps il reste avant d'y arriver.

# Commandes disponibles  

Plusieurs commandes sont disponibles de base lors de la création de l'équipement :  

* Infos :
  * Les différentes prières : `Fajr`, `Dhuhr`, `Asr`, `Maghrib`, `Isha`
  * `Hijri Date` : date selon le calendrier Mulsuman
  * `Holidays` : est-ce un jour de fête particulier (`1er jour du Ramandan`, `Eid`, ... )

Note : les mêmes commandes avec "J+1" sont créés, si vous avez choisi cette option sur l'équipement.

* Actions :
  * `Refresh` : permet de rafraichir les informations

# FAQ  

TBD

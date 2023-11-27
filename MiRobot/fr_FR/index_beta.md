# Plugin MiRobot (mirobot) - BETA

Ce plugin permet de synchroniser sur son Jeedom les robots aspirateurs enregistrés sur son compte Xiaomi afin de pouvoir les piloter depuis Jeedom et depuis les différentes applications mobiles.

<img src="..\img\logo.png" width="20%" />

# Configuration des Robot

Pour commencer il est nécessaire d'installer les dépendances utiles et nécessaires au fonctionnement du plugin. La première installation peut prendre du temps (20min parfois !) en fonction de la puissance de votre machine ; il se peut qu'il faille relancer une 2nd fois l'installation si jamais cela échouait la première fois.  

Il vous faut ensuite indiquer l'adresse email utilisé pour l'application Xiaomi Home ainsi que le mode de passe correspondant.

<br/>
<img src="..\img\config.png" width="50%" />  

Une fois sauvegardée, direction la page des équipements du plugin.  
La configuration des équipements MiRobot est accessible à partir du menu `Plugins`, sous la catégorie `Objets connectés`.  

L'ajout des robots déjà existants sur votre compte Xiaomi et compatible avec le plugin se fait automatiquement après une clic sur le bouton `Détection automatique`  
<br/>
<img src="..\img\all_robot.png" width="50%" />  

<br/>
Deux onglets de configuration sont disponibles :

1. Equipement
2. Commandes
<br/><br/>

# Equipement  

Vous retrouvez ici toute la configuration standard de votre équipement :  

* Nom de l’équipement : définit nom de votre équipement Pense-Bête,
* Objet parent : indique l’objet parent auquel appartient l’équipement,
* Catégorie : catégorise l’équipement (il peut appartenir à plusieurs catégories)
* Activer : permet de rendre votre équipement actif,
* Visible : rend votre équipement visible sur le dashboard

Plus quelques options propres au plugin :  

* Adresse IP du robot : récupérée automatiquement
* Token : récupéré automatiquement
* ID unique : identifiant technique
* Model de Robot
* Type : récupérée automatiquement en fonction de votre model d'aspirateur. Si vous le modifiez, il faut penser à regénérer/syncrhoniser les commandes, avec le bouton orange adéquat présent à l'écran
* Rafraichissement : défini le temps de rafraichissement des données

# Actions  

Cet onglet contient les principales configurations d'actions qui seront utilisées pour tout ou partie de vos robots.  

# Commandes disponibles  

Sont créés et gérées en fonction du model de votre robot, et seront donc plus ou moins nombreuses.

# FAQ  

A faire ...

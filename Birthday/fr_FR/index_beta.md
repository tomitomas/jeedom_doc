# Plugin Anniversaires (Birthday) - BETA

Plus d'excuse pour oublier de fêtre un anniversaire !  
Ce plugin permet d'enregistrer les anniversaires des membres de votre famille, animaux, amis, collègues, etc ... et de réaliser différentes actions en amont (acheter un kdo !) et/ou le jour J (envoyer un sms, mail, ...).

<img src="..\img\logo.png" width="20%" />

# Configuration des Anniversaires

La configuration des équipements Anniversaires est accessible à partir du menu `Plugins`, sous la catégorie `Organisation`.  

Ni dépendances, ni démon, le plugin s'active et s'utilise directement simplement.  

L'ajout d'un nouvel équipement se fait comme sur n'importe quel autre plugin, simplement en cliquant sur `Ajouter`
<br/>
<img src="..\img\all_anniv.png" width="50%" />  

<br/>
Trois onglets de configuration sont disponibles :

1. Equipement
2. Actions
3. Anniversaires  
<br/><br/>

# Equipement  

Vous retrouvez ici toute la configuration standard de votre équipement :  

* Nom de l’équipement : définit nom de votre équipement Pense-Bête,
* Objet parent : indique l’objet parent auquel appartient l’équipement,
* Catégorie : catégorise l’équipement (il peut appartenir à plusieurs catégories)
* Activer : permet de rendre votre équipement actif,
* Visible : rend votre équipement visible sur le dashboard

# Actions  

Cet onglet contient les principales configurations d'actions qui seront utilisées pour tout ou partie de vos anniversaires.  
Vous pouvez par exemple choisir d'avoir plusieurs rappels pour chaque tâche ; chaque rappel pouvant réaliser différentes actions/opérations.  

Par exemple :

* 3 jours avant l'évènement : m'envoyer un rappel pour que j'aille acheter un kdo, des fleurs, ...
* jour J à 9h00 : afficher un rappel sur jeedom / faire une annonce vocale dans la maison que c'est l'anniv de Mamie aujourd'hui...
* jour J à 12h00 : envoyer sms
...

<img src="..\img\list_action.png"  />

Pour les options de la commande, vous pouvez utiliser les tags suivants, qui seront automatiquement remplacés :

* `#eqId#` => numéro de l'équipement Anniversaire
* `#eqName#` => nom de l'équipement Anniversaire
* `#contactName#` => nom du contact
* `#birthdayInfo#` => date d'anniversaire
* `#contactDetail1#` => tél du contact
* `#contactDetail2#` => email du contact
* `#age#` => âge souhaité

# Anniversaires  

C'est ici que sont listées les dates anniversaires qu'il ne faut pas oublier :).  
Chaque tâche recevra 1 à N rappel en fonction de la configuration réalisée sur l'onglet précédent.

<img src="..\img\list_anniv.png" width="60%" />  

Pour ajouter un anniversaire, il faut simplement :

* cliquer sur le bouton `Ajouter un anniversaire`
* définir les éléments suivants :
  * le nom de la personne / évènement concerné
  * la date anniversaire (ou autre) qu'on ne veut surtout pas oublier
  * Contact 1 : permet d'indiquer une première méthode pour contacter la personne (numéro de téléphone perso, email perso, ....) *  
  * Contact 2 : permet d'avoir une seconde méthode pour contacter la personne (numéro de téléphone pro, email pro, ....)  *  
  * Actions : liste les actions disponibles et pouvant être réalisées sur ce contact pour son anniversaire

Il est possible de désactiver (plus ou moins temporairement) un anniversaire (plutôt que de le supprimer puis le recréer plus tard) en décochant la case `Active`.  

# Commandes disponibles  

Aucune pour le moment.

# FAQ  

TBD

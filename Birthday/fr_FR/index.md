# Plugin Anniversaires (Birthday) - BETA

Plus d'excuse pour oublier de fêter un anniversaire (ou une fête) !  
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
Vous pouvez choisir de définir tout un tas d'actions ou groupe d'actions ; chaque anniversaire pourra alors réaliser l'ensemble des actions ou une parmi la liste.  

Par exemple :

* 3 jours avant l'évènement : m'envoyer un rappel pour que j'aille acheter un kdo, des fleurs, ...
* jour J à 9h00 : afficher un rappel sur jeedom / faire une annonce vocale dans la maison que c'est l'anniv de Mamie aujourd'hui...
* jour J à 12h00 : envoyer sms  
...

<img src="..\img\list_action.png"  />

Pour les options de la commande, vous pouvez utiliser les tags suivants, qui seront automatiquement remplacés :

* `#eqId#` => numéro de l'équipement Anniversaire
* `#eqName#` => nom de l'équipement Anniversaire
* `#birthdayName#` => nom du contact
* `#birthdayDate#` => date d'anniversaire
* `#birthdayContact1#` => détail n°1 du contact
* `#birthdayContact2#` => détail n°2 du contact
* `#age#` => âge à souhaiter

# Anniversaires  

C'est ici que sont listées les dates anniversaires qu'il ne faut surtout pas oublier :).  

<img src="..\img\list_anniv.png" width="100%" />  

Pour ajouter un anniversaire, il faut simplement :

* cliquer sur le bouton `Ajouter un anniversaire`
* définir les éléments suivants :
  * le nom de la personne / évènement concerné
  * la date anniversaire (ou autre) qu'on ne veut surtout pas oublier au format `jj/mm/aaaa`
    * Si vous ne connaissez pas l'année, vous avez la possibilité de ne pas la renseigner en décochant la case `conserver l'année`
  * Contact 1 : permet d'indiquer une première méthode pour contacter la personne (numéro de téléphone perso, email perso, ....) *  
  * Contact 2 : permet d'avoir une seconde méthode pour contacter la personne (numéro de téléphone pro, email pro, ....)  *  
  * Actions : liste les actions disponibles et pouvant être réalisées sur ce contact pour son anniversaire.
    * `Toutes` : exécute l'ensemble des actions disponibles dans l'onglet `actions`
    * `Aucune` : aucune action n'est lancée
    * `<autre choix>` (en fonction de ce que vous aurez vous-même créé !) : seule l'action sélectionnée est exécutée

Il est possible de désactiver (plus ou moins temporairement) un anniversaire (plutôt que de le supprimer puis le recréer plus tard) en décochant la case `Active`.  

# Commandes disponibles  

Aucune pour le moment.

# FAQ  

## Prochains développements à venir ?

* Création d'un widget pour les prochaines anniversaires

En cours d'étude :

* Intégration d'un lien avec Facebook pour rappatrier les anniversaires des amis FB
* Intégration d'un lien avec Facebook pour rappatrier les anniversaires des amis FB

## Est-il possible de récupérer automatiquement les infos sur FB ?

Après plusiseurs tests et jours de recherche, Facebook n'autorise plus depuis quelques années à récupérer de façon automatique les anniversaires de ses propres amis. Les API ne permettent plus d'avoir accès à cette information.  
Le plugin ne pourra donc pas créer automatiquement ces dates.  

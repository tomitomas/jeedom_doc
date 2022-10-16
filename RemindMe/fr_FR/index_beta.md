# Plugin Pense-Bête (RemindMe) - BETA

Plus d'excuse pour oublier ceci ou cela !  
Ce plugin permet d'enregistrer des Pense Bêtes et de réaliser différentes actions lorsqu'une tâche est sur le point d'arriver.

<img src="..\img\remindme_icon.png" width="20%" />

# Configuration des Pense-Bêtes

La configuration des équipements Pense-Bête est accessible à partir du menu `Plugins`, sous la catégorie `Organisation`.  

Ni dépendances, ni démon, le plugin s'active et s'utilise directement simplement.  

L'ajout d'un nouvel équipement se fait comme sur n'importe quel autre plugin, simplement en cliquant sur `Ajouter`
<br/>
<img src="..\img\all_pense_betes.png" width="50%" />  

<br/>
Trois onglets de configuration sont disponibles :

1. Equipement
2. Rappel
3. Tâches  
<br/><br/>

# Equipement  

<img src="..\img\equipement.png" width="50%" />  
<br/><br/>
Vous retrouvez ici toute la configuration standard de votre équipement :  

* Nom de l’équipement : définit nom de votre équipement Pense-Bête,
* Objet parent : indique l’objet parent auquel appartient l’équipement,
* Catégorie : catégorise l’équipement (il peut appartenir à plusieurs catégories)
* Activer : permet de rendre votre équipement actif,
* Visible : rend votre équipement visible sur le dashboard
  
La seconde partie gère différentes options.

* Auto-suppression : si cochée, les tâches qui sont passées sont automatiquement supprimées.

# Rappels  

Cet onglet contient les principales configurations de rappel qui seront utilisées sur l'ensemble des tâches.  
Vous pouvez par exemple choisir d'avoir plusieurs rappels pour chaque tâche ; chaque rappel pouvant réaliser différentes actions/opérations.  

Par exemple :

* 10 jours avant : afficher un message sur jeedom
* la veille : m'envoyer un mail
* 3h avant : envoyer sms
* 5 min avant : faire lire la tâche par alexa + envoyer sms

<img src="..\img\rappel.png"  />

Pour les options de la commande, vous pouvez utiliser les tags suivants, qui seront automatiquement remplacés :

* `#eqId#` => numéro de l'équipement Pense-Bête  
* `#eqName#` => nom de l'équipement Pense-Bête  
* `#task#` => nom de la tâche  
* `#deadLine#` => prochaine échéance de la tâche

# Tâches  

C'est ici que sont listées toutes les tâches (liées à cet équipement).  
Chaque tâche recevra 1 à N rappel en fonction de la configuration réalisée sur l'onglet précédent.

<img src="..\img\task.png" width="60%" />  

Pour ajouter une tâche, il faut simplement :

* cliquer sur le bouton `Ajouter une tâche`
* lui définir une date d'échéance :
  * soit une date unique
  * soit avec une reccurence  
  Lors de la sauvegarde, la prochaine échéance est automatiquement calculée

# FAQ  

### à définir ...?

....

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
* Retour à la ligne : permet de choisir quel type de retour chariot est utilisé dans la commande `Toutes les prochaines tâches`
* Affichage du format date : différentes options de format de date. Ce format est pris en compte dans l'affichage sur le widget et sur les commandes de type `info`
* Affichage des tâches : différentes options de format des tâches. Ce format est pris en compte dans l'affichage sur le widget et sur les commandes de type `info`

La dernière partie permet de personnaliser les couleurs utilisées sur le widget :

* Par défaut : les couleurs d'arrière plan et de texte de chaque ligne du widget
* Evènement du jour : si la tâche est prévu aujourd'hui, alors la ligne s'affiche avec des couleurs différentes

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

# Commandes disponibles  

Plusieurs commandes sont disponibles de base lors de la création de l'équipement :  

* Infos :
  * `Toutes les prochaines tâches` : liste l'ensemble des tâches à venir. La façon dont les tâches sont séparées les unes des autres est à définir au niveau de l'équipement (virgule, retour chariot ou break line)
  * `Prochaine Tâche` : retourne la prochaine tâche à venir

* Actions :
  * `Supprimer toutes les Tâches` : permet de retirer toutes les tâches définies sur l'équipement  
  * `Supprimer une tâche` : permet de retirer une tâche en particulier, son `id` doit être passé en argument
  * `Ajouter une tâche` : permet de créer une tâche supplémentaire sur l'équipement. Le nom ainsi que l'échéance (au format `YYYY-MM-DD HH:MM`) sont attendues

# FAQ  

### Je peux bien choisir l’échéance du rappel et l’action a effectuer, mais on ne peut pas spécifier sur quelle taches se base cette échéance ?

En effet, et c’est tout l’idée du plugin !

Tu crées un équipement dans lequel tu définis quels sont (tous) les rappels que tu souhaites avoir et ensuite toutes les tâches liées à cet équipement bénéficient de l’ensemble de ces rappels.  

Par exemple, tu pourrais avoir :  

* 1 équipement A « ultra important », dans lequel tu aurais la définition de plusieurs rappels (car il ne faut vraiment pas oublier cette tache/action !) :
  * 10 jours avant : afficher un message sur jeedom
  * la veille : m’envoyer un mail
  * 3h avant : envoyer sms
  * 5 min avant : faire lire la tâche par alexa + envoyer sms

* 1 autre équipement B « pour info », dans lequel tu définirais seulement un seul rappel (car c’est juste un truc à penser, pas grave si ça n’est pas fait…)
  * 5 min avant : envoie une notif

Du coup, en fonction de « l’importance » de la tâche que tu souhaites créer, tu l’ajouteras soit dans l’équipement A, soit dans l’équipement B
**sans te soucier** du type de rappel que tu recevras, puisque c’est l’équipement qui porte cette info.

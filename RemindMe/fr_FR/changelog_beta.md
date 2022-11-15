# Changelog plugin Pense-Bête (RemindMe) - BETA

>**IMPORTANT**
>
>Pour rappel s'il n'y a pas d'information sur la mise à jour, c'est que celle-ci concerne uniquement de la mise à jour de documentation, de traduction ou de texte.

# 15/11/2022

- Nouveautés :
  - Le changement de statut de tâche  :
    - peut se faire via des intervalles : 3,7-11 --> change les id 3 ainsi que de 7 à 11
    - ajout de l'option `switcher` qui permet d'inverser l'état sans avoir à le spécifier

# 14/11/2022

- Nouveautés :
  - Nouvelles option pour `Affichage du format date` :
    - Ajout `date uniquement` pour l'option
    - Ajout d'un champ `personnalisé` pour que l'utilisateur puisse définir le format de date qu'il souhaite (valide au format PHP --> cf [PHP doc](https://www.php.net/manual/en/datetime.format.php))
  - La suppression de tâche peut se faire via des intervalles : 1-5 --> supprime les id de 1 à 5

# 10/11/2022

- Nouveautés :
  - Réinitialise le compteur des `id` à 1, lorsqu'on utiliser la commande `Supprimer toutes`

- Bug Fix :
  - Trie des tâches sur le widget et sur les commandes de type `info`
  - Ajout du texte `(désactivé)` selon les options

# 07/11/2022

- Nouveautés :
  - Trie insensible à la casse
  - Permettre de désactiver temporairement une tâche
  - Ajout d'une confirmation avant suppression
  - Changement du sous-type de la commande `Supprimer toutes les Tâches`
  - Création d'une commande `Changer le statut` pour passer une tâche active/inactive via scénario & co

# 02/11/2022

- Corrections :
  - Gestion des dates sur les prochaines années

- Nouveautés :
  - Ajout la personnalisation du nom de la colonne « Tâche » sur le widget
  - Ajout d’une option pour définir si une date d’échéance doit être définie sur chaque tâche ou non

# 30/10/2022

- Nouveautés :
  - Ajout d'une tâche cron dédiée au plugin (pour ne pas être impacté sur d'autres traitements par d'autres plugin)

# 26/10/2022

- Nouveautés :
  - Ajout d'un icone sur les tâches récurrentes
  - Possibilité de supprimer une liste de tâches (en séparant les id par des virgules `,`)
  - Ajout du nom du plugin comme source pour les actions de type `messages` (nouveauté core 4.3.7)

# 25/10/2022

- Nouveautés :
  - Option pour afficher l'identifiant des tâches (plus facile pour pouvoir supprimer des tâches à la volée)

# 15/10/2022  

- Création du plugin

# Changelog plugin Pense-Bête (RemindMe) - BETA

>**IMPORTANT**
>
>Pour rappel s'il n'y a pas d'information sur la mise à jour, c'est que celle-ci concerne uniquement de la mise à jour de documentation, de traduction ou de texte.

# 28/08/2024

Let’s go international ! :fr: :us_outlying_islands: :uk: :es: :de:
Pas de nouveautés en tant que telle, « juste » la traduction du plugin en plusieurs langues : FR, US, ES, DE !

# 29/07/2024

- Fix sur les dates fixes (avec core en 4.4.9)
- Ajout d’un bouton « supprimer toutes les tâches »

# 08/07/2024

- Fix chargement lib
- Fix masquage de la ligne d’en-tête

# 24/06/2024

- Fix bouton `Créer un post Community`
- Fix des dates à lancement uniquement (en erreur sur php8)
- Fix sur l'auto-suppression
- Fix sur le rafraichissement du widget sur un équipement dont l'échéance est optionnelle

# 13/04/2024

- Ajout de la commande MaJ une tâche afin de change simplement l’échéance de celle-ci
- Ajout du tag #taskId# dans les données dispo pour réaliser des actions

# 26/03/2023

- Mise à jour du plugin pour un bon fonctionnement avec la version core 4.4
- Passage en version core minimale : 4.2

# 05/02/2023

Mise à jour importante à réaliser.  
Corrige un conflit avec le plugin-mybin.  
A réaliser avant l'update de mybin

# 03/02/2023

- Nouveauté :
  - si le champ `titre de la colonne` est renseigné avec un seul espace, alors la 1ere ligne du tableau dans le widget est masqué

# 19/01/2023

- Bug fix :
  - lors du passage d'une page à une autre, il n'est plus possible de supprimer une tâche

# 18/01/2023

- Nouveautés :
  - Ajout de 2 nouvelles commandes : `Prochaine Tâche (date)` et `Prochaine Tâche (texte)`

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

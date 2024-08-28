# Changelog plugin Pense-Bête (RemindMe)

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

# 05/02/2023

Mise à jour importante à réaliser.  
Corrige un conflit avec le plugin-mybin.  
A réaliser avant l'update de mybin

# 03/02/2023

- Nouveauté :
  - si le champ `titre de la colonne` est renseigné avec un seul espace, alors la 1ere ligne du tableau dans le widget est masqué

# 11/11/2022

- Nouveautés :
  - Réinitialise le compteur des `id` à 1, lorsqu’on utiliser la commande `Supprimer toutes`
  - Trie des tâches sur le widget et sur les commandes de type `info`
  - Ajout du texte `(désactivé)` selon les options
  - Permettre de désactiver temporairement une tâche
  - Ajout d’une confirmation avant suppression
  - Changement du sous-type de la commande `Supprimer toutes les Tâches`
  - Création d’une commande `Changer le statut` pour passer une tâche active/inactive via scénario & co
  - Gestion des dates sur les prochaines années
  - Ajout la personnalisation du nom de la colonne « Tâche » sur le widget
  - Ajout d’une option pour définir si une date d’échéance doit être définie sur chaque tâche ou non

# 01/11/2022

- Nouveautés :
  - Ajout d'une tâche cron dédiée au plugin (pour ne pas être impacté sur d'autres traitements par d'autres plugin)
  - Ajout d'un icone sur les tâches récurrentes
  - Possibilité de supprimer une liste de tâches (en séparant les id par des virgules `,`)
  - Ajout du nom du plugin comme source pour les actions de type `messages` (nouveauté core 4.3.7)
  - Option pour afficher l'identifiant des tâches (plus facile pour pouvoir supprimer des tâches à la volée)

# 21/10/2022  

- Publication du plugin en stable

# Changelog plugin DigiAction - STABLE

>**IMPORTANT**
>
>Pour rappel s'il n'y a pas d'information sur la mise à jour, c'est que celle-ci concerne uniquement de la mise à jour de documentation, de traduction ou de texte.

# 02/01/2023

- Nouveautés :
  - Possibilité de choisir le design des différents mode en personnalisant la couleur d'arrière plan et la couleur du texte  
  - Permet la personnalisation des messages affichés en cas d'etre de saisie de code ou en cas de réussite
  
# 20/10/2022

- Nouveautés :
  - Mise à jour pour intégrer les nouveautés core 4.3

# 05/02/2022

- Nouveautés :
  - Ajout la possibilité de définir le type de contrôle à faire sur les mauvais code : limite basse à atteindre ou une récurrence
  - Ajout du mode `Panic`
  - Ajout d'un nouveau log (en `INFO`) permettant de savoir à quel moment les actions ont été réalisées et par qui
  - Ajout la possibilité de définir une date de validité pour les mots de passe utilisateur
    - Date de début et date de fin de validité sont calculées par le plugin (cf doc) avec l'aide du planificateur (cron)
  - Un code utilisateur peut être activé/désactivé via une case à cocher
  - Nouvelle commande `Changer code utilisateur` qui permet de changer dynamiquement le code d'un utilisateur
  - Les mots de passe sont masqués par défaut sur l'écran

- Bug fixes :
  - Renommage du mode en cours

# 01/08/2021  

Nouveautés :

- Autoriser un mode à s'auto-appeler (sur l'ensemble de l'équipement)
- Définir le temps d'affichage du message d'information (passage au mode xxx) ou d'erreur (par défaut si non renseigné à 10 secondes ; pour un affichage sans limite valoriser à -1 )

# 09/03/2021  

Fixes:  

- autoriser les autres utilisateurs que 'admin'
- rafraichissement du widget si mode activé par un scénario

# 25/02/2021

Nouveautés :

- si un timer est défini :
  - le code utilisateur saisie est d'abord vérifié (inutile d'attendre la fin du timer pour savoir que le code n'est pas bon !)
  - les pré-check sont réalisés une première fois avant de lancer le timer
- ajout de la configuration "pré-check erreur" : ensemble des actions à réaliser si les contrôles échouent
- En cas d’erreur de code : on reste sur le clavier plutôt que de revenir au menu

Fixes :

- Retouches CSS :
  - Adaptation de la taille du texte au bouton (surtout en cas de texte long)
  - Alignement des boutons (mode) « texte » et des boutons « images »
  - Alignement du compte à rebours et bouton « Annuler »
- En cas d’erreur de code successif, le message d'erreur « Code inconnu » est réaffiché  
- Gère le renommage des commandes plutôt que les suppressions  

# 19/02/2021

- Création du plugin

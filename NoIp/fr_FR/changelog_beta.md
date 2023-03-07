# Changelog plugin No-Ip Renew (NoIp) - BETA

>**IMPORTANT**
>
>Pour rappel s'il n'y a pas d'information sur la mise à jour, c'est que celle-ci concerne uniquement de la mise à jour de documentation, de traduction ou de texte.

# 07/03/2023

- Bug Fix :
  - Correction problème d'authentification lors la mise à jour automatique de l'ip

# 02/03/2023

- Nouveautés :
  - Ajout un niveau de log dédié pour l'excution du script python
  - Utilisation d'un parser pour utiliser les arguments du script
  - Ajout d'une nouvelle option sur les équipements de type "Compte" : `Auto suppression` afin de supprimer automatiquement du plugin les équipements "noms de domaine" qui ne sont plus présents sur le site no-ip
  - Ajout d'un cron dédié pour faire la vérification d'IP toutes les 15min (ne dépend plus du cron15 de jeedom)
  - Ajout de 2 options de configuration pour définir la plage horaire dans laquelle le script peut aléatoirement réaliser les contrôles

- Bug Fix :
  - Correction des créations multiple avec le même noms de domaine (suffixé d'un timestamp) lors d'une synchro

# 23/02/2023

- Nouveautés :
  - Ajout d'une nouvelle commande `linked IP` : qui permet de récupérer l'info de redirection du dns
  - Ajout d'une nouvelle option pour permettre de vérifier si l'IP configuré sur NOIP est bien à jour avec notre IP courante, et mettre à jour si nécessaire

# 21/02/2023

- Ajout de la commande `date de fin` sur chaque équipement "Domaine"
- Ajout de la commande  `Statut` sur chaque équipement "Comptes" --> si la synchro du compte est en erreur, alors le statut passera à "error". Je vous invite à créer un scénario pour avoir une alerte si nécessaire.
- Ajout de l'option `Refresh auto si erreur` sur les "Comptes" --> si une synchro tombe en erreur, le plugin doit il tenter de refaire une synchro automatiquement 5 min plus tard ? ou (par défaut) attendre la prochaine synchro le lendemain
- Ajout d'une fenêtre pour voir les screenshot réalisés lors de la synchro pour aider au debug
- Changement couleurs des icônes
- Mise en place de log synchrone lors de l'execution du script python
- Gestion des timeout
- Synchro des comptes en background de façon à ne pas bloquer l'utilisateur (et/ou revoir des erreur 405)

# 17/02/2023

- Reprise du plugin
- Correction fonction deprecated
- Correction erreur 500 à la création d'un équipement

# <u>Précédent changlog !</u>

# 14/11/2021

- Adaptation à un changement de layout du site

# 06/11/2021

- Adaptation à un changement de layout du site

# 15/08/2021

- Adaptation à un changement de layout du site

# 04/05/2021

- Correction problème de login

# 09/04/2021

- Adaptation à un changement de layout du site

# 28/03/2021

- Meilleur contrôle d'erreur
- Support des insallations Jeedom non-standard

# 10/03/2021

- Liste des parents indentée dans le panel de configuration

# 02/03/2021

- Fix sur le mode debug/info

# 21/02/2021

- Icônes de statut colorés

# 29/01/2021

- Première version publique (stable)

# 16/01/2021

- Première version publique (beta)

</details>

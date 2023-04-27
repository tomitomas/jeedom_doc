# Changelog

>**IMPORTANT**
>
>Pour rappel s'il n'y a pas d'information sur la mise à jour, c'est que celle-ci concerne uniquement de la mise à jour de documentation, de traduction ou de texte.

# 27/04/2023

- Nouveautés :
  - Compliance core 4.4
  - Ajout au niveau des équipements de type « compte » d’une nouvelle commande pour avoir un récap global des échéances des domaines (liste de `nom de domaine : X jours`)

# 28/03/2023

- Nouveautés :
  - Ajout un niveau de log dédié pour l'excution du script python
  - Utilisation d'un parser pour utiliser les arguments du script
  - Ajout d'une nouvelle option sur les équipements de type "Compte" : `Auto suppression` afin de supprimer automatiquement du plugin les équipements "noms de domaine" qui ne sont plus présents sur le site no-ip
  - Ajout d'un cron dédié pour faire la vérification d'IP toutes les 15min (ne dépend plus du cron15 de jeedom)
  - Ajout de 2 options de configuration pour définir la plage horaire dans laquelle le script peut aléatoirement réaliser les contrôles

- Bug Fix :
  - Correction des créations multiple avec le même noms de domaine (suffixé d'un timestamp) lors d'une synchro
  - Correction problème d'authentification lors la mise à jour automatique de l'ip

# 20/02/2023

passage en stable

<details>
<summary>Précédent changlog !</summary>

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

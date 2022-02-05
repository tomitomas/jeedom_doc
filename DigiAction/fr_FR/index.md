# Plugin DigiAction


Ce plugin permet de gérer plusieurs équipements DigiAction :  
appliquer un mode réalisant une/des action(s) sous condition(s), et d'ajouter un contrôle par saisie de mot de passe (facultatif) via un digicode.  

<img src="..\img\digiAction_présentation_dashboard.png" width="50%" />


# Configuration des DigiActions

La configuration des équipements DigiAction est accessible à partir du menu `Plugins`, sous la catégorie `Sécurité`  
  
<img src="..\img\digiAction_configuration.png" width="35%" />    
<br/><br/>

L'ajout d'un nouvel équipement se fait comme sur n'importe quel autre plugin, simplement en cliquant sur `Ajouter`    
<br/>
<img src="..\img\digiAction_all_equipements.png" width="25%" />  

<br/>
Trois onglets de configuration sont disponibles :    

1. Equipement
2. Actions 
3. Utilisateurs  
<br/><br/>

# Equipement  

Vous retrouvez ici toute la configuration standard de votre équipement :  

<img src="..\img\digiAction_equipement.png" width="50%" />  
<br/><br/>

* Nom de l’équipement : définit nom de votre équipement DigiAction,
* Objet parent : indique l’objet parent auquel appartient l’équipement,
* Catégorie : catégorise l’équipement (il peut appartenir à plusieurs catégories)
* Activer : permet de rendre votre équipement actif,
* Visible : rend votre équipement visible sur le dashboard
<br/><br/>  
  
# Actions  

Cet onglet contient les principales configurations du widgets.  
C'est ici que vous définissez : 

* les modes disponibles et leurs caractériques
* les contrôles à effectuer (en jaune)  
* les actions à réaliser (en vert)  

<img src="..\img\digiAction_onglet_actions.png"  /> 

1. le bouton `Ajouter mode` permet d'ajouter un nouveau bloc définissant un mode
  <br/>(dans l'exemple : 1a, 1b, 1c => 3 blocs définis pour cet équipement)
2. le nom du mode (cliquer dessus permet de le renommer)  
3. personnalise le mode avec un icône  (si aucun icône n'est sélectionné, alors le nom du mode sera affiché sur le widget)
4. défini un délai (en secondes) avant que le mode s'active (permet d'annuler l'action pendant un laps de temps)  
5. supprime le mode  
6. ajoute un/des contrôle(s) à réaliser avant (l'ensemble des `Pré-check` utilisent l'opérateur 'ET')   
  6a. active/désactive le contrôle  
  6b. ouvre un pop-up pour sélectionner une commande de type `info`  
7. ajoute une/des action(s) à réaliser si jamais le(s) pré-check (défins en 6) échoue(nt)   
  7a. active/désactive l'action  
  7b. permet de choisir une commande
  7c. ouvre un pop-up pour sélectionner une commande de type `action`   
  7d. défini les options de la commande   
8. ajoute une/des action(s) à réaliser pour passer dans le mode 
  8a. active/désactive l'action  
  8b. permet de choisir une commande
  8c. ouvre un pop-up pour sélectionner une commande de type `action`   
  8d. défini les options de la commande<span style="color:red">**</span>   
  8e. si coché, alors l'action est <b>uniquement</b> exécuter si un code "panic" a été saisi.  
9. défini le(s) mode(s) accessible(s) depuis le mode en cours 
  <br/>(pour une alarme par exemple : depuis le mode 'Désactiver' on peut activer les modes 'Partiel' ou 'Total' ; par contre depuis le mode 'Total' on ne peut aller que vers 'Désactiver')
10. demande un mot de passe afin de passer sur ce mode  
11. défini à partir de combien de code faux des actions spécifiques doivent être réalisées  
(par exemple pour vous envoyer un email/notification pour vous prévénir que c'est la 4ième fois de suite qu'un code saisi est erroné)  
  11a. manière qui doit être prise en compte pour réaliser les actions spécifiques en cas de mauvais code : 
      - `jamais` : aucun "action d'alerte" ne sera réalisée
      - `dès qu'il y a plus` : lorsque le nombre de mauvais code est atteint, alors les actions sont systématiquement exécutées lors d'une prochaine mauvaise saisie 
      - `toutes les` : définit une fréquence  (par exemple, si paramétré à "3", alors les actions seront réalisées lors du 3e, 6e, 9e, ... mauvaises saisies, mais pas lors de la 4e, 5e, 7e, 8, .. )
  11b. indique la limite ou la récurrence à utiliser (doit être supérieur ou égal à 1)
12. ajoute une/des action(s) à réaliser lorsque le nombre de mauvais mot de passe défini a été dépassé  
  12a. active/désactive l'action  
  12b. permet de choisir une commande
  12c. ouvre un pop-up pour sélectionner une commande de type `action`   
  12d. défini les options de la commande<span style="color:red">**</span>   


<span style="color:red">**</span> pour les options de la commande, vous pouvez utiliser les tags suivants, qui seront automatiquement remplacés : 

- `#eqId#` => numéro de l'équipement DigiAction  
- `#eqName#` => nom de l'équipement DigiAction  
- `#modeName#` => nom du mode qui tente d'être activé  
- `#nbWrongPwd#` => nombre de mauvais code saisi

<br/>

> #### Note
> au 1er lancement, tous les modes sont affichés afin d'initialiser le widget.  


<br/><br/>

# Utilisateurs  

Permet de gérer des utilisateurs avec leur propre code personnel, à utiliser sur les modes pour lesquels un code est requis.

<img src="..\img\digiAction_onglet_users.png" width="60%" />  

Pour ajouter un code, il faut simplement :
* cliquer sur le bouton `Ajouter un code utilisateur`
* une nouvelle ligne est ajoutée : indiquer le nom de l'utilisateur et son code (chiffre de 0 à 9 ainsi que les lette `A` et `B`)
* vous pouvez également définir une date (fixe ou récurrente) ainsi qu'une durée de validité. Si aucune date n'est renseignée, alors le code est valable sans restriction. 
* la case `Panic` permet de définir un (et un seul) utilisateur/code à utiliser pour déclencher certaines actions spécifiques au mode panic.  

Pour enlever un code, cliquez simplement sur le sigle `-` au bout de la ligne à supprimer.  
Pour désactiver temporairement le code, décocher la case `Actif`
<br/>  
<br/>  

# FAQ  

## Comment utiliser la plannification d'un code utilisateur ? 

On utilise la fonction de plannification (comme pour les scénario) de jeedom afin de pouvoir définir des dates de validité d'un code utilisateur. 

La date de début de validité pourra être : 
  - une date fixe (seulement demain le 17 aout 2021)
  - une date récurrente (tous les mercredis, ....)

La date de fin de validité sera automatiquement calculé par le plugin (en fonction de la date de début) si vous indiquez une `durée de validité`. 

Dans la copie d'écran précédente, il a été défini : 
> un usage unique pour l'utilisateur `User 1`.  
Le code sera valable pour 180 min à partir de 10h00 le 17/8. Le plugin enregistre la date de début le `17/08/2021 à 10h00` et en déduit la date de fin de validité `17/08/2021 à 13h00`  

<br/>

> un usage récurrent pour l'utilisateur `User 2`.  
Le code est valable `tous les mercredis de chaque semaine, à partir de 10h00 et pour 120 min`. Le plugin calcule donc la prochaine date valide -> il s'agit du `mercredi 18/08/2021`, et créé donc la date de début de validité `18/08/2021 à 10h00`, et en déduit la date de fin de validité `18/08/2021 à 12h00`.
<br/><br/>
Une fois que cette date de fin sera dépassée, alors le plugin calculera à nouveau la prochaine date disponible (contrôle fait toutes les 5mins). 
Donc le `18/08/2021 à 12h05`, le plugin verra que le code du `User 2` n'est plus actif, il mettra à jour les dates avec la prochaine période qui correspond aux données renseignées => début de validité mercredi `25/08/2021 à 10h00`, et date de fin de validité `25/08/2021 à 12h00`. Et ainsi de suite...   

<br/>  
<br/>  

## Comment changer dynamiquement un code utilisateur ?  

Il suffit d'utiliser la commande `Changer code utilisateur`, en renseignant correctement : 
- le nom de l'utilisateur dans le champ `Utilisateur` (attention aux majuscules & co!) 
- le nouveau mot de passe dans le champ `Nouveau code`  

<img src="..\img\digiAction_change_password.png" width="60%" />    
 
==> ici, s'il existe un utilisateur `Test` sur l'équipement `DigiNew` alors son code sera mis à jour avec `01A99`

Attention, le code doit respecter la norme uniquement des chiffres de 0 à 9 ainsi que les lette `A` et `B`, sans quoi la mise à jour ne sera pas effectuée.

<br/>  
<br/>  

## A quoi sert le mode panic ? Comment s'en servir ?  

Le `mode panic` permet de réaliser les actions "classique" d'un mode, mais en plus d'y ajouter certaines actions qui ne seront exécutés que si le code saisi pour activer le mode a été paramétré comme `panic`. 
En cas de soucis, on peut par exemple pour vouloir désactiver l'alarme mais envoyer un message SOS à un proche.

Lors de la défition des actions sur un mode, vous pouvez cocher la case "panic", dans ce cas la sécurisation du mode via mot de passe est obligatoire.  
L'inverse est également vrai : en désactivant la sécurisation du mode, cela désactivera l'ensemble des actions 'panic'.  

Lorsqu'un `code panic` est utilisé, les tests de `Pré-Check` <b>ne sont pas</b> effectués, l'ensemble des actions y compris celles flaggués `panic` sont directement réalisées. 
# Plugin Toshiba AC Control


Ce plugin permet de gérer vos climatiseurs Toshiba, connectés via un Adaptateur Wi-Fi (`RB-101S-G`, `RB-102S-G`, ...).  

<img src="..\img\widget_brut.png" width="50%" />

<br/><br/>

# Configuration du Plugin

La configuration des équipements Toshiba AC est accessible à partir du menu `Plugins`, sous la catégorie `Confort`, et se fait en 3 étapes :  
1. installez les dépendances  
2. indiquez le nom d'utilisateur et le mot de passe que vous avez paramétrés sur votre application Toshiba. Il est recommandé de ne pas modifier le port par défaut. 
3. démarrez le démon ! 

Si tout est vert, alors tout va bien ! :)  
  
<img src="..\img\settings_page.png" />    
<br/><br/>


# Ajout des Climatiseurs

Les climatiseurs doivent être ajoutés sur votre compte Toshiba, depuis l'application Toshiba dédiée.  
Le plugin récupère les appareils déjà enregistrés sur l'application et créé les équipements correspondant sur Jeedom.  

Pour se faire, il vous suffit de cliquer sur le bouton `Scan` sur la page principale du plugin.     
<br/>
<img src="..\img\main_page.png" width="80%" />  

<br/>
Les équipements seront automatiquement remontés :    

<br/>
<img src="..\img\clim_added.png" width="50%" />  

<br/><br/>


# Liste des Commandes 

### Actions 
Les commandes suivantes règlent différentes fonctionnalités du climatiseur :  
- `Marche` : met le climatiseur en marche
- `Arrêt` : arrête le climatiseur
- `Température` : permet de régler la consigne de la température souhaitée
- `Mode` : règle le mode du climatiseur : chauffage, refroidissement, séchage, ventilation, automatique
- `Ventilation` : détermine la puissance de soufflerie
- `Oscillation` : rythme le mode d'oscillation de la soufflerie
- `Puissance` : modère la puissance de l'unité : 100%, 75% ou 50%
- `Fonctionnalités avancées A` / `Fonctionnalités avancées B` : gère certaines fonctionnalitées avancées disponibles sur le climatiseur
- `Air Pure` : (dés)active le mode air pure de l'unité

### Infos 
Les commandes suivantes permettent de récupérer différents éléments de l'état du climatiseur :  
- `Etat` 
- `Auto-nettoyage` 
- `Aire Pure ION` 
- `Mode actif` 
- `Temperature (consigne)` 
- `Température int. (sonde)` 
- `Température ext. (sonde)` 
- `Ventilation active` 
- `Oscillation actif` 
- `Puissance active` 
- `Fonctionnalité avancée active (A)` 
- `Fonctionnalité avancée active (B)` 


<br/><br/>


# Options  

## Offset  

Si vous constatez une différence entre la température remontée par votre clim et la température réelle de votre pièce, vous pouvez indiquer un `offset` sur chacun de vos appareils. Cette différence (positive ou négative) est ajoutée à la température du climatiseur, et à la consigne envoyée à l'appareil. 
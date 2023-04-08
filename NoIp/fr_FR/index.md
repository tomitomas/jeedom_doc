# Plugin No-Ip Renew

Ce plugin permet de renouveler automatiquement vos noms domaine gratuits no-ip.com.
Ces domaines expirent tous les 30 jours et sont définitivement supprimés si ils ne sont pas renouvelés à temps.  
*Auteur original @hugoKs3*

# Installation

Ce plugin se repose sur un [script Python](https://github.com/loblab/noip-renew) développé par [loblab](https://github.com/loblab) et adapté pour Jeedom.
Ce script Python requiert les dépendances suivantes qui seront automatiquement installées :

- python3
- python3-pip
- chromium-chromedriver / chromium-driver / chromedriver
- chromium-browser
- selenium

# Configuration

## Cron

Le plugin a sa propre tâche planifiée.
Elle s'exécute tous les jours à une heure et minute aléatoires.
Jusqu'à ce que la date d'expiration soit atteinte, le plugin ne peut pas renouveler le domaine. Il récupèrera juste les différentes informations.
Quand la date d'expiration est atteinte (ou proche de l'être en fonction de votre configuration, voir plus bas), le plugin renouvellera le nom de domaine.

## Configuration du plugin

Sur la page de configuration du plugin, vous pouvez choisir :

- quand le plugin est supposé renouveller vos noms de domaine (par défaut, 7 jours avant expiration mais vous pouvez choisir moins).
- la pièce par défaut dans laquelle chaque domaine sera créé

## Configuration des équipements

Pour accéder aux différents équipements **No-Ip**, allez dans **Plugins → Monitoring → No-Ip Renew**

Cliquer sur "Ajouter un compte No-Ip".

Sur la page de l'équipement, renseignez votre login et mot de passe no-ip.com.

Cliquez sur "Scanner" pour récupérer vos domaines.

Pour chaque domaine, un équipement dédié sera créé.

# Utilisation

Pour chaque compte No-Ip, les commandes suivantes sont disponibles :

- refresh pour forcer un rafraîchissement (et éventuellement un renouvellement)
- La date et heure à laquelle le prochaine vérification automatique s'exécutera
- le statut de synchro du compte: `ok` si la synchro s'est correctement passé, `error` s'il y a eu un soucis. Dans le cas où la synchro serait KO vous avez la possibilité de demander au plugin de relancer un scan 5min plus tard, sans attendre le prochain lancement qui pourrait n'avoir lieu que 24h plus tard.

Pour chaque domaine, les commandes suivantes sont disponibles :

- le nom de domaine
- le nombre de jours avant expiration
- le statut de renouvellement : `ok` si correctement renouvelé ou si pas encore expiré, `warning` si le nombre de jours avant expiration est inférieur à 7, `error` si le renouvellement a échoué (très probablement parce qu'une intervention mannuelle est nécessaire)
- la date d'expiration
- l'adresse ip auquel le dns est lié

Un template de widget est également disponible pour visualiser vos domaines ainsi que leurs status.

# Rafraichissement des IP

Vous avez la possibilité de faire vérifier que l'ip rattachée à votre nom de domain est toujours à jour. Toutes les 15 minutes une tâche check que l'ip enregistrée sur votre domaine est bien la même que celle que vous avez configuré sur votre équipement :

- soit votre ip actuelle récupérée automatiquement,
- soit une ip que vous aurez vous-même fixée

# Limitations

Parfois, le renouvellement échouera car une vérification captcha est nécessaire. Il faudra le faire "manuellement" en se connectant sur votre espace No-Ip. Dans ce cas, la commande "renew" du domaine concerné retournera "error". Je vous encourage à configurer une alerte sur cette commande afin d'être prévenu.

# Contributions

Ce plugin gratuit est ouvert à contributions (améliorations et/ou corrections). N'hésitez pas à soumettre vos pull-requests sur <a href="https://github.com/hugoKs3/plugin-noip" target="_blank">Github</a>

# Credits

Ce plugin s'est inspiré des travaux suivants :

- [loblab](https://github.com/loblab) via son [noip-renew Python script](https://github.com/loblab/noip-renew)

# Disclaimer

- Ce plugin ne prétend pas être exempt de bugs.
- Ce plugin vous est fourni sans aucune garantie. Bien que peu probable, si il venait à corrompre votre installation Jeedom, l'auteur ne pourrait en être tenu pour responsable.

# ChangeLog

Disponible [ici](./changelog.html).

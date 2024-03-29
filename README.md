[![GitHub ajouter le bot](https://img.shields.io/badge/discord-ajouter%20le%20bot-5865F2)](https://discord.com/api/oauth2/authorize?client_id=1054704035892051988&permissions=414464743488&scope=bot) ![GitHub last commit](https://img.shields.io/github/last-commit/thibaultdelgrande/botRappelConso) ![GitHub code size in bytes](https://img.shields.io/github/languages/code-size/thibaultdelgrande/botRappelConso) ![GitHub](https://img.shields.io/github/license/thibaultdelgrande/botRappelConso) ![GitHub top language](https://img.shields.io/github/languages/top/thibaultdelgrande/botRappelConso) ![Libraries.io dependency status for GitHub repo](https://img.shields.io/librariesio/github/thibaultdelgrande/botRappelConso) ![Discord](https://img.shields.io/discord/1063566210861641858)

# Rappel Conso

Code source de bot Discord permettant d'afficher et de recevoir les derniers rappels conso

https://rappel.conso.gouv.fr/

## Ajouter le bot


1. https://discord.com/api/oauth2/authorize?client_id=1054704035892051988&permissions=414464743488&scope=bot
2. Sélectionner le serveur discord
3. Cocher les autorisations que vous souhaitez. Pour que le bot fonctionne, sélectionner au moins `Envoyer des messages` et `Utiliser les commandes de l'application`

## Utilisation

| Commande 	| Description                                          	|
|----------	|------------------------------------------------------	|
| /rappel  	| Envoie le dernier rappel conso                       	|
| /alerte   | Active sur le channel actif les alertes rappel conso 	| 
| /desactive| Désactive sur le channel actif les alertes rappel conso|

## Installation

Installer la version LTS de NodeJS : https://nodejs.org/fr/download/

Installer les dépendances :

`npm install`

Créer un bot discord et obtenir son token : https://discord.com/developers/applications
Pour fonctionner correctement, le bot doit pouvoir :

* Créer des commandes
* Envoyer des messages

Créer le fichier config.json à la racine et ajouter ceci à l'intérieur :
```
	{
		"token": "TOKEN-DU-BOT-DISCORD",
		"client_id": "CLIENT_ID-DU-BOT-DISCORD"
	}
```

Le CLIENT_ID se trouve dans OAuth2 -> General, sous la section Client Information, dans les paramètres de votre application Discord.
Le TOKEN se trouve dans Bot sous la section Build-A-Bot, dans les paramètres de votre application Discord. Il se peut que vous deviez regénérer votre TOKEN.

Si vous souhaitez ajouter la commande /alerte, créer un fichier db.json à la racine si il n'existe pas déjà, et ajouter ces valeurs :
```
	{
		"last_id": [],
		"channels": []
	}
```

Démarrer le bot avec la commande :

`npm start`
  

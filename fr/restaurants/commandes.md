---
lang: fr
role: restaurant
title: Gestion des commandes
ref: restaurant-order
---

---
<br>

## Commandes

#### **L'écran principal est organisé de la manière suivante :**

![restaurant's interface for orders](/assets/images/resto_order_list_fr.png)

- **Par date (celle du jour par défaut) :**
<br>
	Permet également d'avoir un historiques des commandes des jours précédants et futurs en sélectionnant la date de son choix via le calendrier en cliquant sur le boutton suivant
	![date button](/assets/images/resto_date_fr.png).
- **Par section :**
	- **Nouvelles commandes :**
	<br>
	Ici apparaît toutes les nouvelles commandes client en attente de validation de votre part.
	<br>
	Vous pouvez également la refuser, s'offrent alors à vous trois choix :
		- Je suis en rupture de stock
		<br>
		Cette commande sera annulée et vous continuerez à recevoir de nouvelles commandes.
		- Je suis en plein rush
		<br>
		Cette commande sera annulée et vous continuerez à recevoir de nouvelles commandes.
		- Je vais fermer
		<br>
		Cette commande sera annulée et vous ne recevrez plus de nouvelles commandes.
	- **Commandes acceptées :**
	<br>
	Ici s'affichent toutes les commandes acceptées.
	<br>
	A partir de cette étape, si tout se passe bien vous n'avez qu'à préparer la commande, attendre le livreur et automatiquement la commande passera dans la section ci-dessous [commande livrée](#commande-livree).
	<br>
	Dans le cas contraire vous pouvez : 
		- Retarder la commande :
			- De 10 minutes.
			- De 20 minutes.
			- De 30 minutes.
		- Annuler la commande :
			- Annulée par le client
			<br>
			Cette commande sera annulée et vous continuerez à recevoir de nouvelles commandes.
			- Je suis en rupture de stock
			<br>
			Cette commande sera annulée et vous continuerez à recevoir de nouvelles commandes.
			- Je suis en plein rush
			<br>
			Cette commande sera annulée et vous continuerez à recevoir de nouvelles commandes.
	- **Commandes annulées :**
	<br>
		Ici est listé l'ensemble des commandes qui ont été annulées.
	- **<span id="commande-livree">Commandes livrées :</span>**
	<br>
		Ici est listé l'ensemble des commandes qui ont livrées.

Dans chacunes des sections, les commandes sont représentées par leur id, le total de la commande et l'heure à laquelle il faut commencer à la préparer. Pour accéder aux détails de la commande et intéragir avec celle-ci, il suffit de cliquer dessus.

**A noter que vous pouvez à tout moment via le boutton ![resfresh](/assets/images/resto_refresh_btn_fr.png)  rafraîchir la page à la date du jour.**
<br>
<br>
<br>

---
<br>

## Réglages 

#### **Les réglages sont accessibles via l'icône ![settings](/assets/images/resto_param_icon.png) en haut à droite de la page. Ils se décomposent en deux parties :**

- **Passer en mode rush** :
<br>
	Quand le mode rush est activé vous ne recevez plus aucunes commandes, pour de nouveau continuer à recevoir des commandes, désactivez le.
- **Gérer les produits** :
<br>
	Dans cette partie, vous pouvez voir une liste de tous les produits qui composent votre carte et la possibilité de désactiver chacuns d'eux.
	Cette fonction permet de retirer un produit de la carte visible par le client, cela peut vous être utile si par exemple vous êtes en rupture de stock sur un ingrédient indispensable à la préparation d'un plat. 
	Par défaut, tous les produit sont activés.
	
<br>
<br>

---
<br>

## Fermeture et réouverture en ligne de votre restaurant

Ce boutton ![power button icon](/assets/images/resto_power_icon.png) vous permet d'afficher votre restaurant comme fermé sur l'interface du client, il ne pourra donc plus passer de commandes.
<br>
Pour remettre le restaurant sur le statut "ouvert", il vous suffit de cliquer sur le boutton fermer ![close button icon](/assets/images/resto_close_banner_icon.png) de la bannière ci-dessous qui apparaît après avoir fermer votre restaurant.
<br>
<br>
![restaurant is closed banner](/assets/images/resto_closed_banner_fr.png)

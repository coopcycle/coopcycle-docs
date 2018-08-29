---
title: Commandes
lang: fr
role: admin
ref: admin-orders
---

L’onglet de commande affiche les commande passées depuis la plateforme par des clients. Elle permet de gérer les commandes des restaurants.

Il existe deux types de commandes :

* commandes foodtech, passées par des clients finaux
* commandes pour des livraisons, passées via le formulaire embarqué par exemple.

Une commande peut avoir les statuts suivants :

* Nouveau, la commande n’a pas encore été acceptée par le restaurateur
* Acceptée, la commande est en cours de préparation
* Refusée, la commande a été refusée
* Prête, la commande est en attente du livreur ou en cours de livraison
* Fait, la commande a été livrée
* Annulée, la commande a été annulée par le client ou le restaurateur

## Liste des commandes

![Commandes]({{ "/assets/images/orders_fr.png" | absolute_url }})

La liste des commande affiche l’ensemble des commande en cours sur la plateforme. Vous pouvez afficher les commandes annulées en cochant la case “afficher les commandes annulées”.

L’administrateur a la possibilité d’annuler la commande en cliquant sur le bouton `Annuler` d’une commande. Les information affichées sont les suivantes :

* id, le numéro de la commande
* le type de commande
* le client qui a demandé la commande
* l’état de la commande
* le montant total facturé au client
* la facture correspondante, téléchargeable au format PDF
* la date de création
* le bouton d’annulation de la commande.

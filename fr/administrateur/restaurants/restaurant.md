---
title: Restaurant
lang: fr
role: admin
ref: admin-restaurant
---

L’onglet `Restaurants` affiche l’ensemble des restaurants créés sur l’instance. La liste est composée des éléments suivants :
- ID, lien vers le restaurant
- Nom du restaurant
- Adresse
- Horaires d'ouverture

# Gestion d'un restaurant

Les différentes pages de gestion d'un restaurant sont accessibles depuis la page du restaurant.

![Restaurant]({{ "/assets/images/restaurant_detail_fr.png" | absolute_url }})

## Informations du restaurant

### Contrat

### Compte Stripe

## Commandes du restaurant

Toutes les commandes d’un restaurant sont disponibles dans l’onglet “commande” du restaurant. Elles sont listées dans le volet gauche par date de traitement. Une commande possède un identifiant unique, un état (nouveau, validée, prête, annulée), une date de préparation avec un horaire, un résumé ainsi qu’un prix TTC. Cliquez sur un commande présente dans la liste pour afficher ses informations.

Dans le volet de droite sont affichées les informations de la commande sélectionnée. Les plats y sont listés ainsi que le calcul des taxes. Enfin, les boutons permettent au restaurateur/administrateur d’accepter ou de refuser la commande. Après l'avoir indiqué "acceptée", le restaurateur doit indiquer que la commande est prête. Il peut encore à ce stade annuler la commande. Une fois que cette dernière a été notifiée comme prête, il n’est plus possible d’annuler une commande.

## Planning d’ouverture / fermeture du restaurant

Cette fonctionnalité permet de fermer temporairement un restaurant. Les fermetures programmées sont visibles sur le calendrier.

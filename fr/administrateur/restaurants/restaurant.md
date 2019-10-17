---
title: Gestion des restaurants
lang: fr
role: admin
ref: admin-restaurant
parent: Restaurants
grand_parent: Guide de l'administrateur
nav_order: 2
---

# Gestion des restaurants

## Informations du restaurant

Les informations générales du restaurant sont accessibles et modifiables à tout moment sur la page d'accueil de ce dernier ou depuis un onglet en cliquant sur le lien portant le nom du restaurant en haut à gauche de la page.

Vous trouverez également sur cette page **les termes du contrat** entre le collectif local de livraison et le restaurant. Ils couvrent les aspects suivants :

- Zone de livraison
- Prix de la livraison
    - Forfait ou pourcentage
    - Part à la charge du.de la restaurateur.rice
    - Part à la charge du.de la client.e final.e
- Montant minimum du panier
- Frais de paiement (Stripe) : payés par la plateforme ou le.la restaurateur.rice

## Les pages de gestion

Les différentes pages de gestion d'un restaurant sont représentées par des onglets dans le coin supérieur droit de la page du restaurant.

![Restaurant]({{ "/assets/images/restaurant_detail_fr.png" | absolute_url }})

- [Produits](#produits)
- [Options](#options-et-suppléments--ajouter-un-nouveau-supplément)
- [Menus](#menus)
- [Commandes](#commandes)
- [Planning](#planning-douverture--fermeture-du-restaurant)

### Produits

La liste des produits permet d’enregistrer les différents produits que le restaurant livre. Le restaurateur doit créer les plats qu’il rend disponible sur la plateforme :
- le nom du produit
- la description
- l'activation ou non du produit
- le prix et la taxe appliquée

Un produit peut avoir plusieurs options associées (voir ci-dessous), qu'il faut créer auparavant. Par exemple un choix de sauce ketchup, mayonnaise, blanche pour une part de frites.

### Options et suppléments / ajouter un nouveau supplément

Les options permettent de rendre les produits configurables. Elles permettent par exemple d'ajouter des suppléments, ou de choisir les éléments d'un menu (accompagnement, boissons). Un supplément est une liste de produits assigné à un produit du menu.

![Option]({{ "/assets/images/option_fr.png" | absolute_url }})

Cette liste a les caractéristiques suivantes :
- Nom
- Méthode du calcul du prix
    * Gratuit, pas de prix additionnel pour le supplément
    * Prix fixe quelque soit le choix, le prix est le même quelque soit le supplément choisi
    * Prix en fonction du choix, le prix est variable en fonction sur supplément choisi
- Checkbox: le supplément est-il optionnel ou non?

Il faut au préalable créer les suppléments nécessaires dans l’onglet dédié grâce au bouton “ajout” avant de pouvoir les associer à un produit.

Pour assigner un supplément à un produit, il suffit de l’activer dans un produit de votre restaurant. Allez dans l’onglet “produit” de votre restaurant, puis cliquez sur le bouton “modifier” du produitd e votre choix,

En bas de chaque option de produit, vous retrouvez les suppléments que vous avez créé précédemment. Vous n’avez qu’à cocher celui ou ceux de votre choix.

### Menus

Chaque restaurateur peut depuis son backoffice gérer sa carte de manière autonome. Les restaurants disposent de la possibilité de créer plusieurs menus et d’activer celui qui correspond au besoin du moment.

![Menu]({{ "/assets/images/menus_fr.png" | absolute_url }})

#### Créer un menu

Dans l’onglet “Menus”, vous pouvez créer autant de menu que vous le souhaitez. Cela vous permet de configurer à l’avance des menus et d’activer facilement celui qui convient au moment nécessaire.

Pour créer un menu, cliquez sur le bouton Ajouter. Puis indiquez simplement le nom de votre menu et cliquez sur “enregistrer”. Votre menu est prêt à être configuré ! Vous pouvez ensuite activer votre menu en cliquant sur le bouton “Activer”. Un menu est indiqué comme activé grâce à une coche située à coté de son nom.

#### Ajouter une section de menu

Pour configurer votre menu, vous devez dans un premier temps ajouter une ou plusieurs sections de menu. Par exemple : Entrée, plat, dessert. Pour ce faire, entrez le nom de la section que vous souhaitez créer et cliquez sur “Ajouter une section”.

#### Configuration d’un menu

Utilisez l'éditeur de menu pour composer les ajouter ou retirer des produits du menu en les glissant - voir ci-dessous pour la création d'un produit. Pour les rendre disponibles à la vente vous n’avez qu’à glissez-déposez les produits dans les sections sur la gauche. Si vous souhaitez retirer un produit de la vente, déposez-le dans la section « Produits » à droite.

N'oubliez pas de cliquer sur le bouton « Enregistrer les modifications ».


### Commandes

Toutes les commandes d’un restaurant sont disponibles dans l’onglet “commande” du restaurant. Elles sont listées dans le volet gauche par date de traitement. Une commande possède un identifiant unique, un état (nouveau, validée, prête, annulée), une date de préparation avec un horaire, un résumé ainsi qu’un prix TTC. Cliquez sur un commande présente dans la liste pour afficher ses informations.

Dans le volet de droite sont affichées les informations de la commande sélectionnée. Les plats y sont listés ainsi que le calcul des taxes. Enfin, les boutons permettent au restaurateur/administrateur d’accepter ou de refuser la commande. Après l'avoir indiqué "acceptée", le restaurateur doit indiquer que la commande est prête. Il peut encore à ce stade annuler la commande. Une fois que cette dernière a été notifiée comme prête, il n’est plus possible d’annuler une commande.

### Planning d’ouverture / fermeture du restaurant

Cette fonctionnalité permet de fermer temporairement un restaurant. Les fermetures programmées sont visibles sur le calendrier.

---
title: Gerer un restaurant
lang: fr
ref: admin-restaurant
parent: Guide du restaurant
nav_order: 2
redirect_from:
  - /fr/administrateur/restaurants/gerer-un-restaurant.html
---

# Gérer un restaurant

Les différentes pages permettant de gérer un restaurant sont représentées par les onglets en haut à droite de la page du restaurant sur la plate-forme.


![Restaurant]({{ "/assets/images/restaurant_detail_fr.png" | absolute_url }})

- [Produits](#produits)
- [Options](#options-et-suppléments)
- [Menus](#menus)
- [Commandes](#commandes)
- [Horaires](#gestion-des-horaires--Fermer-temporairement-un-restaurant)


### Produits

La liste des produits vous permet de créer les différents produits que le restaurant peut être amené à vendre. Pour chacun de ces produits, il vous faudra préciser
- le nom du produit
- une description du produit (ingrédients, nombre de pièces...)
- déterminer si le produit est activé ou non (cela vous permet de ne plus le rendre disponible en cas de rupture de stock)
- le prix et la catégorie de TVA qui lui est appliquée. (le prix HT se calcule automatiquement après avoir saisi le TTC et la TVA concernée)
- les allergènes (Attention, le restaurant est responsable de la bonne information aux consommateurs des allergènes présents dans ses produits)
- les régimes particuliers auxquels le produit répond (végétarien, vegan, halal, sans gluten...) pour faciliter l'orientation des consommateurs sur la plate-forme.

### Options et suppléments / Ajouter des suppléments

Un produit peut avoir plusieurs options qui lui sont associées. Ces options doivent être créées auparavant dans l'onglet "options" du restaurant.
Ces options peuvent être autant des choix inclus dans le menu. Par exemple la sauce (ketchup/mayonnaise/harissa) mais elles peuvent aussi être des suppléments par exemple "avec votre burger, choisissez l'option frites (+0€) ou l'option onion rings (+1€)".

Les options permettent donc de configurer comme vous le souhaitez vos produits.

![Option]({{ "/assets/images/option_fr.png" | absolute_url }})

Il vous faudra donc remplir pour chaque option:
- Le nom
- Le prix de l'option:
  - Gratuit (cas typique d'une sauce par exemple)
  - Un prix fixe quel que soit le choix par exemple dans le cas où vous suggérez une option payante au client.
  - Un prix variable, en fonction de l'option choisie. (Exemple de boisson gratuite dans un menu, mais un supplément de 1€ pour une bière)
- Déterminer si l'option est additionnelle ou non.
      -Si vous ne cochez pas la case, cela forcera le client à choisir une des options (par exemple la cuisson d'une viande).
      -Cocher la case signifie que l'option est additionnelle, donc qu'elle permet de:
          -Choisir une valeur minimale de 0, permettant au client de ne pas choisir d'option.
          -Choisir une valeur maximale de X, permettant au client de faire plusieurs choix dans la limite de X. (par exemple, plusieurs choix gratuits de sauce "je souhaiterais du ketchup, de la mayonnaise et de la harissa, ou autre exemple, cumuler les suppléments payants "bacon (+1,5€) et onion rings (+1€) + extra steak (+2€).

L'option devra être configurée avant de pouvoir l'assigner à un produit. Pour assigner une option/un supplément, il vous faudra simplement l'activer dans le produit auquel il se réfère en "modifiant" le produit et cochant les cases correspondant aux options que vous voulez activer sur le-dit produit.

### Menus

Chaque restaurateur peut gérer sa propre carte depuis le backoffice de la plate-forme. Chaque restaurant peut créer autant de menus qu'il le souhaite et d'activer ceux qu'il souhaite au moment souhaité.

![Menu]({{ "/assets/images/menus_fr.png" | absolute_url }})

#### Créer un menu

Dans l'onglet "Menu", créez autant de menus que souhaités. Cela vous permet de les préparer à l'avance et de les activer au besoin.

Un menu fait référence à une "carte" de produits spécifiques qu'il est possible d'activer/désactiver selon votre souhait. Par exemple: carte du midi, du soir, Saint Valentin, Carte été, printemps, automne, hiver...
Pour créer un menu, cliquer sur Ajouter. Il suffit ensuite de choisir le nom, de le sauvegarder, et il est ensuite prêt à être configuré. Pour le mettre en ligne et permettre aux clients de commander cette carte, il faut bien penser à activer le menu. Un menu activé doit avoir une check mark à sa gauche.

#### Ajouter une section à un menu.

Pour configurer un menu, vous devez d'abord ajouter une ou plus probablement plusieurs sections. Il peut s'agir de sections "classiques" telles que "entrées" "plats principaux" ou "desserts" mais il est possible d'ajouter d'autres sections telles que des menus "Entrée/Plat/Dessert" tout inclus, des "spécialités de la maison" ou tout autre section qui vous paraisse pertinente. Il vous suffit de nommer les sections qui apparaissent ensuite sur la gauche de l'écran de votre menu.

#### Configurer un menu

Utilisez l'éditeur de menu pour composer celui-ci. Il vous suffit de choisir dans votre liste de produits lesquels attribuer à chaque section de votre menu et faire glisser ces produits dans les sections appropriées. (voir plus loin pour créer un produit). Si vous souhaitez retirer le produit d'une section, faites l'opération inverse et faites glisser le produit de la section vers la liste des produits.
N'oubliez pas de cliquer sur "Sauvegarder" en bas de page après avoir constitué votre menu.

Veuillez noter qu'à ce stade, il est plus confortable de créer l'ensemble des produits relatifs à une section, et les faire glisser ensuite dans la section, plutôt que de rentrer tous les produits puis de les assigner aux sections appropriées (surtout si votre carte est longue).

### Commandes

Toutes les commandes d'un restaurant sont listées dans l'onglet "commandes" du restaurant, chronologiquement. Chaque commande a une référence unique, un statut (nouvelle, acceptée, livrée, annulée, refusée). Les commandes ont aussi un temps de préparation et une heure à laquelle elles doivent être prêtes, un résumé, et un prix incluant les différents niveaux de TVA. Il suffit cliquer sur une commande pour faire apparaitre l'ensemble des informations relatives à cette commande.

Une fois que vous avez cliqué sur une commande, sur la gauche se situent les informations ci-dessus, et sur la droite, la carte représentant le lieu de livraison du client. Sur cette page, la coopérative de livreurs et le restaurant ont la possibilité d'accepter ou de refuser la commande. Une fois acceptée, une commande ne peut plus être refusée.
Vous pouvez aussi activer le mode "rush" sur cette page. Le mode "rush" double les temps de préparation que vous aurez renseigné pour le mode "normal".

### Heures d'ouvertures / Planning

En cliquant sur "plus d'options" puis sur "planning", vous avez la possibilité de procéder à des fermetures temporaires de votre restaurant sur la plate-forme. Cela peut vous permettre de suspendre la collaboration avec la coopérative dans le cas où vous fermez, où dans le cas où votre travail en salle ne vous permet pas d'assurer la livraison.
Pensez à prévoir autant que possible vos fermetures sur la plate-forme pour éviter d'avoir à refuser des commandes, jamais agréable pour un consommateur.

### Comportement des heures d'ouverture.

Dans "Exécution", sous la photo de votre restaurant dans l'onglet d'accueil, vous avez la possibilité de déterminer comment le client peut choisir son mode de livraison.
"Au plus tôt" permet au client de commander pour le plus vite possible, temps qui tiendra compte à la fois du temps de préparation et du temps de livraison.
"Tranche horaire" permet au client plutôt de choisir un créneau horaire à déterminer à l'avance pour la livraison.

### Délai additionnel pour les prises de commande

Cette option vous permet de forcer le client à commander avec un délai pour vous permettre d'anticiper. Par exemple si vous souhaitez avoir un jour pour vous organiser, il vous suffit de noter 1 dans jour et 0 dans heures.

### Nombre de choix pour la livraison (en jours)

Ce paramètre détermine le nombre de jours où il est possible de commander en avance.

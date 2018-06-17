---
layout: page
title: Tableau de bord
lang: fr
nav_order: 1
---

Le tableau de bord d’administration (appelé dashboard dans ce document) permet de contrôler l’ensemble des fonctionnalités de création et de gestion des tâches ainsi que de gérer le dispatch des coursiers manuellement. Il est possible de l’afficher en plein écran en cliquant sur le bouton FullScreen comme illustré ci-dessous.

Menu principal du dashboard
Menu supérieur
Panneau latéral
Zone “Unassigned” (tâches par encore assignées)
Zone “Assigned” (tâches assignées à des coursiers)
Carte interactive

## Créer, assigner et éditer une tâche

Une tâche est crée en cliquant sur le bouton + de la section “Unassigned” du dashboard. Un popup s’ouvre et permet de configurer la tâche. Trois actions sont possible pour une tâche :
- Ajouter, qui permet de créer une tâche
- Editer, qui permet de changer ou de vérifier l’état et l’historique d’une tâche
- Terminer la tâche, qui permet le changement de statut de la tâche en :
  - To Do (à faire)
  - Success (réussie)
  - Failure (échec)

Tant qu’une tâche n’est pas assignée à un coursier, cette dernière reste dans la section “Unassigned”.

## Ajouter / créer une tâche

Les informations suivantes sont disponibles afin de créer une tâche :
Checkbox : type de tâche
Pickup (Récupérer)
DropOff (Déposer)
Champ : adresse du point de dépôt ou de retrait
&plus; plus d'options
Champ : Code postal (remplissage automatique)
Champ : Ville (remplissage automatique)
Champ : Étage
Champ : instructions
Dropdown : créneau de réalisation
Date de début
Date de fin
Dropdown: choisir un tag
Editer la tâche
Les mêmes informations que "ajouter" sont disponibles à l’édition. En plus de  celle-ci il est possible :
Dropdown : Assigner un coursier
Dropdown : Voire l'historique

## Terminer la tâche

Pour terminer une tâche, il suffit de cliquer sur le bouton “finish task” présent en haut à droite de la fenêtre de popup. Les fonctionnalités disponibles sont :
Dropdown: "à faire", "échouée", "réussie"
Champ : Note de fin

## Voir le coursier connecté sur l'instance

Lorsqu’un coursier se log sur l’application et qu’il donne sa position GPS à cette dernière, il apparaît dans la liste d’ajout au planning du tableau de bord et le dispatcheur peut l’assigner à des tâches dès lors.
Ajouter un coursier au planning
Ajouter un coursier au planning signifie qu’il est disponible pour être assigné à des tâches et donc à livrer des commandes. Afin d’ajouter un coursier au planning, il faut cliquer sur le bouton + (plus) de la section “Assigned”. Le choix de l’ajout au planing se fait par le biais d’un drag and drop.
Assigner une tâche à un coursier
S’il est possible d’assigner un coursier à une tâche à partir du popup de création ou d’édition d’une tâche, il est bien plus commode d’utiliser la fonction de drag’n drop du dashboard à déposer directement dans la zone d’assignation d’un coursier.

## Créer une tâche

La tâche apparaît dans la section “Unassigned”
Le dispatcheur drag la tâche sur un coursier préalablement ajouté au planing

## Obtenir l’information d’une livraison

Dès lors que deux tâches sont assignées à un coursier, une livraison est créée. Plusieurs informations sont disponibles :
L'estimation de la durée de la livraison ;
La distance à parcourir (par rapport au tracé de l’itinéraire) ;
Bouton : Afficher / masquer le tracé de livraison, qui est l’itinéraire proposé au coursier pour la livraison.
Donner un ordre d’exécution d'une tâche à un coursier
Le dispatcheur peut optimiser le parcours de livraison du coursier en déplaçant les courses dans la pile de tâche qui sont assignées à ce dernier. Dans l’ordre, le premier dans la pile sera le premier point d’itinéraire pris en compte et ainsi de suite jusqu’à la fin de la pile.
Le dispatcheur drag une tâche dans la pile
Il la drop à un autre endroit de la pile pour la réorganiser

## Créer un tag et tagger une tâche

Les tags sont des valeurs que l’on peut assigner à une tâche afin de les trier dans le tableau de bord. Un tag est composé d’un titre et d’une couleur. Afin de pouvoir assigner un tag à une tâche, il faut d’abord créer les tags dont le dispatcheur a besoin. Pour ce faire :
Aller dans le panneau de configuration, rubrique “Tag” ;
Créer un tag en cliquant sur le bouton “Create a new tag” ;
Donner un nom et une couleur au tag ;
Valider.


Dans le Dashboard, le dispatcheur retrouvera les tags en créant une tâche ou en l’éditant :
Cliquer sur le bouton “Ajouter un tag (roue cranté)” ;
Ajouter le tag ;
Il est possible d’assigner plusieurs tags à une tâche.
Manipuler les différents filtres
Différents filtres sont applicables afin de trier les tâches. Il est possible de :
Dropdown : Filtrer par statut de tâche :
Tâches terminées
Tâches non-taguées
Par tag

## Dropdown calendrier : Filter par jours

Afin de filtrer par statut de tâche, il suffit d’utiliser le menu déroulant de filtre dans le menu supérieur du dashboard. Afin de filtrer par jour, il suffit d’utiliser le calendrier déroulant au même endroit. Il est possible de cumuler les filtres.
Importer les tâches (en fichier CSV de traitement par lot)
Pour éviter de créer manuellement un grand nombre de tâches, il est possible de les importer en masse via un fichier CSV. Sur le tableau de bord, cliquez sur le bouton « Importer » : une fenêtre s'ouvre pour permettre d'uploader un fichier. Vous devez au minimum spécifier une adresse pour chaque tâche, les autres colonnes sont optionnelles. Afin d’importer un fichier, cliquer sur le bouton “Import” situé dans le Dashboard sur la barre supérieure du dashboard.
Les colonnes before et after pour spécifier le créneau horaire acceptent des valeurs sous différents formats. Voici les valeurs des colonnes accompagnées d’un exemple :
Type : pickup
Nom de l’adresse : Mairie du 2e
Adresse : 1, rue de Rivoli Paris
Début du créneau (Before) :15/02/2018 12:00
Fin du créneau (After) : 15/02/2018 14:00
Commentaire : Appeler le client au 01.02.03.04.05
Tag : Important

## Exporter les tâches d'une journée (CSV)

L’exportation d’un fichier regroupant les commandes du jours se fait par le biais du bouton Export situé dans le Dashboard sur la barre supérieure du dashboard.
Fullscreen Mode
Afin de passer en mode FullScreen,  veuillez cliquer sur le bouton vert présent en haut à droite du dashboard.

---
title: Tableau de bord (dashboard)
lang: fr
role: admin
custom_scripts:
  - "https://cdnjs.cloudflare.com/ajax/libs/jquery-zoom/1.7.21/jquery.zoom.min.js"
  - "/assets/scripts/zoom.js"
---

Le tableau de bord d’administration (appelé dashboard dans ce document) permet de contrôler l’ensemble des fonctionnalités de création et de gestion des tâches ainsi que de gérer le dispatch des coursiers manuellement. Il est possible de l’afficher en plein écran en cliquant sur le bouton <span syle="line-height=10px;">![Fullscreen]({{ "/assets/images/fullscreen.png" | absolute_url }})</span>

![Tableau de bord](/assets/images/dashboard_fr.png)

## Créer, assigner et éditer une tâche

Une tâche est crée en cliquant sur le bouton + de la section `Non-assignées` du dashboard. Une popup s’ouvre et permet de configurer la tâche. Trois actions sont possible pour une tâche :
- Ajouter, qui permet de créer une tâche
- Éditer, qui permet de changer ou de vérifier l’état et l’historique d’une tâche
- Terminer la tâche, qui permet le changement de statut de la tâche en :
  - To Do (à faire)
  - Success (réussie)
  - Failure (échec)

Tant qu’une tâche n’est pas assignée à un coursier, cette dernière reste dans la section `Non-assignées`.

## Ajouter / créer une tâche

Les informations suivantes sont disponibles afin de créer une tâche :
* Checkbox : type de tâche
    - Pickup (Récupérer)
    - DropOff (Déposer)
* Champ : adresse du point de dépôt ou de retrait
* `+` : plus d'options
    - Champ : Code postal (remplissage automatique)
    - Champ : Ville (remplissage automatique)
    - Champ : Étage
    - Champ : instructions
* Dropdown : créneau de réalisation
    - Date de début
    - Date de fin
* Dropdown: choisir un tag

## Éditer la tâche
Les mêmes informations que "ajouter" sont disponibles à l’édition. En plus de  celle-ci il est possible :
* Dropdown : Assigner un coursier
* Dropdown : Voire l'historique

## Terminer la tâche

Pour terminer une tâche, il suffit de cliquer sur le bouton “finish task” présent en haut à droite de la fenêtre de popup. Les fonctionnalités disponibles sont :
* Dropdown: "à faire", "échouée", "réussie"
* Champ : Commentaire sur la réalisation de la tâche

## Voir le coursier connecté sur l'instance

Lorsqu’un coursier se connecte sur l’application et que sa localisation est activée, un marqueur indiquant sa position est affiché sur le dashboard.

## Ajouter un coursier au planning

Ajouter un coursier au planning signifie qu’il est disponible pour être assigné à des tâches et donc pour livrer des commandes. Afin d’ajouter un coursier au planning, il faut cliquer sur le bouton `+` de la section `Assignées`.

## Assigner une tâche à un coursier

S’il est possible d’assigner un coursier à une tâche à partir du popup de création ou d’édition d’une tâche, il est bien plus commode d’utiliser la fonction de drag’n drop du dashboard: déposer la tâche directement dans la zone d’assignation d’un coursier.

## Créer une tâche

La tâche apparaît dans la section `Non-assignées`.
Le dispatcheur déplace la tâche sur un coursier préalablement ajouté au planning.

## Obtenir l’information d’une livraison

Dès lors que deux tâches sont assignées à un coursier, une livraison est créée. Plusieurs informations sont disponibles :
* L'estimation de la durée de la livraison ;
* La distance à parcourir (par rapport au tracé de l’itinéraire) (Bouton "carte" : Afficher / masquer le tracé de livraison, qui est l’itinéraire proposé au coursier pour la livraison)

## Donner un ordre d’exécution d'une tâche à un coursier

Le dispatcheur peut optimiser le parcours de livraison du coursier en déplaçant les courses dans la pile de tâche qui sont assignées à ce dernier. Dans l’ordre, le premier dans la pile sera le premier point d’itinéraire pris en compte et ainsi de suite jusqu’à la fin de la pile.
Le dispatcheur peut déplacer les tâches dans la pile pour les ré-organiser.

## Créer un tag et tagguer une tâche

Les tags sont des valeurs que l’on peut assigner à une tâche afin de les trier dans le tableau de bord. Un tag est composé d’un titre et d’une couleur. Afin de pouvoir assigner un tag à une tâche, il faut d’abord créer les tags dont le dispatcheur a besoin.
* Aller dans le panneau de configuration, rubrique “Tag” ;
* Créer un tag en cliquant sur le bouton “Create a new tag” ;
* Donner un nom et une couleur au tag ;
* Valider.


Dans le dashboard, le dispatcheur retrouvera les tags en créant une tâche ou en l’éditant.
* Cliquer sur le bouton `Ajouter un tag` (roue crantée) ;
* Ajouter le tag ;
Il est possible d’assigner plusieurs tags à une tâche.

## Manipuler les différents filtres

Différents filtres sont applicables afin d'afficher uniquement certaines tâches. Il est possible de filtrer par :
* Statut de tâche :
* Tâches terminées
* Tâches non-taguées
* Par tag

Il est possible de cumuler les filtres.

## Dropdown calendrier : changer de jour

Afin de changer de jour, il suffit d’utiliser le calendrier déroulant à gauche de la bar supérieure du dashboard.

## Importer les tâches via un fichier CSV

Pour éviter de créer manuellement un grand nombre de tâches, il est possible de les importer en masse via un fichier CSV. Sur le tableau de bord, cliquez sur le bouton `Importer`: une fenêtre s'ouvre pour permettre d'uploader un fichier. Vous devez au minimum spécifier une adresse pour chaque tâche, les autres colonnes sont optionnelles. Afin d’importer un fichier, cliquer sur le bouton `Importer` situé sur la barre supérieure du dashboard.

Les colonnes before et after pour spécifier le créneau horaire acceptent des valeurs sous différents formats. Voici les valeurs des colonnes accompagnées d’un exemple :
- type
- address.name
- address.telephone
- address
- adress.floor
- adress.description
- after
- before
- comments
- tags

Vous pouvez télécharger un [fichier d'exemple](https://demo.coopcycle.org/help/tasks_import.example.fr.csv).

## Exporter les tâches d'une journée (CSV)

L’exportation d’un fichier .csv résumant les commandes du jours se fait par le biais du bouton `Export` situé sur la barre supérieure du dashboard.

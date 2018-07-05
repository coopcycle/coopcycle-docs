---
layout: page
title: Concepts clés
lang: fr
nav: true
ref: key-concepts
---

Les tâches
----------

Les tâches sont la plus petite unité de travail sur la plateforme.\\
Une tâche est **une action à effectuer à une adresse géographique, sur un créneau horaire défini**.\\
Il existe deux types de tâches différentes :
- **Récupérer**, pour un retrait de marchandise
- **Déposer**, pour un dépôt de marchandise

Cette forme binaire permet de couvrir tous les scénarii du champ de la livraison à vélo.



## Récupérer et Déposer

Le livreur doit récupérer une marchandise à une adresse et l’amener à une autre adresse.\\
Les informations suivantes doivent être renseignées par le dispatcheur pour chaque tâche :
- Créneaux
- Adresse
- Commentaire

Les informations suivantes permettent de suivre l’évolution d’une tâche dans le processus de livraison :
- Statut
- Historique

Créer une livraison
-------------------

Chaque livraison est composée d’au moins deux tâches qu’un dispatcheur assigne à un livreur.
Assigner deux tâches, ou plus, à un livreur créer une livraison.
Lorsque les tâches Récupérer et Déposer sont créées, le dispatcheur assigne ces tâches manuellement dans l’ordre le plus optimal qu’il juge. La création d’une livraison est matérialisé sur la carte par le biais d’un tracé GPS qui est proposé au coursier pour la livraison.

Tarifications
-------------

La tarification se configure dans le tableau de bord d’administration grâce à un ensemble de règles basées sur les variables suivantes :
La distance qui s’évalue en mètre. Cette distance peut être défini avec les opérateurs de :
- &gt; supérieur à *variable en mètre*
- &lt; inférieur à *variable en mètre*
comprise entre deux variable

Le poids qui s’évalue en gramme. Ce poids peut être défini avec les mêmes opérateurs que la distance
La zone qui se défini grâce au chargement d’un fichier GeoJSON dans la configuration de l’instance ;
Le type de vélo qui se défini en le sélectionnant dans une liste dans laquelle sont disponibles :
Le vélo simple
Le vélo cargo

Ces règles sont organisées sous forme de pile rangée en ordre de traitement, la tarification en tête de liste sera la première à être traitée par le logiciel qui vérifiera si elle correspond aux caractéristiques de la livraison, ça ça n’est pas le cas le logiciel passera à la seconde tarification dans la liste et ainsi de suite. A chaque livraison créée, cette pile sera utilisée pour créer la tarification. Le choix s’opère automatiquement en fonction des critères spécifiés pour chaque livraison.

Par exemple, je créer une règle qui spécifie une tarification :
- dans le département du 93 avec vélo cargo placée dans le haut de la pile ;
- dans Paris intra-muros avec vélo cargo placé en milieu de pile ;
- dans paris intra-muros placée dans le bas de la pile.

Si une livraison est créé impliquant une série de tâche dans Paris intra-muros avec un vélo simple, alors la première règle sera ignorée, et la seconde utilisée comme base de livraison. Les règle les précises (c’est à dire comportant le plus de variables) doivent être en haut de la pile et celle les plus générales en bas de la pile de façon à ce que les cas particuliers soient sélectionnés par le logiciel comme base de tarification. Si, par exemple, je reprend ma liste de tarification plus haut de la manière suivante :
dans paris intra-muros ;
dans Paris intra-muros avec vélo cargo ;
dans le département du 93 avec vélo cargo.

Si une livraison dans Paris intra-muros est créée avec la nécessitée de livrer en vélo cargo, la première tarification s’appliquera car aucun type de vélo n’est spécifiée pour celle-ci et le mauvais prix sera facturé. Être précis en haute de la pile et généraliste en bas de la piste permet

Instance CoopCycle
------------------

Le logiciel CoopCycle fonctionne grâce au déploiement d’instances. Ces dernières sont des copies répliquées du logiciel qui sont autonomes les unes des autres. Cela permet à chaque ville de disposer de sa propre instances, des ses propres règles de tarifications, son espace de dispatch et de configurer le logiciel selon les besoins de chaque coopérative.

## Les rôles dans les instances

Chaque instance dispose de rôles pour ses utilisateurs :
- Administrateur
- Coursier
- Restaurant
- Magasin
- Client

A ces rôles sont assignés des droits d’usages dans la plateforme.

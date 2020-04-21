---
title: Tarifications
lang: fr
ref: pricings
parent: Fonctionnalités logistiques
grand_parent: Guide de l'administrateur
nav_order: 1
---

Dans le cadre de la création d'un compte magasin, il est possible de créer des tarifications (ex: tarification express, tarification normale) depuis la partie administration en cliquant sur l'icône <i class="fa fa-cog" aria-hidden="true"></i> puis sur la section Tarification.

![Tarification]({{ "/assets/images/config_pricing_fr.png" | absolute_url }})

Une tarification est constituée de plusieurs **règles ordonnées**. Les règles peuvent utiliser les paramètres suivants :

- La distance qui s’évalue en mètres. Cette distance peut être définie avec les opérateurs suivants :
    * `>` supérieure à *valeur en mètres*
    * `<` inférieure à *valeur en mètres*
    * comprise entre deux valeurs
- Le poids donné en grammes. Ce poids peut être défini avec les mêmes opérateurs que la distance
- La zone de livraison ([voir la page d'aide](/fr/administrateur/fonctionnalites-logistiques/configuration/zones.html) pour sa création);
- Le type de vélo qui se définit en le sélectionnant dans une liste dans laquelle sont disponibles :
    * Le vélo simple
    * Le vélo cargo

![Paramètres de tarification]({{ "/assets/images/param_pricing_fr.png" | absolute_url }})

Ces règles sont rangées par ordre de traitement. La règle en tête de liste sera la première à être testée par le logiciel qui vérifiera si elle correspond aux caractéristiques de la livraison. Si cela n’est pas le cas le logiciel passera à la seconde règle dans la liste et ainsi de suite. À chaque livraison créée, cette pile sera parcourue pour appliquer la tarification automatiquement.

Par exemple, si je crée une tarification avec les règles suivantes :

* dans le département du 93 avec vélo cargo placée dans le haut de la pile ;
* dans Paris intra-muros avec vélo cargo placé en milieu de pile ;
* dans Paris intra-muros placée dans le bas de la pile.

Si une livraison est créée pour Paris intra-muros avec un vélo cargo, alors la première règle sera ignorée. La seconde correspond à la livraison, son tarif sera donc appliqué. La seconde règle étant remplie, la troisième est ignorée.

Les règles les plus précises (c’est-à-dire comportant le plus de paramètres) doivent être en haut de la pile et celles les plus générales en bas de la pile, de façon à ce que les cas particuliers soient sélectionnés par le logiciel comme base de tarification. Si, par exemple, je modifie la tarification ci-dessus de la manière suivante :

* dans Paris intra-muros ;
* dans Paris intra-muros avec vélo cargo ;
* dans le département du 93 avec vélo cargo.

Si une livraison dans Paris intra-muros est créée avec la nécessité de livrer en vélo cargo, le prix spécifié pour la première règle s’appliquera car aucun type de vélo n’est spécifiée pour celle-ci et la seconde sera ignorée.

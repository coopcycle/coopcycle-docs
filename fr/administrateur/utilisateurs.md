---
title: Gestion des utilisateurs
lang: fr
role: admin
ref: admin-users
parent: Guide de l'administrateur
nav_order: 3
---

# Gestion des utilisateurs

La liste des utilisateurs de la plateforme est disponible dans l’onglet `Utilisateurs`. Cette liste détaille l’ensemble de comptes inscrits sur la plateforme ainsi que les informations qui leurs sont relatives et la possibilité d’ajouter / créer un nouvel utilisateur.

## Profil utilisateur

Un compte utilisateur est associé aux information suivantes :

- Nom d'utilisateur
- Prénom
- Nom
- Numéro de téléphone
- Mot de passe
- Email
- Numéro de téléphone

Il est possible d'activer/désactiver les utilisateurs. Un utilisateur désactivé est déconnecté et ne peut plus accéder à la plateforme.

## Rôles

Chaque utilisateur peut avoir un ou plusieurs rôles. Chaque rôle donne accès à des fonctionnalités de la plateforme.

| Rôle                                      | Client   | Livreur   | Restaurant | Magasin    | Admin   |
| -------------------------------           |:------:|:---------:|:----------:| :----------:| :----------:|
| Éditer ses informations personelles       | ✔      | ✔         | ✔          | ✔           | ✔           |
| Créer et modifier des restaurants         |        |           | ✔          |             | ✔           |
| Gérer des commandes                       |        |           | ✔          |             | ✔           |
| Éditer des factures                       |        |           | ✔          |             | ✔           |
| Créer et modifier des menus               |        |           | ✔          |             | ✔           |
| Créer des magasins                        |        |           |            |             | ✔           |
| Modifier des magasins                     |        |           |            | ✔           | ✔           |
| Créer une livraison                       |        |           |            | ✔           | ✔           |
| Gérer des livraisons                      |        | ✔         |            |             | ✔           |
| Accéder à l'API CoopCycle                 |        | ✔         | ✔          |             | ✔           |
| Éditer les rôles utilisateurs             |        |           |            |             | ✔           |
| Éditer les contrats et les tarifications  |        |           |            |             | ✔           |


## Assignation d'un magasin/restaurant

Sur la fiche d'un utilisateur avec le rôle `Restaurant` vous pouvez lui assigner (le rendre propriétaire) un restaurant que vous avez créé précédemment. De même un utilisateur qui a le rôle `Commerçant` peut se voir attribuer un magasin créé précédemment.

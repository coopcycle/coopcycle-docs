---
title: Creation des restaurants
lang: fr
role: admin
ref: admin-restaurant
parent: Restaurants
grand_parent: Guide de l'administrateur
nav_order: 1
custom_scripts:
  - "https://cdnjs.cloudflare.com/ajax/libs/jquery-zoom/1.7.21/jquery.zoom.min.js"
  - "/assets/scripts/zoom.js"
---

# Création des restaurants

Cette page décrit le processus pour créer un restaurant sur la plateforme CoopCycle. N’hésitez pas à demander de l’aide à [contact@coopcycle.org](mailto:contact@coopcycle.org) pour configurer les premiers restaurants. Celui-ci se déroule en deux étapes :

- Créer le restaurant sur la plateforme CoopCycle
- Créer le compte [Stripe](https://dashboard.stripe.com/register){:target="_blank"} lié


Après avoir réalisé ces deux étapes :

- Créer un compte pour le restaurateur dans la partie “Utilisateurs”
- Assigner le restaurant à ce restaurateur pour qu’il puisse accéder au backoffice


Prérequis :

- Avoir configuré correctement le compte Stripe lié à la plateforme (lien vers la page correspondante)


Informations minimum nécessaires au préalable :

- Nom, prénom du restaurateur
- Nom légal du restaurant
- Numéro de téléphone du restaurant
- Adresse du restaurant
- IBAN du restaurant
- **Scan recto/verso en couleur de la carte d’identité du restaurateur au format JPEG ou PNG (demande de Stripe après les premières commandes pour vérification d’identité)**
- Informations contractuelles (quel tarif de livraison pour le restaurateur? pour le client? qui paye les frais de paiement?)


Informations optionnelles :

- Horaires d’ouverture (horaires où la livraison est activée)
- Numéro de SIRET


## 1- Création du restaurant



- Depuis l’onglet “Restaurants”, cliquer sur “Ajouter un restaurant”
- Entrer les informations dans les champs correspondants

<span class="zoomable">![Creation d'un restaurant](/assets/images/creation_resto_fr.png)</span>

- Cliquer sur “Enregistrer”


## 2- Création du compte Stripe lié au restaurant

- **Depuis votre dashboard Stripe**, [https://dashboard.stripe.com/account](https://dashboard.stripe.com/account) , créer un nouveau compte en cliquant en haut à gauche sur “New Account”. Indiquer le nom du restaurant.

<span class="zoomable">![Stripe](/assets/images/stripe_resto_account_fr.png)</span>
![Stripe](/assets/images/stripe_resto_account_fr_2.png)

- **Depuis la page du restaurant sur la plateforme**, dans la section “Compte Stripe”, cliquer sur le bouton “Connexion avec Stripe”. Le processus doit être répété pour un fonctionnement en dev et fonctionnement en live.

![Stripe](/assets/images/stripe_resto_account_fr_3.png)

- Une page Stripe s’ouvre. Dans le dropdown “Switch account” sélectionnez le restaurant correspondant.

![Stripe](/assets/images/stripe_resto_account_fr_4.png)

- Entrer les informations du restaurateur correspondantes. <span style="color: red">**Attention : dans le champ “Customer phone number” indiquez votre numéro de téléphone pas celui du restaurateur.**</span>


- Vérifiez votre numéro de téléphone à l’adresse suivante :  
[https://dashboard.stripe.com/phone-verification?source=email](https://dashboard.stripe.com/phone-verification?source=email): entrez votre numéro de téléphone puis recopiez le code reçu par SMS (vous avez dû recevoir une notification mail)


- Et voilà ! Pour vérifier que tout est bien en ordre avec Stripe :
    - Dans le dashboard Stripe, sélectionnez votre compte principal (le compte de la coopérative) depuis le dropdown en haut à gauche
    - Cliquez sur “Connect” puis “Accounts” dans la colonne de gauche
    - Dans la liste “Recently connected accounts” qui apparaît cliquer sur le premier (le dernier compte lié)
    - Vérifier que “Payments” et “Payouts” sont bien au vert - en cas de problème contactez [dev@coopcycle.org](mailto:dev@coopcycle.org)


![Stripe](/assets/images/stripe_resto_account_fr_5.png)

---
title: Gestion des paiements via Stripe
lang: fr
role: admin
ref: admin-stripe
parent: Guide de l'administrateur
---

## Qu’est ce que Stripe ?

Stripe est un prestataire de paiement, qui nous permet de gérer les paiements par carte bleue de manière sécurisée. Par ailleurs la fonctionnalité “Stripe Connect” nous permet de gérer l’aspect “plateforme” du paiement, i.e la répartition des paiements entre la plateforme (argent revenant à la coopérative de livraison) et le restaurant.

Du fait du financement par cotisation de la coopérative européenne, nous (CoopCycle) ne percevons pas de commission sur les paiements. Stripe prélève une commission de 25cts + 1.4%  par paiement, à la charge du commerçant ou de la plateforme ([Consultez la tarification Stripe à jour ici](https://stripe.com/fr/pricing){:target="_blank"}).

## Pourquoi avoir choisi Stripe?

Stripe s’est imposé comme la “rolls-royce” des services des paiements. Le service fourni, peut-être pas le moins cher, est réputé d’excellente qualité. Il est possible de trouver des services moins chers, mais nous pensons que le prix en vaut la chandelle. Un point négatif connu de Stripe est que la (belle) interface admin Stripe n'est pas toujours disponible dans la langue de l'utilisateur. Elle est toutefois disponible en français.

## Qu’est-ce que le “live mode” et le “test mode” Stripe?

La plateforme CoopCycle peut-être configurée pour utiliser le mode “live” ou le mode “test” depuis la page “paramètres”. En mode test, les clients ne seront pas débités. Il faut utiliser des cartes tests (typiquement 4242 4242 4242 4242). **N’oubliez pas de passer en “live” avant de passer en production !**

## Comment configurer Stripe/Stripe Connect pour votre instance de la plateforme?

1. Créer un compte Stripe <a target="_blank" href="https://dashboard.stripe.com/register">ici</a> puis :
    * Récupérer les quatre clés d’API Stripe (privée/publique live, privée/publique test) ici : <a target="_blank" href="https://dashboard.stripe.com/apikeys">https://dashboard.stripe.com/apikeys</a> (<a target="_blank" href="https://www.youtube.com/watch?v=XLzg_K_0C5k">en vidéo</a>)
    * Récupérer les deux identifiants Stripe Connect (live et test) ici : <a target="_blank" href="https://dashboard.stripe.com/account/applications/settings">https://dashboard.stripe.com/account/applications/settings</a>
    * Les copier dans les champs correspondants dans la page “paramètres” de l’admin

Note: Les clés et identifiants live et test ne s'affichent pas en même temps à l'écran. Il y a sur la page un interrupteur qui permet d'afficher soit les données test, soit les données live.

2. Configurer l’url de redirection pour Stripe Connect
   * Aller sur <a target="_blank" href="https://dashboard.stripe.com/account/applications/settings">https://dashboard.stripe.com/account/applications/settings</a>
   * Cliquer sur "Add redirect URI" (**à faire en live et en test**). Puis entrer cette valeur “https://<nom_de_domaine>/stripe/connect/standard” (par exemple `https://demo.coopcycle.org/stripe/connect/standard`)

## Comment activer son compte Stripe pour utiliser la plateforme?

Vous avez besoin d’activer votre compte Stripe pour commencer à utiliser la plateforme en “live”. Cliquez sur “Activate your account” sur la gauche puis entrez les informations nécessaires. (vidéo : <a target="_blank" href="https://www.youtube.com/watch?v=XLzg_K_0C5k">https://www.youtube.com/watch?v=XLzg_K_0C5k</a>)

## Comment voir l’argent récupéré grâce à la plateforme ?

Les fonds touchés par la plateforme (la coopérative de livraison) sont comptés comme une commission prélevée sur le paiement du commerçant. Aller à cette URL <a target="_blank" href="https://dashboard.stripe.com/test/applications/fees">https://dashboard.stripe.com/test/applications/fees</a>.

## Comment récupérer l’argent sur son compte ?

Des paiements de votre compte Stripe vers votre compte en banque auront lieu régulièrement (“payouts”). Vous pouvez accéder à la liste des payouts ici : <a target="_blank" href="https://dashboard.stripe.com/test/balance/overview">https://dashboard.stripe.com/test/balance/overview</a>. Vous pouvez aussi y demander un virement immédiat vers votre compte.

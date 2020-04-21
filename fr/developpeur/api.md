---
title: Utilisation de l'API CoopCycle
lang: fr
ref: dev-api
parent: Développeur
nav_order: 1
---

# Utilisation de l'API CoopCycle

[Ouvrir la documentation API / Swagger](https://demo.coopcycle.org/api/docs)

## Authentification

La plupart des endpoints de l'API nécessitent une authentification, ainsi qu'une autorisation.
<br>
L'authentification est implémentée en envoyant un [JSON Web Token](https://jwt.io/introduction/) via les en-têtes HTTP.

```
Authorization : Bearer <token>
```
## Authentification en tant qu'application Web

Si vous créez une application Web qui n'a pas besoin d'agir au nom d'un utilisateur, vous devez utiliser le [OAuth client credentials](https://oauth.net/2/grant-types/client-credentials/) flow pour obtenir un jeton d'accès.

**Obtention des identifiants API**

Pour créer des jetons d'accès, vous aurez besoin des identifiants API (une clé publique et une clé secrète).
<br>
Demandez aux administrateurs de la plate-forme de créer une application API et de vous envoyer les identifiants API.

**Utiliser les informations d'identification pour obtenir un jeton d'accès**

La première étape pour faire des demandes authentifiées est d'obtenir un **jeton d'accès**.
<br>
Pour obtenir un jeton d'accès, vous devez d'abord faire une demande au endpoint `/oauth2/token`, avec vos identifiants API encodés en Base64.

Voici un exemple d'encodage de vos identifiants API en PHP:

```
php -r 'echo base64_encode("<api_key>:<api_secret>"), PHP_EOL;'
```

Voici un exemple de requête vers le endpoint `/oauth2/token` utilisant cURL:

```
curl -X POST -d 'grant_type=client_credentials&scope=tasks+deliveries' -H 'Authorization: Basic <base64_credentials>' https://acme.coopcycle.org/oauth2/token
```

La réponse devrait ressembler à ceci:

```
{
    "token_type": "Bearer",
    "expires_in": 3600,
    "access_token": "<access_token>"
}
```

**Utilisation du jeton d'accès pour effectuer des requêtes authentifiées**

Vous pouvez maintenant utiliser le jeton d'accès pour faire des requêtes authentifiées à l'API

```
curl -X POST -d '{ ... }' -H 'Content-Type: application/ld+json' -H 'Authorization: Bearer <access_token>' https://acme.coopcycle.org/api/deliveries
```

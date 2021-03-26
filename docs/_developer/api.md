---
layout: default
title: API
nav_order: 1
---

## Using the CoopCycle API

<div class="alert alert-success" role="alert">
  <a href="https://demo.coopcycle.org/api/docs">Open API / Swagger documentation</a>
</div>

### Authentication

Most of the API endpoints require authentication, and also authorization.

Authentication is implemented by sending a [JSON Web Token](https://jwt.io/introduction/) via HTTP headers.

```
Authorization: Bearer <token>
```

### Authenticating as a web application

If you are creating a web application that does not need to act on behalf of a user, you need to use the [OAuth client credentials](https://oauth.net/2/grant-types/client-credentials/) flow to obtain an access token.

**Obtaining API credentials**

To create access tokens, you will need API credentials (an API key and an API secret).

Ask the platform administrators to [create a API application and send you the API credentials](../_admin/configuration/api.md).

**Using the credentials to obtain an access token**

The first step to make authenticated requests is to obtain an **access token**.

To obtain an access token, you first need to make a request to the `/oauth2/token` endpoint,
with your API credentials encoded as Base64.

Here is an example to encode your API credentials using PHP:

```
php -r 'echo base64_encode("<api_key>:<api_secret>"), PHP_EOL;'
```

Here is an example request to the `/oauth2/token` endpoint using cURL:

```
curl -X POST -d 'grant_type=client_credentials&scope=tasks+deliveries' -H 'Authorization: Basic <base64_credentials>' https://acme.coopcycle.org/oauth2/token
```

The response should look like this:

```
{
    "token_type": "Bearer",
    "expires_in": 3600,
    "access_token": "<access_token>"
}
```

**Using the access token to make authenticated requests**

You can now use the access token to make authenticated requests to the API

```
curl -X POST -d '{ ... }' -H 'Content-Type: application/ld+json' -H 'Authorization: Bearer <access_token>' https://acme.coopcycle.org/api/deliveries
```

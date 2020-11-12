---
id: 110e618f-e566-490b-bdf3-87c4b95476bd
title: Developer
desc: ""
updated: 1605202494564
created: 1604774961045
---

<link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.5.0/css/bootstrap.min.css" integrity="sha384-9aIt2nRpC12Uk9gS9baDl411NQApFmC26EwAOH8WgZl5MYYxFfc+NcPb1dKGj7Sk" crossorigin="anonymous">
<script src="https://code.jquery.com/jquery-3.5.1.slim.min.js" integrity="sha384-DfXdz2htPH0lsSSs5nCTpuj/zy4C+OGpamoFVy38MVBnE+IbbVYUew+OrCXaRkfj" crossorigin="anonymous"></script>
<script src="https://cdn.jsdelivr.net/npm/popper.js@1.16.0/dist/umd/popper.min.js" integrity="sha384-Q6E9RHvbIyZFJoft+2mJbHaEWldlvI9IOYy5n3zV9zzTtmI3UksdQRVvoxMfooAo" crossorigin="anonymous"></script>
<script src="https://stackpath.bootstrapcdn.com/bootstrap/4.5.0/js/bootstrap.min.js" integrity="sha384-OgVRvuATP1z7JjHLkuOU7Xw704+h835Lr+6QL9UvYjZE3Ipu6Tp75j7Bh/kR0JKI" crossorigin="anonymous"></script>
<!-- Font Awesome -->
<script src="https://kit.fontawesome.com/489c6dd9c4.js" crossorigin="anonymous"></script>

# Developer

<div class="alert alert-info" role="alert">
Welcome to the developer's guide for CoopCycle platform.
</div>

---

## Using the CoopCycle API

[Open API / Swagger documentation](https://demo.coopcycle.org/api/docs)

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

Ask the platform administrators to create a API application and send you the API credentials.

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

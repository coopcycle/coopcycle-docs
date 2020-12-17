---
id: 185bdd50-4444-4c31-b8bd-2febd4284760
title: API
desc: ''
updated: 1605290183452
created: 1604774965954
---

<!-- CSS -->
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@4.5.3/dist/css/bootstrap.min.css" integrity="sha384-TX8t27EcRE3e/ihU7zmQxVncDAy5uIKz4rEkgIXeMed4M0jlfIDPvg6uqKI2xXr2" crossorigin="anonymous">
<!-- jQuery and JS bundle w/ Popper.js -->
<script src="https://code.jquery.com/jquery-3.5.1.slim.min.js" integrity="sha384-DfXdz2htPH0lsSSs5nCTpuj/zy4C+OGpamoFVy38MVBnE+IbbVYUew+OrCXaRkfj" crossorigin="anonymous"></script>
<script src="https://cdn.jsdelivr.net/npm/bootstrap@4.5.3/dist/js/bootstrap.bundle.min.js" integrity="sha384-ho+j7jyWK8fNQe+A12Hb8AhRq26LrZ/JpcUGGOn+Y7RsweNrtN/tE3MoK7ZeZDyx" crossorigin="anonymous"></script>
<!-- Font Awesome -->
<script src="https://kit.fontawesome.com/489c6dd9c4.js" crossorigin="anonymous"></script>

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
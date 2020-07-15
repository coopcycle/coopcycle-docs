---
title: Usando a API CoopCycle
lang: pt-BR
ref: dev-api
parent: Developer
---

# Usando a API CoopCycle

[Documentação Open API / Swagger](https://demo.coopcycle.org/api/docs)

## Autenticação

A maioria dos pontos de extremidade da API requer autenticação e também autorização.
<br>
A autenticação é implementada enviando um [JSON Web Token](https://jwt.io/introduction/) através de cabeçalhos HTTP.

`` ``
Autorização: Portador <token>
`` ``

### Autenticando como um aplicativo Web

Se você estiver criando um aplicativo Web que não precise agir em nome de um usuário, precisará usar o fluxo [credenciais do cliente OAuth] (https://oauth.net/2/grant-types/client-credentials/) para obter um token de acesso.

**Obtendo credenciais da API**

Para criar tokens de acesso, você precisará de credenciais da API (uma chave e um segredo da API).
<br>
Peça aos administradores da plataforma para criar um aplicativo de API e enviar as credenciais da API.

**Usando as credenciais para obter um token de acesso**

A primeira etapa para fazer solicitações autenticadas é obter um **token de acesso**.
<br>
Para obter um token de acesso, primeiro você precisa fazer uma solicitação para o terminal `/ oauth2 / token`
com suas credenciais de API codificadas como Base64.

Aqui está um exemplo para codificar suas credenciais de API usando PHP:

`` ``
php -r 'echo base64_encode("<api_key>:<api_secret>"), PHP_EOL;'
`` ``

Aqui está um exemplo de solicitação para o terminal `/ oauth2 / token` usando cURL:

`` ``
curl -X POST -d 'grant_type=client_credentials&scope=tasks+deliveries' -H 'Authorization: Basic <base64_credentials>' https://acme.coopcycle.org/oauth2/token
`` ``

A resposta deve ser assim:

`` ``
{
    "token_type": "Bearer",
    "expires_in": 3600,
    "access_token": "<access_token>"
}
`` ``

**Usando o token de acesso para fazer solicitações autenticadas**

Agora você pode usar o token de acesso para fazer solicitações autenticadas à API

`` ``
curl -X POST -d '{ ... }' -H 'Content-Type: application/ld+json' -H 'Authorization: Bearer <access_token>' https://acme.coopcycle.org/api/deliveries
`` ``
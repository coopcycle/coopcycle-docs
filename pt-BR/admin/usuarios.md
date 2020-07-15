---
title: Usuários
lang: pt-BR
ref: admin-users
parent: Guia do Administrador
nav_order: 5
---

# Gerenciamento de usuários

A lista de administradores está disponível na página `Usuários '. Esta lista descreve contas que estão inscritas na plataforma e suas informações associadas. Também permite adicionar / criar um novo usuário.

## Perfil do usuário

Uma conta de usuário está associada às seguintes informações:

- Nome do usuário
- Primeiro nome
- Último nome
- Número de telefone
- Senha
- Endereço de email

É possível ativar / desativar usuários. Um usuário desativado é desconectado e não pode mais acessar a plataforma.

## Funções

Todo usuário pode ter uma ou várias funções. Cada função fornece acesso a alguns recursos da plataforma.

| Função                                         | Cliente | Mensageiro de bicicleta | Restaurante | Loja | Admin |
| ---------------------------------------------- |:-------:|:-----------------------:|:-----------:|:----:|:-----:|
| Para editar suas próprias informações pessoais | ✔       | ✔                      | ✔           | ✔    | ✔    |
| Para criar e modificar restaurantes            |         |                         | ✔           |      | ✔    |
| Ordens Mannage                                 |         |                         | ✔           |      | ✔ |
| Para editar um recibo                          |         |                         | ✔           |      | ✔ |
| Para criar e modificar menus                   |         |                         | ✔           |      | ✔ |
| Para criar lojas                               |         |                         |             |       | ✔ |
| Para modificar lojas                           |         |                         |             | ✔    | ✔ |
| Para criar uma entrega                         |         |                         |             | ✔    | ✔ |
| Para gerenciar entregas                        |         | ✔                      |              |      | ✔ |
| Para acessar a API CoopCycle                   |         | ✔                      | ✔            |      | ✔ |
| Para editar funções para usuários              |         |                         |              |      | ✔ |
| Para editar contratos e tarificações           |         |                         |              |      | ✔ |

## Atribuição de uma loja/restaurante

Nas informações sobre um usuário que tem a função 'Restaurante', você pode atribuir a ele (Para tornar seu proprietário) uma loja que você criou anteriormente. Também funciona para um usuário que tem uma função de "dono da loja".
---
title: Users
lang: en
ref: admin-users
parent: Admin's guide
nav_order: 6
---

# Management of users

The list of administrators is available in the page `Users`. This list describes accounts which are inscribed on the platform and their associated informations. It also enables to add/create a new user.

## User profil

An user account is associated to the following informations :

- User name
- First name
- Last name
- Telephone number
- Password
- Email adress

It is possible to activate/desactivate users. A desactivated user is disconnected and can't access the platform anymore.

## Roles

Every user can have one or several roles. Every role gives access to some platform features.

| Role                                      | Customer   | Bike messenger   | Restaurant | Shop    | Admin   |
| -------------------------------           |:------:|:---------:|:----------:| :----------:| :----------:|
| To edit his/her own personal informations | ✔      | ✔         | ✔          | ✔           | ✔           |
| To create and modify restaurants         |        |           | ✔          |             | ✔           |
| Mannage orders                           |        |           | ✔          |             | ✔           |
| To edit a receipt                        |        |           | ✔          |             | ✔           |
| To create and modify menus               |        |           | ✔          |             | ✔           |
| To create shops                          |        |           |            |             | ✔           |
| To modify shops                          |        |           |            | ✔           | ✔           |
| To create a delivery                     |        |           |            | ✔           | ✔           |
| To manage deliveries                     |        | ✔         |           |             | ✔           |
| To access CoopCycle API                  |        | ✔         | ✔         |             | ✔           |
| To edit roles for users                  |        |           |            |             | ✔           |
| To edit contracts and tarifications      |        |           |            |             | ✔           |


## Assignation of a shop/restaurant

On the informations about an user which has the `Restaurant` role, you can assignate him/her (To make him/her owner) a shop that you have previously created. It also works for an user who has a `shop-owner` role.

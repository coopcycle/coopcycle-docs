---
id: 55e4d9a3-e1ec-4ddb-acab-e77ee7287c69
title: Creating a restaurant
desc: ''
updated: 1605290072746
created: 1605208498122
custom_scripts:
  - 'https://cdnjs.cloudflare.com/ajax/libs/jquery-zoom/1.7.21/jquery.zoom.min.js'
  - /assets/scripts/zoom.js
---

<!-- CSS -->
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@4.5.3/dist/css/bootstrap.min.css" integrity="sha384-TX8t27EcRE3e/ihU7zmQxVncDAy5uIKz4rEkgIXeMed4M0jlfIDPvg6uqKI2xXr2" crossorigin="anonymous">
<!-- jQuery and JS bundle w/ Popper.js -->
<script src="https://code.jquery.com/jquery-3.5.1.slim.min.js" integrity="sha384-DfXdz2htPH0lsSSs5nCTpuj/zy4C+OGpamoFVy38MVBnE+IbbVYUew+OrCXaRkfj" crossorigin="anonymous"></script>
<script src="https://cdn.jsdelivr.net/npm/bootstrap@4.5.3/dist/js/bootstrap.bundle.min.js" integrity="sha384-ho+j7jyWK8fNQe+A12Hb8AhRq26LrZ/JpcUGGOn+Y7RsweNrtN/tE3MoK7ZeZDyx" crossorigin="anonymous"></script>
<!-- Font Awesome -->
<script src="https://kit.fontawesome.com/489c6dd9c4.js" crossorigin="anonymous"></script>

# Creating restaurants

This page describes the process for creating a restaurant on the CoopCycle platform. Don't hesitate to ask for help [contact@coopcycle.org](mailto:contact@coopcycle.org) to configure the first restaurants.\
This takes place in two stages:
- Create the restaurant on the CoopCycle platform
- Create a [Stripe](https://dashboard.stripe.com/register) account

After performing these two steps:

- Create an account for the restaurateur in the “Users” section
- Assign the restaurant to this restaurateur so that he can access the back office


Prerequisite:

- Having correctly configured the Stripe account linked to the platform (link to the corresponding page)


Minimum information required beforehand:

- Name, first name of the restaurateur
- Legal name of the restaurant
- Restaurant phone number
- Restaurant address
- IBAN of the restaurant
- **Color front / back scan of the restaurant owner's identity card in JPEG or PNG format (Stripe request after the first orders for identity verification)**
- Contractual information (what delivery rate for the restaurant owner? For the customer? Who pays the payment fees?)


Optional information:

- Opening hours (times when delivery is activated)
- Number Siret

## 1 - Creating a restaurant

- From the “Restaurants” tab, click on “Add a restaurant”
- Enter information in the corresponding fields

![Creation d'un restaurant](/assets/images/creation_resto_fr.png)

- Click on “Save”
 
## 2 - Creating a restaurant Stripe account

- **From your Stripe dashboard**, [https://dashboard.stripe.com/account](https://dashboard.stripe.com/account), create a new account by clicking on the top left on “New Account”. Indicate the name of the restaurant.

<span class="zoomable">![Stripe](/assets/images/stripe_resto_account_fr.png)</span>
![Stripe](/assets/images/stripe_resto_account_fr_2.png)
 
- **From the restaurant page on the platform**, in the “Stripe Account” section, click on the “Connect with Stripe” button. The process must be repeated for dev operation and live operation.

![Stripe](/assets/images/stripe_resto_account_fr_3.png)

- A Stripe page opens. In the “Switch account” dropdown select the corresponding restaurant.

![Stripe](/assets/images/stripe_resto_account_fr_4.png)

- Entrer les informations du restaurateur correspondantes. <span style="color: red">**Attention : dans le champ “Customer phone number” indiquez votre numéro de téléphone pas celui du restaurateur.**</span>


- Check your phone number at the following address: [https://dashboard.stripe.com/phone-verification?source=email](https://dashboard.stripe.com/phone-verification?source=email): enter your phone number then copy the code received by SMS (you should have received an email notification)

- And There you go ! To check that everything is in order with Stripe:
  - In the Stripe dashboard, select your main account (the cooperative's account) from the dropdown in the top left
  - Click on “Connect” then “Accounts” in the left column
  - In the “Recently connected accounts” list which appears click on the first (the last linked account)
  - Check that “Payments” and “Payouts” are green - in case of problems contact [dev@coopcycle.org](mailto:dev@coopcycle.org)
  
  ![Stripe](/assets/images/stripe_resto_account_fr_5.png)

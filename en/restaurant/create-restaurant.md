title: Create a Restaurant
lang: en
ref: creation-restaurant
parent: Restaurant's guide
nav_order: 5

# Create a Restaurant

Please contact a cooperative of CoopCycle. Only an administrator can create a new restaurant.

## Step 1 : Add General information

Now you have to add general information about your restaurant. Some of these informations would be possibly editing later with your restaurant account, but other - such as the terms of the contract or options - are only accessible with adminstrator account. 4 tabs have to be complete :

- [General](#General)
- [Options](#Options)
- [Fulfillment](#Fulfillment)
- [Settlement](#Settlement)

### General

On this `General` tab, you can modify general informations about your restaurant :

- Displayed to clients :
  - Name of the Restaurant on CoopCycle
  - Type of Business
  - Adress
  - Description of your restaurant 
  - Web
  
- Not displayed to clients :
  - Website
  - Telephone number
  - Business information 
  
### Options

4 options have to be decided on this tab :

- Restaurant is exclusive which means that it is only available on CoopCycle
- Restaurant is featured on homepage 
- Restaurant also accepts quotes (e.g.:catering)
- Enable Deposit-Refund system

### Fulfillment

#### Schedules
On this page, you can choose between two types of activity, or chose both :
- Collect, which means that the customer comes to the restaurant to take-away his or her order
- Delivery, which means that the cooperative delivers the order to the customer

For each activity, you can edit a schedule which determines when customers can receive their orders or come take them at the restaurant. 

For each schedule you have to choose between *As soon as possible* and *time slot* :
- *As soon as possible* : The customer receives his or her order as soon as possible. On his or her application, the customer during his or her order sees : "in XX minutes"
- *Time slot* : The customer choses when he or she receives the order. On his or her application, the customer during his or her order sees : "Between XX PM/AM and XX PM/AM"

For each schedule, you have to chose with the administrator if the restaurant-owner has the right to change these schedules. Click on `allow editing` if it is the case.

#### Global options

- Define a delivery perimeter
- Define, if needed, an additional delay before ordering. For instance, if you put 1 in the `day` field, customers have to order the day before.
- Define, if needed, a number of shipping choices

### Settlement

You will find on this page **the terms of the contract** between the local delivery collective and the restaurant. They cover the following aspects :
- Delivery price :
    - Part to be paid by the restaurant ("Amount charged by the platform" for a fixed cost and "Platform fee for deliveries" for a proportionnal fee). It is also possible to create your own rule of pricing and apply it in this page. Please see the documentation about pricing in administrator's guide/logistics.
    - Part to be paid by the final client.("Amount paid by the customer" for a fixed cost and "Fees paid by the customer" for a proportionnal fee). It is also possible to create your own rule of pricing and apply it in this page. 
- Minimum basket amount
- Platform fees for take-away.

## Step 2 : Link an account with a restaurant

### Create an account or invitation

#### Method 1 : create your account
Restaurant owner has to create an account on CoopCycle. It has to fill the following informations : 

- Email
- Username
- Password
- Given Name and Family Name
- Telephone Number

Keep secret your username and password, you will have to use it when you are using CoopCycle to manage your restaurant.

#### Method 2 : Invitation

In this second method, it is administrators who invite you on CoopCycle. 

In order to do that, Administrators have to click on `users` tab on the top of the administrator's dashboard. On this new page, a blue button `Invite an user` enables administrators to create an account on behalf of an user. It has to fill following fields :
- Username
- Email (of the invited person)
- Given name and Family name
- The status of the account - In this case, chose *Restaurant* if you invite a restaurant-owner -

At the end, it is the user who will chose his/her password, which is secret.

### Add a role : restaurant-owner

Only administrators can add you a role on your account of *Restaurant*. If you used *Method 2*, you don't need to change the status of the account, because your account has already been created as *Restaurant*.

If you used *Methode 1*, you have to follow theses steps : 
- Administrators click on `users` tab on the top of the administrator's dashboard.
- Administrators search your username of the `searching`field or find you on the list and click on green `edit` button.
- Administrators add you a *Restaurant* role and click on `save`

### Link an account with one or more restaurant.

Only administrators can link an account with a restaurant. On the same `edit`page that before, please fill the `add a restaurant` field with the name of the restaurant.

After step, when restaurant-owner is connecting to CoopCycle with his or her username and password, he/her will only have access to his/her restaurant.

## Step 3 : Create a Stripe account and link it to your restaurant 

About the creation of your Stripe account, please see [Admin's guide/Stripe]{https://docs.coopcycle.org/fr/administrateur/paiements-stripe.html}. Instructions are the same for cooperative and restaurant. The only difference is what you do next with your Stripe account.

When a restaurant has created its Stripe account, this one can be connected to CoopCycle platform and to the restaurant : 
- If administrators enabled restaurant to manage its own Stripe account, restaurant-owner with his/her own account can connect Stripe account by going on *General information* by clicking on the name of the restaurant, or on the `edit` button. Then click on the `Payment` tab and connect with Stripe.
- If administrators disabled restaurant to manage its own Stripe account, you have to follow the same steps but with an administator account to connect restaurant stripe account.

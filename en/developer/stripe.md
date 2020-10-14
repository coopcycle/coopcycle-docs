---
title: Setting up Stripe
lang: en
ref: dev-api
parent: Developer
nav_order: 2
---

This page describes how to create a restaurant as an admin on the CoopCycle platform. Please ask for help at dev@coopcycle.org if you need to. This process has two steps: 
Create the restaurant on the CoopCycle platform
Create the linked Stripe account

Before:
You need to have configured correctly the Stripe account linked to the platform

After this two steps have been achieved :
Create an user account in the “User” section
On the created user page, assign him/her the restaurant so he can access its backoffice

Necessary informations :
Name & first name of the restaurant owner
Legal name of the restaurant
Phone number of the restaurant
Restaurants address
Restaurants IBAN
Contractual informations
What delivery price for the restaurant owner?
What delivery price for the customer?
Who is paying Stripe fees?
Proof of identity of the restaurant

Additional informations :
Delivery hours



2- Creating the Stripe account linked to the restaurant

From your Stripe dashboard,  https://dashboard.stripe.com/account , create a new account by clicking on the top left corner on “New account”. Indicate the restaurants name.

IMAGE

From the restaurant page on the platform, in the “Stripe account” section, click on “Connect with Stripe” button. The process have to be made twice, once for test and once for live payments.

IMAGE

A Stripe page opens. In the “Switch accounts” dropdown select the correct restaurant.

IMAGE

Enter the informations. Attention : in the “Customer phone number” field please indicate your phone number not the restaurant’s one.

Verify your phone number at the following address : https://dashboard.stripe.com/phone-verification?source=email . Enter your phone number then copy the code received by SMS (you may have received a mail notification about the phone verification)

Your done ! To check that everything’s in order :
In the Stripe dashboard select the main account (the one linked to the platform) on the top left corner
Clicked on “Connect” then on “Accounts” on the left column
In the “Recently connected accounts” list click on the first item (= the last account added)
Verify that “Payments” and “Payouts” are well and green - in case of issue please contact dev@coopcycle.org

IMAGE
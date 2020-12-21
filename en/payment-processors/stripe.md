---
title: Stripe
parent: 'Payment Processors'
---



# Stripe
---

## What is Stripe?

Stripe is a payment service provider, which allows us to manage credit card payments in a secure manner. In addition, the "Stripe Connect" functionality allows us to manage the "platform" aspect of the payment, i.e. the distribution of payments between the platform (money going to the delivery cooperative) and the restaurant.

Due to the fact that the european cooperative is fund by contributions, we (CoopCycle) do not charge a commission on payments. Stripe takes a fee on each transaction ([check the pricing for your country here](https://stripe.com/pricing){:target="_blank"}).


## Why Stripe?

Stripe has established itself as the "rolls-royce" of payment services. The service is reputed to be of excellent quality. It is possible to find cheaper services, but we believe the price is worth the candle. A known negative point about Stripe is that the (nice) Stripe admin interface is not always available in the user's language.

For creating and integrating a Stripe account with CoopCycle refer to the links below.

[Create a Stripe account <i class="fas fa-external-link-alt"></i>](https://dashboard.stripe.com/register){:target="_blank"}

<div class="alert alert-info">
    You can also ask you local coop to create a Stripe account on your behalf and they can seamlessly integrate with your e-commerce account. Then they will give you admin access to your Stripe account.
</div>

# Setting up Stripe

<div class="alert alert-info" role="alert">
This page describes how to create a restaurant as an admin on the CoopCycle platform.
</div>
<div class="alert alert-primary" role="alert">
Please ask for help at dev@coopcycle.org if you need to.</div>

---

## What is the “live mode” and “test mode” of Stripe?

The CoopCycle platform can be configured to use the "live" or "test" mode from the "settings" tab. In test mode clients will not be debited. You have to use test cards (typically 4242 4242 4242 4242 4242). **Don't forget to switch to "live" mode before going into production !**

## How to configure Stripe/Stripe Connect on your platform?

1. Create a Stripe account <a target="_blank" href="https://dashboard.stripe.com/register">here</a> , then:
    * Get the four API stripe keys (Private/Public live, Private/Public test) here: <a target="_blank" href="https://dashboard.stripe.com/apikeys">https://dashboard.stripe.com/apikeys</a> (<a target="_blank" href="https://www.youtube.com/watch?v=XLzg_K_0C5k">in video</a>)
    * Get the two Stripe Connect identifiers (Live/Test) here: <a target="_blank" href="https://dashboard.stripe.com/account/applications/settings">https://dashboard.stripe.com/account/applications/settings</a>
    * Past them in the corresponding fields on the administrator's “parameters” tab.

Note: Live and test keys and IDs are not displayed on the screen at the same time. There is a switch on the page to display either test or live data.

2. Configure the redirection url for Stripe Connect
   * Go to <a target="_blank" href="https://dashboard.stripe.com/account/applications/settings">https://dashboard.stripe.com/account/applications/settings</a>
   * Click on "Add redirect URI" (**It has to be done in live and  test mode**). Then enter this value "https://<domain_name>/stripe/connect/standard" (e.g. `https://demo.coopcycle.org/stripe/connect/standard`)

## How to activate your Stripe account to use the platform?

You need to activate your Stripe account to start using the platform in "live". Click on "Activate your account" on the left and enter the required informations. (video: <a target="_blank" href="https://www.youtube.com/watch?v=XLzg_K_0C5k">https://www.youtube.com/watch?v=XLzg_K_0C5k</a>)

## How to see the money earned through the platform?

The funds earned by the platform (the delivery cooperative) are calculated as a commission on the merchant's payment. Go to this URL <a target="_blank" href="https://dashboard.stripe.com/test/applications/fees">https://dashboard.stripe.com/test/applications/fees</a>.

## How to receive this money on your account?

Payments from your Stripe account to your bank account will be made regularly ("payouts"). You can access the list of payouts here : <a target="_blank" href="https://dashboard.stripe.com/test/balance/overview">https://dashboard.stripe.com/test/balance/overview</a>.  You can also request on this page an immediate transfer to your account.

---
This process has two steps:
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

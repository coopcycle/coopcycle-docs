---
title: Stripe payments
lang: en
role: admin
ref: admin-stripe
parent: Administrator's guide
nav_order: 4
---


# Managing payments via Stripe

## What is Stripe?

Stripe is a payment service provider, which allows us to manage credit card payments in a secure manner. In addition, the "Stripe Connect" functionality allows us to manage the "platform" aspect of the payment, i.e. the distribution of payments between the platform (money going to the delivery cooperative) and the restaurant.

Due to the fact that the european cooperative is fund by contributions, we (CoopCycle) do not charge a commission on payments. Stripe takes a commission of 25 cts + 1,4% per payment, payable by the merchant of the platform
([Check the updated pricing here](https://stripe.com/fr/pricing){:target="_blank"}).

## Why Stripe?

Stripe has established itself as the "rolls-royce" of payment services. The service is reputed to be of excellent quality. It is possible to find cheaper services, but we believe the price is worth the candle. A known negative point about Stripe is that the (nice) Stripe admin interface is not always available in the user's language.

## What is the “live mode” and “test mode” of Stripe?

The CoopCycle platform can be configured to use the "live" or "test" mode from the "settings" tab. In test mode clients will not be debited. You have to use test cards (typically 4242 4242 4242 4242 4242). **Don't forget to switch to "live" mode before going into production !**

## How to configure Stripe/Stripe Connect on your platform?

1. Create a Stripe account <a target="_blank" href="https://dashboard.stripe.com/register">ici</a> , then:
    * Get the four API stripe keys (Private/Public live, Private/Public test) here: <a target="_blank" href="https://dashboard.stripe.com/apikeys">https://dashboard.stripe.com/apikeys</a> (<a target="_blank" href="https://www.youtube.com/watch?v=XLzg_K_0C5k">in video</a>)
    * Get the two Stripe Connect identifiers (Live/Test) here: <a target="_blank" href="https://dashboard.stripe.com/account/applications/settings">https://dashboard.stripe.com/account/applications/settings</a>
    * Past them in the corresponding fields on the administrator's “parameters” tab. 
    
Note: Live and test keys and IDs are not displayed on the screen at the same time. There is a switch on the page to display either test or live data.

2. Configure the redirection url for Stripe Connect
   * Go to <a target="_blank" href="https://dashboard.stripe.com/account/applications/settings">https://dashboard.stripe.com/account/applications/settings</a>
   * Click on "Add redirect URI" (** It has to be done in live and  test mode**). Then enter this value "https://<domain_name>/stripe/connect/standard" (e.g. `https://demo.coopcycle.org/stripe/connect/standard`)

## How to activate your Stripe account to use the platform?

You need to activate your Stripe account to start using the platform in "live". Click on "Activate your account" on the left and enter the required informations. (video: <a target="_blank" href="https://www.youtube.com/watch?v=XLzg_K_0C5k">https://www.youtube.com/watch?v=XLzg_K_0C5k</a>)

## How to see the money earned through the platform?

The funds earned by the platform (the delivery cooperative) are calculated as a commission on the merchant's payment. Go to this URL <a target="_blank" href="https://dashboard.stripe.com/test/applications/fees">https://dashboard.stripe.com/test/applications/fees</a>.

## How to receive this money on your account?

Payments from your Stripe account to your bank account will be made regularly ("payouts"). You can access the list of payouts here : <a target="_blank" href="https://dashboard.stripe.com/test/balance/overview">https://dashboard.stripe.com/test/balance/overview</a>.  You can also request on this page an immediate transfer to your account.

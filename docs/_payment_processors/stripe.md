---
layout: default
title: Stripe
nav_order: 1
---

# Stripe
---

- [What is Stripe?](#what-is-stripe)
- [Why Stripe?](#why-stripe)
- [Setting up Stripe](#setting-up-stripe)


## What is Stripe?

Stripe is a payment service provider, which allows us to manage credit card payments in a secure manner. In addition, the "Stripe Connect" functionality allows us to manage the "platform" aspect of the payment, i.e. the distribution of payments between the platform (money going to the delivery cooperative) and the restaurant.

Due to the fact that the european cooperative is fund by contributions, we (CoopCycle) do not charge a commission on payments. Stripe takes a fee on each transaction ([check the pricing for your country here](https://stripe.com/pricing){:target="_blank"}).


## Why Stripe?

Stripe has established itself as the "rolls-royce" of payment services. The service is reputed to be of excellent quality. It is possible to find cheaper services, but we believe the price is worth the candle. A known negative point about Stripe is that the (nice) Stripe admin interface is not always available in the user's language.

For creating and integrating a Stripe account with CoopCycle refer to the link below.

1. [Create and link a Stripe account from the CoopCycle platform](/en/admin/restaurants/general-settings/#payment-%EF%B8%8F)
2. Create a Stripe account separate from the CoopCycle platform.
    a. [Register a Stripe account](https://dashboard.stripe.com/register)
    b. [Link your Stripe account to the CoopCycle platform]()

<div class="alert alert-info">
    You can also ask you local coop to create a Stripe account on your behalf and they can seamlessly integrate with your e-commerce account. Then they will give you admin access to your Stripe account.
</div>

## Setting up Stripe

<div class="alert alert-info" role="alert">
This page describes how to create a restaurant as an admin on the CoopCycle platform.
</div>
<div class="alert alert-primary" role="alert">
Please ask for help at dev@coopcycle.org if you need to.</div>

---

## What is the “live mode” and “test mode” of Stripe?

The CoopCycle platform can be configured to use the "live" or "test" mode from the "settings" tab. In test mode clients will not be debited. You have to use test cards (typically 4242 4242 4242 4242 4242). **Don't forget to switch to "live" mode before going into production !**


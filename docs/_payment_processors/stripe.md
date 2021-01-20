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

Due to the fact that the european cooperative is fund by contributions, we (CoopCycle) do not charge a commission on payments. Stripe takes a fee on each transaction ([check the pricing for your country here](https://stripe.com/pricing){:target="\_blank"}).

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

## Setting up the Cooperative's Stripe account

<div class="alert alert-info" role="alert">
Register and connect the cooperative's Stripe account to your CoopCycle instance.
</div>

<span class="badge badge-info">INFO:</span><span> If you have any questions please contact us at dev@coopcycle.org here</span>

### Register and activate your Stripe account.

<span class="badge badge-info">TIP:</span><span> These are standard account registration and activation steps. If you know what you're doing, then register and activate the account by yourself and then skip to <a href="#connect-your-stripe-account-to-your-coopcycle-instance">Connect your Stripe account to your CoopCycle instance</a>.</span>

1. [Register](https://dashboard.stripe.com/register) a Stripe account by following the steps on Stripe's registration page.
2. As soon as you've registered you will be re-directed to your Stripe dashboard.
3. Before being able to activate your Stripe account you need to verify your email. Click on **Verify your email** and follow the steps there or check your e-mail account for a **Verification email** from Stripe and click on the link provided in the e-mail.
   [![Stripe verify your email](/assets/images/stripeVerifyYourEmail.png)](/assets/images/stripeVerifyYourEmail.png){:target="\_blank"}
4. After verification you will be automatically re-directed to your dashboard and you should see a confirmation message and below **Add business details to activate your account** will be enabled:
   [![Stripe activate your account](/assets/images/stripeActivateYourAccount.png)](/assets/images/stripeActivateYourAccount.png){:target="\_blank"}

5. Click on **Add business details to activate your account** and then click on <span class="badge badge-primary">Start now <i class="fas fa-arrow-right"></i></span>
6. Now follow the steps and complete the details of your Cooperative as required by Stripe.<br>
   <span class="badge badge-info">INFO:</span><span> There is no guide for this step as the set up varies for every country and Stripe may modifiy, add or remove requirements without a specific notification.</span>
7. Once you successfully activate your account you will be re-directed to your dashboard and you should see a confirmation message stating: **Business details added**. You will also see your business name in the top-left corner of your dashboard.

### Connect your Stripe account to your CoopCycle instance

<div class="alert alert-warning" role="alert">
<strong>It is important to follow these steps carefully.</strong>
</div>

1. Go to `Configuration > Settings`
   [![Configuration settings](/assets/images/configurationSettings.png)](/assets/images/configurationSettings.png){:target="\_blank"}
2. Scroll down to **Stripe Account**
   [![Connect Coop Stripe in Test mode](/assets/images/connectCoopStripeTestMode.png)](/assets/images/connectCoopStripeTestMode.png){:target="\_blank"}
3. It is important to connect Stripe in both **TEST** and **LIVE** mode
   #### a. Connecting **TEST** mode.

---

## What is the “live mode” and “test mode” of Stripe?

The CoopCycle platform can be configured to use the "live" or "test" mode from the "settings" tab. In test mode clients will not be debited. You have to use test cards (typically 4242 4242 4242 4242 4242). **Don't forget to switch to "live" mode before going into production !**

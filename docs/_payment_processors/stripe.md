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

   - Head over to your [Strip dashboard](https://dashboard.stripe.com/dashboard){:target="\_blank"}

   - On the left-hand side panel check the **View test data** toggle. When toggled "ON" it turns orange and the name changes to **Viewing test data**<br>
     [![Toggle Stripe test data](/assets/images/toggleStripeViewTestData.png)](/assets/images/toggleStripeViewTestData.png){:target="\_blank"}

   - Click on **Developers** just above **Viewing test data**

   - Click on **API keys**<br>
     [![Stripe API keys](/assets/images/stripeAPIkeys.png)](/assets/images/stripeAPIkeys.png){:target="\_blank"}

   - On the API keys section that opens you will see under the Standard keys heading two (2) keys: **Publishable key** and **Secret Key**. _Secret key_ will be hidden.
     The keys in the image are only sample keys. Your two (2) keys will look similar to the ones in the image.
     Before you copy the keys, check again that you are actually in **TEST** mode. See nos. 1 and 2 in the image.

   - _Copy_ the **Publishable key** (see no. 3 in the image) and head over to **Stripe account** in Settings on your CoopCycle instance and _paste_ the key into the first field of **TEST**.
     <span class="badge badge-primary">SAVE SETTINGS</span>

   - Head back to Stripe and next to **Secret key** click on **Reveal test key** (no. 4 in the image) and _copy_ it into the second **TEST** field on your CoopCycle instance.
     <span class="badge badge-primary">SAVE SETTINGS</span>

   - Head back to Stripe and click **Settings** at the bottom of the left-hand side panel.

   - In the new section that opens click **Get started** in the **Connect block**<br>
     [![Stripe Connect Get Started](/assets/images/stripeConnectGetStarted.png)](/assets/images/stripeConnectGetStarted.png){:target="\_blank"}

   - A new page will load, **Payments for platforms** and you can click on the <span class="badge badge-primary">Get started</span> button.

   - From the pop-up select the **Platform for marketplace** option and click <span class="badge badge-primary">Continue <i class="fas fa-arrow-right"></i></span><br>
     [![Stripe Connect Platform Marketplace](/assets/images/stripeConnectPlatformMarketplace.png)](/assets/images/stripeConnectPlatformMarketplace.png){:target="\_blank"}
     This will enable **Connect settings**.

   - Click on **Settings** on the left-hand side panel.

   - Click on the new **Settings** option in the **Connect** block.

     <span class="badge badge-warning">ALERT:</span><span> Check if Stripe is still in <strong>TEST</strong> mode, if it's not, enable it.</span>

     **OAuth settings**

   - Scroll to the very bottom of the new opening page and toggle the option **OAuth for Standard accounts**<br>
     [![Stripe Enable OAuth](/assets/images/stripeEnableOAuth.png)](/assets/images/stripeEnableOAuth.png){:target="\_blank"}

   - Under **OAuth settings** in the **Redirects** section click on the **+ Add URI** button<br>
     [![Stripe Connect Add URI](/assets/images/stripeConnectAddURI.png)](/assets/images/stripeConnectAddURI.png){:target="\_blank"}

   - In the pop-up you need to write an URI address specific to your CoopCycle instance.<br>
     Sample URI address:
     `https://xxx.coopcycle.org/stripe/connect/standard` <br>
     If your CoopCycle address is `https://supercoop.coopcycle.org/`, replace `xxx` with `supercoop` in the _Sample URI address_ above.<br>
     It should look like this:
     `https://supercoop.coopcycle.org/stripe/connect/standard`<br>
     Copy it in the pop-up in Stripe and click **Add URI**
     [![Stripe Add URI](/assets/images/stripeAddURI.png)](/assets/images/stripeAddURI.png){:target="\_blank"}

     Once added you will see the URI in the **Redirects** section.

     In the **Test mode cliend ID** section copy the client ID in the third **TEST** field (Stripe Connect Identifier) on your CoopCycle instance.<br><span class="badge badge-primary">SAVE SETTINGS</span>
     [![Stripe Connect Test client ID](/assets/images/stripeConnectTestCliendID.png)](/assets/images/stripeConnectTestCliendID.png){:target="\_blank"}

   - Head back to Stripe in **Connect settings** and scroll to the top.

   #### Account types

   - In **Account types** click **Manage...**<br>
     [![Stripe Connect Account Types](/assets/images/stripeAccountTypes.png)](/assets/images/stripeAccountTypes.png){:target="\_blank"}

   - In section no. 1 **Select countries to onboard accounts** uncheck **Select all** and then only check ☑️ your country.<br>
     [![Stripe Select Country Express and Standard settings](/assets/images/stripeDeselectAllCountries.png)](/assets/images/stripeDeselectAllCountries.png){:target="\_blank"}

   - Section no. 2 **Select capabilities for your accounts** has three (3) outputs depending on the country. 

   **OUTPUT 1:**<br>
   If your country is **United Kingdom** you will see two (2) options in Section no. 2. Make sure you check ☑️ **Card payments** and <span class="badge badge-primary">Save</span> settings.

   **OUTPUT 2:**<br>
   If your country is not **United Kingdom** or **United States** then you can skip Section no. 2 because the **Card payments and transfers** option is mandatory and is enabled by default.

   **OUTPUT 3:**<br>
   If your country is **United States** the option **Card payments and transfers** is mandatory and is enabled by default and you can check ☑️ the following *tax reporting* option according to the tax status of your Coop. <span class="badge badge-primary">Save</span> settings.

---

## What is the “live mode” and “test mode” of Stripe?

The CoopCycle platform can be configured to use the "live" or "test" mode from the "settings" tab. In test mode clients will not be debited. You have to use test cards (typically 4242 4242 4242 4242 4242). **Don't forget to switch to "live" mode before going into production !**

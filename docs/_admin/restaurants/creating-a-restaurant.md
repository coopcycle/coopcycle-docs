---
layout: default
title: "Setting up a restaurant"
parent: Restaurants
nav_order: 1
---

# Setting up a restaurant

- [Create a Restaurant on CoopCycle](#creating-a-restaurant-on-coopcycle)
- [Create a Restaurant Stripe Account](#creating-a-restaurant-stripe-account)

---

<span class="badge badge-primary">TIP:</span><span> Click on any image to open it to full scale.</span><br>

<span class="badge badge-info">INFO:</span><span> Only after the restaurant has been set up properly will you be able to switch the **Disabled/Enabled** toggle.</span><br>

[![](/assets/images/enablerestotoggle.png)](/assets/images/enablerestotoggle.png){:target="\_blank"}

---

## Creating a Restaurant on CoopCycle

1. Select <i class="fas fa-utensils"></i> **Restaurants** from the header.
   <br>

2. Click on the <span class="badge badge-success">+ Create a new restaurant</span> button.<br>

   [![](/assets/images/createrestaurant.png)](/assets/images/createrestaurant.png){:target="\_blank"}<br>

<span class="badge badge-warning">ATTENTION:</span><span> After clicking on <span class="badge badge-success">+ Create a new restaurant</span> please go to <a href="/en/admin/restaurants/general-settings/">Restaurant general settings</a> and configure the Restaurant before continuing on this page.</span>

## Creating a Restaurant Stripe account

<div class="alert alert-primary" role="alert">
If your are here, it means you have already set up your <strong>Coop's Stripe account</strong>.<br>If that's not the case, please proceed by doing the aforementioned <a href="/en/payment_processors/stripe/#setting-up-the-cooperatives-stripe-account"><strong>here</strong></a>.
</div>

1. [Log in](https://dashboard.stripe.com/login) on the Coop Stripe account.<br>

2. Create the Restaurant Stripe account from within the Coop's Stripe account by clicking on the drop-down menu on the top-left corner where you see your Coop's name and click on **New account**.<br>

   [![Sripe New Account Add](/assets/images/stripeNewAccount.png)](/assets/images/stripeNewAccount.png){:target="\_blank"}<br>

3. In the pop-up write the name of the Restaurant that you want to link to on the platform and click **Create account**.<br>

   [![Stripe Resto Account Name](/assets/images/stripeRestoAccountName.png)](/assets/images/stripeRestoAccountName.png){:target="\_blank"}<br>

4. In the top-left corner click on **Activate your account** and follow the steps to fill in the Restaurant account details required by Stripe.<br>

   [![Stripe Activate Account](/assets/images/stripeActivateAccount.png)](/assets/images/stripeActivateAccount.png){:target="\_blank"}<br>

<span class="badge badge-info">INFO:</span><span> Request to the Restaurant owner the correct information as in this guide only the Coop can fill in these details on Stripe. After it's all set up you will be able to transfer ownership of the Stripe account to the Restaurant.</span><br>

After you've completed the activation of the account you should see the Restaurant name in the top-left drop-down menu under the Coop's name (the same place where you added a **New account**). We call this a "sub-account" because the ownership of the account belongs to the restaurant owner and not the Coop.<br>

Now you can proceed with connecting the Restaurant on CoopCycle to the Restaurant Stripe sub-account you've just activated.

### Connecting TEST mode

In the Restaurant **Payment** section on CoopCycle click the **Connect with Stripe** button.<br>

[![Stripe](/assets/images/stripeTest.png)](/assets/images/stripeTest.png){:target="\_blank"}

This will open a Stripe website where at the very top it will specify **Development Mode**, this means you are connecting the Stripe account in **TEST** mode.
You sould see the logo, name and email of your Coop on that page.
Most importantly, you should see a **Switch account** drop-down menu where the first option will be your Coop and the other options are the Stripe sub-account/s. Select the Restaurant account.<br>

<span class="badge badge-warning">ALERT:</span><span> If you don't see the <strong>Switch account</strong> drop-down menu and instead you are prompted into filling in details of the Restaurant, this means you are not logged in the Coop's Stripe account. On the same page, click on the **Log in** link on the top-right of the page in order to log in your Coop Stripe account and the page will refresh and you will be able to select the Restaurant sub-account from the drop-down menu.

[![Stripe Choose Resto](/assets/images/stripeTestChooseResto.png)](/assets/images/stripeTestChooseResto.png){:target="\_blank"}

Once you click on the restaurant from the drop-down menu the website page will refresh and below the drop-down menu now you'll see a **Connect my Stripe account** blue button. Click on it and the restaurant platform account will be linked to the Test Stripe account and you will be redirect to the restaurant's account on the platform where you will see the following message in green at the top: **Stripe account connected successfully**.

[![Stripe Connect Test Account](/assets/images/connectMyStripeAccountButton.png)](/assets/images/connectMyStripeAccountButton.png){:target="\_blank"}

### Connecting LIVE mode

In the Payment section click the **Connect with Stripe** button. _Where the Test row is you should see a green checkmark_ ✔️ _instead of the blue button._

A very similar Stripe website will open. You will notice the **Development Mode** banner is no longer there. The drop-down menu will already show selected the restaurant and you have to simply click on the **Connect my Stripe account** blue button.

If the connection was succesful you will be redirect to the restaurant's account on the platform where you will see the following message in green at the top: **Stripe account connected successfully**.

<!--

You don't have to fill in the details of the Restaurant on this page, simply proceed by clicking **Skip this account form**. The Stripe website page will close and you will return to the Restaurant settings page on the platform. If connection was successful you will see the following message in green at the top: **Stripe account connected successfully**.

[![Stripe](/assets/images/stripeTestSkip.png)](/assets/images/stripeTestSkip.png){:target="\_blank"}

-->

<!--


  - Check that “Payments” and “Payouts” are green - in case of problems contact [dev@coopcycle.org](mailto:dev@coopcycle.org)

  ![Stripe](/assets/images/stripe_resto_account_fr_5.png)


After performing these steps:

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

-->

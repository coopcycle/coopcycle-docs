---
layout: default
title: 'Setting up a restaurant'
parent: Restaurants
nav_order: 1
---

# Setting up a restaurant

<div class="alert alert-info" role="alert">
Setting up a restaurant and Stripe account in order to make it available on the platform.
</div>

[![](/assets/images/enablerestotoggle.png)](/assets/images/enablerestotoggle.png){:target="\_blank"}

---

## Creating a restaurant

1. Select <i class="fas fa-utensils"></i> **Restaurants** from the header in your instace.
2. Click on the <span class="badge badge-success">+ Create a new restaurant</span> button.

<span class="badge badge-info">TIP:</span><span> Click on the image to open it to full scale.</span>

[![](/assets/images/createrestaurant.png)](/assets/images/createrestaurant.png){:target="\_blank"}

After clicking on **Create a new restaurant** a new page will open where you have to fill in all the restaurant's account details.<br>

<span class="badge badge-warning">ATTENTION:</span><span> Before continuing on this page go to [General settings](/en/admin/restaurants/general-settings/) and configure your restaurant.</span>

## Creating a Stripe account

First of all:
1. [Log in](https://dashboard.stripe.com/login) on the Stripe account (of the cooperative)
2. Click on the drop-down menu on the top-left corner where you see your cooperative's name and click on **New account**

[![Sripe New Account Add](/assets/images/stripeNewAccount.png)](/assets/images/stripeNewAccount.png){:target="\_blank"}
3. In the pop-up write the name of the Restaurant that you want to link to on the platform and click **Create account**

[![Stripe Resto Account Name](/assets/images/stripeRestoAccountName.png)](/assets/images/stripeRestoAccountName.png){:target="\_blank"}

4. In the top-left corner click on **Activate your account**
5. Follow the steps to fill in the details of the restaurant. 
<span class="badge badge-info">INFO:</span><span> As the restaurant Stripe account is created as a sub-account of the coop, only the coop can fill in the details of the restaurant on Stripe. Further on you will be able to transfer ownership of the Stripe account to the restaurant.</span>


### Connecting Test mode

In the Payment section click the **Connect with Stripe** button. 

[![Stripe](/assets/images/stripeTest.png)](/assets/images/stripeTest.png){:target="\_blank"}

This will open a Stripe website where at the very top it will specifiy **Development Mode**, this means you are connecting the Stripe account in **Test** mode.
You don't have to fill in the details of the Restaurant on this page, simply proceed by clicking **Skip this account form**. The Stripe website page will close and you will return to the Restaurant settings page on the platform. If connection was successful you will see the following message in green at the top: **Stripe account connected successfully**.

[![Stripe](/assets/images/stripeTestSkip.png)](/assets/images/stripeTestSkip.png){:target="\_blank"}


[![](/assets/images/)](/assets/images/){:target="\_blank"}


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

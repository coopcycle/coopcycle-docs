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

<span class="badge badge-info">INFO:</span><span> Only after the restaurant has been set up properly will you be able to switch the **Disabled/Enabled** toggle.</span>

[![](/assets/images/enablerestotoggle.png)](/assets/images/enablerestotoggle.png){:target="\_blank"}

---

## Creating a restaurant

1. Select <i class="fas fa-utensils"></i> **Restaurants** from the header.
2. Click on the <span class="badge badge-success">+ Create a new restaurant</span> button.
  [![](/assets/images/createrestaurant.png)](/assets/images/createrestaurant.png){:target="\_blank"}<br>
  
<span class="badge badge-info">TIP:</span><span> Click on the image to open it to full scale.</span>

After clicking on **Create a new restaurant** a new page will open where you have to fill in all the restaurant's account details.<br>

<span class="badge badge-warning">ATTENTION:</span><span> Before continuing on this page go to [General settings](/en/admin/restaurants/general-settings/) and configure your restaurant.</span>

## Creating a Stripe account

1. [Register](https://dashboard.stripe.com/register) a Stripe account for your cooperative. If you already have a Stripe account go to step number 2.
1. [Log in](https://dashboard.stripe.com/login) on the Stripe account (of the cooperative).
2. Create the restaurant's Stripe account from within the coop's account by clicking on the drop-down menu on the top-left corner where you see your cooperative's name and click on **New account**. 
  [![Sripe New Account Add](/assets/images/stripeNewAccount.png)](/assets/images/stripeNewAccount.png){:target="\_blank"}
  
3. In the pop-up write the name of the Restaurant that you want to link to on the platform and click **Create account**.
  [![Stripe Resto Account Name](/assets/images/stripeRestoAccountName.png)](/assets/images/stripeRestoAccountName.png){:target="\_blank"}

4. In the top-left corner click on **Activate your account** and follow the steps to fill in the fields with the restaurant's details.<br>
  [![Stripe Activate Account](/assets/images/stripeActivateAccount.png)](/assets/images/stripeActivateAccount.png){:target="\_blank"}

<span class="badge badge-info">INFO:</span><span> Request to the restauant owner the correct information as only the coop can fill in the details of the restaurant on Stripe. After it's all set up you will be able to transfer ownership of the Stripe account to the restaurant.</span>

After you've completed the set up of the Stripe Account you should see the restaurant account in the top-left drop-down menu under the coop's name (the same place where you added a **New account**). We call this a sub-account because the ownership of the account belongs to the restaurant owner and not the coop.

Now you can proceed with connecting the restaurant account on CoopCycle with the Stripe account you've just finished setting up.

### Connecting TEST mode

In the Payment section of the restaurant account on CoopCycle click the **Connect with Stripe** button. 

[![Stripe](/assets/images/stripeTest.png)](/assets/images/stripeTest.png){:target="\_blank"}

This will open a Stripe website where at the very top it will specify **Development Mode**, this means you are connecting the Stripe account in **Test** mode.
You sould see the logo, name and email of your coop on that page. 
Most importantly, you should see a **Switch account** drop-down menu where the first option will be your coop and the other options are the Stripe sub-accounts. Select the restaurant account.<br>

<span class="badge badge-info">TIP:</span><span> If you don't see the <strong>Switch account</strong> drop-down menu and instead you are prompted into filling in details of the restaurant, that means you are not logged in Stripe with the coop's account. Open a new browser tab, log in into Stripe and after that go back to the Payment section on the platform and click again <strong>Connect with Stripe</strong>.</span>

[![Stripe Choose Resto](/assets/images/stripeTestChooseResto.png)](/assets/images/stripeTestChooseResto.png){:target="\_blank"}

Once you click on the restaurant from the drop-down menu the website page will refresh and below the drop-down menu now you'll see a **Connect my Stripe account** blue button. Click on it and the restaurant platform account will be linked to the Test Stripe account and you will be redirect to the restaurant's account on the platform where you will see the following message in green at the top: **Stripe account connected successfully**.

[![Stripe Connect Test Account](/assets/images/connectMyStripeAccountButton.png)](/assets/images/connectMyStripeAccountButton.png){:target="\_blank"}

### Connecting LIVE mode

In the Payment section click the **Connect with Stripe** button. *Where the Test row is you should see a green checkmark* ✔️ *instead of the blue button.*

A very similar Stripe website will open. You will notice the **Development Mode** banner is no longer there. The drop-down menu will have already selected the restaurant and you have to simply click on the **Connect my Stripe account** blue button.

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

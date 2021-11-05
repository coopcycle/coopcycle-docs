---
layout: default
title: Wordpress
parent: Plugins
---

# Set up the CoopCycle plugin

This requires that you've previously [set up a Store account](/en/admin/stores/) on your instance.

## Set up the plugin on WordPress (WooCommerce)

1. Go to **`Plugins` → `Add New`**

2. Search for **`CoopCycle`** or download the plugin from [here](https://github.com/coopcycle/coopcycle-plugins/releases/download/wordpress-0.11.2/wordpress-0.11.2.zip) and upload it manually.

3. Click **`Install Now`** to install CoopCycle plugin.

4. Click **`Activate`** after installation has finished

5. Go to **`Plugins`** → **`Installed Plugins`**

6. In the plugins panel go to **`CoopCycle`** → **`Settings`**

7. In the **Base URL** enter the URL of your instance: [https://demo.coopcycle.org/](https://demo.coopcycle.org/)

   <div class="shadow p-3 mb-3 bg-white rounded border border-danger">
   <span class="badge badge-danger">IMPORTANT:</span>
   <span> Make sure you type the forward slash <code>/</code> at the end of the URL</span>
   </div>
   
8. If you are the developer of the Business's website, request the API keys from the Coop administrator.  
   (Without API Keys you won't be able continue setup of the plugin).

9.  Click **Save Changes** 


10. Go to **`WooCommerce`** → **`Settings`** → **`Shipping`** tab

11. Click **`Add Shipping Zone`**

    <div class="shadow p-3 mb-3 bg-white rounded border border-warning">
    <span class="badge badge-warning">ATTENTION:</span>
    <span> If you have more than one (1) <code>Shipping zones</code> make sure to move the smnaller shipping to the top. Otherwise the Coop shipping method will not be displayed at checkout.</span>
    </div>

12. Fill out the **details** as follows:

    ### Zone name
    Type in the name of the city or the name of the Coop.


    ### Zone region
    Select the specific region from the dropdown menu.

    <!--Click on **Limit to specific postcodes** to open an input field where you will need to enter a list of postcodes which correspond the delivery area. 
    Download/open this file below ↓ and copy the whole list of postcodes and paste it in the `Zone regions` under United Kingdom.-->

    Click `Save changes`.


13. Click **Add shipping method** on the same screen.


14. Select **`CoopCycle`** from the dropdown menu and click **Add shipping method**.

15. Click **Save Changes**

16. Done! Add an item to your shop's cart, open your cart, and the Coop shipping method should be automatically displayed or allowed to select it.

<!--Overview
--------

The CoopCycle plugin for WordPress allows to add a [shipping method](https://docs.woocommerce.com/document/setting-up-shipping-zones/) to WooCommerce,
and to transmit the shipping data to CoopCycle directly, using the API.

If one of your partners already has an e-commerce website based on WooCommerce, it the best way to have a seamless integration.

On CoopCycle, the shipping data sent will be attached to a [store](../_admin/stores.md), so you will need to create a store if you don't have one already.
The settings of the store modify the behavior of the plugin, in particular the configuration of the time slot used.

Obtaining an API token
----------------------

The first thing to do is to obtain an API token, so that the website running WooCommerce can interact with the CoopCycle API.

Go to Configuration › API, and click « Add ». Enter the name of the app (for example, the name of the website running WooCommerce), select the store you want to generate an API token for, and hit « Save ».

You should obtain a pair of credentials, a « API Key » and « API Secret », that you will need to configure the plugin.

Installing and configuring the plugin
-------------------------------------

The CoopCycle plugin for WooCommerce can be installed from [wordpress.org](https://wordpress.org/plugins/coopcycle/).

In the WordPress admin area, go to the Plugins page, and search for « coopcycle ».

In the settings page of the plugin, enter the base url of the CoopCycle instance, the « API Key » and « API Secret », and save changes.

Configuring WooCommerce
-----------------------

Once the CoopCycle plugin is configured, you need to add to a [shipping method to a zone](https://docs.woocommerce.com/document/setting-up-shipping-zones/#section-6).

Go to WooCommerce › Settings › Shipping. If you haven't already, click on « Add shipping zone », or edit one of your existing shipping zones.

Click on « Add shipping method », and select « CoopCycle ».

Once the shipping method has been added, you can configure it. The settings are the same as the standard [Flat Rate Shipping](https://docs.woocommerce.com/document/flat-rate-shipping/) method of WooCommerce.

The most important thing that you need to configure is the **shipping cost**.

Congratulations! 🎉

Now, when entering an address that matches with the shipping zone, customers will be allowed to choose the CoopCycle shipping method.-->

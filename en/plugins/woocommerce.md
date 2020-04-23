---
lang: en
title: WooCommerce
ref: plugins-woocommerce
parent: Plugins
---

CoopCycle ships with a [WordPress plugin for WooCommerce](https://wordpress.org/plugins/coopcycle/).

Overview
--------

The CoopCycle plugin for WordPress allows to add a [shipping method](https://docs.woocommerce.com/document/setting-up-shipping-zones/) to WooCommerce,
and to transmit the shipping data to CoopCycle directly, using the API.

If one of your partners already has an e-commerce website based on WooCommerce, it the best way to have a seamless integration.

On CoopCycle, the shipping data sent will be attached to a [store](en/admin/stores), so you will need to create a store if you don't have one already.
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

Now, when entering an address that matches with the shipping zone, customers will be allowed to choose the CoopCycle shipping method.

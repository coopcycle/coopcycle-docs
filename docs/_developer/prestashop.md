---
layout: default
title: PrestaShop
parent: Plugins
---

# Set up the CoopCycle plugin

This requires that you've previously [set up a Store account](/en/admin/stores/) on your instance.

1. Unfortunately, our PrestaShop plugin is not available on PrestaShop Addons. You will need to download [the latest version of the PrestaShop module from GitHub, as a .zip file](https://github.com/coopcycle/coopcycle-plugins/releases).

2. In the PrestaShop back-office, go to **`Modules`** → **`Module Manager`**, click on **`Upload a module`**, and select the .zip file that you downloaded on your computer.

3. Once installed, you will need to configure the plugin. In the **Base URL** enter the URL of the target instance (for example, [https://demo.coopcycle.org/](https://york.coopcycle.org/)). If you are the developer of the Business's website, request the API keys from the Coop administrator. (Without API Keys you won't be able continue setup of the plugin).

4. The module will create a **carrier** named CoopCycle. You will need to configure this carrier according to your requirements & agreements.

![Configure CoopCycle Carrier](/assets/images/ps_carrier_config.gif)

5. Done! Add an item to your shop's cart, open your cart, and the CoopCycle carrier should be selectable. Once selected, a dropdown with time slot choices should be presented to the customer.

![Shopping Cart Example](/assets/images/prestashop_shopping_cart.png)


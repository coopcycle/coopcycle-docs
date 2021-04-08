---
layout: default
title: "TEST mode"
parent: Stripe
nav_exclude: true
---

# Place orders in TEST mode

<div class="alert alert-info" role="alert">
You can only place TEST orders if you have set up:<br>

<ul>
<li><a href="http://localhost:4000/en/payment_processors/stripe/#setting-up-the-cooperatives-stripe-account">the Stripe CoopCycle account</a></li>
<li><a href="/en/admin/restaurants/creating-a-restaurant/#creating-a-restaurant-on-coopcycle">a Restaurant on the Platform</a></li>
<li><a href="http://localhost:4000/en/admin/restaurants/creating-a-restaurant/#creating-a-restaurant-stripe-account">a Restaurant Stripe account</a></li>
</ul>
</div>

---

After every new Restaurant you set up, it's always best practice to place a TEST order with that Restaurant. This can help avoid any issues when **real customers** place **real orders**.

## Enable TEST mode on the Platform

1. On the top-level menu go to `Configuration` > `Settings`<br>

   [![Configuratio settings Test Mode](/assets/images/001TESTmodeConfigSettings.png)](/assets/images/001TESTmodeConfigSettings.png){:target="\_blank"}<br>

2. Scroll down at the bottom of the **Stripe Account** section toggle the **User Stripe in << live >> mode** off.<br>

   [![Toggle Off Stripe Live](/assets/images/002TESTmodeToggleOffStripeLive.png)](/assets/images/002TESTmodeToggleOffStripeLive.png){:target="\_blank"}<br>

3. On the popup click on <span class="badge badge-danger">Switch to << test >> mode and enable maintenance</span> to enable TEST mode on the Platform.<br>

    <div class="alert alert-danger" role="alert">
    <h3>WARNING</h3>
    When Maintenance mode is ON (enabled) the Platform is completely disabled and it's only operable by an Admin user.
    <hr><p class="mb-0">Once the Platform is in LIVE and real orders are placed, make sure to use TEST mode after working hours, as customers won't be able to place REAL orders in TEST mode.</p>

    </div>
    

    Here is what the Platform looks like for non-admin users when **Maintenance mode** is ON.<br>

    [![TEST mode Platform Disabled Non Admin User](/assets/images/003TESTmodePlatformDisabledNonAdminUser.png)](/assets/images/003TESTmodePlatformDisabledNonAdminUser.png){:target="\_blank"}<br>

4. Above the **Stripe Account** section you can toggle OFF **Maintenance mode** and clicking on <span class="badge badge-success">Disable maintenance</span> from the pop-up<br>

    [![Disable Maintenance Mode](/assets/images/004TESTmodeToggleOffMaintenanceMode.png)](/assets/images/004TESTmodeToggleOffMaintenanceMode.png){:target="\_blank"}

    <span class="badge badge-info">TIP:</span><span> You can decide whether to keep <strong>Maintenance mode</strong> ON or toggle it OFF whilst he Platform is on <strong>TEST</strong> mode. When <strong>Maintenance mode</strong> is OFF you can place TEST orders as a non-admin user.</span><br>

## Place a TEST order

1. Go to the Restaurant homepage.
2. Proceed with the steps of placing an order

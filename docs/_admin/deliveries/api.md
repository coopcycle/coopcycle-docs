---
layout: default
title: API
parent: Deliveries
---

# API

<div class="alert mt-3 alert-info" role="alert">
This allows for integration of the CoopCycle platform via the WordPress (WooCommerce) and Prestashop plugins.
<hr><p class="mb-0">An API is a pair of <em>keys</em> (<strong>Identifier</strong> and <strong>Secret key</strong>) which is use to integrate different softwares.</p>
</div>

---

## First things first

If you need to create and use this API it means your client (a business you deliver for) have their own website with e-commerce.

## What does the API do?

It allows for deliveries placed on a third-party website to be sent directly to the Store account on your CoopCycle instance.

These purchases (deliveries) will show up under your client's Store account.

## Create the API keys

<div class="alert mt-3 alert-warning" role="alert">
Before creating the <em>keys</em> (<strong>Identifier</strong> and <strong>Secret key</strong>) you need to <a href="/en/admin/stores/">create a Store</a> for that business. A pair of API keys are created for each individual Store.
</div>

On the API main page a list of all create API keys will be displayed.

1. Click the <span class="badge badge-success"> <i class="fa fa-plus"></i> Add</span> button to create an API key
2. Give your API key pair an easily indentifable name under `App name`
3. Choose the Store under `Store`
4. Click <span class="badge badge-primary">Save</span>

After you've created the keys, you will be automatically directed to the API main page. 
## Use the API keys

<div class="alert mt-3 alert-danger" role="alert">
⚠️ Only share the API with the developer of your client's website who will set up the CoopCycle plugin.
</div>

Use the <i class="fa fa-copy"></i> `Copy` button for each key and send them securely to the person who will configure the plugin.

See here on how to set up the CoopCycle plugin go.

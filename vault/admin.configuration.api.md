---
id: 70e34ac3-b89c-4d64-9dfa-2ab23ce85083
title: API
desc: ""
updated: 1604793287789
created: 1604769912018
---

<link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.5.0/css/bootstrap.min.css" integrity="sha384-9aIt2nRpC12Uk9gS9baDl411NQApFmC26EwAOH8WgZl5MYYxFfc+NcPb1dKGj7Sk" crossorigin="anonymous">
<script src="https://code.jquery.com/jquery-3.5.1.slim.min.js" integrity="sha384-DfXdz2htPH0lsSSs5nCTpuj/zy4C+OGpamoFVy38MVBnE+IbbVYUew+OrCXaRkfj" crossorigin="anonymous"></script>
<script src="https://cdn.jsdelivr.net/npm/popper.js@1.16.0/dist/umd/popper.min.js" integrity="sha384-Q6E9RHvbIyZFJoft+2mJbHaEWldlvI9IOYy5n3zV9zzTtmI3UksdQRVvoxMfooAo" crossorigin="anonymous"></script>
<script src="https://stackpath.bootstrapcdn.com/bootstrap/4.5.0/js/bootstrap.min.js" integrity="sha384-OgVRvuATP1z7JjHLkuOU7Xw704+h835Lr+6QL9UvYjZE3Ipu6Tp75j7Bh/kR0JKI" crossorigin="anonymous"></script>
<!-- Font Awesome -->
<script src="https://kit.fontawesome.com/489c6dd9c4.js" crossorigin="anonymous"></script>

# API

<div class="alert alert-info" role="alert">
API to integrate the CoopCycle plugin for WordPress websites with WooCommerce.
<hr><p class="mb-0">API is a pair of <em>keys</em> (<strong>Identifier</strong> and <strong>Secret key</strong>) which you use to integrate different softwares.</p>
</div>

---

## First things first

If you need to create and use this API it means your client (a business you deliver for) have a **WordPress** online shop with **WooCommerce**.

## What does the API do?

It allows for purchases on a WordPress website with WooCommerce be sent directly into your CoopCycle instance.

These purchases (orders) will show up under your client's Store account.

## Create the API keys

<div class="alert alert-warning" role="alert">
Before creating the <em>keys</em> (<strong>Identifier</strong> and <strong>Secret key</strong>) you need to create a Store for that business.
</div>

<div class="alert alert-info" role="alert">
A pair of API keys are created for each individual Store.
</div>

1. Click the <span class="badge badge-success">+ Add</span> button
2. Give your API key pair a name under `App name`
3. Choose the Store under `Store`
4. Click the blue button <span class="badge badge-primary">Save</span>

After you've created the keys, you will be automatically directed to the API main page. The newly created API keys should like this with the respective name and Store you chose.

![](/assets/images/2020-11-07-20-21-25.png)

## Use the API keys

<div class="alert alert-danger" role="alert">
⚠️ You have to share these keys only with the developer of the WordPress website who will set up the CoopCycle plugin.
</div>

Use the <i class="fa fa-copy"></i> `Copy` button for each key and send them securely to the person who will configure the plugin.

To learn how to set up the CoopCycle plugin go [here]().



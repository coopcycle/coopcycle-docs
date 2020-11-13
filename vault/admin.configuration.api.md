---
id: 70e34ac3-b89c-4d64-9dfa-2ab23ce85083
title: API
desc: ""
updated: 1605290701864
created: 1604769912018
---

<!-- CSS -->
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@4.5.3/dist/css/bootstrap.min.css" integrity="sha384-TX8t27EcRE3e/ihU7zmQxVncDAy5uIKz4rEkgIXeMed4M0jlfIDPvg6uqKI2xXr2" crossorigin="anonymous">
<!-- jQuery and JS bundle w/ Popper.js -->
<script src="https://code.jquery.com/jquery-3.5.1.slim.min.js" integrity="sha384-DfXdz2htPH0lsSSs5nCTpuj/zy4C+OGpamoFVy38MVBnE+IbbVYUew+OrCXaRkfj" crossorigin="anonymous"></script>
<script src="https://cdn.jsdelivr.net/npm/bootstrap@4.5.3/dist/js/bootstrap.bundle.min.js" integrity="sha384-ho+j7jyWK8fNQe+A12Hb8AhRq26LrZ/JpcUGGOn+Y7RsweNrtN/tE3MoK7ZeZDyx" crossorigin="anonymous"></script>
<!-- Font Awesome -->
<script src="https://kit.fontawesome.com/489c6dd9c4.js" crossorigin="anonymous"></script>

# API

<div class="alert alert-info" role="alert">
API to integrate the CoopCycle plugin with third-party websites, such as a WordPress websites with WooCommerce.
<hr><p class="mb-0">API is a pair of <em>keys</em> (<strong>Identifier</strong> and <strong>Secret key</strong>) which you use to integrate different softwares.</p>
</div>

---

## First things first

If you need to create and use this API it means your client (a business you deliver for) have their own website with e-commerce.

## What does the API do?

It allows for orders placed on a third-party website to be sent directly to the Store account on your CoopCycle instance.

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
⚠️ Only share these keys with the developer of your client's website who will set up the CoopCycle API.
</div>

Use the <i class="fa fa-copy"></i> `Copy` button for each key and send them securely to the person who will configure the plugin.

To learn how to set up the CoopCycle plugin go [here]().

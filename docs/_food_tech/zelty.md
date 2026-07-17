---
layout: default
title: Zelty
---

# Zelty Integration

[Zelty](https://zelty.fr) is a POS (point-of-sale) system used by some restaurants. The integration does two things:

1. **Catalog sync** — Zelty pushes its product catalog to CoopCycle so the ordering UI always reflects what's available in the POS.
2. **Order push** — When a customer places an order on CoopCycle, it is forwarded to Zelty so kitchen staff see it on the POS.

## Connecting CoopCycle to Zelty

To connect CoopCycle to Zelty, you first need to enable CoopCycle on [Zelty Marketplace](https://www.zelty.fr/pourquoi-zelty/zelty-partenaire-digitalisation-restaurant).

<a type="button" class="btn btn-primary" href="https://bo.zelty.fr/marketplace/coopcycle/status" target="_blank">Enable CoopCycle on Zelty</a>

Once enabled, Zelty will generate an API Key. 

<span class="zoomable">![Zelty Marketplace](/assets/images/zelty_marketplace.png)</span>

---

Copy the Zelty API Key from the Marketplace, paste it in the Zelty tab of your restaurant in CoopCycle, and click on « Connect to Zelty »

<div class="alert alert-warning" role="alert">
Make sure to save your API Key somewhere, Zelty will show the API Key only during a few minutes.
</div>

<span class="zoomable">![Zelty Connect - Step 1](/assets/images/zelty_connect_step_1.png)</span>

If the API Key is valid, you will be asked to configure the dish that will be used to hold the delivery fee.
You may also let us create it for you, by clicking on the « Create "Delivery fee" on Zelty » button.

<span class="zoomable">![Zelty Connect - Step 2](/assets/images/zelty_connect_step_2.png)</span>

## Sending your catalog to CoopCycle

It's now time to send us your catalog so that we can display the same menus & dishes on the platform.

In Zelty, go to the catalog you want use on CoopCycle (this may be a different catalog than the one you are using on site), and click on « Envoyer vers ». 

<span class="zoomable">![Zelty Catalog Push - Step 1](/assets/images/zelty_catalog_push_step_1.png)</span>

Select « CoopCycle », and click on « Envoyer »

<span class="zoomable">![Zelty Catalog Push - Step 3](/assets/images/zelty_catalog_push_step_2.png)</span>

After a few seconds, a new catalog should appear on CoopCycle. Enable it, and you are done!

<span class="zoomable">![Zelty Catalog Push - Step 3](/assets/images/zelty_catalog_push_step_3.png)</span>

---
layout: default
title: Introduction
parent: Pricing
nav_order: 1
---

# Pricing

<div class="alert mt-3 alert-info" role="alert">

Pricing can be configured on the <a href="/en/web/admin/deliveries/pricing">Pricing page</a>

</div>

CoopCycle's pricing rules are the result of many different people asking for many different types of pricing rules over time. This means that pricing rules are highly complex, but if you understand how they work and have a bit of imagination, you can probably do most anything. Here we will talk exclusively about the pricing rules that apply to **non-platform deliveries** (i.e. restaurant food tech orders paid over Stripe). There are 4 main types of deliveries that are easily programmed in CoopCycle currently:

1. [**Old School Bike Messenger Pricing**](/en/admin/pricing_old_school/)

   Rates based on kilometers, with supplemental charges based on weight and other characteristics.
   
   <span class="badge badge-info">EXAMPLE:</span> <span>A fruit shop that has a dozen orders a week, and has 3 sizes of fruit boxes with different weights that are charged differently. These clients get a call from their own client, open CoopCycle, and make the order while talking to their client over the phone in order to charge the final client a part of the CoopCycle delivery fee based on the calculation they see in the website. This could also be lawyers, clothing shops, or any other type of small local commerce with unpredictable but constant deliveries. <span>

   <span class="badge badge-primary">FORMAT:</span> <span>A pricing rule of this type will usually have a km-based rule, plus supplemental charges for extra weight or volume. <span>



2. [**Very Complete But Complex Pricing**](/en/admin/pricing_complex/) <span class="badge badge-success">**Recommended if Possible**</span>

   Rates based on many characteristics, attempting to have a rule that will apply to as many types of clients possible in as many parts of the city as possible.

   <span class="badge badge-info">EXAMPLE:</span> <span>This is when a cooperative works over a large geographic area, uses zones to reflect distances instead of kilometers, and has clients with a wide variety of services they might request. An example of this could be a bakery that has regular deliveries of large quantities of bread to local shops and points of sale in the morning, but then also has irregular deliveries of gift baskets throught the week of varying sizes. A single pricing rule will have to reflect multiple types of services, many different areas, and once it has been completed, it may make sense to use for many different shops and thereby standarize the commercial, delivery, and invoicing tasks. <span>

   <span class="badge badge-primary">FORMAT:</span> <span>A pricing rule of this type will often combine base prices to move between zones, plus weight and volume supplements, plus charges that relate to how urgent a delivery is and to how much advance warning the delivery is made. <span>

3. [**Multi-Dropoff Pricing**](/en/admin/pricing_multi_dropoff/) <span class="badge badge-success">**Recommended if Possible**</span>

   Rates that allow for clients to ask for many deliveries at once, instead of one by one.

   <span class="badge badge-info">EXAMPLE:</span> <span>A service the is often requested multiple times a week to move blood and urine samples from homes for the elderly, to a laboratory and then return the package. However, there are multiple elderly homes and multiple laboratories so sometimes the task is a single pickup and a single dropoff, or it may be multiple pickups and one dropoff, or a pickup + a dropoff + a dropoff. In order to facilitate the client, we want all these possible use cases to be made in one type of purchase process. <span>

   <span class="badge badge-primary">FORMAT:</span> <span>A price of this type will usually have a base price per "point" (a pick-up of dropoff) with suppliments of weight or volume or urgency for each point. <span>

4. [**Last Mile At Volume**](/en/admin/pricing_lastmile/)

   Simple rates made for a client that gives you a large volume of orders with relatively standardized characteristics.

   <span class="badge badge-info">EXAMPLE:</span> <span>This is usually when a large entity requests that a cooperative delivers 50+ of a standarized item like a magazine over the course of multiple days. <span>

   <span class="badge badge-primary">FORMAT:</span> <span>This often is a price that is a simple price per point that reflets an average that both sides agree is equitable. The client likely uses an excel to upload their large list of tasks. <span>

---
## First Steps
The first thing you need to do is think carefully about how you want to charge your client. As about their needs in detail so that you make a complete rule, and don't have to remake it a week after starting service in order to account for something they forgot to mention. Remember, a price rule really is made up of a series of rules in the `Pricing` page, rules that base themselves on characteristics like kilometers or time that are built off of the configurations you make of `Time slots`, `Packages` and `Zones`. 

Given this, first think about the geographic realities of this delivery. Are there zones in your city that are easier to pass between than others? What natural barriers are there that impede delivery?

Think about the types of packages they will be giving you. Should you differentiate between a 5kg box and a 10kg box or can you use an average of the two to make a standard price? 

Think about the time requirements. Do you want to incentivize them economically to program deliveries for the next day instead of immedaitely? Or do you prefer immedaite and more expensive deliveries? How do their deliveries fit into your existing workflow? You can offer delivery windows of 15 minutes, or the entire morning, or you can offer both and charge differently. 

Once you have thought about these factors and created some zones, package lists, and delivery time slots, **now** you are ready to make your first pricing rule.

---

## Next Steps

[Create a custom pricing](/en/admin/pricing_basics/)


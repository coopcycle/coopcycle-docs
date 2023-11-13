---
layout: default
title: Pricing
parent: Deliveries
---

# Pricing

<div class="alert mt-3 alert-info" role="alert">
Here you can configure a custom pricing to use for Orders forms, Restaurants and Stores.<br>
The custom pricing can contain multiple Rules and each Rule can be configured by combining the different Conditions. <!--See <a href="/en/admin/deliveries/pricing/#definitions-of-conditions">Definitions of Conditions</a> to know more.-->

</div>

---

## The Basics
CoopCycle's pricing rules are the result of many different people asking for many different types of pricing rules over time. This means that pricing rules are highly complex, but if you understand how they work and have a bit of imagination, you can probably do most anything. Here we will talk exclusively about the pricing rules that apply to **non-platform deliveries** (i.e. restaurant food tech orders paid over Stripe). There are 4 main types of deliveries that are easily programmed in CoopCycle currently:

1. **Old School Bike Messenger Pricing:** Rates based on kilometers, with supplemental charges based on weight and other characteristics.
   
    <span class="badge badge-info">EXAMPLE:</span> <span>A fruit shop that has a dozen orders a week, and has 3 sizes of fruit boxes with different weights that are charged differently. These clients get a call from their own client, open CoopCycle, and make the order while talking to their client over the phone in order to charge the final client a part of the CoopCycle delivery fee based on the calculation they see in the website. This could also be lawyers, clothing shops, or any other type of small local commerce with unpredictable but constant deliveries. <span>
    <span class="badge badge-info">FORMAT:</span> <span>A pricing rule of this type will usually have a km-based rule, plus supplemental charges for extra weight or volume. <span>

3. **Very Complete But Complex Pricing:** Rates based on many characteristics, attempting to have a rule that will apply to as many types of clients possible in as many parts of the city as possible. This is when a cooperative works over a large geographic area, uses zones to reflect distances instead of kilometers, and has clients with a wide variety of services they might request. An example of this could be a bakery that has regular deliveries of large quantities of bread to local shops and points of sale in the morning, but then also has irregular deliveries of gift baskets throught the week of varying sizes. A single pricing rule will have to reflect multiple types of services, many different areas, and once it has been completed, it may make sense to use for many different shops and thereby standarize the commercial, delivery, and invoicing tasks. A pricing rule of this type will often combine base prices to move between zones, plus weight and volume supplements, plus charges that relate to how urgent a delivery is and to how much advance warning the delivery is made. 

4. **Multi-Dropoff Pricing:** Rates that allow for clients to ask for many deliveries at once, instead of one by one. An example of this is a service the is often requested multiple times a week to move blood and urine samples from homes for the elderly, to a laboratory and then return the package. However, there are multiple elderly homes and multiple laboratories so sometimes the task is a single pickup and a single dropoff, or it may be multiple pickups and one dropoff, or a pickup + a dropoff + a dropoff. In order to facilitate the client, we want all these possible use cases to be made in one type of purchase process. A price of this type will usually have a base price per "point" (a pick-up of dropoff) with suppliments of weight or volume or urgency for each point. 

5. **Last Mile At Volume:** Simple rates made for a client that gives you a large volume of orders with relatively standardized characteristics. This is usually when a large entity requests that a cooperative delivers 50+ of a standarized item like a magazine over the course of multiple days. This often is a price that is a simple price per point that reflets an average that both sides agree is equitable. The client likely uses an excel to upload their large list of tasks. 

---

## Create a custom pricing
1. From the top menu go to `Deliveries`
2. On the left-hand side go to `Pricing`
3. Click on <span class="badge badge-success"><i class="fa fa-plus"></i> Create a new pricing</span>
4. Give the Pricing a name.
   
   <span class="badge badge-info">TIP:</span><span> The pricing name can be the name of the Order Form, Store, Restaurant or a specific name that makes it easy to know what the custom pricing is meant for</span>.
5. Under **Rules** click on <span class="badge badge-success"> <i class="fa fa-plus"></i> Add rule</span>
6. Write the price of the rule at the bottom
7. Click on <span class="badge badge-warning"><i class="fa fa-plus"></i> Add condition</span> to add one or as many conditions as necessary (to know more see Definitions of conditions).
8. Choose a **method of calculation**:
   
      <span class="badge badge-info">INFO: </span><span> <strong>A matching rule</strong> is a rule where <strong>all</strong> the Conditions are true </span>.
   
   a. **The first rule that matches** works best with **Fixed price**.

      [![](/assets/images/pricingFirstRulePlusFixedPrice.png)](/assets/images/pricingFirstRulePlusFixedPrice.png){:target="\_blank"}

    Because you can have multiple Rules under one Pricing, **the first rule that matches** means that, beginning from top to bottom, the first Rule that complies with all the Conditions will be the only one which will display the price to the customer and the remaining rules, if any, will be skipped.
    **Example**:
     - In the image below there are three (3) Rules, each in a coloured box and each with the same type of condition (**Weight (kg)**) but different variables.
     - If a customer places an order where the parcel weighs `2 kg` the cost of that order will be `3` (the curreny is set depending on the country you're in).
     - If a customer places an order where the parcel weighs `5.5 kg` the cost of that order will be `5`.
     - If a customer places an order where the parcel weighs `10 kg` the cost of that order will be `7`.
  
         [![](/assets/images/pricingFirstMatchingRule.png)](/assets/images/pricingFirstMatchingRule.png){:target="\_blank"}  


    b. **All the matching rules** works best with **Price by range**

      In any given number of **rules** if **ALL** the **conditions** are true, the price of **ALL** those rules will be added together. If there is one or more rule where one or more conditions are not true, those rules are excluded and get skipped.

      In the example below, all the conditions in Rule 1, 2 and 4 are true, meaning the total price the customer pays is 12.

      |           | Rule 1 ✔️ | Rule 2 ✔️ | Rule 3 ❌ | Rule 4 ✔️ | TOTAL  |
      | --------- | -------- | -------- | -------- | -------- | ------ |
      | **Price** | 4        | 3        | 7        | 5        | **12** |

      An usual *use case* for this custom pricing is the following:

      |                    | Rule 1 ✔️ | Rule 2 ✔️              |
      | ------------------ | -------- | --------------------- |
      | **Fixed price**    | 4        | -                     |
      | **Price by range** | -        | 1 🔄                   |
      | **Distance (km)**  | > 0km    | between 3.1 and 3.9km |
      | **TOTAL AMOUNT**   | **4**    | **5**                 |

      **Rule 1** is usally set with a **Fixed price** and **Rule 2** is set with **Price by range** where the set amount gets added over and over again 🔄 as many times as the formula indicates.

      [![](/assets/images/pricingAllMatchingRules.png)](/assets/images/pricingAllMatchingRules.png){:target="_blank"}


      <span class="badge badge-info">IMPORTANT:</span><span> Make sure the condition(s) in <strong>Rule 1</strong> are always true. E.g.: `Distance (km) > 0`</span>

      - if the customer lives less then or up to 3km away from the **collection** address, they will pay `4`, because `Distance (km)` is more `>` than `0` and more `>` than `3` in **Rule 2**.
      - if the customer lives between 3.1 and 3.9 km from the **collection** address, they will pay `5` and if they live between 4 km and 4.1 km from the **collection** address they will pay `6` and so on, because `Distance (km)` is more `>` than `3` and they pay extra `1` for each `1 km` above `3 km`  
  
9.  After you've configured your custom pricing, click <span class="badge badge-primary">Save</span>


### Definitions of conditions
Brief description on each condition.

| CONDITIONS             | DEFINITION                                                                                                              |
| ---------------------- | ----------------------------------------------------------------------------------------------------------------------- |
| **Distance (km)**      | Determines the radius delivery area with the Business as the centre                                                     |
| **Weight (kg)**        | Conditions the price depending on the inputted weight of the parcel                                                     |
| **Bike type**          | Allows for a choice of "regular" or "cargo" bike                                                                        |
| **Pickup address**     | Allows the selection of a Zone that contains the Pickup address                                                         |
| **Dropoff address**    | Allows the selection of a Zone that contains the Dropoff address                                                        |
| **Difference (hours)** | Allows inputting a number indicating how many hours ahead a Delivery has to be placed. It can also condition the price. |
| **Difference (days)**  | Allows inputting a number indicating how many days ahead a Delivery has to be placed. It can also condition the price.  |
| **Doorstep dropoff**   | Indicates if a delivery should be handed to the customer                                                                |
| **Packages**           | Conditions the price depending on the type of package                                                                   |
| **Items total**        | Conditions the price dependand on the total amount of money on an order                                                 |

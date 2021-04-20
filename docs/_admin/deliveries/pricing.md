---
layout: default
title: Pricing
parent: Deliveries
---

# Pricing

<div class="alert alert-info" role="alert">
Here you can configure a custom pricing to use for Orders forms, Restaurants and Stores.<br>
The custom pricing can contain multiple Rules and each Rule can be configured by combining the different Conditions. <!--See <a href="/en/admin/deliveries/pricing/#definitions-of-conditions">Definitions of Conditions</a> to know more.-->

</div>

---

## Create a custom pricing
1. From the top menu go to `Deliveries`
2. On the left-hand side go to `Pricing`
3. Click on <span class="badge badge-success">+ Create a new pricing</span>
4. Give the Pricing a name.
   
   <span class="badge badge-info">TIP:</span><span> The pricing name can be the name of the Order Form, Store, Restaurant or a specific name that makes it easy to know what the custom pricing is meant for</span>.
5. Under **Rules** click on <span class="badge badge-success">+ Add rule</span>
6. Write the price of the rule at the bottom
7. Click on <span class="badge badge-warning">+ Add condition</span> to add one or as many conditions as necessary (to know more see Definitions of conditions).
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
Brief description on each condition and its use.

**COMING SOON**

<!--
<strong>Delivery</strong>
<ul>
<li>Distance (km)</li>
<li>Weight (kg)</li>
<li>Bike type</li>
<li>Pickup address</li>
<li>Dropoff address</li>
<li>Difference (hours)</li>
<li>Difference (days)</li>
<li>Doorstep dropoff</li>
<li>Packages</li>
</ul>
<strong>Order</strong>
<ul>
<li>Items total</li>
</ul>
-->





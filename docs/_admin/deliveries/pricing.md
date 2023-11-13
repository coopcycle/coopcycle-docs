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

   <span class="badge badge-primary">FORMAT:</span> <span>A pricing rule of this type will usually have a km-based rule, plus supplemental charges for extra weight or volume. <span>

3. **Very Complete But Complex Pricing:** Rates based on many characteristics, attempting to have a rule that will apply to as many types of clients possible in as many parts of the city as possible.

    <span class="badge badge-info">EXAMPLE:</span> <span>This is when a cooperative works over a large geographic area, uses zones to reflect distances instead of kilometers, and has clients with a wide variety of services they might request. An example of this could be a bakery that has regular deliveries of large quantities of bread to local shops and points of sale in the morning, but then also has irregular deliveries of gift baskets throught the week of varying sizes. A single pricing rule will have to reflect multiple types of services, many different areas, and once it has been completed, it may make sense to use for many different shops and thereby standarize the commercial, delivery, and invoicing tasks. <span>

    <span class="badge badge-primary">FORMAT:</span> <span>A pricing rule of this type will often combine base prices to move between zones, plus weight and volume supplements, plus charges that relate to how urgent a delivery is and to how much advance warning the delivery is made. <span>

6. **Multi-Dropoff Pricing:** Rates that allow for clients to ask for many deliveries at once, instead of one by one.

    <span class="badge badge-info">EXAMPLE:</span> <span>A service the is often requested multiple times a week to move blood and urine samples from homes for the elderly, to a laboratory and then return the package. However, there are multiple elderly homes and multiple laboratories so sometimes the task is a single pickup and a single dropoff, or it may be multiple pickups and one dropoff, or a pickup + a dropoff + a dropoff. In order to facilitate the client, we want all these possible use cases to be made in one type of purchase process. <span>

   <span class="badge badge-primary">FORMAT:</span> <span>A price of this type will usually have a base price per "point" (a pick-up of dropoff) with suppliments of weight or volume or urgency for each point. <span>

9. **Last Mile At Volume:** Simple rates made for a client that gives you a large volume of orders with relatively standardized characteristics.

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

---
## Example Rules

### 1. **Old School Bike Messenger Pricing**
   
   <span class="badge badge-success">When to use</span> <span>When you have clients who have deliveries that may go to any place in the city in unpredictable ways, so you must default to km-based pricing rules. **Pros:** Simple, can't accidentally give a wrong price, easy for clients to understand<span>

    <span class="badge badge-danger">When **not** to use</span> <span>If you can avoid it, do. Do not use if you have any type of client other than that described above. **Cons:** This pricing rule is easy, but cannot be used for deliveries with multiple points since they will be charged more or less based on if they order the deliveries efficiently or not, which is not their concern. It also imagines you are only delivering their package, and not mixing with other clients in an effective way. Effectively, this is a pricing rule made for a type of delivery that is not longer common or strategically interesting for your business, creating unintended limitations long-term.<span>

   **Configuration of the shops**
   ![image](https://github.com/coopcycle/coopcycle-docs/assets/77277854/114d03e9-be37-440b-b0eb-a7fd82f254f2)

   **Standard Time Slot**
   ![image](https://github.com/coopcycle/coopcycle-docs/assets/77277854/ad0a2f29-4fac-4c07-afcb-3291f2e211b3)

   **Pacakge Set**
   ![image](https://github.com/coopcycle/coopcycle-docs/assets/77277854/d4b540a0-8f7c-47ca-bef1-349c65c9aced)

   **Price Rules**
   ![image](https://github.com/coopcycle/coopcycle-docs/assets/77277854/692c1da7-caaf-45d7-9311-3a6b3ce5b12b)

   **A Typical Delivery**
   ![image](https://github.com/coopcycle/coopcycle-docs/assets/77277854/7b47c7c7-6b23-4643-87b7-4f7bcad5894b)

### 2. **Very Complete But Complex Pricing** <span class="badge badge-success">**Recommended if Possible**</span>
   
   <span class="badge badge-success">When to use</span> <span>Clients who have many different types of deliveries, multiple pickup locations in different parts of the city. Bakeries, florists, other types of local commerce. **Pros:** Can be used to make a standard pricing rule that simplifies commercial capture and operations, is more "fair" and precise<span>

     <span class="badge badge-danger">When **not** to use</span> <span>A simple client who wants a simple price they understand and will be put off by math and large tables **Cons:** Can confuse small business owners and make the commercial process harder. The more complex a rule gets, the harder it is to modify later.<span>

   **Configuration of the shop**
   ![image](https://github.com/coopcycle/coopcycle-docs/assets/77277854/d1e5aecc-6f68-497c-8e84-bc42e38d75e2)
   ![image](https://github.com/coopcycle/coopcycle-docs/assets/77277854/e2d59949-0a4b-4cf9-98b9-1410d23e48dc)

   **Time Slot with small delivery windows**
   ![image](https://github.com/coopcycle/coopcycle-docs/assets/77277854/d58ea419-e57c-4ff9-822c-7f790631110d)

   **Time Slot with wide delivery windows**
   ![image](https://github.com/coopcycle/coopcycle-docs/assets/77277854/6054e5b7-01e0-458f-a287-d226a8d3b734)

   **Zones**
   ![image](https://github.com/coopcycle/coopcycle-docs/assets/77277854/513d39fe-71ce-4f78-93e5-9a894b0d55e2)

   **Package Set**
   ![image](https://github.com/coopcycle/coopcycle-docs/assets/77277854/fbb52a62-e4e5-4422-8684-1d42fea7b1c6)

   **Price Rules**
   ![image](https://github.com/coopcycle/coopcycle-docs/assets/77277854/0ead7512-8cd9-4577-8193-561045dbc02d)
   ![image](https://github.com/coopcycle/coopcycle-docs/assets/77277854/c3c64d55-06b1-4eb2-98eb-ba372310277a)

   **A Typical Delivery**
   ![image](https://github.com/coopcycle/coopcycle-docs/assets/77277854/32bcb683-6266-4d2f-8704-f1fa0cc3d923)

### 3. **Multi-Dropoff Pricing** <span class="badge badge-success">**Recommended if Possible**</span>

   <span class="badge badge-success">When to use</span> <span>When you have a client with a clear set of possible deliveries, but they may change or be arranged differently in each delivery. Any one order may be between 2 and 10 points, and there is not a huge variation between the types of packages you are carrying, or the time slots in which they are being delivered. Ex. notifications, fruit boxes, moving stock between stores. **Pros:** Avoids clients getting annoyed at slowly making orders one at a time, clean and simple pricing rule you can explain to a client that covers a wide range of use cases.<span>

    <span class="badge badge-danger">When **not** to use</span> <span>If the client cannot use CoopCycle as they should, or if they have a very high volume of orders **Cons:** This pricing rule is still being developed and still cannot be used with pricing rules that are based on time like `Difference (hours)`, `Difference (days)` or `time range length (hours)` and in no circumstances can be used with rules based on kilometers of distance. <span>

   **Configuration of the shop**
   ![image](https://github.com/coopcycle/coopcycle-docs/assets/77277854/d995c0e1-2ccf-40d7-a612-c5f5004d2930)

   **Time Slot with standardized delivery windows**
   ![image](https://github.com/coopcycle/coopcycle-docs/assets/77277854/12cd420c-4259-49ac-a3d4-dc69893d2c62)

   **Package Set**
   ![image](https://github.com/coopcycle/coopcycle-docs/assets/77277854/959b7bf1-d531-45fe-b51e-7af93246d8eb)

   **Price Rules**
   ![image](https://github.com/coopcycle/coopcycle-docs/assets/77277854/2c7cf3c3-d4f4-4ae1-bb9d-774ee4db2c0f)

   **A Typical Delivery**
   ![image](https://github.com/coopcycle/coopcycle-docs/assets/77277854/677cc645-fb40-4f85-9955-b2e229077703)
   ![image](https://github.com/coopcycle/coopcycle-docs/assets/77277854/7a5e623f-9848-4bfb-a0aa-8a2c9c3bdec8)

### 4. **Last Mile At Volume**

   <span class="badge badge-success">When to use</span> <span>For clients who give you a high volume of standarized packages such as magazines, small last mile pacakges from a provider like DHL, or any other delivery that can easily have an "average" price. **Pros:** Simple for client and invoicing. <span>

    <span class="badge badge-danger">When **not** to use</span> <span>Any client with deliveries that cannot be "averaged" **Cons:** If your average is wrong, later you will have made less money than you hope. Maybe the client says they have a simple and easily averaged need, but then ask for special or different deliveries in specific moment that should be more expensive, but the rule charges the "cheap" option. <span>

   **Configuration of the shop**
   ![image](https://github.com/coopcycle/coopcycle-docs/assets/77277854/d67e80a2-56ef-4c39-b06b-91674db7ee02)

   **Price Rules**
   ![image](https://github.com/coopcycle/coopcycle-docs/assets/77277854/677cc645-fb40-4f85-9955-b2e229077703)
   ![image](https://github.com/coopcycle/coopcycle-docs/assets/77277854/fa81824b-e925-4c92-831e-786f91f0c77c)

   **A Typical Delivery in Excel**
   ![image](https://github.com/coopcycle/coopcycle-docs/assets/77277854/6d087faa-a476-447e-9385-f8713033c1e0)

---

### Definitions of conditions
Brief description on each condition.

| CONDITIONS                   | DEFINITION                                                                                                              |
| ----------------------       | ----------------------------------------------------------------------------------------------------------------------- |
| **Distance (km)**            | Determines the radius delivery area with the Business as the centre                                                     |
| **Weight (kg)**              | Conditions the price depending on the inputted weight of the parcel                                                     |
| **Bike type**                | Allows for a choice of "regular" or "cargo" bike                                                                        |
| **Pickup address**           | Allows the selection of a Zone that contains the Pickup address                                                         |
| **Dropoff address**          | Allows the selection of a Zone that contains the Dropoff address                                                        |
| **Difference (hours)**       | Allows inputting a number indicating how many hours ahead a Delivery has to be placed. It can also condition the price. |
| **Difference (days)**        | Allows inputting a number indicating how many days ahead a Delivery has to be placed. It can also condition the price.  |
| **Doorstep dropoff**         | Indicates if a delivery should be handed to the customer                                                                |
| **Packages**                 | Conditions the price depending on the type of package                                                                   |
| **Volume Units**             | Conditions the price depending on the inputted volume of the parcel                                                     |
| **Pickup time range length** | Conditions the price depending on the length of time in which the pickup can be done                                    |
| **Dropoff time range length**| Conditions the price depending on the length of time in which the dropoff can be done                                   |
| **Type of Task**             | Conditions the price depending on the type of task, plus whatever other condition. **Must use for multidropoff**        |
| **Items total**              | Conditions the price dependand on the total amount of money on an order                                                 |

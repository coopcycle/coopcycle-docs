---
layout: default
title: Pricing
parent: Deliveries
---

# Pricing

<div class="alert alert-info" role="alert">
Here you can configure custom pricings to use for Orders forms, Restaurants and Stores.<br>
The custom pricing can contain multiple Rules and each Rule can be configured by combining the following Conditions:<br>
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
</div>

---

## Create a custom pricing
1. From the top menu go to `Deliveries`
2. Go to <i class="fa fa-percent mr-2"></i> Pricing
3. Click on <span class="badge badge-success">+ Create a new pricing</span>
4. Give the `Pricing` a name. 
   <span class="badge badge-info">TIP:</span><span>The name can be the name of the Order Form, Store, Restaurant or a specific name that makes it easy to know what the custom pricing is meant for</span>.
5. Under **Rules** click on <span class="badge badge-success">+ Add rule</span>
6. Write the `Price` of the Rule
7. Click on <span class="badge badge-warning">+ Add condition</span> to add a condition (to know more see Definitions of conditions).
8. Choose a **method of calculation**
   a. **The first rule that matches**.
    Because you can have multiple Rules under one Pricing, **the first rule that matches** means that, beginning from top to bottom, the first Rule that complies with all the Conditions will be the only one which will show the price to the customer.
    **Example**:
    - In the image below there are three (3) Rules, each in a coloured box and each with the same type of conditions but different variables. The conditions are `Weight`, `Pickup address` and `Drop-off address`. 
     - If a customer places an order where the parcel weighs `3.5 kg` and if both the **Pickup address** and **Drop-off address** are within the `City centre` then the cost of that order will be `5` (the curreny is set depending from the country you are in).
     - If a customer places an order where the parcel weighs `14 kg` and if both the Pickup address and Drop-off address are within the `City centre` then the cost of that order will be `10`. Here the system will skip the first two rules (because only two (2) of the Conditions are true) and select the one where all the Conditions comply with the customer's details.
     [![](/assets/images/)](/assets/images/){:target="\_blank"} 

    b. **All the matching rules**
    <!--Waiting for answer from mex and Adrien-->


### Definitions of conditions








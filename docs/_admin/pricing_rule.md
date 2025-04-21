---
layout: default
title: Pricing rule
parent: Create a custom pricing
nav_order: 2

---

# Pricing rule

During the price calculation, the system checks if the conditions inside the rule are met. If they are, the price of the rule is added to the total price of the order.

<span class="zoomable">![image1](/assets/images/pricingPricingRule.png)</span>

## <span class="badge badge-info">NEW in 3.31</span> Types of rules

Depending on the type of rule, the conditions will be evaluated either **once** (against the whole order) (**Rule per order**) or **multiple times** (against each point/task in the order) (**Rule per point**).

- **Rule per order**: A rule to be applied once per order, recommended for simple deliveries (one pickup, one dropoff) and Food Tech orders
- **Rule per point**: A rule to be applied per each point (PICKUP and/or DROPOFF task), recommended for complex, multi-point deliveries

## Conditions

<span class="badge badge-info">INFO:</span> Conditions are evaluated differently depending on the **Type of rule**. For example,

- if a rule is applied **per order** `Weight (kg)` is compared with the total weight (sum of all tasks) and
- if a rule is applied **per point** `Weight (kg)` is compared with the weight of each task.

Brief description of each condition.

| CONDITION                  | DEFINITION                                                                             | Type of rule: Rule per order | Type of rule: Rule per point |
| ----------------------       |----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| **Distance (km)**          | Determines the radius delivery area with the Business as the centre                    | ✅                                                                             | ❌ - not supported                                                             |
| **Items total**            | Conditions the price dependand on the total amount of money on an order                | ✅                                                                             | ❌ - not supported                                                             |
| **Pickup address**         | Allows the selection of a Zone that contains the Pickup address                        | ✅ - evaluated on the first pickup task                                        | ✅ - evaluated on each Pickup task                                             |
| **Dropoff address**        | Allows the selection of a Zone that contains the Dropoff address                       | ✅ - evaluated on the last dropoff task                                        | ✅ - evaluated on each Dropoff task                                            |
| **Difference (hours)**     | Allows inputting a number indicating how many hours ahead a Delivery has to be placed. | ✅ - evaluated on the first pickup task                                        | ⛔️ - deprecated (evaluated on each Pickup task)                               |
| **Difference (days)**      | Allows inputting a number indicating how many days ahead a Delivery has to be placed.  | ✅ - evaluated on the first pickup task                                        | ⛔️ - deprecated (evaluated on each Pickup task)                               |
| **Pickup time range length** | Conditions the price depending on the length of time in which the pickup can be done   | ✅ - evaluated on the first pickup task                                        | ✅ - evaluated on each Pickup task                                             |
| **Dropoff time range length**| Conditions the price depending on the length of time in which the dropoff can be done  | ✅ - evaluated on the last dropoff task                                        | ✅ - evaluated on each Dropoff task                                            |
| **Weight (kg)**            | Conditions the price depending on the inputted weight of the parcel                    | ✅ - Total weight of all tasks                                                 | ✅ - Weight of each task (use only with Type of task: Dropoff)                 |
| **Packages**               | Conditions the price depending on the type of package                                  | ✅ - Total number of packages                                                  | ✅ - Number of packages for each task (use only with Type of task: Dropoff)    |
| **Volume Units**           | Conditions the price depending on the inputted volume of the parcel                    | ✅ - Total volume of all tasks                                                 | ✅ - Volume of each task (use only with Type of task: Dropoff)                 |
| **Type of Task**           | Conditions the price depending on the type of task, plus whatever other condition.     | ❌ - not supported                                                             | ✅                                                                             |
| **Bike type**              | Allows for a choice of "regular" or "cargo" bike                                       | ⛔️ - deprecated                                                               | ⛔️ - deprecated                                                               |
| **Doorstep dropoff**       | Indicates if a delivery should be handed to the customer                               | ⛔️ - deprecated                                                               | ⛔️ - deprecated                                                               |

## Price

Price can be calculated using the following methods:

- **Fixed price**: A fixed price for the rule
- <span class="badge badge-info">SOON</span> **Percentage**: A percentage to be added or subtracted from the current subtotal. 

<span class="badge badge-info">INFO:</span>In most use cases, the **[Method of calculation](/en/admin/pricing_method_of_calculation)**: "All the matching rules" is required for the percentage-based price.

| DEFINITION | Type of rule: Rule per order                                 | Type of rule: Rule per point         |
|------------|--------------------------------------------------------------|--------------------------------------|
| SUBTOTAL| Sum of all Rules per point and all preceding rules per order | Sum of all preceding Rules per point |


- **Price by ranges** : A price per kilometer, kilogram, or volume unit
- **Price per package**: A price per package

---
layout: default
title: Definitions of conditions
parent: Create a custom pricing
nav_order: 3

---

# Definitions of conditions

<span class="badge badge-info">INFO:</span> Some conditions are only available for certain [**Type of rule**](/en/admin/pricing_type_of_rule). For example, the condition `Distance (km)` is only available for **Rule per order** and not for **Rule per point**.

<span class="badge badge-info">INFO:</span> Conditions are evaluated differently depending on the [Type of rule](/en/admin/pricing_type_of_rule). For example,

- if a rule is applied **per order** `Weight (kg)` is compared with the total weight (sum of all tasks) and
- if a rule is applied **per task** `Weight (kg)` is compared with the weight of each task.

Brief description on each condition.

| CONDITIONS                   | DEFINITION                                                                                                       |
| ----------------------       |------------------------------------------------------------------------------------------------------------------|
| **Distance (km)**            | Determines the radius delivery area with the Business as the centre                                              |
| **Weight (kg)**              | Conditions the price depending on the inputted weight of the parcel                                              |
| **Pickup address**           | Allows the selection of a Zone that contains the Pickup address                                                  |
| **Dropoff address**          | Allows the selection of a Zone that contains the Dropoff address                                                 |
| **Difference (hours)**       | Allows inputting a number indicating how many hours ahead a Delivery has to be placed.                           |
| **Difference (days)**        | Allows inputting a number indicating how many days ahead a Delivery has to be placed.                            |
| **Pickup time range length** | Conditions the price depending on the length of time in which the pickup can be done                             |
| **Dropoff time range length**| Conditions the price depending on the length of time in which the dropoff can be done                            |
| **Packages**                 | Conditions the price depending on the type of package                                                            |
| **Volume Units**             | Conditions the price depending on the inputted volume of the parcel                                              |
| **Type of Task**             | Conditions the price depending on the type of task, plus whatever other condition. **Must use for multidropoff** |
| **Items total**              | Conditions the price dependand on the total amount of money on an order                                          |
| **Bike type**                | Allows for a choice of "regular" or "cargo" bike                                                                 |
| **Doorstep dropoff**         | Indicates if a delivery should be handed to the customer                                                         |

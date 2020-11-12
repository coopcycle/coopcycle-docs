---
id: 5d597864-b0c0-4248-ac5d-1152de165149
title: Pricing
desc: ''
updated: 1605205124873
created: 1604769872326
---

# Pricing (for Stores and Order forms)

---

As part of the creation of a store account, it is possible to create prices (e.g. express prices, normal prices) from the administration section by clicking on the icon then on the Prices section.

[screenshot]

Pricing is configured in the administration dashboard through a set of rules based on the following variables:
The distance that is measured in meters. This distance can be defined with the operators of:
- &gt; greater than * variable in meter *
- &lt; less than * variable in meter *
between two variables

The weight which is evaluated in gram. This weight can be defined with the same operators as the distance
The zone defined by loading a GeoJSON file into the instance configuration;
The type of bike that is defined by selecting it from a list in which are available:
The simple bike
The cargo bike

[screenshot]

These rules are organized as a stack in order of processing, the pricing at the top of the list will be the first to be processed by the software that will check if it matches the characteristics of the delivery, that is not the case the software will go to the second pricing in the list and so on. With each delivery created, this stack will be used to create the pricing. The choice is automatically made according to the criteria specified for each delivery.

For example, I create a rule that specifies a pricing:
- in the department of 93 with cargo bike placed at the top of the pile;
- in Paris intramural with cargo bike placed in the middle of the pile;
- in intramural Paris placed at the bottom of the pile.

If a delivery is created involving a series of tasks in Paris intramural with a single bike, then the first rule will be ignored, and the second used as delivery basis. The precise rules (ie with the most variables) must be at the top of the stack and the most general ones at the bottom of the stack so that special cases are selected by the software as a basis for pricing. . If, for example, I take my pricing list higher as follows:
in intramural paris;
in Paris intramural with cargo bike;
in the department of 93 with cargo bike.

If a delivery is created for intramural Paris with a cargo bike, then the first rule will be ignored. The second corresponds to the delivery, its price will therefore be applied. The second rule being fulfilled, the third is ignored.

The most precise rules (i.e. with the most parameters) must be at the top of the stack and the most general rules at the bottom of the stack, so that the specific cases are selected by the software as a basis for pricing. If, for example, I modify the above pricing as follows:

in intramural Paris;
in intramural Paris with cargo bike;
in the 93 department with cargo bike.
If a delivery in intramural Paris is created with the need to deliver by cargo bike, the price specified for the first rule will apply because no type of bike is specified for it and the second will be ignored.
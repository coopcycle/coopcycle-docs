---
title: Key concepts
lang: en
role: admin
ref: key-concepts
parent: Administrator's guide
nav_order: 2
---

# Key concepts

## Create a task

Each delivery consists of at least two tasks that a dispatcher assigned to a deliveryman.
There are two different types of tasks: a "Recover" task and a "Submit" task.
This binary form covers all the scenarios of the bike delivery field.

### Retrieve and Deposit

The deliverer must pick up merchandise at an address and bring it to another address. The following information must be completed by the dispatcher for each task:
- Crenellations
- Address
- Commentary
- The following information is used to track the progress of a task in the delivery process:
- Status
- History

## Create a delivery

Assign two or more tasks to a delivery person creating a delivery. When the Retrieve and Drop tasks are created, the dispatcher assigns these tasks manually in the most optimal order that they judge. The creation of a delivery is materialized on the map by means of a GPS track which is proposed to the courier for delivery.

### Pricing

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

These rules are organized as a stack in order of processing, the pricing at the top of the list will be the first to be processed by the software that will check if it matches the characteristics of the delivery, that is not the case the software will go to the second pricing in the list and so on. With each delivery created, this stack will be used to create the pricing. The choice is automatically made according to the criteria specified for each delivery.

For example, I create a rule that specifies a pricing:
- in the department of 93 with cargo bike placed at the top of the pile;
- in Paris intramural with cargo bike placed in the middle of the pile;
- in intramural Paris placed at the bottom of the pile.

If a delivery is created involving a series of tasks in Paris intramural with a single bike, then the first rule will be ignored, and the second used as delivery basis. The precise rules (ie with the most variables) must be at the top of the stack and the most general ones at the bottom of the stack so that special cases are selected by the software as a basis for pricing. . If, for example, I take my pricing list higher as follows:
in intramural paris;
in Paris intramural with cargo bike;
in the department of 93 with cargo bike.

If a delivery within Paris is created with the need to deliver by cargo bike, the first pricing will apply because no type of bike is specified for it and the bad price will be charged. Being precise at the top of the pile and GP at the bottom of the track allows

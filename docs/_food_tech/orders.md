---
layout: default
title: Foodtech orders
---

# Foodtech orders

An order can have these following status :

- New, the order was not accepted by the restaurant yet
- Accepted, the order is in preparation
- Refused, the order has been refused
- Ready, the order is waiting a bike messenger or its delivery is underway
- Done, the order was delivered
- Cancelled, the order was cancelled by the client or the restaurant

# Foodtech orders live management dashboard

From the admin, go to the "Orders" page, then click on "Dashboard" icon. This will lead you to the "live order management" where foodtech dispatch can manage incoming orders.

<span class="zoomable">![Dashboard](/assets/images/foodtech_dashboard.png)</span>

## Delay

The delay means "A rider can not pickup things in the next 30min". The restaurant owner has his own delay (rush mode) which means "I can not start preparing an order in the next Xmin" (for now 25min).
So if prep time is 20min, a restaurant set rush mode (+25min) and dispatcher set a 20min delay. Then restaurant and dispatch are operating with the same "lateness", then the customer is just delayed 25min not 25min + 20min.

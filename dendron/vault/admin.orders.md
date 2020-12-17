---
id: 222abb37-c573-45fd-88db-983c22d39e9f
title: Orders
desc: ''
updated: 1605290067919
created: 1604766106158
---

<!-- CSS -->
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@4.5.3/dist/css/bootstrap.min.css" integrity="sha384-TX8t27EcRE3e/ihU7zmQxVncDAy5uIKz4rEkgIXeMed4M0jlfIDPvg6uqKI2xXr2" crossorigin="anonymous">
<!-- jQuery and JS bundle w/ Popper.js -->
<script src="https://code.jquery.com/jquery-3.5.1.slim.min.js" integrity="sha384-DfXdz2htPH0lsSSs5nCTpuj/zy4C+OGpamoFVy38MVBnE+IbbVYUew+OrCXaRkfj" crossorigin="anonymous"></script>
<script src="https://cdn.jsdelivr.net/npm/bootstrap@4.5.3/dist/js/bootstrap.bundle.min.js" integrity="sha384-ho+j7jyWK8fNQe+A12Hb8AhRq26LrZ/JpcUGGOn+Y7RsweNrtN/tE3MoK7ZeZDyx" crossorigin="anonymous"></script>
<!-- Font Awesome -->
<script src="https://kit.fontawesome.com/489c6dd9c4.js" crossorigin="anonymous"></script>

# Orders

Orders page displays the orders engaged by clients on the platform. It enables to manage restaurant's orders.

There are two types of orders :

- Foodtech orders, engaged by end customers
- Orders of deliveries, engaged with the integrated form for instance.

An order can have these following status :

- New, the order was not accepted by the restaurant yet
- Accepted, the order is in preparation
- Refused, the order has been refused
- Ready, the order is waiting a bike messenger or its delivery is underway
- Done, the order was delivered
- Cancelled, the order was cancelled by the client or the restaurant

## List of orders

![Commandes](/assets/images/orders_fr.png)

The list of orders displays orders which are underway on the platform. You can display the cancelled orders by ticking the option : "Display cancelled orders”.

The administrator can cancel an order by clicking on the button `Cancel` d’une commande. Displayed informations are :

- id, order's number
- The type of order
- Customer who engaged the order
- The order's statut
- Total amount charged for the customer
- The associated bill, that you can download in pdf format
- Date of creation
- The `Cancel` button for an order

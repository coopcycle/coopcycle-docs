---
id: 7ad2b44e-ecaf-4934-b1f3-b0a5ff244a16
title: Restaurant
desc: ''
updated: 1605290172314
created: 1605207746067
---

<!-- CSS -->
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@4.5.3/dist/css/bootstrap.min.css" integrity="sha384-TX8t27EcRE3e/ihU7zmQxVncDAy5uIKz4rEkgIXeMed4M0jlfIDPvg6uqKI2xXr2" crossorigin="anonymous">
<!-- jQuery and JS bundle w/ Popper.js -->
<script src="https://code.jquery.com/jquery-3.5.1.slim.min.js" integrity="sha384-DfXdz2htPH0lsSSs5nCTpuj/zy4C+OGpamoFVy38MVBnE+IbbVYUew+OrCXaRkfj" crossorigin="anonymous"></script>
<script src="https://cdn.jsdelivr.net/npm/bootstrap@4.5.3/dist/js/bootstrap.bundle.min.js" integrity="sha384-ho+j7jyWK8fNQe+A12Hb8AhRq26LrZ/JpcUGGOn+Y7RsweNrtN/tE3MoK7ZeZDyx" crossorigin="anonymous"></script>
<!-- Font Awesome -->
<script src="https://kit.fontawesome.com/489c6dd9c4.js" crossorigin="anonymous"></script>

# Order management

## Orders

### The main screen is organized as follows :

![restaurant's interface for orders](/assets/images/resto_order_list_fr.png)

- **By date (the default current date) :**
  <br>
  Also allows you to have a history of previous and future orders by selecting the date of your choice via the calendar by clicking on the following button
  ![date button](/assets/images/resto_date_fr.png).
- **By section :**
  - **New orders :**

    Here you will see all new customer orders awaiting validation from you.

    You can also refuse it, then you have three choices: - I'm out of stock

    This order will be cancelled and you will continue to receive new orders. - I'm in the middle of a rush.

    This order will be cancelled and you will continue to receive new orders. - I'm going to close up.

    This order will be cancelled and you will not receive any more new orders.

  - **Accepted orders :**

    Here you can see all accepted orders.

    From this step, if everything goes well you only have to prepare the order, wait for the delivery person and automatically the order will be placed in the section below [delivered order](#order-delivery).

    If not, you can : - Delay the order : - By 10 minutes. - 20 minutes. - By 30 minutes. - Cancel the order : - Cancelled by the customer

    This order will be cancelled and you will continue to receive new orders. - I'm out of stock

    This order will be cancelled and you will continue to receive new orders. - I'm in the middle of a rush.

    This order will be cancelled and you will continue to receive new orders.

  - **Orders cancelled :**

    Here is a list of all the orders that have been cancelled.

  - **<span id="order-delivery">Orders delivered:</span>**

    Here is a list of all the orders that have been delivered.

In each of the sections, the orders are represented by their id, the total of the order and the time to start preparing it. To access the details of the order and interact with it, simply click on it.

**Note that you can at any time via the button ![resfresh](/assets/images/resto_refresh_btn_fr.png) refresh the page to the current date.**

---

## Settings

### The settings are accessible via the icon ![settings](/assets/images/resto_param_icon.png) at the top right of the page. They are divided into two parts :

- **Switch to rush mode :**

  When the rush mode is activated you no longer receive any orders, to continue receiving orders again, disable it.

- **Manage products :**

  In this section, you can see a list of all the products that make up your catalog and the ability to disable each of them.
  Disabled products are not visible by the customer, this can be useful if, for example, you are out of stock on an ingredient essential for preparing a dish.
  By default, all products are enabled.

---

## Online closing/reopening restaurant

This button ![power button icon](/assets/images/resto_power_icon.png) allows you to display your restaurant as closed on the customer's interface, so he will no longer be able to place orders.

To reset the restaurant to "open" status, simply click on the close button ![close button icon](/assets/images/resto_close_banner_icon.png) of the banner below that appears after you close your restaurant.

![restaurant is closed banner](/assets/images/resto_closed_banner_fr.png)

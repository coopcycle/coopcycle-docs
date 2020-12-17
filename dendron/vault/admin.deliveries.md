---
id: 35eab0e1-02a6-49e8-a513-7759157e193b
title: Deliveries
desc: ''
updated: 1605290060590
created: 1604767433483
custom_scripts:
  - 'https://cdnjs.cloudflare.com/ajax/libs/jquery-zoom/1.7.21/jquery.zoom.min.js'
  - /assets/scripts/zoom.js
---

<!-- CSS -->
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@4.5.3/dist/css/bootstrap.min.css" integrity="sha384-TX8t27EcRE3e/ihU7zmQxVncDAy5uIKz4rEkgIXeMed4M0jlfIDPvg6uqKI2xXr2" crossorigin="anonymous">
<!-- jQuery and JS bundle w/ Popper.js -->
<script src="https://code.jquery.com/jquery-3.5.1.slim.min.js" integrity="sha384-DfXdz2htPH0lsSSs5nCTpuj/zy4C+OGpamoFVy38MVBnE+IbbVYUew+OrCXaRkfj" crossorigin="anonymous"></script>
<script src="https://cdn.jsdelivr.net/npm/bootstrap@4.5.3/dist/js/bootstrap.bundle.min.js" integrity="sha384-ho+j7jyWK8fNQe+A12Hb8AhRq26LrZ/JpcUGGOn+Y7RsweNrtN/tE3MoK7ZeZDyx" crossorigin="anonymous"></script>
<!-- Font Awesome -->
<script src="https://kit.fontawesome.com/489c6dd9c4.js" crossorigin="anonymous"></script>

The delivery tab is used to display the list of deliveries and tasks.

## Orders list

<span class="zoomable">![Tableau de bord](/assets/images/livraisons_fr.png)</span>

This list groups together all the tasks and deliveries carried out on the platform. The following information is available:
  - ID, the task number
  - Type of task
  - Deposit
  - Withdrawal
  - Deadline (date and time)
  - Name of the courier
  - Delivery address

## Create / Edit an order

Creating a delivery is done by clicking on the button at the top right of the task list screen. A delivery consists of the following elements:
- Vehicle type
  - Bike
  - Cargo bike
- Weight (in grams)
- Withdrawal
  - Field: address
  - Postal code
  - City
  - Time and day of withdrawal
  - Textarea field: specific instructions for the delivery man
- Deposit
  - Field: address
  - Postal code
  - City
  - Time and day of filing
  - Textarea field: specific instructions for the delivery person

On the right, in addition to the map which displays the delivery route, you can either choose a price to apply to the delivery, or enter a free price.

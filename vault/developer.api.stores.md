---
id: 8970feb9-8e81-4775-aa3b-72d51e75d1ea
title: Stores
desc: ''
updated: 1605214637781
created: 1605214513727
---

<link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.5.0/css/bootstrap.min.css" integrity="sha384-9aIt2nRpC12Uk9gS9baDl411NQApFmC26EwAOH8WgZl5MYYxFfc+NcPb1dKGj7Sk" crossorigin="anonymous">
<script src="https://code.jquery.com/jquery-3.5.1.slim.min.js" integrity="sha384-DfXdz2htPH0lsSSs5nCTpuj/zy4C+OGpamoFVy38MVBnE+IbbVYUew+OrCXaRkfj" crossorigin="anonymous"></script>
<script src="https://cdn.jsdelivr.net/npm/popper.js@1.16.0/dist/umd/popper.min.js" integrity="sha384-Q6E9RHvbIyZFJoft+2mJbHaEWldlvI9IOYy5n3zV9zzTtmI3UksdQRVvoxMfooAo" crossorigin="anonymous"></script>
<script src="https://stackpath.bootstrapcdn.com/bootstrap/4.5.0/js/bootstrap.min.js" integrity="sha384-OgVRvuATP1z7JjHLkuOU7Xw704+h835Lr+6QL9UvYjZE3Ipu6Tp75j7Bh/kR0JKI" crossorigin="anonymous"></script>
<!-- Font Awesome -->
<script src="https://kit.fontawesome.com/489c6dd9c4.js" crossorigin="anonymous"></script>

# API for Store deliveries

<div class="alert alert-success" role="alert">
A common usage of the API is to create deliveries. For example, an external e-commerce website offering local shipping options may want to push deliveries directly to our system.
</div>

---

### Creating a delivery

To create a delivery, you will need to make a `POST` request to the `/api/deliveries` endpoint.
A delivery consists of two tasks, a `pickup` task and a `dropoff` task.
The **minimal information** we need is the address, and the timeframe of each task.

```
POST /api/deliveries
{
  "pickup": {
    "address": "24, Rue de la Paix, Paris, France",
    "before": "tomorrow 12:00"
  },
  "dropoff": {
    "address": "48, Rue de Rivoli, Paris, France",
    "before": "tomorrow 13:30"
  }
}
```

If possible, you should provide as much additional information as possible, like the phone number & name of the recipient.
There are multiple fields that can be specified.
Take a look at our [functional tests](https://github.com/coopcycle/coopcycle-web/blob/master/features/deliveries.feature) to learn more about available fields.

### Tracking the status of a delivery

When the delivery has been created, you obtain a response like below:

```
{
  "@context":"/api/contexts/Delivery",
  "@type":"http://schema.org/ParcelDelivery",
  "@id":"/api/deliveries/123",
  "pickup": {
    "@id":"/api/tasks/456",
    "@type":"Task",
    "status":"TODO",
    // ... other fields
  },
  "dropoff": {
    "@id":"/api/tasks/457",
    "@type":"Task",
    "status":"TODO",
    // ... other fields
  }
}
```

To be able to track the status of the parcel, make sure to store in your system the IRIs of the created resources.
Then, you can later poll the API to know if the tasks have been completed.

```
GET /api/tasks/456
{
  "@id":"/api/tasks/456",
  "@type":"Task",
  "status":"DONE",
  // ... other fields
}
```

When a task is completed, the `status` property will change from `TODO` to `DONE`.
When both tasks are completed, it means the delivery is completed!

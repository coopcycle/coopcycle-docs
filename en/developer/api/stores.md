---
title: Stores
parent: API
---

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

---
layout: default
title: Creating deliveries
slug: creating-deliveries
nav_order: 2
---

<div class="alert alert-success" role="alert">
A common usage of the API is to create deliveries. For example, an external e-commerce website offering local shipping options may want to push deliveries directly to our system.
</div>

---

<div class="alert alert-warning" role="alert">
⚠️ Make sure to send the following HTTP headers with your requests!
</div>

```
Accept: application/ld+json
Content-Type: application/ld+json
```

---

### Creating a delivery

To create a delivery, you will need to make a `POST` request to the `/api/deliveries` endpoint.
A delivery consists of two tasks, a `pickup` task and a `dropoff` task.

The **very minimal information** we need is the **dropoff** address, and a maximum hour for dropoff.

```
POST /api/deliveries
{
  "dropoff": {
    "address": "48, Rue de Rivoli, Paris, France",
    "before": "tomorrow 13:30"
  }
}
```

When you don't specify the pickup address, we will use the **default address** configured for your API client.
Of course, you can also specify information about the pickup address, and provide a **time slot** for tasks:

```
POST /api/deliveries
{
  "pickup": {
    "address": "24, Rue de la Paix, Paris, France",
    "timeSlot": "2018-08-29 10:00-11:00"
  },
  "dropoff": {
    "address": "48, Rue de Rivoli, Paris, France",
    "timeSlot": "2018-08-29 11:00-12:00"
  }
}
```

There are multiple fields that can be specified. Take a look at our [functional tests](https://github.com/coopcycle/coopcycle-web/blob/master/features/deliveries.feature) to learn more about available fields.

### Making sure the address is geolocated accurately 🌍

When you send the address as text, we will geocode it. Make sure to format it correctly so that we can geocode it accurately.

Learn more about [formatting the address](https://opencagedata.com/guides/how-to-format-your-geocoding-query)

### Sending more information about the address

If possible, you should provide as much additional information as possible, like the phone number & name of the recipient.

```
POST /api/deliveries
{
  "dropoff": {
    "address": {
      "streetAddress": "48, Rue de Rivoli, Paris, France",
      "description": "Code A1B2",
      "contactName": "John Doe",
      "telephone": "+33612345678"
    },
    "before": "tomorrow 13:30"
  }
}
```

If you are able to geolocate the address on your side (for example, if you are using an address autocomplete),
and you are confident about the location, you can send it directly using the `latLng` property.

```
POST /api/deliveries
{
  "dropoff": {
    "address": {
      "streetAddress": "48, Rue de Rivoli Paris",
      "latLng": [
        48.857127,
        2.354766
      ],
      // ... other address properties
    },
    "timeSlot": "2018-08-29 10:00-11:00"
  }
}
```

### Tracking the status of a delivery

When the delivery has been created, you obtain a response like below:

```
{
  "@context":"/api/contexts/Delivery",
  "@type":"http://schema.org/ParcelDelivery",
  "@id":"/api/deliveries/123",
  "pickup": {
    // ... other fields
  },
  "dropoff": {
    // ... other fields
  }
}
```

Make sure to store the `@id` property somewhere on your system, and associate it with your internal representation of an order.

Once you have created a delivery, you can track its status (when it has been picked, delivered…) using [webhooks](webhooks.md)

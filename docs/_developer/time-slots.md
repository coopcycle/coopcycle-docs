---
layout: default
title: Obtaining time slots
slug: time-slots
nav_order: 3
---

You can use the API to obtain time slots for delivery. For example, you may want to do this to build a dropdown in a user interface.

To obtain time slots, use the `/time_slots/choices` endpoint. It will return both a [ISO 8601 time interval](https://en.wikipedia.org/wiki/ISO_8601#Time_intervals) and a human readable version.

```
GET /api/time_slots/choices
{
  "choices":[
    {
      "value":"2020-04-02T10:00:00Z/2020-04-02T12:00:00Z",
      "label":"Aujourd\u0027hui entre 12:00 et 14:00"
    },
    {
      "value":"2020-04-02T12:00:00Z/2020-04-02T15:00:00Z",
      "label":"Aujourd\u0027hui entre 14:00 et 17:00"
    },
    {
      "value":"2020-04-03T10:00:00Z/2020-04-03T12:00:00Z",
      "label":"Demain entre 12:00 et 14:00"
    },
    {
      "value":"2020-04-03T12:00:00Z/2020-04-03T15:00:00Z",
      "label":"Demain entre 14:00 et 17:00"
    }
  ]
}
```

You can then use the `value` to create a delivery.


```
POST /api/deliveries
{
  "dropoff": {
    // ... other properties
    "timeSlot": "2020-04-02T12:00:00Z/2020-04-02T15:00:00Z"
  }
}
```

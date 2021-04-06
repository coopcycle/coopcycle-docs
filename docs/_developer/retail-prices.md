---
layout: default
title: Obtaining retail prices
slug: retail-prices
nav_order: 3
---

You can use our API to obtain retail prices for deliveries.

To obtain a retail price, send your payload to the `/retail_prices/calculate` endpoint.

```
POST /api/retail_prices/calculate
{
  "dropoff": {
    "address": "48, Rue de Rivoli, Paris, France",
    "before": "+2 hours"
  }
}
```

You will obtain a response like this:

```
{
  "@context":"/api/contexts/RetailPrice",
  "@id":@string@,
  "@type":"RetailPrice",
  "amount":900,
  "currency":"EUR",
  "tax":{
    "amount":150,
    "included":true
  }
}
```

By default, the retail price returned is **tax included**.
To obtain the tax excluded price, you will need to make `amount - tax.amount`.

You can also obtain the tax excluded price directly by passing `tax=excluded` when calculating the retail price.

```
POST /api/retail_prices/calculate?tax=excluded
```

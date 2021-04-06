---
layout: default
title: Webhooks
nav_order: 4
---

### Creating webhooks

If you want to receive notifications about events happening on CoopCycle, you can register [webhooks](https://resthooks.org/).

```
POST /api/webhooks
{
    "event": "delivery.completed",
    "url": "https://example.com/webhook"
}
```

The response will contain a `secret` property. Save it on your system, you will need it later.

```
{
    "@context": "/api/contexts/Webhook",
    "@id": "/api/webhooks/1",
    "@type": "Webhook",
    "url": "https://example.com/webhook",
    "event": "delivery.completed",
    "secret": "4mCOyJ7UAa371oUjYcC2R9BZRx5eQT08qTzLAnh4e8M="
}
```

### Receiving webhooks

Now, whenever an event you are subscribed to is triggered in our system, your endpoint will receive a POST request.

```
POST https://example.com/webhook
{
    "data": {
        "object": "/api/deliveries/1",
        "event": "delivery.completed"
    }
}
```

### Verifying webhooks signature

When receiving webhooks, it is important to make sure they are originating from our system.

To achieve this, each webhook HTTP request contains a `X-CoopCycle-Signature`, which is a SHA256 HMAC of the request body, signed with the `secret`.

Here is an example PHP function to verify the signature.

```
function verify_signature($payload, $signature, $secret)
{
    $hex_hash = hash_hmac('sha256', $payload, $secret);

    return $signature === base64_encode(hex2bin($hex_hash));
}
```

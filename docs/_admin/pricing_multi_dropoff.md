---
layout: default
title: Multi-Dropoff Pricing
parent: Example Rules
nav_order: 3
---

### **Multi-Dropoff Pricing** <span class="badge badge-success">**Recommended if Possible**</span>

Rates that allow for clients to ask for many deliveries at once, instead of one by one.

<span class="badge badge-info">EXAMPLE:</span> <span>A service the is often requested multiple times a week to move blood and urine samples from homes for the elderly, to a laboratory and then return the package. However, there are multiple elderly homes and multiple laboratories so sometimes the task is a single pickup and a single dropoff, or it may be multiple pickups and one dropoff, or a pickup + a dropoff + a dropoff. In order to facilitate the client, we want all these possible use cases to be made in one type of purchase process. <span>

<span class="badge badge-primary">FORMAT:</span> <span>A price of this type will usually have a base price per "point" (a pick-up of dropoff) with suppliments of weight or volume or urgency for each point. <span>

---

<span class="badge badge-success">When to use</span> <span>When you have a client with a clear set of possible deliveries, but they may change or be arranged differently in each delivery. Any one order may be between 2 and 10 points, and there is not a huge variation between the types of packages you are carrying, or the time slots in which they are being delivered. Ex. notifications, fruit boxes, moving stock between stores. **Pros:** Avoids clients getting annoyed at slowly making orders one at a time, clean and simple pricing rule you can explain to a client that covers a wide range of use cases.<span>

<span class="badge badge-danger">When **not** to use</span> <span>If the client cannot use CoopCycle as they should, or if they have a very high volume of orders **Cons:** This pricing rule is still being developed and still cannot be used with pricing rules that are based on time like `Difference (hours)`, `Difference (days)` or `time range length (hours)` and in no circumstances can be used with rules based on kilometers of distance. <span>

---

Configuration of the shop
![image](https://github.com/coopcycle/coopcycle-docs/assets/77277854/d995c0e1-2ccf-40d7-a612-c5f5004d2930)

Time Slot with standardized delivery windows
![image](https://github.com/coopcycle/coopcycle-docs/assets/77277854/12cd420c-4259-49ac-a3d4-dc69893d2c62)

Package Set
![image](https://github.com/coopcycle/coopcycle-docs/assets/77277854/959b7bf1-d531-45fe-b51e-7af93246d8eb)

Price Rules
![image](https://github.com/coopcycle/coopcycle-docs/assets/77277854/2c7cf3c3-d4f4-4ae1-bb9d-774ee4db2c0f)

A Typical Delivery
![image](https://github.com/coopcycle/coopcycle-docs/assets/77277854/677cc645-fb40-4f85-9955-b2e229077703)
![image](https://github.com/coopcycle/coopcycle-docs/assets/77277854/7a5e623f-9848-4bfb-a0aa-8a2c9c3bdec8)

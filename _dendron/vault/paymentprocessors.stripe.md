---
id: 45f0d392-ea3d-4836-bebb-1052282382ec
title: Stripe
desc: ''
updated: 1605290295548
created: 1605215048714
---
<!-- CSS -->
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@4.5.3/dist/css/bootstrap.min.css" integrity="sha384-TX8t27EcRE3e/ihU7zmQxVncDAy5uIKz4rEkgIXeMed4M0jlfIDPvg6uqKI2xXr2" crossorigin="anonymous">
<!-- jQuery and JS bundle w/ Popper.js -->
<script src="https://code.jquery.com/jquery-3.5.1.slim.min.js" integrity="sha384-DfXdz2htPH0lsSSs5nCTpuj/zy4C+OGpamoFVy38MVBnE+IbbVYUew+OrCXaRkfj" crossorigin="anonymous"></script>
<script src="https://cdn.jsdelivr.net/npm/bootstrap@4.5.3/dist/js/bootstrap.bundle.min.js" integrity="sha384-ho+j7jyWK8fNQe+A12Hb8AhRq26LrZ/JpcUGGOn+Y7RsweNrtN/tE3MoK7ZeZDyx" crossorigin="anonymous"></script>
<!-- Font Awesome -->
<script src="https://kit.fontawesome.com/489c6dd9c4.js" crossorigin="anonymous"></script>

# Stripe
---

## What is Stripe?

Stripe is a payment service provider, which allows us to manage credit card payments in a secure manner. In addition, the "Stripe Connect" functionality allows us to manage the "platform" aspect of the payment, i.e. the distribution of payments between the platform (money going to the delivery cooperative) and the restaurant.

Due to the fact that the european cooperative is fund by contributions, we (CoopCycle) do not charge a commission on payments. Stripe takes a fee on each transaction ([check the pricing for your country here](https://stripe.com/pricing){:target="_blank"}).


## Why Stripe?

Stripe has established itself as the "rolls-royce" of payment services. The service is reputed to be of excellent quality. It is possible to find cheaper services, but we believe the price is worth the candle. A known negative point about Stripe is that the (nice) Stripe admin interface is not always available in the user's language.

For creating and integrating a Stripe account with CoopCycle refer to the links below.

- [Create a Stripe account <i class="fas fa-external-link-alt"></i> ](https://dashboard.stripe.com/register){:target="_blank"}
    <div class="alert alert-info"> 
    You can also ask you local coop to create a Stripe account on your behalf and they can seamlessly integrate with your e-commerce account. Then they will give you admin access to your Stripe account.</div>
- [[Integrate with CoopCycle|developer.paymentprocessors.stripe]]

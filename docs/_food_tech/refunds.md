---
layout: default
title: Refunds
---

# Refunds
<div class="alert mt-3 alert-info" role="alert">
The liable party depends on whether the refund is for an invididual Restaurant order or for a Hub order. 
</div>
---
<div class="shadow p-3 mb-5 bg-white rounded border border-danger">
<span class="badge badge-danger">IMPORTANT:</span>
<span> Hubs is still a <em>work in progress</em>, the following docs abou Refunds is only for individual Restaurants.</span>
</div>

When making a refund of an order, the refunded amount is returned to the customer from the Restaurant Stripe account. This is because the Restaurant is the one responsible for paying the Stripe fees.

<div class="shadow p-3 mb-5 bg-white rounded border border-danger">
<span class="badge badge-danger">IMPORTANT:</span>
<span> Each time a Refund is made, the Coop owes the Restaurant the refunded amount if the Coop is the liable party.<br><strong>Be aware that Stripe charges a fee for each refund transaction. <a href="https://stripe.com/pricing">See fees here</a></strong>.</span>
</div>

## How to make a refund

1. Go to <span><i class="fa fa-cube" aria-hidden="true"></i> Orders</span>
2. Click on the Order number to view the order in question
3. Click <span class="badge badge-danger"> Refund</span> on the bottom right  

   **On the pop-up window you will find**:
   
   ### Refunded amount
   By default you will see the total order amount including delivery fee.  
   You can change the amount if a refund is only partial.  
   You cannot make a refund larger than the amount of the order.  
   
   ### Liable party
   Selecting one of the two options here, all it does is keep a record of who is the liable party under [Statistics → Refunds](/en/admin/restaurants/product-settings/#refunds).
   
   <div class="shadow p-3 mb-5 bg-white rounded border border-danger">
   <span class="badge badge-danger">IMPORTANT:</span>
   <span> If the Merchant is liable, the Coop always has to pay the delivery fee to the Restaurant unless stated otherwise through a previous agreement between Coop and Restaurant.</span>
   </div>
   
   ### Comments
   Write a comment that is clear and concise regarding the refund.  

4. Click on <span class="badge badge-danger">Refund</span>
   
Once a refund has been made you can check the refunded amount on the same page of the order under **Refunded Amount** or by going to [Statistics → Refunds](/en/admin/restaurants/product-settings/#refunds).





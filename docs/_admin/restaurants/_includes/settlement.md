<div class="alert alert-info" role="alert">
Here is where you set up all payments 
<ul>
<li>fee paid by customers</li>
<li>fee paid by restaurants</li>
</ul>
</div>

<span class="badge badge-warning">IMPORTANT:</span><span> <strong>Enable variable amount charged by the platform</strong> and <strong>Enable variable amount paid by the customer</strong> both need to have the same option selected, either <code>yes</code> or <code>no</code></span>. 

## Selecting `No`

Selecting `no` is the default option and will allow you to use a fixed amount when charging the delivery fee to the customer. 

**Amount charged by the platform** is the fixed delivery fee that the Coop will receive (the platform being the Coop).  
**Amount paid by the customer** is the fixed delivery fee that the Customer will pay when ordering.

There are two ways this can be configured.
#### Option 1:
If the **Amount charged by the platform** is equal to the **Amount paid by the customer** it means the customer gets charged a certain fee and the Coop receives that exact fee.

|Amount charged by the platform|Amount paid by the customer|Coop receives|
|:-:|:-:|:-:|
|5|5|**5**|

#### Option 2:

If the **Amount charged by the platform** is higher than the **Amount paid by the customer** it means the Restaurant pays the difference between the platform and the customer fee.

|Charged by the platform|Paid by the customer|Paid by the Restaurant|Coop receives|
|:-:|:-:|:-:|:-:|
|5|2|3|**5**|

<span class="badge badge-info">TIP:</span><span> This option allows for Restaurants to sponsor the Customers by offering their products at a smaller delivery fee.</span>

## Selecting `Yes`

Selecting `yes` will allow you to use a custom delivery fee. This fee can be configured [here]
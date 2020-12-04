---
id: 4eb2409c-253d-4023-bd8f-e26c49675177
title: Fulfillment
desc: ""
updated: 1607111717514
created: 1605205695947
---

<!-- CSS -->

<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@4.5.3/dist/css/bootstrap.min.css" integrity="sha384-TX8t27EcRE3e/ihU7zmQxVncDAy5uIKz4rEkgIXeMed4M0jlfIDPvg6uqKI2xXr2" crossorigin="anonymous">
<!-- jQuery and JS bundle w/ Popper.js -->
<script src="https://code.jquery.com/jquery-3.5.1.slim.min.js" integrity="sha384-DfXdz2htPH0lsSSs5nCTpuj/zy4C+OGpamoFVy38MVBnE+IbbVYUew+OrCXaRkfj" crossorigin="anonymous"></script>
<script src="https://cdn.jsdelivr.net/npm/bootstrap@4.5.3/dist/js/bootstrap.bundle.min.js" integrity="sha384-ho+j7jyWK8fNQe+A12Hb8AhRq26LrZ/JpcUGGOn+Y7RsweNrtN/tE3MoK7ZeZDyx" crossorigin="anonymous"></script>
<!-- Font Awesome -->
<script src="https://kit.fontawesome.com/489c6dd9c4.js" crossorigin="anonymous"></script>

# Fulfillment / [[Restaurants|admin.restaurants]]

<div class="alert alert-info" role="alert">
This section allows you to configure the Collection and Delivery schedule along with other related settings.
</div>

---

## Fulfillment methods

- **Delivery** - the orders placed by customers are delivered by the coop
- **Collection** - the order placed by customers are collected by the customers

Checking either option will enable editing the corresponding schedule section.
Make sure you scroll down too see the settings for each section.

## Delivery section

<div class="alert alert-info" role="alert">
These settings apply for the Collection section as well.
</div>

<span class="badge badge-info">TIP:</span><span> By unchecking either <strong>Delivery</strong> or <strong>Collection</strong> the business will have its products greyed out, respectively of each option, not allowing customers to order.</span>

### Delivery time slots

<div class="alert alert-warning" role="alert">
<ul>
<li>Time slots will be displayed on the homepage of the business</li>
<li>They will act as the Delivery Hours of the business.</li>
<li>The overall opening hours of the business can be 09:00 to 18:00 but for deliveries they may only be open from 12:00 to 18:00.</li></ul>
</div>

When you've just created a business/restaurant from <span class="badge badge-success">+ Create a new restaurant</span> the Delivery Time slot under Fulfillment will show no time slots.
Click <span class="badge badge-success">Add</span> to create a new time slot.

[![](/assets/images/deliveryTimeSlotsAdd.png)](/assets/images/deliveryTimeSlotsAdd.png){:target="\_blank"}

By clicking add a new time slot field will become available. Choose the corresponding Time and Days. See example below:

[![](/assets/images/deliveryTimeSlotsSelectedWeekend.png)](/assets/images/deliveryTimeSlotsSelectedWeekend.png){:target="\_blank"}

<span class="badge badge-info">TIP:</span><span> Saving settings only works if a Time Slot has a selected time and at least one (1) checked day. See below:</span>

[![](/assets/images/deliveryTimeSlotSave.png)](/assets/images/deliveryTimeSlotSave.png){:target="\_blank"}

If you need to remove a Time Slot click the <i class="fas fa-times"></i> button on the right-end of the Time Slot.

[![](/assets/images/deliveryTimeSlotRemove.png)](/assets/images/deliveryTimeSlotRemove.png){:target="\_blank"}

**As soon as possible (ASAP)**<br>
This option works best when the delivery opening hours of the business is set in a single Time Slot. See the above image, e.g. `9:00 AM - 12:00 PM`.
This option allows the customer to place an order to be delivered as quickly as possible. Go to [[Prepration|admin.restaurants.productsettings.preparation]] to check how the **ASAP** times are configured.
See images below for **ASAP** delivery times examples:

| Cart                                                                                         | Popup                                                                                          |
| -------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- |
| [![](/assets/images/ASAPTimesCart.png)](/assets/images/ASAPTimesCart.png){:target="\_blank"} | [![](/assets/images/ASAPTimesPopup.png)](/assets/images/ASAPTimesPopup.png){:target="\_blank"} |

**Time slot**<br>
This option works best when you create multiple time slots within the delivery opening hours of the business. Se image below:

[![](/assets/images/multipleDeliveryTimeSlots.png)](/assets/images/multipleDeliveryTimeSlots.png){:target="\_blank"}

In this case, the delivery opening hours of the business are `10:00 AM - 5:00 PM`. But the whole schedule has been split into hourly slots. When **Time slots** is selected, customers will see multiple hourly slots as delivery times. See images below (click to open full-size images in a new tab):<br>
<span class="badge badge-info">TIP:</span><span> You don't necessarily have to create hourly slots, you can create shorter or longer slots.</span>

| Cart                                                                                             | Popup                                                                                              |
| ------------------------------------------------------------------------------------------------ | -------------------------------------------------------------------------------------------------- |
| [![](/assets/images/hourlySlotsCart.png)](/assets/images/hourlySlotsCart.png){:target="\_blank"} | [![](/assets/images/hourlySlotsPopup.png)](/assets/images/hourlySlotsPopup.png){:target="\_blank"} |

<span class="badge badge-info">TIP:</span><span> You can use the <strong>ASAP</strong> option with multiple slots.</span><br>
<span class="badge badge-warning">WARNING:</span><span> If you have one (1) slot, `09:00 AM - 6:00 PM`, and you choose <strong>Time Slots</strong>, the delivery option for the customer will show up as only one time slot of 9 hours.</span>

### Minimum cart amount

By setting a minimum cart amount the system doesn't allow purchases under the set amount.
If minimum cart amount is £8 than only purchases that equal or are above £8 can be placed.

### Additional delay before ordering

This option is one of the methods that allows pre-ordering.
When either **Day(s)** or **Hour(s)** is set with a value equal or greater than `1` the delivery time will be displayed in the future from the current time of ordering.

If **Day(s)** is set to `1` the first available delivery time will always be displayed as +1 day from the current day. See images below (these screenshots were taken on a Friday):

| Delay: 1 Day                                                                                             | Delay: 2 Days                                                                                              |
| -------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| [![](/assets/images/additionalDelay1Day.png)](/assets/images/additionalDelay1Day.png){:target="\_blank"} | [![](/assets/images/additionalDelay2Days.png)](/assets/images/additionalDelay2Days.png){:target="\_blank"} |

If **Hour(s)** is set to `1` the first available delivery time will always be displayed as +1 day from the current day. See images below (these screenshots were taken at 13:00. The extra time after o'clock is the delivery and preparation times):

| Delay: 1 Hour                                                                                              | Delay: 2 Hours                                                                                               |
| ---------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------ |
| [![](/assets/images/additionalDelay1Hour.png)](/assets/images/additionalDelay1Hour.png){:target="\_blank"} | [![](/assets/images/additionalDelay2Hours.png)](/assets/images/additionalDelay2Hours.png){:target="\_blank"} |

### Allow editing

When this option is checked ☑️ it allows the business owner to edit the Delivery Time Slots.<br>
This option is unchecked by default.

### Slot approximation

**5 minutes**<br>
Is the default option for the delivery range time which is displayed on the cart.<br>

**15 minutes**<br>
By selecting this option it allows for a wider delivery range time and bring it closer to the current time of ordering. See images below.

| 5 Minutes                                                                                              | 15 Minutes                                                                                               |
| ------------------------------------------------------------------------------------------------------ | -------------------------------------------------------------------------------------------------------- |
| [![](/assets/images/slotApprox5Minutes.png)](/assets/images/slotApprox5Minutes.png){:target="\_blank"} | [![](/assets/images/slotApprox15Minutes.png)](/assets/images/slotApprox15Minutes.png){:target="\_blank"} |

### Number of shipping choices (in days)

The default value is 2. It cannot be changed to anything lower than 2.
The default value 2 means the cutomer will be presented with two delivery days (current day and the next day). If the value is 3 the customer will be presented with three (3) delivery days. See images below:<br>
<span class="badge badge-info">TIP:</span><span> The days when the business is closed do not count towards the **Number of shipping choices (in days)**.</span>

| Shipping choices: 2                                                                                | Shipping choices: 3                                                                                |
| -------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- |
| [![](/assets/images/shippingChoices2.png)](/assets/images/shippingChoices2.png){:target="\_blank"} | [![](/assets/images/shippingChoices3.png)](/assets/images/shippingChoices3.png){:target="\_blank"} |

### Delivery perimeter

The first dropdown menu has two options:

- **Zone**
- **Distance (km)**
  When selecting either option the second dropdown menu to the right changes accordingly allowing you to input the necessary settings.

**Zone**
Selecting **Zone** allows you select a delivery zone previously configured and uploaded under [[Settings > Zones|admin.settings.zones]]

**Distance (km)**
Selecting **Distance (km)** allows you to input a value in numbers representing the radius of deliveries in kilometers with the center at the address of the business.


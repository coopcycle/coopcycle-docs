---
id: 8cf91d4a-3465-4fe9-b730-b9ed84f0ba18
title: Timeslots
desc: ''
updated: 1605290038153
created: 1604769924300
---

<!-- CSS -->
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@4.5.3/dist/css/bootstrap.min.css" integrity="sha384-TX8t27EcRE3e/ihU7zmQxVncDAy5uIKz4rEkgIXeMed4M0jlfIDPvg6uqKI2xXr2" crossorigin="anonymous">
<!-- jQuery and JS bundle w/ Popper.js -->
<script src="https://code.jquery.com/jquery-3.5.1.slim.min.js" integrity="sha384-DfXdz2htPH0lsSSs5nCTpuj/zy4C+OGpamoFVy38MVBnE+IbbVYUew+OrCXaRkfj" crossorigin="anonymous"></script>
<script src="https://cdn.jsdelivr.net/npm/bootstrap@4.5.3/dist/js/bootstrap.bundle.min.js" integrity="sha384-ho+j7jyWK8fNQe+A12Hb8AhRq26LrZ/JpcUGGOn+Y7RsweNrtN/tE3MoK7ZeZDyx" crossorigin="anonymous"></script>
<!-- Font Awesome -->
<script src="https://kit.fontawesome.com/489c6dd9c4.js" crossorigin="anonymous"></script>

# Time slots (for Stores and Order forms)
---

**Time Slots** allow to configure what time ranges will be proposed to a user requesting a delivery.

In most cases, we don't want to let users decide of a precise time when the delivery needs to be done.
Instead, we want them to choose a time range (for example, between 2PM and 4PM), so that we can organize with the other jobs.

In the end, a **Time Slot** will translate to a dropdown like on the image below

![Time Slot Dropdown](/assets/images/time_slot_dropdown_en.png)

---

## Configuring Time Slots

Depending on the way ou are working, you can either create a unique **Time Slot** for everybody, or create a custom **Time Slot** per customer.

![Time Slots](/assets/images/time_slots_en.png)

### Interval

The **Interval** setting allows to change the number of days that will appear in the dropdown.
More or less, it allows to configure how much time in advance the user will be allowed to order a delivery.

Actually, it's more complicated than that… because there are weekends.

For example, let's say that you configure « 2 days », only during the week (from Monday to Friday).
On Saturdays, the user will still be allowed to choose time ranges on Monday and Tuesday.

### Prior Notice

The **Prior Notice** setting allows to decide how much time in advance the user will be allowed to choose a time range.

For example, let's say that you configure a time range from 4PM to 6PM, with a 2 hours prior notice.
It means that the user will be able to select the 4PM-6PM time range until 2PM.

### Same Day Cutoff

The **Same Day Cutoff** setting allows to decide until which time of the day it is possible to order for the same day.

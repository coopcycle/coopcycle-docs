---
layout: default
title: Courier
---

<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.14.0/css/all.css">

# Courier <span class="badge badge-primary">APP</span>

<div class="alert mt-3 alert-info" role="alert">
How to use the App as a Courier.
</div>

## Log in
See [Log in](/en/app/install/#log-in).


## Main screen

<span class="badge badge-danger">1</span> App menu<br><span class="badge badge-danger">2</span> User account role<br><span class="badge badge-danger">3</span> App settings<br><span class="badge badge-danger">4</span> Date picker<br><span class="badge badge-danger">5</span> Map screen<br><span class="badge badge-danger">6</span> Task list screen<br><span class="badge badge-danger">7</span> Map

<a href="/assets/images/appCourierMainScreen.png" target="\_blank" rel="noopener noreferrer"><img style="width: 400px" src="/assets/images/appCourierMainScreen.png" alt=""></a>

<!--| Instructions  | Main screen  |
| ------- | ------- |
| <span class="badge badge-danger">1</span> App menu<br><span class="badge badge-danger">2</span> User account role<br><span class="badge badge-danger">3</span> App settings<br><span class="badge badge-danger">4</span> Date picker<br><span class="badge badge-danger">5</span> Map screen<br><span class="badge badge-danger">6</span> Task list screen<br><span class="badge badge-danger">7</span> Map|<a href="/assets/images/appCourierMainScreen.png" target="\_blank" rel="noopener noreferrer"><img style="width: 400px" src="/assets/images/appCourierMainScreen.png" alt=""></a>.|-->

### <span class="badge badge-danger">1</span> App menu

Here you can find:

<span><i class="fa fa-user" aria-hidden="true"></i> <strong>User</strong> account and </strong>Sign out</strong></span>.

The list of Restaurants/Shops under **Find restaurants...**

<i class="fas fa-biking"></i> <strong>Tasks</strong> is where you go to see the available tasks (orders and deliveries) to do. Clicking on Tasks takes you to the **Main screen**.

Bottom of the menu screen:
- The name of Coop is displayed. Clicking on it will display an "About us" page. To add or edit content please contact the developer at dev[at]coopcycle[dot]org.
- The Coop email is displayed. This is the email set up in Setting on the Platform website.
- Version number of the App.

### <span class="badge badge-danger">2</span> User account role
This simply displays the role your user account. If your user account has multiple roles, the role would change depending on where you navigate within the app.

### <span class="badge badge-danger">3</span> App settings
<div class="alert mt-3 alert-info" role="alert">
App settings is split into two sections.
</div>

#### **Tasks**
<span><i class="fa fa-check" aria-hidden="true"></i> <strong>Hide done tasks</strong> hides on the map the tasks that have been completed.</span>  
<span><i class="fa fa-times" aria-hidden="true"></i> <strong>Hide failed tasks</strong> hides on the map the tasks that have been cancelled or refused.</span>  
<span><i class="fa fa-tag" aria-hidden="true"></i> <strong>Hide done tasks</strong> hides on the map the tasks that have been completed.</span>  
<span><i class="fa fa-volume-up" aria-hidden="true"></i> <strong>Tasks changed alert sound</strong> if enabled the app will notify when a tasks has been modified. If disabled notification will only happen for new assigned tasks.</span>

#### **Settings**
<span><i class="fas fa-signature" aria-hidden="true"></i> <strong>Signature screen as default</strong> if enabled it displays the Signature screen when completing a task after clicking on <span class="badge badge-secondary"><i class="fas fa-signature" aria-hidden="true"></i> Add a proof of delivery <i class="fas fa-camera" aria-hidden="true"></i></span>. If disabled the Camera opens instead of the Signature screen.</span>
<!--<span><i class="fas fa-power-off" aria-hidden="true"></i> Disable screen lock</span>-->

### <span class="badge badge-danger">4</span> Date picker

Clicking on the date it displays the calendar where you can navigate to any date you need.
Clicking on the left and right arrows it displays tasks from the previous or next date based on the date you're on currently.

### <span class="badge badge-danger">5</span> Map screen

This is the default screen when opening the app. The <span><i class="fa fa-map" aria-hidden="true"></i> icon at the bottom if blue indicates you're on the Map screen.</span>.
Here you can see all available tasks as pins on the map. Completed tasks will be displayed as greyed out pins. 

Tasks (pins) depending on the number of tasks and the zoom level of the map are automatically bundled together in Clusters. A cluster is a solid grey pin with a number on it indicating the number of tasks contained in the cluster. Clicking on the cluster 

### <span class="badge badge-danger">6</span> Task list screen

This screen allows yo to see all the available tasks in list form. To select the Task list screen click on <i class="fa fa-list" aria-hidden="true"></i> icon next to the map icon.

<span class="badge badge-info">INFO:</span><span> Each Task when opened displays a mini-map.</span> 

### <span class="badge badge-danger">7</span> Map

This is the map on the Main screen where you can see all the available tasks.

## Complete an Order or Delivery
<div class="alert mt-3 alert-info" role="alert">
Each Order or Delivery are completed one Task at a time. 
</div>

| From the Map screen  | From the Task list screen  |
| ------- | ------- |
| 1. Click on the desired Task (pin) on the map<br>2. Click on the Task from the pop-up<br>3. Swipe **Right** on the **Complete** button at the bottom<br>4. Click the <span class="badge badge-success"><i class="fa fa-check"></i></span> button.<br> 5. If needed, add a note and proof of delivery [see here]()<br>6. Click <span class="badge badge-success"><i class="fa fa-check"></i> Validate</span>|1. Swipe **Right** on the desired Task<br>2. Click the <span class="badge badge-success"><i class="fa fa-check"></i></span> button. <br>3. If needed, add a note and proof of delivery [see here]()<br>4. Click <span class="badge badge-success"> <i class="fa fa-check"></i> Validate</span>  |
| ![Complete a delivery from the map screen](/assets/images/appFulfillTaskFromMap.gif){:target="_blank"}| ![Complete a delivery from the Task list screen](/assets/images/appFulfillTaskFromTaskList.gif){:target="_blank"}|

### Start a Task

Starting a task records the time you started a task. It is used to indicate when a Courier is on they way towards a pickup or a dropoff. Starting a task is useful for the Dispatcher to know at what stage in an Order or Delivery the Courier is located.

Start a Task can only be selected from the Map screen after. See the first instuction `GIF` above.

### Add proof of delivery

<div class="alert mt-3 alert-info" role="alert">
This option allows taking a photograph and/or a signature as proof of delivery. 
</div>

Before completing a task, at the bottom of the screen you'll find the <span class="badge badge-secondary"><i class="fas fa-signature" aria-hidden="true"></i> Add a proof of delivery <i class="fas fa-camera" aria-hidden="true"></i></span> button.

<a href="/assets/images/appAddProofOfDeliverySignatureAndPhoto.gif" target="\_blank" rel="noopener noreferrer"><img style="width: 300px" src="/assets/images/appAddProofOfDeliverySignatureAndPhoto.gif" alt=""></a>.

### Add name of the recipent customer

Here you can change the name of the customer that received the parcel before you complete the delivery.

<p><a href="/assets/images/appChangeRecipientName.gif" target="\_blank" rel="noopener noreferrer"><img style="width: 300px" src="/assets/images/appChangeRecipientName.gif" alt=""></a></p>

## Cancel or Refuse a Task

| From the Map screen  | From the Task list screen  |
| ------- | ------- |
| 1. Click on the desired Task (pin) on the map<br>2. Click on the Task from the pop-up<br>3. Swipe **Left** on the **Complete** button at the bottom<br>4. Click the <span class="badge badge-danger"><i class="fa fa-times"></i></span> button.<br> 5. If needed, add a note and proof of *failed* delivery [see here](/en/app/courier/#add-proof-of-delivery)<br>6. Click <span class="badge badge-danger"><i class="fa fa-times"></i> Mark task as failed</span>|1. Swipe **Right** on the desired Task<br>2. Click the <span class="badge badge-danger"><i class="fa fa-times"></i></span> button. <br>3. If needed, add a note and proof of delivery [see here]()<br>4. Click <span class="badge badge-danger"> <i class="fa fa-times"></i> Mark task as failed</span>  |
| ![Complete a delivery from the map screen](/assets/images/appMarkTaskAsFailedFromMap.gif){:target="_blank"}| ![Complete a delivery from the Task list screen](/assets/images/appMarkTaskAsFailed.gif){:target="_blank"}|
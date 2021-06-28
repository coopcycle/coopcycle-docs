---
layout: default
title: Admin / Dispatcher
---

<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.14.0/css/all.css">


# Admin / Dispatcher <span class="badge badge-primary">APP</span>

<div class="alert mt-3 alert-info" role="alert">
How to use the App as an Admin and Dispatcher
</div>

## Log in

See [Log in](/en/app/install/#log-in).

## Dispatch (main screen)

When you Log in the the default main screen is **Dispatch**.

<div class="shadow p-3 mb-3 bg-white rounded border border-info">
<span class="badge badge-info">TIP:</span>
<span> A Admin/Dispatch user can also be assigned a Courier role, that way they can assign tasks to themselves, not only to other couriers.</span>
</div>

|   | Dispatch screen  |
| ------- | ------- |
| <span class="badge badge-danger">1</span> App menu<br><span class="badge badge-danger">2</span> User account role<br><span class="badge badge-danger">3</span> Date picker<br><span class="badge badge-danger">4</span> Create Task<br><span class="badge badge-danger">5</span> Refresh task screen<br><span class="badge badge-danger">6</span> Unassigned tasks screen<br><span class="badge badge-danger">7</span> Assigned tasks screen|<a href="/assets/images/appDispatchMainScreen.png" target="\_blank" rel="noopener noreferrer"><img style="width: 400px" src="/assets/images/appDispatchMainScreen.png" alt=""></a>.|

### <span class="badge badge-danger">1</span> App menu

Here you can find:

<span><i class="fa fa-user" aria-hidden="true"></i> <strong>User</strong> account settings, Log in and Sign out</span>.

**Find restaurants...**: the list of Restaurants/Shops where you can order from.

<i class="fas fa-utensils"></i> <strong>Restaurants</strong> is the Restaurant admin screen. For documentation on Restaurants go [here](/en/app/restaurant/).

<i class="fas fa-biking"></i> <strong>Dispatch</strong> is the main Dispatch screen. 

#### **Bottom of the menu screen**:
- The name of Coop is displayed. Clicking on it will display an "About us" page. To add or edit content please contact the developer at dev[at]coopcycle[dot]org.
- The Coop email is displayed. This is the email set up in Setting on the Platform website.
- Version number of the App.

### <span class="badge badge-danger">2</span> User account role
This simply displays the role your user account. If your user account has multiple roles, the role would change depending on where you navigate within the app.

### <span class="badge badge-danger">3</span> Date picker
Here you can change the date to view tasks on the specified date.

### <span class="badge badge-danger">4</span> Create Task
This displays a Task creation screen. These tasks are not attached to a Store or Restaurant. 

|Task creation |Task date picker|
|-|-|
|1. Choose between creating a Pickup or Dropoff task. The active task is highlighted in blue.<br>2. Type the Pickup or Dropoff address.<br>3. Click <span class="badge badge-primary"> Edit</span> to bring up the date picker. A time frame needs to be selected.<br>4. Write a note/comment for the specific task.<br>5. Click <span class="badge badge-info"> Add task</span> at the bottom to create the task.|This is the date picker popup. The date picker needs to be opened separately, for the beginning of the task and end of the task.|
|<a href="/assets/images/appAddTaskScreen.png" target="\_blank" rel="noopener noreferrer"><img style="width: 780px" src="/assets/images/appAddTaskScreen.png" alt=""></a>.|<a href="/assets/images/appAddTaskDatePicker.png" target="\_blank" rel="noopener noreferrer"><img src="/assets/images/appAddTaskDatePicker.png" alt=""></a>.|

### <span class="badge badge-danger">5</span> Refresh task screen
New tasks should appear automatically on the Dispatch screen, if they don't you can click on the empty screen to refresh it. 
This is also the screen where you can view all the [Unassigned tasks](#6-unassigned-tasks-screen).

### <span class="badge badge-danger">6</span> Unassigned tasks screen
Select this to view all the Unassigned tasks screen for a specified date. To change date see [Date picker](#3-date-picker). 

Here you can assign tasks to Couriers. On how to assign tasks, see [here](). Assigned tasks will be moved to the [Assigned tasks screen](#7-assigned-tasks-screen).

### <span class="badge badge-danger">7</span> Assigned tasks screen
This screen will display a list of Couriers with a number in parenthesis next to their names, indicating the amount of tasks each is assigned.

## Assign a task

<div class="alert mt-3 alert-info" role="alert">
You can assign a task by swiping on the desired task and then selecting the courier or by selecting the desired courier first and then picking the task.
</div>

<span class="badge badge-info">TIP:</span><span> Click on each <code>.gif</code> to open it full size.</span>

|Assign task from task list |Assign task from courier|Assign task to me|
|-|-|-|
|<a href="/assets/images/appAssignTaskSwipe.gif" target="\_blank" rel="noopener noreferrer"><img src="/assets/images/appAssignTaskSwipe.gif" alt=""></a>.|<a href="/assets/images/appAssignTasksFromCourier.gif" target="\_blank" rel="noopener noreferrer"><img src="/assets/images/appAssignTasksFromCourier.gif" alt=""></a>.|<a href="/assets/images/appAssignTaskToMe.gif" target="\_blank" rel="noopener noreferrer"><img src="/assets/images/appAssignTaskToMe.gif" alt=""></a>.|

<span class="badge badge-primary">TIP:</span><span> When assigning either a Pickup or Dropoff <strong>task</strong> that is part a Delivery or Order, the other task gets assigned automatically.</span> 
<p>Tasks that form a Delivery or Order, both have the same colour on the left-hand side.</p>

### On how to fulfill/complete a task, see [here](/en/app/courier/#complete-an-order-or-delivery).

### On how to refuse/cancel a task, see [here](en/app/courier/#cancel-or-refuse-a-task).
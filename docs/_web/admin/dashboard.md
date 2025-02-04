---
layout: default
title: Dispatch dashboard
parent: Admin
nav_order: 1
---

# Dispatch dashboard

---

The administration dashboard (called dashboard in this document) allows you to control all the functions for creating and managing tasks as well as to manage the dispatch of couriers manually.

<span class="zoomable">![Dashboard](/assets/images/dashboard_fr.png)</span>

## <s>Add / Create a task</s>

Creating standalone tasks is deprecated, create [deliveries](/en/web/admin/deliveries) instead.

## Edit a task

The same information as "add" is available for editing. In addition to this it is possible:

- Dropdown: Assign a courier
- Dropdown: See history

## Complete a task

To complete a task, just click on the “Finish task” button at the top right of the popup window. The available features are:

- Dropdown: "to do", "failed", "successful"
- Field: Comment on the completion of the task

## See the courier connected on the dashboard

When a courier connects to the application and its location is activated, a marker indicating its position is displayed on the dashboard.

## Add a courier to the Assigned section.

Adding a courier to the schedule means that he is available to be assigned to tasks and therefore to deliver orders. In order to add a courier to the schedule, click on the `+` button in the `Assigned` section.

## Assign a task to a courier.

If it is possible to assign a courier to a task from the popup for creating or editing a task, it is much more convenient to use the drag'n drop function of the dashboard: drop the task directly in the courier assignment area.


## Get information from an order

As soon as two tasks are assigned to a courier, a delivery is created. Several information is available:

- Estimated duration of delivery;
- The distance to be covered (relative to the route of the route) ("Map" button: Show / hide the delivery route, which is the route proposed to the courier for delivery)

## Assign tasks to a courier considering optimization

The dispatcher can optimize the delivery route of the courier by moving the races in the task stack which are assigned to the latter. In order, the first in the stack will be the first route point taken into account and so on until the end of the stack.
The dispatcher can move the tasks in the stack to re-organize them.

## Create a tag and tag a task

Tags are values that can be assigned to a task in order to sort them in the dashboard. A tag is made up of a title and a color. In order to assign a tag to a task, you must first create the tags that the dispatcher needs.

- Go to the configuration panel, “Tag” section;
- Create a tag by clicking on the “Create a new tag” button;
- Give a name and a color to the tag;
- Validate.

In the dashboard, the dispatcher will find the tags by creating a task or by editing it.

- Click on the button `Add a tag` (toothed wheel);
- Add the tag;
  It is possible to assign multiple tags to a task.

## Manipulate the different filters

Different filters are applicable in order to display only certain tasks. It is possible to filter by:

- Task status:
- Completed tasks
- Untagged tasks
- By tag

It is possible to combine the filters.

## Dropdown calendar : change the date

To change the day, just use the drop-down calendar to the left of the top bar of the dashboard.

## <s>Import tasks from a CSV file</s>

Creating standalone tasks is deprecated, create [deliveries](/en/web/admin/deliveries) instead.

## Export tasks in a CSV file

To export a list of tasks you have to provide a date range. You will receive a download of all tasks in that range.

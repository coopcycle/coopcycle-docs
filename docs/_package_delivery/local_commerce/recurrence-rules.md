---
layout: default
title: Recurrence rules
parent: Recurring orders
---

# Recurrence rules

Recurrence rules enable the automation of creating recurring orders. Currently, the platform supports the following recurrence rules:

- **Daily**: the order is created every day
- **Weekly**: the order is created on specific days of the week
- <span class="badge badge-info">NEW in 3.37</span> **Advanced mode**: the order is created based on a custom recurrence rule, which can be defined using the [iCal recurrence rules](https://datatracker.ietf.org/doc/html/rfc5545#section-3.3.10).

<span class="zoomable">![List](/assets/images/recurrenceRulesList.png)</span>

<span class="badge badge-info">TIP:</span> The list also includes the recurrence rules created from the Dispatch dashboard. However, orders (and tasks) will NOT be created automatically for them.

## How to create a recurrence rule

The recurrence rule can be configured while creating a new Delivery order:

<span class="zoomable">![List](/assets/images/recurrenceRulesSetup.png)</span>

### How to set up a custom recurrence rule

To set up a custom recurrence rule, select the **Override recurrence rule** option under **Advanced** section and define the recurrence rule using the iCal format. For example:

* To create an order every 2 weeks on Monday and Thursday, you can use the following rule:

```
RRULE:FREQ=WEEKLY;INTERVAL=2;BYDAY=MO,TH
```

* To temporarily pause a recurrence rule: add a `COUNT` element equal to 1. To resume: remove the `COUNT` element

```
RRULE:FREQ=WEEKLY;COUNT=1;BYDAY=MO,TH
```

<span class="zoomable">![List](/assets/images/recurrenceRulesOverride.png)</span>

<span class="badge badge-info">TIP:</span> You can use the [iCal recurrence rule generator](https://jkbrzt.github.io/rrule/) to create the rule.

<span class="zoomable">![List](/assets/images/jkbrztRrule.png)</span>

## Using recurrence rules

Orders (and tasks) will be automatically created based on the Recurrence rules

<span class="zoomable">![List](/assets/images/recurrenceRulesUsage.png)</span>

## How to modify a recurrence rule

To modify a recurrence rule, you can edit the existing rule in the **Recurrence rules** page. Click on the **Edit** button next to the rule you want to modify:

<span class="zoomable">![List](/assets/images/recurrenceRulesList.png)</span>

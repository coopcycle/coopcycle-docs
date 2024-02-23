---
layout: default
title: Data Analytics
---

<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.14.0/css/all.css">

# Introduction

CoopCycle aims to be more than a logistics platform, but to a software that can help small cooperatives and associations better run their economic, political, and social activities. This means we need to have the ability to tell these organizations about their activities, leading to the creation of the Data Analytics part of CoopCycle. While this is still in its first implimentation, we are excited for these first steps. 
  
# Business Impact

The goal of the Data Analytics dashboard in the short term is **to be able to tell an organization if it is making or loosing money during a specific time period** (Tuesday the 23rd between 4 and 6 pm for example). By showing the costs and income of an organization, divided by the different activities that the organization has, it is possible to help them focus on the most effective types of deliveries, avoid difficult financial situations, and better understand their democratic life.

# How will we do this?

This requires have coherent and accurate data about income, variable costs, and fixed costs. 

### Income
Until recently it has been impossible to put many types of deliveries with their prices onto the CoopCycle platform. Some client orders came through the API, which didn't have prices (they do now!), some types of deliveries like multiple dropoffs couldn't calculate pricing (now they can!) and large imports were not being attached to stores (now they can be!). Check out the [Pricing](https://docs.coopcycle.org/en/admin/deliveries/pricing/) page to see how to update your instance.

Now that we are wrapping up our [Pricing feature](https://github.com/coopcycle/coopcycle/issues/31) we can begin to help cooperatives make sure that the data generated in CoopCycle is reliable. This means having "create orders" activated on Shops, completing tasks in the application at the correct time and making sure orders are on the platform. In the next months we will finish the [Version 1 of Incidents and Reporting](https://github.com/coopcycle/coopcycle/issues/9) and [Version 2 of Incidents and Reporting](https://github.com/coopcycle/coopcycle/issues/10), adding more detail and specificity to this income data.

### Variable Costs and Fixed Costs
In our sector, our variable costs are more of less the hours of delivery by messengers. To have this information we are building an interface within CoopCycle described in our [Human Resources Portal feature](https://github.com/coopcycle/coopcycle/issues/20) that will link together with [APIs](https://www.howtogeek.com/343877/what-is-an-api/) with shift planning software in order to track delivery hours. dispatch hours, administrative hours, and all other labour costs. Additionally, the portal in CoopCycle will allow the cooperative to input their monthly material costs such as rent, bikes, etc. By collecting all this data accurately and defining to which activity each cost is related, we have a complete picture of the cooperatives cost structure. We will be integrating with [Sling](https://getsling.com/) due to its frequent use throughout the federation, and will evaluate further integartions over the course of the next year. If you are thinking about using a new shift management software, picking Sling might be a good idea.

### Outcome
The outcome we will be what is described in the [Profitability](https://github.com/coopcycle/coopcycle/issues/23) feature: The ability to accurately tell cooperatives when they loose and make money, and where those profits or losses are coming from. 

# What We Have Now
So far we have finished setting up the income side of this feature, which can be useful for cooperatives while we finish the Human Resources portal. For now we have used Tablou, a for profit software that we could set up fast and our team already had experience with. We are building up the structure to switch from Tablou to an internal system based on open source software during the rest of 2024. This means each cooperative has a link to a page where they can see their own data, outside of their CoopCycle instance. 

### Things to know when using the tables
1. There is a bar at the top of each dashboard that represents time. Move the sliders to the right and left to change the dates that is creating the visulizations.
2. There are dropdown menus on the right hand side that change what data is shown in the visualization. We for example distinguish between food orders and non-food orders. In each tab there are different conditions to change based on how your cooperative functions.
3. At the bottom there is a button to download any page with its information in multiple formats.
4. We have the numbers in **net** not **gross** because we assume that the most important thing to know is how much money you will earn **after VAT tax**.

Right now the dashboard has the following features:
**Income Overview:** Where you can see the total income per month separated between food and non-food orders, and some basic statistics at the bottom. This page exists to help cooperatives understand how their business is evolving globally.
**Venues Overview:** An overview of the **number** of orders made per week with information about average income per order and total values. This page is meant to help understand the evolution of food orders over time, and especially to look at specific partners to see their demand fluxuation.
**Commission:** A tab for analyizing the commisions that are charged to restaurants, and simulate what effects price changes could have on your profitability. This page is mean to allow a cooperative to try out new pricing concepts to see their impact based on historical data using simulations.
**Delivery Fee:** A visulaization of the different delivery fee charges that are being charged to food order customers based on distance of the delivery. This page exists to help a cooperative understand which delivery fees are most frequent and how much more they are being paid the farther they extend deliveries.
**Delivery Fee Map:** A map that visualizes where food order destinations are in your city, and the delivery fee paid by each one. Try drawing a circle on the map to look at areas of interest. This page exists to understand the geography of your deliveries and what zones your income is coming from.
**Invoicing Table:** A pivot table that shows the income for each client on the platform for a certain month to facilitate invoicing. 
**Performance:** A visualization of the average income generated during a particular hour and day of the week. Remember you can change the hours shown! This is meant to let a cooperative understand what times and days are more active, and with some basic math about number of messengers in the street, can give an idea about profitability.
**Pickups and Dropoffs:** A visualization of in what time periods of the day are your pickups and dropoffs. The idea is to understand when to program shifts based on historical demand.
**Pickups and Dropoffs Comparison:** A tab that allows you to compare pickups against dropoffs, or pickups from one time range to pickups from another time range. This allows you to understand when to have shifts, as well as compare you volume of work to past months or years. 

What we have now is interested, but limited by its focus on income, the only data we have at the moment. As we develop the other parts of the system we will update this documentation page. 












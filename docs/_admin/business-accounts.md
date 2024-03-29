---
layout: default
title: Business Accounts
---

<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.14.0/css/all.css">

# Introduction
CoopCycle identified that the food delivery platform was not set up to efficiently and effectively offer services to businesses that are looking to cater business meetings, have lunch delivered to their employees, or offer special deals to businesses who which to help pay for employee food costs. This is a common practice, especially in France, which goes hand in hand with EdenRed and other ["Ticket Restaurant"](https://frenchly.us/frances-ticket-restaurant-or-ticket-resto-program-explained/) platforms. We identified that by creating a Business Accounts feature and by integrating with EdenRed other French ticket restaurant providers, both French and non-French cooperatives can offer a service to businesses that can represent regular and well-paid work with stable clients (something hard to find in food delivery) during strategic times (weekday lunch). We call this service "Platform Catering" because it reflects catering services (bringing food to large events and gatherings) but with a platform. 

# What is it?
This feature exists to allow a business to have a private account with a CoopCycle instance so that its employees to make an order that comes from multiple restaurants and is delivered simultaneously. The local cooperative can associate specific restaurants to this business account and apply specific characteristics to these orders such as pricing rules, delivery time conditions, cutoff times, etc. This allows the local cooperative to only do multiple-pickup orders with restaurants that they know will have the orders prepared at the correct time, offer specialized prices and menus for these services that are different from the normal platform, and limit the service times to those that make sense for the business case.

The goal is for a cooperative to be able to offer tailored agreements to different businesses. Maybe the cooperative wants to charge a flat fee per month and the business gets free deliveries for all its employees. Or maybe the business wants to make large catering orders regularly, so the cooperative decides to lower the percentage that they request from the restaurants. 

# How to set up Business Accounts
First, go to the [Restaurants page](https://demo.coopcycle.org/admin/restaurants) represented by a cart icon in the top right menu and click on "More Options", then click on "Business Restaurant Groups". 

### Business Restaurant Groups
Here you can create a new restaurant group or edit an existing one. In the general settings of each group you can change the name of the restaurant group and add restaurants and the menu they would like to offer to these clients. 

Remember to make sure the restaurant has made a menu that works with this service model! If they have something that takes particularly long to prepare or can cause problems, they should make a new menu in their restaurant configuration that only has the products they wish to offer for this service. They can also modify the prices of their products for a specific restaurant group in the products configutaion page if they would like to offer special deals for business clients.

<img width="1449" alt="Screenshot 2024-02-22 at 23 59 29" src="https://github.com/coopcycle/coopcycle-docs/assets/77277854/d3e4096c-894a-4a2a-b5e5-25f876fbb7b7">
<img width="1449" alt="Screenshot 2024-02-23 at 00 00 03" src="https://github.com/coopcycle/coopcycle-docs/assets/77277854/cdcbd0d5-a538-444f-8770-ce9567a37e45">

<img width="1033" alt="Screenshot 2024-02-22 at 10 44 49" src="https://github.com/coopcycle/coopcycle-docs/assets/77277854/1da7b19b-0ddc-45e7-bc2a-e2260ced5556">


In the Fulfilment page the Restaurant Group must have its own time range and other conditions just like a restaurant on the normal platform. This will only impact orders made through the business acconut portal, not other normal orders. 

Finally, the Settlement page is where the cooperative must create the specific pricing they would like to apply to this use case. This way they can offer special deals to encourage restaurants to join the service, or offer deals to the business itself such as a lower delivery fee. Remember that this will globally impact all orders made in the Business Account associated to this Business Restaurant Group, overriding your normal pricing rules. If you don't want different rules, just add the same as you have for the restaurants normally. 

After finishing this section, the administrators of the cooperative need to go back to the Restaurants page, click on the "More Options" and then "Business Accounts"

### Business Accounts
Here there are the options to create a new Business Group or edit existing ones. Here there only is the option to name the group, add an administrator email to give access to the account for an adminstraator of the business, and associate a Restaurant Group. The users that an administrator has associated to their account and the orders they have made throught the service appear in the other two tabs, which allows the busines to understand what impact the service has had. 

<img width="1449" alt="Screenshot 2024-02-23 at 00 00 31" src="https://github.com/coopcycle/coopcycle-docs/assets/77277854/7b8fa7fe-7ed1-4c58-9721-95445cb9534c">

The administrator from the client business who is connected to the Business Account will now have new optons in their "My Account" page where they can see this information and manage the users associated to the account. 

### What are we still working on?
1. Right now we have not made any changes to dispatch to facilitate these orders. The next step will be looking at a series of improvements that will facilitate the combination of orders from multiple restuarants. This will likely include a reworking of how order codes are generated, and a feature to "combine" pickups and pass packages from one messenger to another with tracking throughout the process.
2. We will soon have the ability for a cooperative to upload invoices to the Business Account in pdf format so that a business can see their invoices in one place. This will also set the stage for when automated invoices can be generated directly through CoopCycle.
3. Group orders are obviously a useful feature to combine with Business Accounts. We will be doing a trial run in the coming weeks (March 2024) in order to make sure it works correctly when combined with business accounts. Since things can often break when big changes are made, especially when two of them together, we want to tread carefully before making this feature public.

## Example 1 - Company Meetings
Perhaps a cooperative has a relationship with a business who has frequent meetings, and the business would like to have an easier way of making orders from multiple restaurants in order to cater to the different needs of the participants. In this case, the cooperative might make a business account with a variety of restaurants that they know will work professionally, setting up menus that have special items that are smaller and more like taster items that full dishes. Due to the large sizes of the expected orders, the cooperative may change the pricing rules to eliminate the delivery fee and slightly discount the percentage charged to the restaurants (regular orders and high quality may justify making special deals). In this case a manager or a couple managers at the business have acess to the business account and use it when needed, infrequently looking at the administration page. 

## Example 2 - Platform Lunches
Another company has decided to take advantage of the "Ticket Restaurant" system in France after noticing that many employees bring their lunch in tuppers and eat together in the break room. This will be an added value to the employees without significant costs for the businesses, while also helping to encourage social elements of the company culture. Since CoopCycle is integrated with EdenRed, they are able to use our platform with their own system. In this case the cooperative may make a business account with associated restaurants, but without modifying their menus other than to take off the very time-intensive products. The cooperative only takes away the delivery fee for the orders, since they have negotiated a 100,00 € monthly fee with the business to cover all delivery fees. The business administrators then invite their employees to make associated accounts in the local CoopCycle instance and check in regularly to see how much the service is being used, and if the 100,00 € per month are paying off as an investment. 

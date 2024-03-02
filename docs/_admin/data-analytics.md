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
5. If you don't know where you dashboard is, reach out to the team on Slack or by email!

Right now the dashboard has the following features:


- **Income Overview:** Where you can see the total income per month separated between food and non-food orders, and some basic statistics at the bottom. This page exists to help cooperatives understand how their business is evolving globally.
- **Venues Overview:** An overview of the **number** of orders made per week with information about average income per order and total values. This page is meant to help understand the evolution of food orders over time, and especially to look at specific partners to see their demand fluxuation.
- **Commission:** A tab for analyizing the commisions that are charged to restaurants, and simulate what effects price changes could have on your profitability. This page is mean to allow a cooperative to try out new pricing concepts to see their impact based on historical data using simulations.
- **Delivery Fee:** A visulaization of the different delivery fee charges that are being charged to food order customers based on distance of the delivery. This page exists to help a cooperative understand which delivery fees are most frequent and how much more they are being paid the farther they extend deliveries.
- **Delivery Fee Map:** A map that visualizes where food order destinations are in your city, and the delivery fee paid by each one. Try drawing a circle on the map to look at areas of interest. This page exists to understand the geography of your deliveries and what zones your income is coming from.
- **Invoicing Table:** A pivot table that shows the income for each client on the platform for a certain month to facilitate invoicing.
- **Performance:** A visualization of the average income generated during a particular hour and day of the week. Remember you can change the hours shown! This is meant to let a cooperative understand what times and days are more active, and with some basic math about number of messengers in the street, can give an idea about profitability.
- **Pickups and Dropoffs:** A visualization of in what time periods of the day are your pickups and dropoffs. The idea is to understand when to program shifts based on historical demand.
- **Pickups and Dropoffs Comparison:** A tab that allows you to compare pickups against dropoffs, or pickups from one time range to pickups from another time range. This allows you to understand when to have shifts, as well as compare you volume of work to past months or years. 

What we have now is interesting, but limited by its focus on income, the only data we have at the moment. As we develop the other parts of the system we will update this documentation page. 

# Examples

### Income Overview
This is an example of a cooperative that is either primarily foodn tech based, or has not put its other activities on the CoopCycle platform. On the right a user can change the time periods shown, include or not both food and non-food orders, and include or exclude tips. Some cooperatives pay tips directly to the messengers individually, and some mutualize the tips. If tips are paid out by what was given in each order that a messenger has done, do not include them. If you mutualize the tips, include them. On the bottom right are aggregated averages for the data and totals.


![F3765B78-CB24-4641-BF02-B0669CC90C02](https://github.com/coopcycle/coopcycle-docs/assets/77277854/1d096934-832f-460d-9951-020236eabfeb)


Next we have a picture of a primarily last mile cooperative that began to input all their deliveries as orders in March of 2023, and their volume of business went up in September dramatically. In their case, there are so few food tech orders that they barely show up.

![622FC7BB-9CED-4FFE-BB4F-EDD7B87B711E](https://github.com/coopcycle/coopcycle-docs/assets/77277854/5da52077-d498-4f41-9b86-1ad45fb99226)

### Venus Overview
Foodtech
![11F05D5B-0926-41E0-9A47-D9CCAEA60532](https://github.com/coopcycle/coopcycle-docs/assets/77277854/1bfa28b3-f2a4-4ed0-a19a-e32ea5a179e9)


Here we can see the fluctuation of the food deliveries and the pick-up/collection deliveries. On the bottom left there is an explanation of the average and total incomes for food deliveries, collections, and for last mile orders. on the right side the averages are shown in bar graph form in order to understand better where the revenues are coming from. On the right hand side you can select which shops and stores you would like to visualize and change the time period being analyzed. 

Last Mile

![88EEC863-362E-492E-99B4-8884828419C4](https://github.com/coopcycle/coopcycle-docs/assets/77277854/5f3ed8a0-9594-45ab-acda-a23fc2e1abf2)


Here we have the same information, but for a cooperative that works almost exclusively in last mile. 

### Commission

Without Simulation

![1C671C38-A6EB-48A5-A90F-92EA994D4B8F](https://github.com/coopcycle/coopcycle-docs/assets/77277854/cc13ac77-fb53-45b9-b89c-836dbf69c54c)


Here a food tech cooperative can analyze the amount of commission that they earn on the deliveries. This only reflects the money taken from the basket of food purchased, **not** the delivery fee or tips. The first use of this page is to understand what amount of money your percentages and pricing rules turn into for different restaurants. Maybe for one restaurant you have a flat percentage fee, and another is using a percentage plus a €2,00 charge per order and you would like to know which is making more money. By changing the values of the restaurants and order values visualized you can better understand the way your pricing rules turn into actual €X,XX in income for your cooperative.

With Simulation
![1135AC79-CA52-4281-BFC2-9C7C079C329A](https://github.com/coopcycle/coopcycle-docs/assets/77277854/3536148e-7787-4262-bb83-fb24c1ad2c08)


The second use of this page is to simulate pricing modifications. Since many of our prices are not simply a flat percentage, we do not always understand clearly the impact of a pricing rule change. The change my act differently on a restaurant with a higher or lower average order value in ways we have difficulty imagining. By putting in a new price rule in the bottom right and pressing enter we will be shown on the left what this pricing rule **would have** earned us in the time period defined and for the restaurants chosen. In this way we can try out new prices before negotiating with our clients and come better prepared. 

### Delivery Fee
Simple three tier system
![2CAAAE05-C428-4F72-AE35-7A534EFBA0B1](https://github.com/coopcycle/coopcycle-docs/assets/77277854/33338fd0-45c2-458d-9196-109d929311cf)


Here we have the example of a food tech cooperative with a very simple delivery fee rule for clients. They have 3 types of delivery fees, apart from some outliers. The goal of this page is to understand the relationship between how far a messenger must go, and therefore how much work/time is being invested in a delivery, and the amount of money that is being earned. For example, there aree a few deliveries in orange towards the right that represent almost 5,5km in which the client is being charged the lowest possible delivery fee. Maybe this is due to a strategy by the cooperative to have cheap delivery for large orders, or maybe this is an indicator that the zone should be changed. Conversly, there are expensive fees for deliveries only going 500m. In general, there is a **very** wide range of distances travelled for each delivery fee, and perhaps the way the fees are structured should be reconsidered to make sure those who are farther away are paying more. 

Complex delivery fee
![A463C0C3-DABE-4BB5-A2B9-80FA59C2AF5C](https://github.com/coopcycle/coopcycle-docs/assets/77277854/8b404a5c-f8b7-4c55-985f-7d3c4a9039d8)

Here we have a food tech cooperative with a highly complex delivery fee structure. They have different rules for different types of services, with the blue line representing a catering service with large order sizes that have a low flat fee. 

### Delivery Fee Map
Simple
![84E46A31-4361-44C6-8F02-323E36905568](https://github.com/coopcycle/coopcycle-docs/assets/77277854/fb69f340-62c1-4c02-97b6-3b4deaa9bcff)

In this map we can see what appear to be three pricing rules based on zones, but by looking at different restaurants it is clear that in reality there are two zone configurations happening at once, one based on orders being picked up in the north and another for orders being picked up in the center. In the bottom there is a table that shows information about the averages and totales for the selected deliveries. \ Other than the options on the right as usual, by clicking and dragging on the map it is possible to select only certain geographic areas. This page also helps understand how much work we are investing to earn our delivery fees, as well as helps us understand where we might want to focus communication and marketing efforts. 

Complex
![C51BD4AE-0545-4240-B78D-D93466F2B8F6](https://github.com/coopcycle/coopcycle-docs/assets/77277854/26bce07a-44c9-495e-947a-dbe471e50491)

In a more complex delivery fee pricing rule we can see that there are many factors to consider. In this case the delivery fee is being calculated on the distance from the restaurant, something that makes the map much more diverse when there are restaurants all over the city. By selecting different delivery fee amounts it is possible to start undetstanding the geography of the pricing structure and understand which delivery fees make sense and which do not. 

### Invoicing Table
![5DD9B0CD-D6C4-463C-AB16-296B82F55F1C](https://github.com/coopcycle/coopcycle-docs/assets/77277854/143ffbc0-7463-4b77-9199-439ca07e062f)


Here we have a simple pivot table which shows the Net, VAT, Gross, and Refunds for each customer. This is meant to facilitate invoicing. We still have a few issues to clean up in our [Pricing V.1 Epic](https://github.com/coopcycle/coopcycle/issues/31) such as allowing kilometer based prices to function for multi-dropoff deliveries, but if a cooperative has put all of its prices inside of their CoopCycle instance effectively it means that this page will show them how much to charge each client at the end of the month.  

### Performance
Food Tech
![7299F447-22AF-4893-A9E2-B1E77C7DA15D](https://github.com/coopcycle/coopcycle-docs/assets/77277854/80064bf8-40ca-4940-a1fd-d65b199a0023)


This page shows the average income in an hour/day of the week for a food-tech cooperative. While we are working on a second version of this portal that will reflect profitability, for now this only shows income. The use case for this page is to use the average income per hour shown in each bubble compared to your labor cost per hour in order to understand how many messengers should be working in any given hour on average. 

Last Mile
![E404E12D-A051-42CF-948A-B0E4276CAF1F](https://github.com/coopcycle/coopcycle-docs/assets/77277854/b68f31f4-e941-4e77-b9e6-defd16aa1e2a)

The same priciple and goals, but show for a Last Mile cooperative working principally weekdays during the mornings. 

### Pickups and Dropoffs
Food Tech
![15458739-6D90-4CB6-AD97-10A328CA8AD4](https://github.com/coopcycle/coopcycle-docs/assets/77277854/c9cd99a2-8684-478d-b0bc-a7116e6c9dc0)


This page is also designed to help a cooperative understand how many messengers they may want in a given hour of the day. It also can help understand the flow of orders over time. In this case, for a food-tech cooperative, most hours are similar in regards to pickups and dropoffs.

Last Mile
![6CC0AE93-9D6D-4E51-A64A-B715580762A9](https://github.com/coopcycle/coopcycle-docs/assets/77277854/68a140b8-1832-41ab-99e0-4c535cfee5d2)


Here we can see that a last mile cooperative is recieving many orders in the first hours of the day and then is delivering them throughout the morning and afternoon. This may have implications for shift planning, maybe the cooperative needs efficient pickers in the morning who then pass of organized routes to messengers for example. This then would help the cooperative understand at what hours should the shifts begin and end.

### Pickups and Dropoffs Compared
Food Tech pickups vs dropoffs
![6E177E07-A27A-4725-9E8E-14B776E27CE1_1_201_a](https://github.com/coopcycle/coopcycle-docs/assets/77277854/4a099370-a7a7-47c9-afb0-1120b718798c)

This page allows a cooperative to compare the pickups or dropoffs of any day or series of customers to the pickups or dropoffs of another day or another series of clients. This can be done to better understand the fluctuations between days of the week or clients, or to help with shift planning. In this case the coparison is between pickups and dropoffs for a food-tech cooperative.

Last Mile pickups vs dropoffs
![4BFEEE39-1DA3-45E4-B0C6-90BABBDFC7D5](https://github.com/coopcycle/coopcycle-docs/assets/77277854/8e2acf9b-e39f-4302-91a9-0dcde36e6617)


Here we have a similar comparison, but it is the last mile cooperative from the example above. 

Comparing one year to another
![3A42A8D3-9E9C-4332-AB6E-37E7926BF7AC](https://github.com/coopcycle/coopcycle-docs/assets/77277854/4599d208-356f-4390-acf3-ec17daee80a7)

Lastly, we can compare volume from one time period to another. In this case the comparison is between the pickups from fanuary 2024 and the dropoffs of 2023. This can help us understand why certain months are more or less profitable, or at least to understand how much of those differences can be attributed to changes in volume. 


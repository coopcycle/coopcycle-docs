---
layout: default
title: Excel Imports
---

<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.14.0/css/all.css">

# Introduction
We have two types of excel imports that are used frequently on the platform. One is uploading to the [Admin Panel](https://demo.coopcycle.org/admin/dashboard). This import creates unlinked, individual tasks. This was the first import that was created in CoopCycle, and it is the most complete in some ways, but also has some missing features. 

On the other hand, we have an excel import for the Deliveries page that can be uploaded from the [Dispatch Deliveries Panel](https://demo.coopcycle.org/admin/deliveries) if your excel has a column specifying the Client (a Store), but it is recommended to go the a [Store's Deliveries History](https://demo.coopcycle.org/admin/stores/48) page to simplify and avoid possilbe errors. 

Keep in mind, these excels are currently being redesigned to improve the workflow, and there may be improvements and changes soon. 

## Deliveries Imports
There are a lot of different types of possible deliveries, clients, and situations. Let's start with something easy!

### A Simple Delivery Import
If you have a shop with few configurations, you can use this excel to create linked deliveries that will appear in the map. A Store like the demo's [Boats on Fire](https://demo.coopcycle.org/admin/stores/90#settings) will make deliveries, it will not create prices for a number of reasons. However, the deliveries will exist in CoopCycle and on your map. If you are a new cooperative and just need to make some deliveries, this is a perfectly fine solution to get started. 

#### Getting Everything Set Up
1. Know my VAT tax (in this example, 20%)
2. Make a Store
3. Make a basic pricing rule
4. Make sure you are correctly connected to the Google Maps API

<br>
<div class="shadow p-3 mb-3 mt-n4 bg-white rounded border border-warning">
   <span class="badge badge-warning">IMPORTANT:</span>
   <span> Remember that this will create a pickup for each delivery. So if you upload 50 deliveries that will be dropped off at your warehouse to be delivered, you will have 50 pickup tasks in the same location. For this reason, you can either **complete multiple tasks at once in the CoopCycle app as a courier** or **close multiple tasks at once in the admin panel** </span>
   </div>

#### The Context 
I am a new cooperative, and I want to work with a new client who is going to give me 20 orders a week, and instead of making the orders one by once, I would like the client to upload an excel, or do it myself. 

#### The Pricing Rule
I am going to charge 7 euros + VAT tax per delivery normally because they don't mind delivery windows of 2 hours, but if they want something urgent it needs to be 10 euros + VAT tax. To do this I create a pricing rule like this:
<img width="1089" alt="Screenshot 2024-01-16 at 14 45 50" src="https://github.com/coopcycle/coopcycle-docs/assets/77277854/184d5929-4b3f-425f-968c-dd2ecd56cf5f">

#### The Store Profile
I am going to go to the [Stores Dashboard](https://demo.coopcycle.org/admin/stores) and click on "Create a New Store" and fill out the basic information associated with the client and click "Save". Then, go to the Settings menu for that client, and associate the pricing rule to their profile. 
Step 1
<img width="1097" alt="Screenshot 2024-01-16 at 14 46 45" src="https://github.com/coopcycle/coopcycle-docs/assets/77277854/1ddc6f64-bd63-4aaf-bde9-786bb64bb448">
Step 2
<img width="1465" alt="Screenshot 2024-01-16 at 14 51 50" src="https://github.com/coopcycle/coopcycle-docs/assets/77277854/e441a669-89cc-4975-a6b4-221d62603896">

#### The Simple Excel Import
Fill out the [Simple Delivery Example](./coopcycle-deliveries-simple-example.csv) and upload it in the delivery page of your client. 

In this case you want to simply fill out the columns 
- pickup.address: Copy and paste the address directly from Google maps
- pickup.timeslot: Add a date range in the format YYYY-MM-DD HH:MM - YYYY-MM-DD HH:MM
- dropoff.address: Copy and paste the address directly from Google maps
- dropoff.timeslot: Add a date range in the format YYYY-MM-DD HH:MM - YYYY-MM-DD HH:MM

<img width="1469" alt="Screenshot 2024-01-16 at 14 58 04" src="https://github.com/coopcycle/coopcycle-docs/assets/77277854/053b602f-b2fe-4d66-86bc-4acfb1a135ba">

#### Simple Deliveries Example
|pickup.address|pickup.timeslot|dropoff.address|dropoff.timeslot
|-|-|-|-|
|24 rue de rivoli paris |	2019-12-12 10:00 - 2019-12-12 11:00 |	58 av parmentier paris	| 2019-12-12 12:00 - 2019-12-12 13:00 |
|24 rue de rivoli paris	| 2019-12-12 10:00 - 2019-12-12 11:00	| 34 bd de magenta paris	| 2019-12-12 12:00 - 2019-12-12 13:00 |

#### Something went wrong? 
Go to the [bottom of the page](#bottom) to see how errors work and we'll figure something out :) Get in contact with us through whatever channel you have or email us if you can't figure it out on your own. 

### A Complex Delivery Import
#### etting Everything Set Up
1.Know my VAT tax (in this example, 20%)
2. Make a Store
3. Make a package set that reflects the client's needs
4. Make one or multiple time slot ranges that reflect your delivery options
5. Make tags if you want to differentiate between different types of orders that they make (ex: VIP, urgent, needs trailer)
6. Make a basic pricing rule
   - If your pricing rules need zones, create zones
   - If your pricing rule needs a vehicle concept, create vehicles
7. Make sure you are correctly connected to the Google Maps API

#### The Context
I have a client with many possible types of delivery situations and complex needs. There may be many delvieries, up to 50 a day, and some deliveries will come through manual creation in the web platform, but some will come through imports to save time.

#### The Pricing Rule
- I am going to charge 7 euros + VAT tax per delivery normally because they don't mind delivery windows of 2 hours.
- If the delivery can be done any time all day, it is only 5 euros + VAT.
- If it is an urgent delivery with a time range of less than 1 hour, there is an extra chage of 5 euros + VAT.
- I need to know what the packages are, it they are small, no change. But if the package is large, extra charge of 3 euros + VAT, and 10 euros + VAT if enormous because I must use the trailer.
- I have multiple delivery zones, center is same charge, but zone 2 adds 2 euro + VAT and zone 3 adds 5 euros + VAT
- I need at least 1 hour of prior notice, I don't accept orders with less than 1 hour of notice.
- I'm not using weight as a price, but I would like to know it if they have it
<img width="989" alt="Recurrent Rules" src="https://github.com/coopcycle/coopcycle-docs/assets/77277854/ab855c64-9d00-4e47-9702-ff3db5ea404e">

#### The Store Profile
In the Store's settings page: Associate the pricing rule with the client, activate that package set and weight are required, that the client creates orders, and associate the correct package set with the client. 
<img width="995" alt="Recurrent Rules (2)" src="https://github.com/coopcycle/coopcycle-docs/assets/77277854/f8f072b2-9248-46d1-9759-61389f3dcd4a">

#### The Complex Excel Import

Fill out the [Complex Delivery Example](https://demo.coopcycle.org/spreadsheets/examples/coopcycle-deliveries-example.csv) and upload it in the delivery page of your client. 

In this case you want to simply fill out the columns 
- pickup.address: Copy and paste the address directly from Google maps
- pickup.address.name: The public name of the business
- pickup.address.description: Information relevant to the pickup (ex: "the door is hard to find, it's blue")
- pickup.address.telephone: A valid phone number (ex: 666 666 666) (IMPORTANT: this will break if you use phone numbers with country codes that are not your country)
- pickup.comments: Extra information that you would like to have in the comments section of the pickup task
- pickup.tags: Names of tags that you want to use with a space between tags, and "-" to show a space between words in a single tag (ex: "VIP urgent-delivery")
- pickup.timeslot: Add a date range in the format YYYY-MM-DD HH:MM - YYYY-MM-DD HH:MM
  
- dropoff.address: Copy and paste the address directly from Google maps
- dropoff.address.name: The name of the business or organization to which the package is being delivered
- dropoff.address.description: Information relevant to the dropoff (ex: "the dog is friendly)
- dropoff.address.telephone: A valid phone number (ex: 666 666 666) (IMPORTANT: this will break if you use phone numbers with country codes that are not your country)
- dropoff.timeslot: Add a date range in the format YYYY-MM-DD HH:MM - YYYY-MM-DD HH:MM
- dropoff.comments: Extra information that you would like to have in the comments section of the dropoff task
- dropoff.packages: Each package needed with the quantity with a space between tags, and "-" to show a space between words in a single package name (ex: small=1 medium=2)
- dropoff.tags: Names of tags that you want to use with a space between tags, and "-" to show a space between words in a single tag (ex: "VIP urgent-delivery")
- weight: How many kilos in format XX.XX (better . than , )

<img width="1469" alt="Screenshot 2024-01-16 at 14 58 04" src="https://github.com/coopcycle/coopcycle-docs/assets/77277854/053b602f-b2fe-4d66-86bc-4acfb1a135ba">

#### Complex Deliveries Example

| pickup.address | pickup.address.name	| pickup.address.description | pickup.address.telephone | pickup.comments | pickup.timeslot | pickup.tags |	dropoff.address |	dropoff.address.name | dropoff.address.description |	dropoff.address.telephone | dropoff.comments | dropoff.timeslot | dropoff.packages | dropoff.tags | weight |
| - | - | - | - |	- | - | - |	- | - | - |	- | - | - |	- | - | - |
| 24 rue de rivoli paris | Awesome business | - | 33612345678 | Fragile | 2019-12-12 10:00 - 2019-12-12 11:00 | warn heavy	| 58 av parmentier paris | Awesome business | Buzzer AB12 | 33612345678 | 2019-12-12 12:00 - 2019-12-12 13:00 | small-box=1 big-box=2 | warn heavy | 5.5 |
| 24 rue de rivoli paris | Awesome business | - | 33612345678 | Fragile	| 2019-12-12 10:00 - 2019-12-12 11:00	| warn | 34 bd de magenta paris | Awesome business | Buzzer AB12 | 33612345678 | 2019-12-12 12:00 - 2019-12-12 13:00 | small-box=1 big-box=2 | warn | 8.0 |

<img width="1827" alt="image" src="https://github.com/coopcycle/coopcycle-docs/assets/77277854/61e69f9f-e577-4080-ad0a-1017231efe9e">

<div id="bottom"></div>

## Something went wrong! 


Historically there have been a large number of errors that were difficult to understand as users of CoopCycle when trying to use the excel upload. Good news! We have done a redesign of the upload system, and things are working properly! Now if you upload an excel it will load asynchronously to eliminate time-out errors, and if there is a problem with your excel the plaform uploads the lines of the file that it understands correctly, shows you which lines were not understood well, and can give back to you an excel with the lines of the file that did not upload correctly for you to modify and try again. 

![telegram-cloud-photo-size-4-5830347650132722643-y](https://github.com/coopcycle/coopcycle-docs/assets/77277854/a5f7733f-ef53-45de-9401-2b28bd716e3a)

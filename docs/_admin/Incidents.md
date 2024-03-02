---
layout: default
title: Incidents and Reporting
---

<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.14.0/css/all.css">

# Introduction
Incidents are a fact of life in logistics. Things break, things get lost, things arrive later than expected, clients decide that two boxes are actually one (oops!), the list goes on forever. Managing these incidents is a key part of your branding and service quality. Imagining that you will simply not have incidents is unrealistic, we must plan for accidents and mistakes and create effective protocols that allow us to keep clients happy with our service. The goals of this section are to explain:
1. Best practices for incident management as an organization
2. Explain the workflow that CoopCycle's software has designed to manage incidents in Local Commerce and Last Mile services
3. Explain how to set up personalized incident management on your instance of CoopCycle

By sharing best practices and explaining how we have taken them into account when designing CoopCycle’s incident management system we believe that we can help our federation keep growing and gaining new clients. 

# Best practices

Many readers may have spent time online researching customer service, or may have taken some business class related to the subject. In a typical business context the incentive structure creates a dynamic in which a business values the possible future revenue from a customer no matter how wrong or problematic they may be against the possible cost that this customer will create. This leads businesses to say things like “the customer is always right” no matter how frustrating and emotionally draining this may be for a customer service representative. 

These classes and online guides will also prioritize highly rigid service protocols that dehumanize the process and allow for high levels of business analysis that turn customer service workers into little more than a human robot. 

In the context of a CoopCycle cooperative, we have a different incentives structure. We are messenger-managers and so we must work with our clients day after day. We do not have the money to invest large amounts of time and discounts in customers with the hope to recoup this investment over many years. We likely only want to work with specific types of clients who act within certain political, ecological, and social limits. Additionally, in logistics it is clear to anyone with any amount of experience that some clients are not worth the time. 

With this in mind, here we propose a few key guidelines that take into account our sector, our values, and our vulnerabilities:

## Key tips:

1. **80/20 rule or the Pareto Rule:** [Studies have shown](https://en.wikipedia.org/wiki/Pareto_principle) that 80% of a business’s income and profits generally come from 20% of its most dedicated and motivated customers. Especially in B2C services like food delivery, it is key to identify who these customers are and find ways to keep them happy.
2. **80/20 rule or the Pareto Rule again:** The inverse is also true. 80% of your customer service costs, incidents, problems, and general frustration will likely come from 20% of your customers. In our businesses, unless you have an urgent need for turnover at any cost (you just started), a key factor for success is to find ways to limit the time you invest in these clients and create clear limitations. These relationships are often toxic and should be thought of inside that framework (insert how to deal with toxic relationships link to feminist literature)
3. **Systematize, but humanize:** Making protocols and systems to deal with incidents is an important process to undertake as a business grows. If you have more than one dispatcher, having shared ways of dealing with customers and passing information between shifts will quickly become necessary. However, make sure these systems support human-focused and autonomous decision-making. An example of a robotic systematization would be to only allow dispatchers to cancel orders, never to modify their characteristics in order to reduce problematic and unprofitbale deliveries. An example of a human-focused system would be to have a set of suggested incident resolutions based on different possible situations and to make sure incidents are recorded so that others know they happened, so that others can better judge how to react in future situations and have a guide while making these subjective decisions.
4. **Be where your customer is:** Remember that you are not your customers, and therefore what you think of as the best ways to interact with customers may not be the complete picture. For example, many cooperatives have artistic members who gravitate towards instagram as their main communication tool, without considering that facebook remains a highly used platform for the middle-aged and older demographic. As members of the social and solidarity economy we often have a wider customer base than other similar businesses, and should identify the ways that these clients look to interact with us. Other than whatsapp and instagram, consider facebook, email, and phone calls as communication tools. Doing a quick survey of your customers is never a bad idea either.
5. **Know how to deal with problems:** This is a basic customer service concept. A customer with a problem will be upset and feel a lack of control. Having a framework or step by step processcan offer a much-needed guide: 
 - Control the situation
 - Acknowledge the error or problem
 - Refocus the conversation towards clear solutions
 - Problem solve

Other [links](https://hiverhq.com/blog/b2c-customer-service) to [guides](https://blog.hubspot.com/service/customer-service) to customer service written by normal business people.

# Design of CoopCycle Incident Management
\
**Goals of the CoopCycle Incident Management System**
1. Allow cooperatives to track all the incidents that occur during service
2. Create specific incident resolution paths that are not overly complex
3. Create specific incident resolution paths that address all use cases
 - We want to charge more for an incident. Ex: customer made a mistake, we need to charge more due to the extra work involved.
 - We want to take away the entire charge of an order. Ex: The customer called just after making the order to cancel, it didn’t require any work on our part, so we don’t mind canceling it and not charging for the service.
 - We want to charge part of the order. Ex: We went to do a pickup but they forgot to prepare the delivery. We want to charge the cost for the pickup but not the dropoff, and we will create a new delivery for tomorrow.
 - We don’t want to change the price, but we need to register the incident in case we need to address the issue in the future. Ex: The client was not at home and we have to deliver to a neighbor with permission from the client.
4. Allow the rescheduling of deliveries without loosing traceability
5. Facilitate effective, efficient, and human-focused management of incidents for both Business to Business clients and Business to Customer customers.
6. Create a simplified process that is accessable and understandable to new dispatchers and administrators. 

In practice, this becomes a flowchart of decisions that represent ations inside the CoopCycle platform that go from the creation of an order to its completion:

![Admin Panel (1)](https://github.com/coopcycle/coopcycle-docs/assets/77277854/e9871050-9df5-4a50-9c2d-7a8a48a3b4a4)

---
## In this workflow there are four possible conclusions to an Order:
\
 <span class="badge badge-success">Completion without incident:</span>  <span> If an order is created, assigned, all of its tasks are completed without incidents, the order is completed. The original price will be charged to the customer with no modifications. <span> 

<span class="badge badge-success">Completion with incidents:</span>  <span> An order is created, assigned, all of its tasks are completed but with an incident that is not critical (the package is delivered, but extra information must be recorded), and the order is completed. The original price will be charged with no modifications. <span> 

<span class="badge badge-warning">Completion with critical incident:</span>  <span> An order is created, assigned, and something has happened that must change the order's price. This can be an increase or a decrease. For example, maybe you arrive and instead of one box, there are two. The incident report will allow the messenger to suggest a change of the package set from one box to two, which will recalculate the price if the price is based on how many boxes. On the other hand, maybe there is one box instead of two. <span> 

<span class="badge badge-warning">Parcial completion:</span>  <span>  An order is created, but for one reason or another, one of the tasks should not be charged. Perhaps you arrive at the pickup and the delivery is for the next day and the customer put in the information wrong. In this case, you may want to charge for the pickup but not the dropoff, since you have gone out to the customer. You can complete the pickup with an incident, and the dispatcher can cancel the dropoff. This will eliminate the price of the elements related to the dropoff task, but keep the price related to the elements of the pickup task. <span>

<span class="badge badge-danger">Cancelation:</span>  <span> An order is created, then cancelled. You can either cancel the order from the Orders Dashboard, or cancel all of the related tasks. In this case, there will be no charge registered in CoopCycle and the price will have a strikethrough in the panel. <span> 

Right now this workflow exists, but all of the management of the incidents must happen outside of the platform on your excels, emails and other communication tools. In the next versions of instances we will be progressing towards the goals outlined about using ticketing systems and preprogramed responses when useful, as well as finishing the development of the feature where an incident changes the price of an order. 

<span class="badge badge-info">IMPORTANT!</span> \
Right now the only incidents do not change the price of a task! Cancelling a task with change the total price of the order by subtracting the price associated with that task, but this is the only current way to modify the price. The feature where incidents modify the price of a task will be in Incidents V.2

# Setting up CoopCycle Incident Management with current version

## The Situation Right Now
**Currently we have finished [CoopCycle Incident Management V.1](https://github.com/coopcycle/coopcycle/issues/9)  which includes the following features:**
1. A messenger can flag an incident for a pickup or dropoff task and add a photo and comments to explain the situation.
2. A last mile provider can automatically recieve incidents related to their packages based on the incidents that they have configured in their system.
3. A dispatcher can reschedule a task after an incident has been created.
4. An administrator can create customized sets of incidents that can be associated to specific stores and shops (ex. Food arrived cold would not need to be an incident for a flower shop)
5. Shops can see that incidents have occurred during a delivery in their panel. 



**We are working on Incidents V.2 which will include:**
1. Specific types of incidents will change the price of a shop delivery to reflect the cooperative’s service agreement (ex: if the client has two boxes instead of one, the incident can propose to charge for two instead of one, and a dispatcher can approve this change).
2. A ticket management system to facilitate best practices and information transparency between different dispatchers.
3. Ability to automize certain customer service responses for frequent issues, especially for food tech services. 

## How does Incidents V.1 work?

### Step 1 - Setup
First, an administrator must go to the deliveries page and click on the “[Faliure Reasons](https://demo.coopcycle.org/admin/deliveries/failures)” tab on the left-side menu. Here the different incident rules can be managed and new rules can be created. After creating the appropriate incident rules, these can be associated to a shop or store in their configuration pages. 

<img width="1058" alt="Screenshot 2024-03-01 at 13 49 12" src="https://github.com/coopcycle/coopcycle-docs/assets/77277854/083ce7ed-ddce-4c5d-bf0b-c0417f1560dd">

---

<img width="1057" alt="Screenshot 2024-03-01 at 13 50 09" src="https://github.com/coopcycle/coopcycle-docs/assets/77277854/70f75c04-d157-4a23-8251-cb2515b7da8f">

---

<span class="badge badge-info">Tip!</span> \
Make sure you have used the settings in the Admin Panel to visualize incident-related tasks
<img width="1469" alt="Screenshot 2024-03-02 at 09 57 24" src="https://github.com/coopcycle/coopcycle-docs/assets/77277854/5abf91d9-2700-4608-96dc-26492ecea2c6">

---


**During Service**\
Once this is completed, when a messenger is completing a task they can slide the bar to the right to complete the task without issues, or slide to the left and click the yellow button to complete the task with an incident. They should they take a photo and provide comments if necessary to help the dispatcher or administrator manage the incident with the customer. 

<span class="badge badge-info">Info</span> \
Right now the button is red, it will be yellow next week ;)


**Incident Resolution** \
After this, a dispatcher or administrator can chose three options:
1. Leave the incident as is (ex: the package was delivered, just late) and the incident remains as a register of the problem for future analytics
2. Reschedule the delivery for a future date (ex: client not at home, try again)
3. Cancel the delivery (ex: lost package). This option will make the price for this delivery go to zero, and should only be used when you do not want to charge the client for the service. 

![incident3](https://github.com/coopcycle/coopcycle-docs/assets/77277854/2163ed4f-dae0-494c-a0c0-522c7db04f61)

---
layout: default
title: Stores
parent: Deliveries
nav_order: 1
---

# Stores

<div class="alert mt-3 alert-info" role="alert">
Stores, also known as <em>Backoffice</em>, are accounts without an e-commerce output. They allow businesses to create deliveries and don't handle payments. 
</div>

---

## Create a Store

1. Click on <span class="badge badge-success"> <i class="fa fa-plus"></i> Create a new store</span>
2. Fill in the fields in **General** and **Settings** tabs from the left.
   
   ### General
   #### **Name**
   Type the name of the store.

   #### **Legal name**
   Type the legal name of the store.

   #### **Website**
   Type the website of the store

   #### **Telephone**
   Type the Telephone of the store.

   ### Settings

   #### **Pricing**
   Choose a pricing that corresponds for each Store. As Stores don't handle payments, the Pricing is mostly used for record-keeping and invoicing (the latter is done outside the platform).

   See here on how to [create a pricing](/en/admin/deliveries/pricing/).

   #### **Additional settings**  
<br>
   <div class="shadow p-3 mb-3 mt-n4 bg-white rounded border border-warning">
   <span class="badge badge-warning">IMPORTANT:</span>
   <span> Make sure to check ☑️ the <strong>Create orders</strong> option. This will allow store owners to create orders.</span>
   </div>
   
   - Pre-fill automatically pickup address will fill in the store address each time a store owner creates a delivery.
   - Require input of weight will make the **weight** field mandatory when creating an order.
   - Require input of packages will make the **packages** option mandatory when creating an order.
  
   #### **Time slot**
   Choose a time slot that corresponds for each Store. 

   See here on how to [create a time slot](/en/admin/deliveries/timeslots/).

   #### **Package set**

   Choose a package that corresponds for each Store.

   See here on how to [create a package](/en/admin/deliveries/packages/).
   
   #### **Tags**

   A store tag is different than a task tag. Choosing a tag for a Store will automatically place the tag to both tasks when a delivery is created.

   See here on how to [create a tag](/en/admin/deliveries/tags/).  

1. Click <span class="badge badge-success"> <i class="fa fa-plus"></i> Save</span>
   After saving settings new settings will be visible on the right-hand pane.

   ### Address book

   This settings allows you to add as many addresses as you want and they will be displayed as a dropdown menu when typing in either the Pickup or Dropoff address when creating an order. 

   The system will make the Store address as default. You can change this once you added a second or more addresses.

   ### Users

   This section displays all the users assigned to a Store. 
   
   <!--The button <span class="badge badge-success"> <i class="fa fa-plus"></i> Invite user</span> displays a pop-up that allows you to input an e-mail address and it sends an e-mail inviting the user to register an account on the Instance.-->

   <div class="shadow p-3 mb-3 bg-white rounded border border-danger">
   <span class="badge badge-danger">IN PROGRESS:</span>
   <span> The <span class="badge badge-success"> <i class="fa fa-plus"></i> Invite user</span> feature is a work in progress. Instead, send them the the <em>Register</em> URL and then assign the user to a Store.</span>
   </div>
   

   In the search box you can search for a user and when selecting the desired user it will be assigned to the Store. 

   <div class="shadow p-3 mb-3 bg-white rounded border border-warning">
   <span class="badge badge-warning">IMPORTANT:</span>
   <span> Make sure the selected user has the <strong>Role</strong> <code>Store</code> checked ☑️, otherwise the user doesn't get assigned. After assigning a user you can also check ☑️ the Store role for that user and it will be automatically assigned.</span>
   </div>

   See here on how to <a href="">assign Roles to Users</a>.

   ### Deliveries

   This sections displays all the Past, Upcoming and Current deliveries.

   <p class="shadow-sm p-1 mb-3 bg-white rounded"><a href="/assets/images/deliveryLinkInfo.png/" target="\_blank" rel="noopener noreferrer"><img src="/assets/images/deliveryLinkInfo.png/" alt=""></a></p>

   <span class="badge badge-danger">1</span><span> This is the Delivery number. By clicking on it it will display the Delivery details.</span>

   <span class="badge badge-danger">2</span><span> This is the Store to which the Delivery belongs. By clicking on it it will filter all the deliveries and show only the deliveries of that Store.</span>

   <span class="badge badge-danger">3</span><span> This is the courier that fulfilled the Delivery. By clicking on it it will display the courrier's details.</span>

   <span class="badge badge-danger">4</span><span> This displays the Delivery details.</span>
---
layout: default
title: Invoicing with Odoo
---

# Invoicing with Odoo

# Prerequisites

### 1\. An active account on Odoo Online: [https://www.odoo.com/](https://www.odoo.com/) or a self-hosted Odoo instance

### 2\. `On Demand Delivery` product name on CoopCycle must match product name on Odoo (configurable in [Settings](/en/web/admin/settings)):

<span class="zoomable">![image1](/assets/images/invoicing_16.24.02.png)</span>

### 3\. Account code must match an account used on Odoo (configurable in [Settings](/en/web/admin/settings))

<span class="zoomable">![image2](/assets/images/invoicing_16.24.11.png)</span>

### 4\. Client/Store ‘Legal names’ on CoopCycle must match Customer names on Odoo:

<span class="zoomable">![image3](/assets/images/invoicing_16.24.19.png)</span>

<span class="zoomable">![image4](/assets/images/invoicing_16.24.26.png)</span>

# Preparing data for Invoicing

### 1\. Open [Invoicing page](/en/web/admin/deliveries/invoicing) and select a period to prepare invoices for:

<span class="zoomable">![image5](/assets/images/invoicing_16.57.49.png)</span>

### 2\. Click Refresh to find all clients/stores with orders during the selected period:

<span class="zoomable">![image51](/assets/images/invoicing_16.59.02.png)</span>

### 3\. Click on the "plus" icon to view orders for each client and verify that all data is entered correctly

Make sure that all prices are entered correctly and match the amount you are going to charge a client.   
If something is not correct click on the `View` button next to each order to go to the order details page and modify the data.

<div class="alert mt-3 alert-warning" role="alert">

❗️Avoid modifying the price after the export is done to avoid discrepancies between the Client’s CoopCycle Dashboard or Orders history and the totals on the Invoice.

</div>

<span class="zoomable">![image6](/assets/images/invoicing_16.59.30.png)</span>

### 3\.1\. On the order details page you can:

- Update a Description and/or an original price: click on the `Edit` button:

<span class="zoomable">![image61](/assets/images/invoicing_17.05.08.png)</span>

- Modify a price via an Incident; click on the `Create an incident` button:

<span class="zoomable">![image62](/assets/images/invoicing_17.05.20.png)</span>

<div class="alert mt-3 alert-info" role="alert">

TIP: Use the `Refresh` button to refresh the table after editing instead of a reload page button in the browser

</div>

### 4\. After all orders have been verified select the clients/stores you want to include in the export and click on the `Download` button:

<span class="zoomable">![image7](/assets/images/invoicing_17.20.25.png)</span>

### 5\. Select `Odoo (CSV)` format and click on the `Download` button to download the file on your computer:

<span class="zoomable">![image71](/assets/images/invoicing_17.20.36.png)</span>

<div class="alert mt-3 alert-info" role="alert">

TIP: The orders included in each export will be marked with a file ID. That can be used to track in which file an order was exported. You can also use a filter to see only orders that are not invoiced (not-included in the previous exports).

</div>

<span class="zoomable">![image8](/assets/images/invoicing_17.25.40.png)</span>

<span class="zoomable">![image81](/assets/images/invoicing_17.31.38.png)</span>

<span class="zoomable">![image82](/assets/images/invoicing_17.31.46.png)</span>

# Importing data into Odoo

### 1\. On your Odoo instance go to the Invoicing app and choose `Import records`:

<span class="zoomable">![image10](/assets/images/invoicing_16.24.55.png)</span>

### 2\. Click on `Upload File` and choose a file that you downloaded from CoopCycle

Odoo should process the file and prefill Odoo Fields. Make sure that the fields are the same as on the screenshot and select a field manually if anything is missing  

<span class="zoomable">![image11](/assets/images/invoicing_16.25.02.png)</span>

### 3\. Click on `Test` to validate the file

<span class="zoomable">![image12](/assets/images/invoicing_16.25.14.png)</span>

If you get any error messages most probably (1) a Client/Store/Partner name or (2) a Product name or (3) an Account code do not match between Odoo and CoopCycle.

There are two options to solve it:

1. Modify the data on CoopCycle to match the data on Odoo; see `Prerequisites` section and then repeat the steps from `Prepare data for invoicing` section again.  
   OR
2. Select `Create new values` option; that will create a new Client/Partner or a Product entry on Odoo for each missing value (❗️be careful as it might lead to multiple entries for the same Client on Odoo)  

<span class="zoomable">![image13](/assets/images/invoicing_16.25.31.png)</span>

### 4\. Click `Test` to re-run the validation. When ‘Everything seems valid’ click on `Import`:

<span class="zoomable">![image14](/assets/images/invoicing_16.25.42.png)</span>

### 5\. After the file is uploaded (might take a few minutes depending on the number of orders) you should see a new Invoice draft created in the list of Invoices

<span class="zoomable">![image15](/assets/images/invoicing_16.25.50.png)</span>

6\. Confirm the invoice and send it to a client using your preferred communication method using a standard Odoo workflow

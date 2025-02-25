---
layout: default
title: Configuring Google Maps
has_children: false
---

# Change the map suggestions provider
<div class="alert mt-3 alert-info" role="alert">
On the Settings Page at the bottom section you can choose a different suggestions provider. Different providers work better depending on the region you are in.
</div>

The options are:
- Algolia
- Location IQ
- Geocode.Earth
- Google

## Configuring Google Maps as a suggestions provider

In order to use Google Maps as a suggestions provider, you need to request a Google API Key and enable Billing on it.


### Log into the [Google Console](https://console.cloud.google.com) with a google account.
### Select your country.
### Accept **Terms of Service**
### Click **AGREE AND CONTINUE**.

<p class="shadow-sm p-1 mb-3 bg-white rounded"><a href="/assets/images/google1.png" target="\_blank" rel="noopener noreferrer"><img style="width: 800px" src="/assets/images/google1.png" alt=""></a></p>    

### Click on **Select a project** on the top bar.

<p><a href="/assets/images/google1b.png" target="\_blank" rel="noopener noreferrer"><img class="shadow-sm p-1 mb-3 bg-white rounded" style="width: 800px" src="/assets/images/google1b.png" alt=""></a></p>

### On the pop-up, click on **New Project** on the top right

### Type a **Project name** and click <span class="badge badge-success"> <i class="fa fa-plus"></i> CREATE</span> at the bottom.

<p><a href="/assets/images/google2.png" target="\_blank" rel="noopener noreferrer"><img class="shadow-sm p-1 mb-3 bg-white rounded" style="width: 800px" src="/assets/images/google2.png" alt=""></a></p>

### Go to the Billing settings
<p><a href="/assets/images/google11.png" target="\_blank" rel="noopener noreferrer"><img class="shadow-sm p-1 mb-3 bg-white rounded" style="width: 800px" src="/assets/images/google11.png" alt=""></a></p>

### Select **CREATE BILLING ACCOUNT**
### Enter the required information and agree to the **Google Cloud Platform Free Trial Terms**
### Click <span class="badge badge-success"> <i class="fa fa-plus"></i> CONTINUE</span>.
### Enter your personal information, including bank account 
### A Welcome Message should be displayed
### Click on **Ready**. 
    
This means you have successfully enabled Billing for this google project.

<p><a href="/assets/images/google12.png" target="\_blank" rel="noopener noreferrer"><img class="shadow-sm p-1 mb-3 bg-white rounded" style="width: 800px" src="/assets/images/google12.png" alt=""></a></p>

### Select **API and Services**, then **Library** on the left sidebar.

<p><a href="/assets/images/google3.png" target="\_blank" rel="noopener noreferrer"><img class="shadow-sm p-1 mb-3 bg-white rounded" style="width: 800px" src="/assets/images/google3.png" alt=""></a></p>

### Search for the following 3 settings and **Enable** them:

| Geocoding API                                     | Maps JavaScript API                               | **Places API (New)**                              |
| ------------------------------------------------- | ------------------------------------------------- | ------------------------------------------------- |
|<img style="width: 800px" src="/assets/images/google6.png" alt="">|<img style="width: 800px" src="/assets/images/google7.png" alt="">|<img style="width: 800px" src="/assets/images/google8.png" alt="">|


There is a Places service and Places (New) service you need Places (new)!
 

<div class="shadow p-3 mb-3 bg-white rounded border border-danger">
    <span class="badge badge-danger">IMPORTANT:</span>
    <span> Now you need to <strong>create</strong> the API key.</span>
</div>

### Back on the [https://console.cloud.google.com](https://console.cloud.google.com) settings screen click on **APIs & Services** again
### Select **Credentials** in the left sidebar
### Select **+ CREATE CREDENTIALS** at the top of the screen
### Select the first option: **API Key**.
<p ><a href="/assets/images/google10.png" target="\_blank" rel="noopener noreferrer"><img class="shadow-sm p-1 mb-3 bg-white rounded" style="width: 800px" src="/assets/images/google10.png" alt=""></a></p>

<div class="shadow p-3 mb-3 bg-white rounded border border-danger">
    <span class="badge badge-danger">IMPORTANT:</span>
    <span> An alphanumeric code will de displayed which is the API Key, copy it to the clipboard.</span>
    </div>

Finally, in the CoopCycle platform, the API Key you copied earlier needs to be entered in the **Google API Key** field that is displayed once **Google** is selected as a **Suggestions provider**.

![](/assets/images/google-settings.gif)

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


1. Log into the [Google Console](https://console.cloud.google.com) with a google account.
2. Select your country.
3. Accept **Terms of Service**
4. Click **AGREE AND CONTINUE**.
    <p class="shadow-sm p-1 mb-3 bg-white rounded"><a href="/assets/images/google1.png" target="\_blank" rel="noopener noreferrer"><img style="width: 800px" src="/assets/images/google1.png" alt=""></a></p>

    

5. Go to the navigation menu (☰) on the left-hand side.
6. Scroll down until you see **Google Maps Platform** and hover over it.
7. Choose **Credentials**.
   <p ><a href="/assets/images/google1a.png" target="\_blank" rel="noopener noreferrer"><img class="shadow-sm p-1 mb-3 bg-white rounded" style="width: 800px" src="/assets/images/google1a.png" alt=""></a></p>
8. Click on **Select a project** on the top blue bar.
   <p ><a href="/assets/images/google1b.png" target="\_blank" rel="noopener noreferrer"><img class="shadow-sm p-1 mb-3 bg-white rounded" style="width: 800px" src="/assets/images/google1b.png" alt=""></a></p> 
9. On the pop-up, click on **New Project**
   <p><a href="/assets/images/google1c.png" target="\_blank" rel="noopener noreferrer"><img class="shadow-sm p-1 mb-3 bg-white rounded" style="width: 800px" src="/assets/images/google1c.png" alt=""></a></p>
10. Type a **Project name** and click <span class="badge badge-success"> <i class="fa fa-plus"></i> CREATE</span> at the bottom.
    <p><a href="/assets/images/google2.png" target="\_blank" rel="noopener noreferrer"><img class="shadow-sm p-1 mb-3 bg-white rounded" style="width: 800px" src="/assets/images/google2.png" alt=""></a></p>

11. Go to the navigation menu (☰) again 
12. Select **API and Services**, then **Library**.
    <p ><a href="/assets/images/google3.png" target="\_blank" rel="noopener noreferrer"><img class="shadow-sm p-1 mb-3 bg-white rounded" style="width: 800px" src="/assets/images/google3.png" alt=""></a></p>
13. Search for the following three (3) settings and **Enable** them:

    | Geocoding API                                     | Maps JavaScript API                               | Places API                                        |
    | ------------------------------------------------- | ------------------------------------------------- | ------------------------------------------------- |
    | <a href="/assets/images/google6.png" target="\_blank" rel="noopener noreferrer"><img style="width: 800px" src="/assets/images/google6.png" alt=""></a>|<a href="/assets/images/google7.png" target="\_blank" rel="noopener noreferrer"><img style="width: 800px" src="/assets/images/google7.png" alt=""></a>|<a href="/assets/images/google8.png" target="\_blank" rel="noopener noreferrer"><img style="width: 800px" src="/assets/images/google8.png" alt=""></a>|
 
14. Select **Google Maps Platform**, select **APIs** again and you should see 3 APIs enabled: **Geocoding API**, **Maps JavaScript API** and **Places API**.
    <p><a href="/assets/images/google9.png" target="\_blank" rel="noopener noreferrer"><img class="shadow-sm p-1 mb-3 bg-white rounded" style="width: 800px" src="/assets/images/google9.png" alt=""></a></p>

    <div class="shadow p-3 mb-3 bg-white rounded border border-danger">
    <span class="badge badge-danger">IMPORTANT:</span>
    <span> Now you need to <strong>create</strong> the API key.</span>
    </div>

15. Still on the **Google Maps Platform** settings screen click on **Credentials** again
16. Select **+ CREATE CREDENTIALS** at the top of the screen
17. Select the first option: **API Key**.
    <p ><a href="/assets/images/google10.png" target="\_blank" rel="noopener noreferrer"><img class="shadow-sm p-1 mb-3 bg-white rounded" style="width: 800px" src="/assets/images/google10.png" alt=""></a></p>

    <div class="shadow p-3 mb-3 bg-white rounded border border-danger">
    <span class="badge badge-danger">IMPORTANT:</span>
    <span> An alphanumeric code will de displayed which is the API Key, copy it to the clipboard.</span>
    </div>



18. The last step is to enable **Billing**. 
19. Go to the Billing settings by clicking [here](https://console.cloud.google.com/projectselector2/billing/enable).
20. Choose the project that you have already configured,  
21. Select **CREATE BILLING ACCOUNT** 
    <p><a href="/assets/images/google11.png" target="\_blank" rel="noopener noreferrer"><img class="shadow-sm p-1 mb-3 bg-white rounded" style="width: 800px" src="/assets/images/google11.png" alt=""></a></p>
22. Enter the required information and agree to the **Google Cloud Platform Free Trial Terms**
23. Click <span class="badge badge-success"> <i class="fa fa-plus"></i> CONTINUE</span>.
24. Enter your personal information, including bank account and select the option **Begin Free Trial**. 
25. A Welcome Message should be displayed
26. Click on **Ready**. 
    
This means you have successfully enabled Billing on your Google API Key.

<p><a href="/assets/images/google12.png" target="\_blank" rel="noopener noreferrer"><img class="shadow-sm p-1 mb-3 bg-white rounded" style="width: 800px" src="/assets/images/google12.png" alt=""></a></p>


Finally, the API Key you copied earlier, needs to be entered in the **Google API Key** field that is displayed once **Google** is selected as a **Suggestions provider**.

See the exmaple `.gif` below:

![](/assets/images/google-settings.gif)

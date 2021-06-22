---
layout: default
title: Configuring Google Maps
has_children: false
nav_order: 4
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
    ![](/assets/images/google1.png)

2. Go to the navigation menu (☰) on the left-hand side.
3. Scroll down until you see **Google Maps Platform** and hover over it.
4. Choose **Credentials**.
   ![](/assets/images/2021-06-22-12-31-36.png)
5. Click on **Select a project** on the top blue bar.
   ![](/assets/images/2021-06-22-12-30-19.png) 
6. On the pop-up, click on **New Project**
   ![](/assets/images/2021-06-22-12-33-12.png)
7. Type a **Project name** and click <span class="badge badge-success"> <i class="fa fa-plus"></i> CREATE</span>
![](/assets/images/google2.png)


4. Go to the navigation menu (☰) again 
5. Select **API and Services**, then **Library**.
    ![](/assets/images/google3.png)
5. Search for the following three (3) settings and **Enable** them:
   1. **Geocoding API**
   2. **Maps JavaScript API**
   3. **Places API**
   
        | Geocoding API                    | Maps JavaScript API              | Places API                       |
        | -------------------------------- | -------------------------------- | -------------------------------- |
        | ![](/assets/images/google6.png)| ![](/assets/images/google7.png)| ![](/assets/images/google8.png)|
 
6. Select **Google Maps Platform**, select **APIs** again and you should see 3 APIs enabled: **Geocoding API**, **Maps JavaScript API** and **Places API**.
    ![](/assets/images/google9.png)

    <div class="shadow p-3 mb-5 bg-white rounded border border-danger">
    <span class="badge badge-danger">IMPORTANT:</span>
    <span> Now you need to <strong>create</strong> the API key.</span>
    </div>

7. Still on the **Google Maps Platform** settings screen click on **Credentials** again
8. Select **+ CREATE CREDENTIALS** at the top of the screen
9. Select the first option: **API Key**.
    ![](/assets/images/google10.png)

    <div class="shadow p-3 mb-5 bg-white rounded border border-danger">
    <span class="badge badge-danger">IMPORTANT:</span>
    <span> An alphanumeric code will de displayed which is the API Key, copy it to the clipboard.</span>
    </div>



10. The last step is to enable **Billing**. 
11. Go to the Billing settings by clicking [here](https://console.cloud.google.com/projectselector2/billing/enable).
12. Choose the project that you have already configured,  
13. Select **CREATE BILLING ACCOUNT** 
14. Enter the required information and agree to the **Google Cloud Platform Free Trial Terms**
15. Click <span class="badge badge-success"> <i class="fa fa-plus"></i> CONTINUE</span>.
    ![](/assets/images/google11.png)


16. Enter your personal information, including bank account and select the option **Begin Free Trial**. 
17. A Welcome Message should be displayed
18. Click on **Ready**. 
    
This means you have successfully enabled Billing on your Google API Key.

![](/assets/images/google12.png)


Finally, the API Key you copied earlier, needs to be entered in the **Google API Key** field that is displayed once **Google** is selected as a **Suggestions provider** 

See the exmaple `.gif` below:

![](/assets/images/google-settings.gif)

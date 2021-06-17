---
layout: default
title: Configuring Google Maps
has_children: false
nav_order: 4
---

#Change the suggestions provider

On the Dashboard, at the bottom section you can choose a different suggestions provider. Different providers work better depending on the region you are.
The options are:
- Algolia
- Location IQ
- Geocode.Earth
- Google Maps

## Configuring Google Maps as suggestions provider

Google
If you want to use Google as a suggestions provider, you need to get a Google Api Key and enable Billing on it.


1. Log into the Google Console with a google account: https://console.cloud.google.com, agree to ther terms and services to continue.
![](/assets/images/google1.png)


2. Go to the navigation menu (☰), choose the option Google Maps Platform, then  Credentials.


3. Create a New Project. In the next screen, click on New Project, name it and create it.
![](/assets/images/google2.png)


4. In the next screen, select on the menu API and Services, then Library.
![](/assets/images/google3.png)

5. You should see a grid with the different APIs available, select “Geocoding API” and enable it.
![](/assets/images/google6.png)


6. You should also select and enable “Maps JavaScript API” and “Places API”.
![](/assets/images/google7.png)

![](/assets/images/google8.png)


7. After this, you should have 3 APIs  enabled: “Geocoding API”, “Maps JavaScript API” and “Places API”.
![](/assets/images/google9.png)


8. Then you need to create the API key. Click on Credentials again, and select “+ Create Credentials” on the top of the screen,  and select the first option: “Create API Key ”.

![](/assets/images/google10.png)


9. You will obtain an alphanumeric code which is the API Key, copy it to the clipboard.


10. The last step is to enable Billing. First, go to the next link: https://console.cloud.google.com/projectselector2/billing/enable
Choose the project which you have already configured,  select “Create Billing Account”, then enter your data and agree to the “Google Cloud Platform Free Trial Terms”, click on Continue.
![](/assets/images/google11.png)


Enter your personal information, including bank account and select the option “Begin Free Trial”, you should get a Welcome Message, click on Ready, this means you have successfully enabled Billing on your Google API Key.

![](/assets/images/google12.png)


11. Finally, after having the API Key, you should enter it on the filed “Google API Key”, the process is shown in the following GIF:

![](/assets/images/google-settings.gif)

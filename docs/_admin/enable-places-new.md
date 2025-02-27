---
layout: default
title: Enable Places (New)
has_children: false
---

This document describes how to enable the new places API for existing google accounts.

### Activate Google places (new) for your google project

- Go to [https://console.cloud.google.com/welcome](https://console.cloud.google.com/welcome) (this exact URL)
- Click "API and services"
- click "enable APIs and services"
- in the search field write "place" and select "places API (new)"
- click on the big "ENABLE" button

### Activate google places api new for your API key

- Go to [https://console.cloud.google.com/welcome](https://console.cloud.google.com/welcome) (this exact URL)
- Click "API and services"
- On the left click "credentials"
- In API keys list select the API key you are using for CoopCycle
- **In API restrictions section either** :
    * select "don't restrict key"
OR
    * select "restict key" + in the selected APIs add "Places API (New)"

<img style="width: 800px" src="/assets/images/google-key-restrictions.png" alt="">
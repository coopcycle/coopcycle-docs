---
layout: default
title: Enable Places (New)
has_children: false
---

This document describes how to enable the new places API for existing google accounts.

1. Activate Google places (new) for your google project

- Go to https://console.cloud.google.com
- Click "API and services"
- click "enable APIs and services"
- in the search field write "place" and select "places API (new)"
- click on the big "activate" button

2. Activate google places api new for your API key

- Go to https://console.cloud.google.com
- Click "API and services"
- On the left click "credentials"
- In API keys list slect the API key you are using for CoopCycle
- In API restrictions section either :
    * select "don't restrict key"
    * select "restict key" + in the selected APIs add "Places API (New)"
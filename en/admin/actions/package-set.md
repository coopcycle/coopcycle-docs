---
title: Package Sets
lang: en
ref: packages-set
parent: Logistics
grand_parent: Admin's guide
nav_order: 4
---

**Package Sets** allow to configure different units of volume when stores create orders.

It is useful to diffenciate the price depending on the type of packages.

In the end, a **package** will translate in the creation of orders by the stores like in the image below
![Packages Sets](/assets/images/package_order.png)

---

## Configuring Package Set

Depending on the needs of your clients you can create a common package set (defining that small = a defined volume) or create different packages sets (for a flowershop it can depend on the size of bouquets).
To create a Package Set you need to go on the Packages section of the Configuration dropdown.

When creating a Package Set you have to create different Packages associated to units of volume like the image below :
![Packages Sets](/assets/images/package_config.png)

### Creating a pricing rule

Incorporating a Packages to the Pricing Rule is not difficult, you have to determine the price when orders contain at least one type of Package.
You can combine different types of Packages to create the most adequate rule.
Remember that the most specific rules have to be in the top of the hierarchy of rules.
![Packages Sets](/assets/images/package_pricing.png)

### Linking a store to a Package Set
Once you defined your sets and pricings, it's necessary to add the package options to the store.
Just go in the settings of the desired stroe, link it to the correct pricing and toggle the **Require input of packages** option.

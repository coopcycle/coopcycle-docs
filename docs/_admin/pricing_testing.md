---
layout: default
title: Testing
parent: Create a custom pricing

---

# Testing

To try the pricing in action, you can use a pricing debug tool. Open a new delivery page and enable the debug mode by adding the `?debug=true` at the end of the page address.

For example:

```
https://demo.coopcycle.org/admin/stores/97/deliveries/new?debug=true
https://demo.coopcycle.org/admin/stores/97/deliveries/new/beta?debug=true
```

Enter the delivery details and see (1) which pricing rules were evaluated for each point/task and on entire order (with rules that matched displayed in green) and (2) how the final price was calculated based on the matched rules.

<span class="zoomable">![image1](/assets/images/pricing_debug_1.png)</span>

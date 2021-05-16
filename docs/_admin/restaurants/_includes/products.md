
<div class="alert alert-info" role="alert">
Here you can add and modify products. These will show on the homepage of each Business.<br><br>
There are two ways of adding new products:
Using the <span class="badge badge-success"><i class="fa fa-plus"></i> Add</span> button on the top-right corner or by <strong>importing</strong> a <code>.csv</code> file using the <span class="badge badge-success"><i class="fa fa-upload"></i> Import</span> button.
</div>

---
### Using the <span class="badge badge-success"><i class="fa fa-plus"></i> Add</span> button

<div class="alert alert-info" role="alert">
You can add an image for each product after you've filled in the respective fields and saved your settings.
</div>

#### **Name**
Type here the name of the product. E.g.: *Vegan Chicken Bowl*

---

#### **Description**
Type here the description of the product, especially listing the ingredients and the type of dish.  
<span class="badge badge-primary">TIP:</span><span> It's recommended to <strong>not</strong> write in the Description the <strong>allergens</strong> or <strong>restricted diets</strong> of the product, there are dedicated sections for those options.</span>

---
#### **Enabled**
By ticking the checkbox ☑️ the product will be visible and available for purchase.  
By unticking the checkbox ⬜️ the product will still be visible yet it will be greyed out and unavailable for purchase.  
<span class="badge badge-primary">TIP:</span><span> In order to remove a product completely from being visible on the Restaurant homepage, please see these docs (COMING SOON).</span> 

---
#### **Price (tax excl.)**
Type here the price of the product excluding the tax.  
E.g.: £8 

---
#### **Price (tax incl.)**
Type here the price of the product including the tax.
E.g.: £10 (tax for this product is 20%)

<span class="badge badge-primary">TIP:</span><span> Both Price fields will be filled in automatically disregarding what field you fill in first. Once you select the tax category from the Tax dropdown option, the Price (tax excl.) field will be automatically calculated from the number in the Price (tax incl.) field.</span>  

Below are a few exmaples of how this works.  

**Selected Tax is 20%**

| Price (tax excl.) | Price (tax incl.) |  Taxes  |
| :---------------: | :---------------: | :-----: |
|         2         |        2.4        | Tax 20% |

**Selected Tax is 0% or tax exempt**

| Price (tax excl.) | Price (tax incl.) | Taxes  |
| :---------------: | :---------------: | :----: |
|         2         |         2         | Tax 0% |

**Both price fields with the same value but without having selected a Tax category**  

| Price (tax excl.) | Price (tax incl.) |         Taxes         |
| :---------------: | :---------------: | :-------------------: |
|         2         |         2         | Select a tax category |

**After having selected a Tax category, the Price (tax excl.) field will change accordingly.**  

| Price (tax excl.) | Price (tax incl.) |  Taxes  |
| :---------------: | :---------------: | :-----: |
|       1.67        |         2         | Tax 20% |

---
#### **Taxes**
Here you can select the tax category corresponding to each product. These tax categories are configured according to your country.  

<span class="badge badge-info">INFO:</span><span> If the tax categories are different or change for your country please contact the developer [here](mailto:dev@cooopcycle.org).</span>

---

#### **Options**
Here you will see the Options or Extras that you can append to each product. Before being able to select options for each product you need to create new Options. To learn how to do that go [here](#-options).

Under Options you should see the newly created Option called `Sauces`.
By checking ☑️ the box next to the name it will make it visible to Customers. When a Customer clicks on the product which has an Option appended to it, this option will be displayed in a pop-up where the Customer can choose between the different sauces.

<span class="badge badge-primary">TIP:</span><span> You can create multiple Options, and you can append any combination you want under one Product.</span>

<span class="badge badge-info">INFO:</span><span> All Options will show for every Product, so make sure you name the Options such that you know which to select for which Product.</span>

---
#### **Allergens**
Here you can select multiple allergens to be found in the overall Product (including the Options).  
<span class="badge badge-info">INFO:</span><span> The selected allergens will show under the description of the product after the exclamation mark symbol <i class="fa fa-warning"></i>.</span>

---
#### **Restricted diets**
Here you can select multiple diets that fit the overall Product (including the Options).  
<span class="badge badge-info">INFO:</span><span> The selected diets will show under <strong>allergens</strong> after a checkmark symbol <i class="fa fa-check"></i>.</span>

Remember to click <span class="badge badge-primary">Save</span> when you finished setting up the product.

After clicking Save you will be taken to the Product page list, assuming this is the first product you created you will only see one product on that page. 
It is not mandatory to add a photograph of the product. If you need to do so, click on the <span class="badge badge-light"><i class="fa fa-pencil"></i> Edit</span> button.

---
### Adding a photo to a product

On the left-hand side of the Product name and description you will see a camera icon <i class="fa fa-camera" aria-hidden="true"></i>.
1. Click on the camera icon
2. There will be two buttons at the top
   1. <i class="fa fa-picture-o" aria-hidden="true"></i> **Gallery**
   Gallery is where you can view or delete the pictures you uploaded. These pictures will be visible to the Customer.
   2. <i class="fa fa-upload"></i> **Upload**
   Under Upload you can Drag & Drop one picture at a time or you can click in the blank area and you can select a picture from your device. 
   On the left-hand side you can select the crop proprtions you want to crop the picture in. You can make both 1:1 and 16:9 crops from one picture and Upload them to the Gallery.  

      <span class="badge badge-warning">IMPORTANT:</span><span> <strong>Gallery</strong> and <strong>Upload</strong> sections are still <em>Work in Progress</em>, so it's recommended to not use the 16:9 crop and make sure to upload last the picture you want at the front of each Product on the homepage of the Restaurant.</span>

---
## Using the <span class="badge badge-success"><i class="fa fa-upload"></i> Import</span> button

By clicking on the <span class="badge badge-success"><i class="fa fa-upload"></i> Import</span> button you can upload a spreadsheet in the `.csv` file previously created on your device and you can download an example spreadsheet on how to populate your products `.csv` file.

<div class="shadow p-3 mb-5 bg-white rounded border border-info"><span class="badge badge-info">INFO:</span><span> Because tax categories are different with each country, the example spreadsheet is different on the Platform for each country.</span></div>

<div class="shadow p-3 mb-5 bg-white rounded border border-warning">
<span class="badge badge-warning">IMPORTANT:</span> The content highlighted in <kbd>black</kbd> has to stay exactly the same in the <code>.csv</code> file. The same applies for all the other tax wordings.
<ul>
<li>Make sure the price includes the correspoding tax</li>
<li>Price is translated this way: <code>150</code> → <code>1.50</code> and <code>2500</code> → <code>25.00</code></li>
</ul>
</div>

Below you can find an example as well:

**Sample spreadsheet:**
This spreadsheet only shows general examples of tax category. Below this example you will find a table with **every** the tax wording for each tax category. 

| <kbd>name</kbd>  | <kbd>description</kbd> | <kbd>price_tax_incl</kbd> | <kbd>tax_category</kbd>                   |
| :--------------- | :--------------------- | ------------------------: | :---------------------------------------- |
| Pizza Margherita | Famous pizza           |            <kbd>500</kbd> | <kbd>tax_category.base_standard</kbd>     |
| Croissant        | French croissant       |            <kbd>300</kbd> | <kbd>tax_category.base_intermediary</kbd> |
| Orange juice     | Fresh orange           |            <kbd>100</kbd> | <kbd>tax_category.base_exempt</kbd>       |

**Tax wording**: The table below is only to reference each tax wording, to understand what tax % it corresponds to. If the tax % has been updated in your country, please contact the developer at `dev [at] coopcycle [dot] org`.

| Tax wording                               | Tax type            | Argentina | Belgium |        Canada BC | France | Germany | Poland | Spain |   UK |
| :---------------------------------------- | ------------------- | --------: | ------: | ---------------: | -----: | ------: | -----: | ----: | ---: |
| <kbd>tax_category.base_standard</kbd>     | Base standard       |       21% |     21% |  GST 5% + PST 7% |    20% |     16% |    23% |   21% |  20% |
| <kbd>tax_category.base_intermediary</kbd> | Base intermediary   |     10.5% |     12% |  GST 5% + PST 0% |    10% |       - |     8% |   10% |   5% |
| <kbd>tax_category.base_reduced</kbd>      | Base reduced        |      2.5% |      6% |               0% |   5.5% |      5% |     5% |    4% |   5% |
| <kbd>tax_category.base_exempt</kbd>       | Base exempt         |        0% |      0% |               0% |     0% |      0% |     0% |    0% |   0% |
|                                           |                     |           |         |                  |        |         |        |       |      |
| <kbd>tax_category.food_takeaway</kbd>     | Takeaway food       |         - |      6% |               0% |    10% |     16% |     8% |   10% |   0% |
| <kbd>tax_category.drink</kbd>             | Beverages           |           |       - |                - |   5.5% |       - |      - |   10% |      |
| <kbd>tax_category.drink_alcohol</kbd>     | Alcoholic beverages |         - |     21% | GST 5% + PST 10% |    20% |     16% |    23% |   21% |  20% |
|                                           |                     |           |         |                  |        |         |        |       |      |
| <kbd>tax_category.service</kbd>           | Services            |       21% |     21% |               5% |    20% |     16% |    23% |   21% |  20% |

After your `.csv` file is ready, click on <span class="badge badge-success"><i class="fa fa-upload"></i> Import</span> and Drag & Drop the file onto the pop-up. Your file will upload and when the pop-up closes by itself you will see the list of uploaded products all enabled. 

<span class="badge badge-warning">IMPORTANT:</span><span> After the products have been uploaded you need to set an **picture**, **options/extras**, **allergens** and **restricted diets** individually for each product.</span>

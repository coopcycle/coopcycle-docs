
<div class="alert alert-info" role="alert">
Here is where you can add and modify products. These will show on the homepage of each Business.<br><br>
There are two ways of adding new products:
Using the <span class="badge badge-success"><i class="fa fa-plus"></i> Add</span> button on the top-right corner or by **importing** a `.csv` file using the <span class="badge badge-success"><i class="fa fa-upload"></i> Import</span> button.
</div>

### Using the <span class="badge badge-success"><i class="fa fa-plus"></i> Add</span> button

<div class="alert alert-info" role="alert">
You can add an image for each product after you've filled in the respective fields and saved your settings.
</div>

#### Name
Type here the name of the product. E.g.: *Vegan Chicken Bowl*

#### Description
Type here the description of the product, especially listing the ingredients and the type of dish.  
<span class="badge badge-primary">TIP:</span><span> It's recommended to <strong>not</strong> write in the Description the <kbd>allergens</kbd> or <kbd>restricted diets</kbd> of the product, there are dedicated sections for those options.</span>

#### Enabled
By ticking the checkbox ☑️ the product will be visible and available for purchase.  
By unticking the checkbox ⬜️ the product will still be visible yet it will be greyed out and unavailable for purchase.  
<span class="badge badge-primary">TIP:</span><span> In order to remove a product completely from being visible on the Restaurant homepage, please see these docs.</span> 

#### Price (tax excl.)
Type here the price of the product excluding the tax.  
E.g.: £8 

#### Price (tax incl.)
Type here the price of the product including the tax.
E.g.: £10 (tax for this product is 20%)

<span class="badge badge-primary">TIP:</span><span> Both Price fields will be filled in automatically disregarding what field you fill in first. Once you select the tax category from the Tax dropdown option, the Price (tax excl.) field will be automatically calculated from the number in the Price (tax incl.) field.</span>  

Below are a few exmaples of how this works.  

**Selected Tax is 20%**

|Price (tax excl.)|Price (tax incl.)|Taxes|
|:-:|:-:|:-:|
|2|2.4|Tax 20%|  

**Selected Tax is 0% or tax exempt**

|Price (tax excl.)|Price (tax incl.)|Taxes|
|:-:|:-:|:-:|
|2|2|Tax 0%|  

**Both price fields with the same value but without having selected a Tax category**  

|Price (tax excl.)|Price (tax incl.)|Taxes|
|:-:|:-:|:-:|
|2|2|Select a tax category|  

**After having selected a Tax category, the Price (tax excl.) field will change accordingly.**  

|Price (tax excl.)|Price (tax incl.)|Taxes|
|:-:|:-:|:-:|
|1.67|2|Tax 20%|  

#### Taxes
Here you can select the tax category corresponding to each product. These tax categories are configured according to your country.  

<span class="badge badge-info">INFO:</span><span> If the tax categories are different or change for your country please contact the developer [here](mailto:dev@cooopcycle.org).</span>

#### Options
Here you will see the Options or Extras that you can append to each product. For setting up Options see the docs [here]().

#### Allergens
Here you can select multiple allergens to be found in the overall Product (including the Options).  
<span class="badge badge-info">INFO:</span><span> The selected allergens will show under the description of the product after the eclamation mark symbol <i class="fa fa-warning"></i>.</span>

#### Restricted diets
Here you can select multiple diets that fit the overall Product (including the Options).  
<span class="badge badge-info">INFO:</span><span> The selected diets will show under <strong>allergens</strong> after a checkmark symbol <i class="fa fa-check"></i>.</span>

Remember to click <span class="badge badge-primary">Save</span> when you finished setting up the product.

After clicking Save you will be taken to the Product page list, assuming this is the first product you created you will only see one product on that page. 
It is not mandatory to add a photograph of the product. If you need to do so, click on the <span class="badge badge-light"><i class="fa fa-pencil"></i> Edit</span> button.

### Adding a photo to a product

On the left-hand side of the Product name and description you will see a camera icon <i class="fa fa-camera" aria-hidden="true"></i>.
1. Click on the camera icon
2. There will be two buttons at the top
   1. <i class="fa fa-picture-o" aria-hidden="true"></i> **Gallery**
   Gallery is where you can view or delete the pictures you uploaded. These pictures will be visible to the Customer.
   2. <i class="fa fa-upload"></i> **Upload**
   Under Upload you can Drag & Drop one picture at a time or you can click in the blank area and you can select a picture from your device. 
   On the left-hand side you can select the crop proprtions you want to crop the picture in. You can make both 1:1 and 16:9 crops from one picture and Upload them to the Gallery.  
   <span class="badge badge-warning">IMPORTANT:</span><span> Gallery and Upload sections are still Work in Progress, so it's recommended to not use the 16:9 crop and make sure to upload last the picture you want at the front of each Product on the homepage of the Restaurant.</span>

How to import products coming soon...


<!---### Using the <span class="badge badge-success">Import</span> button-->

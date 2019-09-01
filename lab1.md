## Table of contents

* TOC
{:toc}

# Introduction

Build a complete web application using visual builder.

# Initial Configuration Wizard

Lets get started by logging into visual builder account and creating a new application. Use your oracle trial account.

## Step 1: Click **New Application**  button to start the application create wizard.

![img](assets/LabGuide100-f9530cdb-20190829225248630.png)

![image2019-8-21_9-6-20.png](assets/image2019-8-21_9-6-20-7144997.png)


## Step 2: Click on change template. Choose the sample component starter template.

![image2019-8-21_19-46-45.png](assets/image2019-8-21_19-46-45-7145013.png)

## Step 3: Choose Sample Component Starter Template

![img](assets/image2019-8-21_9-17-42.png)

## Step 4: Click Finish

![img](assets/image2019-8-21_19-49-33.png)

- You now have a new application, in which you can begin building pages and adding data.
- We will begin by creating a web application

![img](assets/image2019-8-21_19-52-52.png)

## Step 5: Choose navigation template

Upon click on web application, you will now the ability to choose the default web application navigation template. Please choose the one with navigation items.

![img](assets/image2019-8-21_9-20-14.png)

Lets change the labels to

- Products
- Orders
- Reports

## Step 6 : The application is now ready. You are presented with a complete visual development environment.  Click on the "run" icon on the top right hand side to launch the application.

![img](assets/image2019-8-21_19-56-20.png)

Step 7: Clicking on run should launch an additional browser tab with the basic app. It should look something like this

![img](assets/image2019-8-21_19-57-54.png)

# Import Business Data



One of the first step in the project will be to load the business data that the application relies on to get started with the data model. In our case, we are going to load the product categories and product list as a data import into Visual Builder. This will create the necessary business objects, which can then be used in the UI layer.

- Product List CSV : [products.csv](assets/products.csv)

## Step 1 : First click on business objects icon, indicated by number 1 screen shot below.

- Upon clicking on business objects a list of business objects will be displayed. Since this is a new application, there are none.
- Now click on the hamburger icon indicated by number 2 and then click data manager.



![img](assets/image2019-8-21_20-2-25.png)

The data manager should open up at this point. The screen will look something like this.

## Step 2 : Click on Import Business Objects. Choose the following file to load the product data set

- [products.csv](assets/products.csv)

![img](assets/image2019-8-21_20-22-12.png)

Click through the business objects import wizard.

**Step 1 :** 

![img](assets/image2019-8-21_20-23-28.png)

**Step 2:** 

![img](assets/image2019-8-21_20-23-41.png)

**Step 3:** 

![img](assets/image2019-8-21_20-56-23.png)



The business objects with the name Products should now be created. Click on the business object and observe the following sections

![img](assets/image2019-8-21_20-59-19.png)

- Overview : Name , label etc of the business object
- Fields : All the fields of the imported BO.
- Security : Role based security definition for the BO
- Business Rules: This is place one can define the rules
- EndPoints : Rest Endpoints for the BO that were automatically created
- Data : Data Browser to view the data in the BO

------

## Adding List View to Web Application
We will now add a list view to the products page to display the products that we just imported into the application as business object.

## Step 1 : Click on orders in the web application view

![img](assets/image2019-8-22_21-3-55.png)

## Step 2 : Scroll down in the component palette till you locate List View. Drag and drop the list view onto the application canvas.

![img](assets/ListView.gif) 
## Step 3: Click on add data 

![img](assets/image2019-8-22_21-16-18.png)

## Step 4: Choose the business object that we just created

![img](assets/image2019-8-21_21-11-33.png)

![img](assets/image2019-8-21_21-12-27.png)

## Step 5 : Bind variables to the slots in the list view. Add URL to slot one. You can do that by clicking on the checkbox or dragging it into that slot. Since we want this to be displayed an an image, click on image from the drop down as indicated.



![img](assets/image2019-8-22_10-21-21.png)

## Step 6: Choose other fields like product name, price , rating and category. Click through and hit finish.

![img](assets/image2019-8-22_10-23-34.png)



# Styling and Composite Listview

We want to display the image instead of the URL in the list view. So once you are back in visual designer , search for image in the component palette 

## Step1: Drag and Drop image from the component palette into the canvas, right above the URL item. Copy the URL data and bind that to the Source URL under the image as shown in the gif animation below.

Set the image width to 100. URL To : [[ $current.data.url ]]

Delete the Text entry for url, since we don't need that any longer.

Run the page and ensure that it is rendering properly.

![img](assets/IMage_list_view.gif)

Hit run on the top right hand side of the page to view how the page renders after making this change.

![img](assets/image2019-8-22_16-23-3.png)


## Step 2: Changing the rating display to a rating component. 

Instead of displaying the rating as a number, we can use the built in rating gauge component to display it as star rating. In order to do that, drag the rating component from the component and drag it above the rating text field.

![img](assets/rating.gif)

## Step 3: Set data value for rating gauge to [[ $current.data.rating ]]

![img](assets/image2019-8-22_16-27-48.png)

Now the rating should be displayed as star component instead of a number as shown below.

![img](assets/image2019-8-22_16-28-59.png)

## Step 4: We would also like to change the price filed to have a "$" symbol. 

To do that change the value to [[ '$' + $current.data.price ]] as shown below

![img](assets/image2019-8-22_16-30-33.png)



# Adding an edit page to edit the product listing

We would now like to add some screens to allow us to modify/edit the values being displayed in the list. Following are the steps to create an edit page.

## Step 1: Click on the list view and then click on Quick Start Icon

![img](assets/image2019-8-22_16-34-22.png)

## Step 2: Click on Add Edit Page from the options presented

![img](assets/image2019-8-22_16-36-24.png)

## Step 3: Choose Products from the list of BO's presented

![img](assets/image2019-8-22_16-37-38.png)

## Step 4: Choose the fields you want to make editable.

![img](assets/image2019-8-22_16-38-31.png)

Visual builder will automatically build a new page with the required logic and routing to create a seamless editing flow. 

Observe the edit product page that was generated by Visual Builder

![img](assets/image2019-8-22_16-40-23.png)

At this point there are now additional steps. You are ready to edit the contents of the list view. 

There should be a Edit Products Button on top the page. 

![img](assets/image2019-8-22_16-41-19.png)


First click on one of the products to select it and then click on edit products button to reveal the edit products page.

![img](assets/image2019-8-22_16-42-24.png)

Observe that Visual Builder is smart in picking up the appropriate control to display based on the data type. Make some edits and hit save. You should be take back to the products page and the page should get refreshed with the new values.

# Adding a create page to add new products

Now we will add a create products page, which will allow us to add new products to the product listing.

## Step1 : Click on List View and then click on quick start icon

![img](assets/image2019-8-22_16-53-55.png)

## Step 2: Click on add create page



![img](assets/image2019-8-22_16-54-25.png)

## Step 3: Choose products from the list of Business Objects

![img](assets/image2019-8-22_16-55-23.png)

## Step 4: Choose the following fields from the list of values

![img](assets/image2019-8-22_16-56-10.png)

## Step 5: Now run the page and you should see a new button for create product

![img](assets/image2019-8-22_16-57-56.png)

## Step 6: Click on create products to add new products

![img](assets/image2019-8-22_16-59-45.png)

Upon saving you should be taken back to the products listing page. Observe that the product you just added is now visible in the product listing page.

# Adding a delete button

## Step1 : Click on List View and then click on quick start icon

![img](assets/image2019-8-22_16-54-25.png)

## Step 2: Click on delete action

![img](assets/image2019-8-22_20-16-12.png)

## Step 3: Choose Products BO and click finish

You should now see a delete button on the screen. First select a list item and then hit delete to delete the item.

![img](assets/image2019-8-22_20-17-45.png)


# Change the layout of list view 

By default the listview stretches to take the whole width of the screen. We want to reduce the width of the listview to improve the user experience. There are a few options here

- Reduce the width
- Display in a card layout.

Lets get started by reducing the width. 

## Step 1: Set the width of the list view to take 50% of the screen.

Set the class of Flex-Row to "oj-md-6"

![img](assets/image2019-8-23_13-25-52.png)

Now the width of the product list should shrink to 50% of the screen width.


![img](assets/image2019-8-23_13-27-36.png)


Changing the layout to card view

## Step 2: Remove the styling done in step 1 above.

## Step 3: Click on list view and then choose "Card Layout" from property inspector

![img](assets/image2019-8-23_13-29-38.png)

The layout of the list view should change from a vertical layout to a card layout as shown in the screen shot below.

![img](assets/image2019-8-23_13-30-43.png)

Congratulations, you have completed lab 3 [Click here to goto Lab 2](lab2)
---
layout: default
title: "Getting Started with RAMEN"

---

RAMEN is an inventory tracking system developed by [Ontario Institute for Cancer Research](https://oicr.on.ca) for use with MISO LIMS.

For more information, please email [Morgan Taschuk](mailto:morgan.taschuk@oicr.on.ca).

<object data="presentations/RAMENTraining.pdf" width="800" height="500" type='application/pdf'> </object>


# RAMEN Tutorials

Formatting used:

* **bold**: anything clickable - links, buttons, keyboard keys
* _italics_: important text found on the page - titles, headings, field names
* `unformatted`: text or values to type or select

## 1. Logging In

Ensure that you can log into RAMEN. If you are unsure of how to do so, ask your RAMEN
administrator.

## 2. Locations

A location in RAMEN is a place where stock can be stored. Freezers, closets, shelves, and any
other places you would like to record as storage areas for stock may be created as locations in
RAMEN. Products may have a default location, which means that when receiving an order, there is no
need to select a location for stock that is stored in the default location for that product.

### 2.1. Adding New Locations

In this exercise, you will create two new locations.

1. In the navigation menu, click **Locations**. This takes you to the _Locations_ list page showing
   all of the locations already saved in RAMEN
1. Above the table, click **Add New Location**. This takes you to the _Create Location_ page
1. Fill out the location details as follows:
    * _Name_: `XX Freezer`, replacing `XX` with your own initials
    * _Description_: `My -20 freezer`
1. Click **Save** at the bottom of the form
1. Return to the _Locations_ list page. Your new freezer should appear in the list. If you don't
   see it on the first page, enter its name in the _Search_ box above the table to filter the list
1. Add a second location with the following properties:
    * _Name_: `XX Shelf`
    * _Description_: `Shelf by my desk`

## 3. Products

Before stock for a product can be received in an order, information about the product must exist in
RAMEN.

### 3.1. Adding a New Product

In this exercise, we will create two new products.

1. In the navigation menu, click **Products**. This takes you to the _Products_ list page showing
   all of the products already saved in RAMEN
1. Above the table, click **Add New Product**. This takes you to the _Create Product_ page
1. Fill out the product details as follows:
    * _Name_: `XX Kit 1`, replacing `XX` with your own initials
    * _Description_: leave blank
    * _Part Number_: `XX001`, replacing `XX` with your own initials. This will usually come from a
      barcode that can be scanned to identify the product. The same barcode will be located on every
      item of this product type
    * _Vendor_: `OICR`
    * _Version_: leave blank. This would be used if there were multiple versions of the same product
    * _Catalog Number_: leave blank. This is the code used to identify the product when ordering
      from the vendor
    * _Product Category_: `Library Kit`
    * _Storage Temperature_: `-20C`
    * _Warning Level_: `10`. If there are less items in stock than the warning level, this will be
      displayed in the _Low Stock_ section of the home page
    * _Default Storage Location_: `XX Freezer`, replacing `XX` with your own initials
    * _Archived_: leave unchecked
1. Click **Save** at the bottom of the form
1. Return to the _Products_ list page. Your new product should appear in the list. If you don't see
   it on the first page, enter its name in the _Search_ box above the table to filter the list
1. Add a second product with the following properties:
    * _Name_: `XX Kit 2`, replacing `XX` with your own initials
    * _Description_: leave blank
    * _Part Number_: `XX002`, replacing `XX` with your own initials
    * _Vendor_: `OICR`
    * _Version_: leave blank
    * _Catalog Number_: leave blank
    * _Product Category_: `Library Kit`
    * _Storage Temperature_: `-20C`
    * _Warning Level_: leave blank
    * _Default Storage Location_: `XX Freezer`
    * _Archived_: leave unchecked
1. In the navigation menu, click **Home** to get to the home page. Notice that your first kit shows
   up in the _Low Stock_ list. This is because you set a warning level, and there are less than
   that many currently in stock, as you have not yet entered any stock. Your second kit does not
   appear in the _Low Stock_ list because you did not set a warning level for it.

## 4. Orders

To add stock to RAMEN, you must receive an order. The order details include an order number and
date received, and several line items describing the stock received. You can also attach a PDF of
the packing slip.

### 4.1. Receiving an Order

1. In the navigation menu, click **Receive Order**. This takes you to the _Receive Order_ page
1. Enter the following Order information:
    * _Order Number_: `XX0001`, replacing `XX` with your own initials
    * _Date Received_: choose yesterday's date
1. In the table, fill out the first line as follows. Notice that as you use a line, a blank line
   will always be available at the bottom, so you can add as many lines as you need
    * _Part Number_: enter `XX001`, replacing `XX` with your own initials, then press the **Tab** key
      on your keyboard to move to the next cell. When you do, RAMEN will search for the part number
      and make the search results available in the _Product Name_ column
    * _Product Name_: `XX Kit 1` should be selected automatically
    * _Location_: `XX Freezer` should be selected automatically since that is the default storage
      location for this product
    * _LOT Number_: `XX_LOT_1`, replacing `XX` with your own initials. The LOT number identifies
      units of stock that were manufactured in the same batch
    * _Quantity_: `25`
    * _Expiration Date_: select next Friday
    * _Rejected?_: leave unchecked. Stock can be marked as rejected to indicate that it was sent
      back to the vendor, or will not be used. Rejected items are not counted as current stock
    * _Replacement?_: leave unchecked. This is used to indicate whether the stock being received was
      ordered to replace other items that were rejected/returned
    * _Note_: leave blank. This can be used to record any other information about the received items
1. In the second row of the table, enter the _Part Number_: `XX003`, replacing `XX` with your own
   initials
1. Press the **Tab** key to move to the next cell. A message appears saying "Product not found." It
   appears we haven't created this item in RAMEN yet!
1. In the navigation menu, right-click on **Products** and select **Open Link in New Tab**
1. Switch to the new tab and click **Add New Product**
1. Enter the following product information
    * _Name_: `XX Kit 3`, replacing `XX` with your own initials
    * _Description_: leave blank
    * _Part Number_: `XX003`, replacing `XX` with your own initials
    * _Vendor_: `OICR`
    * _Version_: leave blank
    * _Catalog Number_: leave blank
    * _Product Category_: `Library Kit`
    * _Storage Temperature_: `-20C`
    * _Warning Level_: leave blank
    * _Default Storage Location_: leave blank
    * _Archived_: leave unchecked
1. Click **Save** at the bottom of the form
1. Close the tab that you used to create the new product, and return to your original tab where you
   are entering the order
1. In the second row of the table, clear the _Part Number_ field and re-enter `XX003`, replacing
   `XX` with your own initials
1. Press the **Tab** key to move to the next cell. This time, your new product should be found
1. Fill out the rest of the second line as follows
    * _Product Name_: `XX Kit 3` should be selected automatically
    * _Location_: `XX Freezer`. You must select this manually this time, as you did not set a default
      location for the new product
    * _LOT Number_: `XX_LOT_1`, replacing `XX` with your own initials. Note that while this matches
      the LOT number you entered for the first item, it is actually a different LOT because the
      product it is not the same product
    * _Quantity_: `10`
    * _Expiration Date_: select March 4 of next year
    * _Rejected?_: leave unchecked
    * _Replacement?_: leave unchecked
    * _Note_: leave blank
1. At the bottom of the page, click **Save**
1. In the navigation menu, click **Home** to return to the home page
1. Notice that the stock you entered for `XX Kit 1` shows up in the _Expiring Within 30 Days_ list

## 5. Checkouts

When you remove an item from storage for use, you should check it out in RAMEN. This will decrease
its stock, and record who checked it out and when. You can check out stock from the _Stock_ list
page or the _Edit Product_ page.

### 5.1. Checking Out Items from the Stock Page

1. In the navigation menu, click **Stock**. This takes you to the _Stock_ list page showing all of
   the current stock for all products
1. Find the stock for `XX Kit 1`. You can enter the product name or part number in the search box
   to find it quickly if you do not see it
1. In the row for `XX Kit 1`, click the **Checkout** button
1. In the dialog that appears, enter `1` item to be checked out and click **OK**
1. Notice in the list that the _Quantity_ of stock has been reduced by 1
1. In the navigation menu, click **Products**. This takes you to the _Products_ list page
1. Find `XX Kit 1` in the list and click its _Name_. This takes you to the _Edit Product_ page
1. Scroll down to the _Checkouts_ section to see the record of your checkout

### 5.2. Checking Out Items from the Edit Product Page

1. In the navigation menu, click **Products**. This takes you to the _Products_ list page
1. Find `XX Kit 3` in the list and click its _Name_. This takes you to the _Edit Product_ page
1. There should only be one row in the _Current Stock_ list. Click the **Checkout** button in the
   list.
1. In the dialog that appears, enter `2` items to be checked out and click **OK**
1. Notice in the _Current Stock_ list that the _Quantity_ of stock has been reduced by 2
1. Scroll down to the _Checkouts_ section to see the record of your checkout
1. In the navigation menu, click **Checkouts**. This takes you to the _Checkouts_ list page, which
   shows all checkouts for all products and all users
1. Find your checkouts in the list. If you don't see them, you can enter your name in the _Search_
   box to filter the table


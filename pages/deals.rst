=====
Deals
=====

Create new deal in back-end
---------------------------

To create a new deal in your Joomla!'s back-end as an administrator, you go to Components -> CM Live Deal to access CM Live Deal component.

.. image:: ../images/com_cmlivedeal_menu.jpg

On the toolbar, you click "Deals" item to access the list of deals.

.. image:: ../images/com_cmlivedeal_dashboard.jpg

Click "New" button on the toolbar to create a new deal.

.. image:: ../images/deal_backend_list.jpg

The form to create/edit deal looks like the screenshot below.

.. image:: ../images/deal_backend_form.jpg

You need to enter your deal's details: name, description, fine print, starting date and ending date. You also need to select a merchant and a category for your deal.

To assign an image to your deal, you click "Select" button to open image popup. Before selecting/uploading a new image, you must select a merchant first, this merchant will be the owner of any image you upload while you are creating/modifying the deal, unless you select a different merchant. You can only assign 1 image to a deal.

If you enable "Prices and discount input" option in the component's configuration, "Discount info" is displayed in the form, there are 3 types of discount info available:

* Original price and discounted price. For example: original price was $50 but now discounted price is $30.
* Fixed discount value. For example: $10 discount for orders over $50.
* Fixed discount percent. For example: 10% discount for orders over $50.

If deal has a discount method which is not fit to these 3 discount types, you can select "None" option. Original price, discounted price can be displayed in deal list and deal popup. Fixed discount value and fixed discount percent can be dispayed in deal list.

If you want to publish the deal, you need to set "Status" to "Published" and "Approval" to "Yes". However the deal is visible to users or not also depends on starting and ending time.

"Approval" is for marking that if administrator has already reviewed and approved the deal which is submitted by merchant in front-end. When deal is approved, merchant can't change deal details any more, he/she only can modify starting and ending date.

If you enable "Limit coupon quantity" in the component's configuration, "Coupon quantity" field is displayed in the form. You can enter the quantity of coupons that you allow customers to capture, if you want unlimited quantity, you can enter 0.

Other fields in the form:

* **Meta description**: Meta description for SEO. Only administrator can see this field in back-end.
* **Meta keywords**: Meta keywords for SEO. Only administrator can see this field in back-end.
* **Impressions**: The number of times this deal is displayed in deal list.
* **Clicks**: The number of times users click this deal to view its detail.
* **Created Date**: The date the deal is created.
* **Created by**: The person who creates the deal.
* **Modified Date**: The date the deal is modified the last time.
* **Modified by**: The person who does the last modification.
* **ID**: The ID of the deal.

After saving the deal, it is displayed in your deal list.

.. image:: ../images/deal_backend_list_saved.jpg

Create new deal in front-end
----------------------------

Merchant's deal list
^^^^^^^^^^^^^^^^^^^^

To allow merchants access the list of their deals, you need to create a new menu item for "Deal Management" page.

Create a new menu item, select CM Live Deal -> Deal Management as the menu item type.

.. image:: ../images/deal_frontend_menu.jpg

In your front-end, login as a merchant and access the new menu item, you can see the list of merchant's deals.

.. image:: ../images/deal_frontend_merchant_list.jpg

The list has 8 columns:

* **Title**: Displays deal name and the name of the category which the deal is in.
* **Impressions**: How many times the deal is showed in deal list to users.
* **Clicks**: How many times users click the deal to view its details.
* **Captured**: How many coupons of the deal that users have captured.
* **Redeemed**: The number of redeemed coupons of the deal.
* **Approved**: The deal is approved by administrators or is still in review.
* **Published**: The deal is published.
* **Ending time**: When the deal expires.

Click on deal name to edit the deal. If deal is already approved, merchant can only change starting date, ending date and published status. If the deal is not approved yet, merchant still can modify the deal's details.

Submit new deal
^^^^^^^^^^^^^^^

In deal list, merchant can click "New deal" button to submit a new deal.

The form has the following fields:

* **Title**: The deal's name.
* **Category**: The category which the deal is in.
* **Image**: Merchant can click "Select" button to open a popup and select an uploaded image, merchant can also upload a new image.
* **Discount info**: Similar to the deal submission form in back-end, this option provides 3 types of discount, if the deal has a different discount info you can select "None" option. This field only appear if "Prices and discount input" option is enabled in the component's configuration

  * Original price and discounted price. For example: original price was $50 but now discounted price is $30.
  * Fixed discount value. For example: $10 discount for orders over $50.
  * Fixed discount percent. For example: 10% discount for orders over $50.

* **Description**: The deal's description.
* **Fine print**: The deal's terms and conditions.
* **Coupon quantity**: This field is only visible if "Limit coupon quantity" in the component's configuration is enabled. You can enter the quantity of how many coupon you want customers to get, if you want unlimited quantity you can enter "0".
* **Starting time**: When the deal starts public to users.
* **Ending time**: When the deal expires and is not visible to users any more.
* **Published**: Deal's published status.

.. image:: ../images/deal_frontend_form.jpg

To insert merchant's images into deal's description and deal's fine print, you need to enable the plugin "Button - CMLiveDeal Image".

You will receive message "Item successfully submitted." if deal is saved successfully.

.. image:: ../images/deal_frontend_merchant_list_saved.jpg

Deal Submission page
^^^^^^^^^^^^^^^^^^^^

Instead of accessing Deal Management page and click "New deal" button to create a new deal. You can also create a menu item for "Deal Submission" page and let merchants directly access and create new deal.

Deal list
---------

Deal list is where users browse and find the deals that they are interested in.

In your back-end, you create a new menu item for "Deal List" page. You can check the menu item in front-end, the deal list is similar to the below screenshot.

.. image:: ../images/deal_frontend_list.jpg

Deal detail
-----------

There are 2 styles of deal detail which you can configure in :ref:`ref-configuration-deal` section in Configuration:

* Popup:

.. image:: ../images/deal_detail_popup.jpg

* Separate detail page:

.. image:: ../images/deal_detail_page.jpg

There is a menu item for deal detail page but it is optional. If you create this menu item (as a hidden menu item), its alias will be used for deal detail page. But if this menu item doesn't exist, your deal list's alias will be used instead.

For example, if your deal list's URL is www.yoursite.com/deal-list and you don't create menu item for deal detail page, your deal URL could look like:

www.yoursite.com/deal-list/1-50-off-cocktails-and-2-tacos-at-rocks-lakeview-s-tuesday-specials

But if you create menu item for deal detail page with alias "deal", your deal URL would be

www.yoursite.com/deal/1-50-off-cocktails-and-2-tacos-at-rocks-lakeview-s-tuesday-specials

The benefit of creating a separate menu item for deal detail page is you can assign different modules to detail page or not showing specific modules in deal detail page. By using deal list's menu item, all modules in deal list page will be displayed in deal detail page.
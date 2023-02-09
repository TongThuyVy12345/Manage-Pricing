---
description: Stores and Purchase Experience
---

# Taxes

Original Link: [https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/taxes/taxes.html?lang=en](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/taxes/taxes.html?lang=en)

Default Magento 2 lets store owners set up a tax system to aim at taxing customer groups, products, and specific places.&#x20;

## 6.1. Tax rule  <a href="#6-1-tax-rule" id="6-1-tax-rule"></a>

A tax rule is constituted by product class, customer class, and tax rate.&#x20;

Each customer belongs to a specific customer group and is assigned to a customer class. Each product is also assigned to a product class. The default Magento checks the shopping cart of each customer, then calculate the complete tax based on customer class, product class, and the region (shipping address, billing address).&#x20;

It can be said that the tax rule is created after product class, customer class and tax rate settings are completed.&#x20;

{% hint style="info" %}
When numerous taxes must be defined, you can simplify the process by importing them.
{% endhint %}

ing address, billing address or shipping origin).

When numerous taxes must be defined, you can simplify the process by importing them.

_Tax Rules_

<figure><img src="https://docs.magento.com/user-guide/v2.3/images/images/tax-rules.png" alt=""><figcaption></figcaption></figure>

#### Step 1: Complete the tax rule information

1. On the _Admin_ sidebar, go to **Stores** > _Taxes_ > **Tax Rules**.
2. In the upper-right corner, click Add New Tax Rule.
3. Under _Tax Rule Information_, enter a **Name** for the new rule.
4.  Choose the **Tax Rate** that applies to the rule.

    If you need to edit an existing tax rate, do the following:

    * Hover over the tax rate and click the **Edit**![](https://docs.magento.com/user-guide/v2.3/images/images/btn-edit.png) icon.
    * Update the form as needed and click Save.

    _Tax Rule Information_

    <figure><img src="https://docs.magento.com/user-guide/v2.3/images/images/tax-rule-information.png" alt=""><figcaption></figcaption></figure>
5. To enter tax rates, use either of the following methods:

#### Method 1: Enter tax rates manually

1. Click Add New Tax Rate.
2. Complete the form as needed (see [Tax Zones and Rates](https://docs.magento.com/user-guide/v2.3/tax/tax-zones-rates.html)).
3.  When complete, click Save.

    _New Tax Rate_

    <figure><img src="https://docs.magento.com/user-guide/v2.3/images/images/tax-rate-create-new.png" alt=""><figcaption></figcaption></figure>

#### Method 2: Import tax rates

1. Scroll down to the section at the bottom of the page.
2. To import tax rates, do the following:
   * Click **Choose File** and navigate to the CSV file with the tax rates to be imported.
   * Click **Import Tax Rates**.
3. To export tax rates, click **Export Tax Rates** (see [Import/Export Tax Rates](https://docs.magento.com/user-guide/v2.3/system/data-transfer-tax-rates.html)).

_Import / Export Tax Rates_

<figure><img src="https://docs.magento.com/user-guide/v2.3/images/images/tax-rule-new-import-export.png" alt=""><figcaption></figcaption></figure>

#### Step 2: Complete the additional settings

1. Click **Additional Settings** to open the section.
2. Choose the **Customer Tax Class** to which the rule applies.
   * To edit a customer tax class, click the edit ![](https://docs.magento.com/user-guide/v2.3/images/images/btn-edit.png) icon, update the form as needed, and click Save.
   * To create a new tax class, click Add New Tax Class, complete the form as needed, and click Save.
3. Choose the **Product Tax Class** to which the rule applies.
   * To edit a product tax class, click the edit ![](https://docs.magento.com/user-guide/v2.3/images/images/btn-edit.png) icon, update the form as needed, and click **Save**.
   * To create a new tax class, click Add New Tax Class, complete the form as needed, and click Save.
4.  When more than one tax applies, enter a number to indicate the priority of this tax for **Priority**.

    If two tax rules with the same priority apply, the taxes are added together. If two taxes with different priority settings apply, the taxes are compounded.
5. If you want taxes to be based on the order subtotal, select the **Calculate off Subtotal Only** checkbox.
6.  For **Sort Order**, enter a number to indicate the order of this tax rule when listed with others.

    _Additional Settings_

    <figure><img src="https://docs.magento.com/user-guide/v2.3/images/images/tax-rule-new-additional-settings.png" alt=""><figcaption></figcaption></figure>
7. When complete, click Save Rule.

## 6.2 Tax role and rate

Tax rates generally apply to transactions that take place within a specific geographical area. Use the _Tax Zones and Rates_ tool to specify the tax rate for each geographical area from which you collect and remit taxes. Because each tax zone and rate has a unique identifier, you can have multiple tax rates for a given geographic area (such as places that do not tax food or medicine, but do tax other items).

Store tax is calculated based on the store’s address. The actual customer tax for an order is calculated after the customer completes the order information. Commerce then calculates the tax according to the tax configuration of the store.

![Tax Zones and Rates](https://experienceleague.adobe.com/docs/commerce-admin/assets/tax-zones-rates.png?lang=en)

#### Define a new tax rate <a href="#define-a-new-tax-rate" id="define-a-new-tax-rate"></a>

1. On the _Admin_ sidebar, go to **Stores** > _Taxes_ > **Tax Zones and Rates**.
2. In the upper-right corner, click **Add New Tax Rate**.
3. Enter a **Tax Identifier**.
4.  To apply the tax rate to a single ZIP or postal code, enter the code for **Zip/Post Code**.

    The asterisk wildcard (`*`) can be used to match up to ten characters in the code. For example, `90*` represents all ZIP codes from 90000 through 90999.
5. To apply the tax rate to a range of ZIP or postal codes, do the following:
   *   Select the **Zip/Post is Range** checkbox and define the range by entering the first and last ZIP or postal code for **Range From** and **Range To**.

       ![ZIP/Post is Range](https://experienceleague.adobe.com/docs/commerce-admin/assets/tax-rate-new-zip-post-range.png?lang=en)
   * Choose the **State** where the tax rate applies.
   * Choose the **Country** where the tax rate applies.
   * Enter the **Rate Percent** that is used for the tax rate calculation.
6.  If you have multiple stores, you can set **Tax Titles** for each store view.

    NOTE

    Leave this field empty if you want to use the tax identifier.
7.  When complete, click **Save Rate**.

    ![New Tax Rate](https://experienceleague.adobe.com/docs/commerce-admin/assets/tax-rate-new.png?lang=en)

#### Edit an existing tax rate <a href="#edit-an-existing-tax-rate" id="edit-an-existing-tax-rate"></a>

1. On the _Admin_ sidebar, go to **Stores** > _Taxes_ > **Tax Zones and Rates**.
2.  Find the tax rate in the _Tax Zones and Rates_ grid, and open the record in edit mode.

    If there are many rates in the list, use the [filter controls](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/tools/admin-grid-controls.html?lang=en) to find the rate you need.
3. Make the necessary changes to the **Tax Rate Information**.
4. Update the **Tax Titles** as needed.
5. When complete, click **Save Rate**.

#### Delete tax rate <a href="#delete-tax-rate" id="delete-tax-rate"></a>

1. On the _Admin_ sidebar, go to **Stores** > _Taxes_ > **Tax Zones and Rates**.
2. Find the tax rate to be deleted and open it in edit mode.
3. In the menu bar, click **Delete Rate**.
4. To confirm the action, click **OK**.

## 6.3 Tax configuration settings

### Configure the general tax settings <a href="#configure-the-general-tax-settings" id="configure-the-general-tax-settings"></a>

1. On the _Admin_ sidebar, go to **Stores** > _Settings_ > **Configuration**.
2. For a multisite configuration, set **Store View** to the website and store that is the target of the configuration.
3. In the left panel, expand **Sales** and choose **Tax**.
4.  Complete the following configuration settings.

    If necessary, clear the **Use system value** checkbox of any settings that are dimmed.

* **Tax classes**
* **Calculation Settings**
* #### Default Tax Destination Calculation <a href="#default-tax-destination-calculation" id="default-tax-destination-calculation"></a>
* #### Price Display Settings <a href="#default-tax-destination-calculation" id="default-tax-destination-calculation"></a>
* #### Shopping Cart Display Settings <a href="#default-tax-destination-calculation" id="default-tax-destination-calculation"></a>
* **Orders, Invoices, Credit Memos Display Settings**
*   #### Fixed Product Taxes <a href="#fixed-product-taxes" id="fixed-product-taxes"></a>

    ****

### **1. Tax classes**

1.  Expand ![Expansion selector](https://experienceleague.adobe.com/docs/commerce-admin/assets/icon-display-expand.png?lang=en) the **Tax Classes** section.

    ![Tax Classes](https://experienceleague.adobe.com/docs/commerce-admin/assets/tax-tax-classes.png?lang=en)

    * **Tax Class for Shipping** — Set to the appropriate class. The default classes are: `None` and `Taxable Goods`
    * **Tax Class for Gift Options** — ![Adobe Commerce](https://experienceleague.adobe.com/docs/commerce-admin/assets/adobe-logo.svg?lang=en) (Adobe Commerce only) Set to the appropriate class. The default classes are: `None` and `Taxable Goods`
    * **Default Tax Class for Product** — Set to the appropriate class. The default classes are: `None` and `Taxable Goods`
    * **Default Tax Class for Customer** — Set to the appropriate class. The default class is: `Retail Customer` and `Wholesale Customer`
2. When complete, click **Save Config**.

### 2. Calculation Settings

1. Expand ![Expansion selector](https://experienceleague.adobe.com/docs/commerce-admin/assets/icon-display-expand.png?lang=en) the **Default Tax Destination Calculation** section.

#### Default Tax Destination Calculation <a href="#default-tax-destination-calculation" id="default-tax-destination-calculation"></a>

1.  Expand the **Calculation Settings** section.

    ![Calculation Settings](https://experienceleague.adobe.com/docs/commerce-admin/assets/tax-calculation-settings.png?lang=en)
2. Set **Tax Calculation Method Based On** to one of the following:
   * `Unit Price` - The price of each product
   * `Row Total` - The total of the line item in the order, less discounts
   * `Total` - The order total
3. Set **Tax Calculation Based On** to one of the following:
   * `Shipping Address` - The address where the order is to be shipped
   * `Billing Address` - The billing address of the customer or company
   * `Shipping Origin` - The address that is specified as the [point of origin](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/delivery/shipping-settings.html?lang=en#point-of-origin) for your store
4. Set **Catalog Prices** to `Excluding Tax` or `Including Tax`.
5. Set **Shipping Prices** to `Excluding Tax` or `Including Tax`.
6. Set **Apply Customer Tax** to one of the following to determine whether tax is applied to the original or discounted price: `After Discount` or `Before Discount`
7. Set **Apply Discount on Prices** to one of the following to determine if discounts include or exclude tax: `Excluding Tax` or `Including Tax`
8. Set **Apply Tax On** to `Custom price if available` or `Original price only`.
9.  Set **Enable Cross-Border Trade** to one of the following:

    * `Yes` - Use consistent pricing across different tax rates. If the catalog price includes tax, choose this setting to fix the price regardless of the customer’s tax rate.
    * `No` - Vary the price by tax rate.

    IMPORTANT

    If cross-border trade is enabled, the profit margin changes by tax rate. Profit is determined by the formula (`Revenue - CustomerVAT - CostOfGoodsSold`). To enable cross-border trade, prices must be set to include tax.

### &#x20;

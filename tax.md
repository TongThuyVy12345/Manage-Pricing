# Tax

## 1. Tax Zones and Rate

Tax rates generally apply to transactions that take place within a specific geographical area. Use the _Tax Zones and Rates_ tool to specify the tax rate for each geographical area from which you collect and remit taxes. Because each tax zone and rate has a unique identifier, you can have multiple tax rates for a given geographic area (such as places that do not tax food or medicine, but do tax other items).

Store tax is calculated based on the store’s address. The actual customer tax for an order is calculated after the customer completes the order information. Commerce then calculates the tax according to the tax configuration of the store.

![Tax Zones and Rates](https://experienceleague.adobe.com/docs/commerce-admin/assets/tax-zones-rates.png?lang=en)

### Define a new tax rate <a href="#define-a-new-tax-rate" id="define-a-new-tax-rate"></a>

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
7. When complete, click **Save Rate**.

![New Tax Rate](https://experienceleague.adobe.com/docs/commerce-admin/assets/tax-rate-new.png?lang=en)

### Edit an existing tax rate <a href="#edit-an-existing-tax-rate" id="edit-an-existing-tax-rate"></a>

1. On the _Admin_ sidebar, go to **Stores** > _Taxes_ > **Tax Zones and Rates**.
2.  Find the tax rate in the _Tax Zones and Rates_ grid, and open the record in edit mode.

    If there are many rates in the list, use the filter controls to find the rate you need.
3. Make the necessary changes to the **Tax Rate Information**.
4. Update the **Tax Titles** as needed.
5. When complete, click **Save Rate**.

## 2. Tax Rule

A tax rule is constituted by product class, customer class, and tax rate.&#x20;

Each customer belongs to a specific customer group and is assigned to a customer class. Each product is also assigned to a product class. The default Magento checks the shopping cart of each customer, then calculate the complete tax based on customer class, product class, and the region (shipping address, billing address).&#x20;

It can be said that the tax rule is created after product class, customer class and tax rate settings are completed.&#x20;

{% hint style="info" %}
When numerous taxes must be defined, you can simplify the process by importing them.
{% endhint %}

ing address, billing address or shipping origin).

When numerous taxes must be defined, you can simplify the process by importing them.

<figure><img src="https://docs.magento.com/user-guide/v2.3/images/images/tax-rules.png" alt=""><figcaption><p><em>Tax Rules</em></p></figcaption></figure>

### Step 1: Complete the tax rule information

1. On the _Admin_ sidebar, go to **Stores** > _Taxes_ > **Tax Rules**.
2. In the upper-right corner, click Add New Tax Rule.
3. Under _Tax Rule Information_, enter a **Name** for the new rule.
4.  Choose the **Tax Rate** that applies to the rule.

    If you need to edit an existing tax rate, do the following:

    * Hover over the tax rate and click the **Edit**![](https://docs.magento.com/user-guide/v2.3/images/images/btn-edit.png) icon.
    * Update the form as needed and click Save.

    <figure><img src="https://docs.magento.com/user-guide/v2.3/images/images/tax-rule-information.png" alt=""><figcaption><p><em>Tax Rule Information</em></p></figcaption></figure>
5. To enter tax rates, use either of the following methods:

#### Method 1: Enter tax rates manually

1. Click Add New Tax Rate.
2. Complete the form as needed (see Tax Zones and Rates).
3.  When complete, click Save.

    __

    <figure><img src="https://docs.magento.com/user-guide/v2.3/images/images/tax-rate-create-new.png" alt=""><figcaption><p><em>New Tax Rate</em></p></figcaption></figure>

#### Method 2: Import tax rates

1. Scroll down to the section at the bottom of the page.
2. To import tax rates, do the following:
   * Click **Choose File** and navigate to the CSV file with the tax rates to be imported.
   * Click **Import Tax Rates**.
3. To export tax rates, click **Export Tax Rates** (see Import/Export Tax Rates).

_Import / Export Tax Rates_

<figure><img src="https://docs.magento.com/user-guide/v2.3/images/images/tax-rule-new-import-export.png" alt=""><figcaption></figcaption></figure>

### Step 2: Complete the additional settings

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

## 3. Tax Classes

Tax classes can be assigned to customers, products, and shipping. Magento analyzes the shopping cart of each customer and calculates the appropriate tax according to the class of the customer, the class of the products in the cart, and the region (as determined by the customer’s shipping address, billing address or shipping origin). New tax classes can be created when a [tax rule](tax.md#2.-tax-rule) is defined.

* Customer — You can create as many customer tax classes as you need, and assign them to customer groups. For example, in some jurisdictions, wholesale transactions are not taxed, but retail transactions are. You can associate members of the Wholesale Customer group with the Wholesale tax class.
* [Product ](https://app.gitbook.com/s/kyzqRYpSaLUja91IhXgX/)— Product classes are used in calculations to determine the correct tax rate is applied in the shopping cart. When you create product, it is assigned to a specific tax class. For example, food might not be taxed, or be taxed at a different rate.
* Shipping — If your store charges an additional tax on shipping, you should designate a specific product tax class for shipping. Then in the configuration, specify it as the tax class that is used for shipping.

The tax class that is used for shipping, and the default tax classes for products and customers are set in the Sales configuration.

<figure><img src="https://docs.magento.com/user-guide/v2.3/images/images/config-sales-tax-tax-classes.png" alt=""><figcaption><p><em>Tax Classes</em></p></figcaption></figure>

### Configure tax classes

1. On the _Admin_ sidebar, go to **Stores** > _Settings_ > **Configuration**.
2. In the left panel, expand **Sales** and choose **Tax**.
3. Expand ![](https://docs.magento.com/user-guide/v2.3/images/images/btn-expand.png) the **Tax Classes** section.
4. Choose the tax class for each of the following:
   * **Set Tax Class for Shipping**
   * **Default Tax Class for Product**
   * **Default Tax Class for Customer**
5. When complete, click Save Config.

### Adding New Tax Classes

Tax classes for customers and products can be easily added, and then assigned to individual customers and products, and used in tax rules.

<figure><img src="https://docs.magento.com/user-guide/v2.3/images/images-ee/tax-classes-updated.png" alt=""><figcaption><p><em>New Tax Classes</em></p></figcaption></figure>

### Add a new tax class

1. On the _Admin_ sidebar, go to **Stores** > _Taxes_ > **Tax Rules**.
2. Click **Add New Tax Rule**.
3. Expand ![](https://docs.magento.com/user-guide/v2.3/images/images/btn-expand.png) the **Additional Settings** section.
4.  Under _Customer Tax Class_, click **Add New Tax Class**.

    __

    <figure><img src="https://docs.magento.com/user-guide/v2.3/images/images/tax-class-customer-add-new.png" alt=""><figcaption><p><em>Add New Tax Class</em></p></figcaption></figure>
5.  Enter the **Name** of the new tax class in the text box and click the checkmark to add the new class to the list of available customer tax classes.

    __

    <figure><img src="https://docs.magento.com/user-guide/v2.3/images/images/tax-class-customer-add-new-wholesale.png" alt=""><figcaption><p><em>Wholesale Tax Class</em></p></figcaption></figure>

### Add a new product tax class

1. Under _Product Tax Class_, click **Add New Tax Class**.
2. Enter the **Name** of the new tax class in the text box and click the checkmark to add the new class to the list of available product tax classes.

<figure><img src="https://docs.magento.com/user-guide/v2.3/images/images-ee/tax-class-product-add-new-digital.png" alt=""><figcaption><p><em>Digital Product Tax Class</em><br><em>Adobe Commerce only</em></p></figcaption></figure>

3. When complete, click **Back** in the button bar to return to the _Tax Rules_ grid.


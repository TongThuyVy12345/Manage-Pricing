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

    If there are many rates in the list, use the [filter controls](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/tools/admin-grid-controls.html?lang=en) to find the rate you need.
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

_Tax Rules_

<figure><img src="https://docs.magento.com/user-guide/v2.3/images/images/tax-rules.png" alt=""><figcaption></figcaption></figure>

### Step 1: Complete the tax rule information

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

## 4.Calculation

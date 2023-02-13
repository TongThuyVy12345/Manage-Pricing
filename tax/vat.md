---
description: Taxe
---

# VAT

Original Link: [https://docs.magento.com/user-guide/v2.3/tax/vat.html](https://docs.magento.com/user-guide/v2.3/tax/vat.html)

Value-added tax (VAT) is a type of indirect tax levied on goods and services for value added at every point of production or distribution cycle, starting from raw materials and going all the way to the final retail purchase.

> State-wise VAT laws: Each state has its own VAT laws for proper implementation and levying. Different states apply different VAT rates according to their implied laws.

## Merchant Information <a href="#merchant-information" id="merchant-information"></a>

#### Stores > Configuration > General > General > Store Information

<figure><img src="../.gitbook/assets/image (2).png" alt=""><figcaption><p>Store Information</p></figcaption></figure>

## Customer Information <a href="#customer-information" id="customer-information"></a>

#### ~~Customers > All Customers > Edit~~

### ~~**Addresses**~~

#### Configure > Customers > Customer Configuration > Create New Account Options <a href="#configure--customers--customer-configuration--create-new-account-options" id="configure--customers--customer-configuration--create-new-account-options"></a>

<figure><img src="../.gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure>

|                                                                   |                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| ----------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Show VAT Number on Storefront                                     | Determines if the customer VAT Number field is included in the Address Book that is available in the customer account.                                                                                                                                                                                                                                                                                                                                     |
| Default Value for Disable Automatic Group Changes Based on VAT ID | VAT ID is an internal identifier for the VAT Number of the customer when used in VAT Validation. During [VAT Validation](https://docs.magento.com/user-guide/v2.3/tax/vat-validation.html), Magento confirms that the number matches the [European Commission](https://ec.europa.eu/taxation\_customs/vies/#/vat-validation) database. Customers can be automatically assigned to one of the four default customer groups based on the validation results. |

## &#x20;Example Configuring VAT

### Step 1: Set up customer tax classes <a href="#step-1-set-up-customer-tax-classes" id="step-1-set-up-customer-tax-classes"></a>

1. On the _Admin_ sidebar, go to **Stores** > _Taxes_ > **Tax Zones and Rates**.
2.  Ensure that there is a customer tax class that is appropriate to use with the VAT.

    For this example, ensure that there is a customer tax class named Retail Customer. If Retail Customer does not exist, click Add New and add it.

### Step 2: Set up product tax classes

1. On the _Admin_ sidebar, go to **Stores** > _Taxes_ > **Tax Rules**.
2. Click **Add New Tax Rule**.
3. Expand ![](https://docs.magento.com/user-guide/v2.3/images/images/btn-expand.png) the **Additional Settings** section.
4. Under _Product Tax Class_, click **Add New Tax Class**.
5. Enter the **Name** of the new tax class and click the checkmark to add the new class to the list of available product tax classes and create three new classes:
   * `VAT Standard`
   * `VAT Reduced`
   * `VAT Zero`
6. Click Save Class for each new class that you add.

### Step 3: Set up tax zones and rates

1.  On the _Admin_ sidebar, go to **Stores** > _Taxes_ > **Tax Zones and Rates**.

    For this example you can remove the U.S. tax rates, or leave them as they are.
2.  Click Add New Tax Rate and add new rates as follows:

    **VAT Standard**

    | Tax Identifier:    | VAT Standard   |
    | ------------------ | -------------- |
    | Country and State: | United Kingdom |
    | Rate Percent:      | 20.00          |

    **VAT Reduced**

    | Tax Identifier:    | VAT Reduced    |
    | ------------------ | -------------- |
    | Country and State: | United Kingdom |
    | Rate Percent:      | 5.00           |
3. Click Save Rate for each rate.

### Step 4: Set up tax rules

A tax rule is a combination of a customer tax class, a product tax class, and a tax rate.

1. On the _Admin_ sidebar, go to **Stores** > _Taxes_ > **Tax Rules**.
2. Add new tax rules as follows:

**-------------------------------------------------------------------------------------------------**

**VAT Standard**

| Name:               | VAT Standard      |
| ------------------- | ----------------- |
| Customer Tax Class: | Retail Customer   |
| Product Tax Class:  | VAT Standard      |
| Tax Rate:           | VAT Standard Rate |

**-------------------------------------------------------------------------------------------------**

**Vat Reduced**

| Name:               | VAT Reduced      |
| ------------------- | ---------------- |
| Customer Tax Class: | Retail Customer  |
| Product Tax Class:  | VAT Reduced      |
| Tax Rate:           | VAT Reduced Rate |

3. Click Save Rule for each rate.

### Step 5: Apply tax classes to products

1. On the _Admin_ sidebar, go to **Catalog** > **Manage Products**.
2. Open a product from your catalog in edit mode.
3. On the _General_ page, find the **Tax Class** option and select the **VAT Class** that applies to the product.
4. When complete, click Save.

## VAT ID Validation

* VAT is charged if the merchant and customer are located in the same EU country.
* VAT is not charged if the merchant and customer are located in different EU countries, and both parties are EU-registered business entities.

<figure><img src="../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

## Configuring VAT ID Validation

The following instructions include a sample procedure to set up a 20% VAT in the U.K. for sales to retail customers. For other tax rates and countries, follow the general procedure but enter specific information that corresponds to your country, VAT rate, customer types, and so on.

Before proceeding, make sure to find out which rules and regulations apply to VAT in your area.

In certain business-to-business transactions, VAT is not assessed. Magento can validate a customer’s VAT ID to ensure that VAT is assessed (or not assessed) properly. See [VAT ID Validation](https://docs.magento.com/user-guide/v2.3/tax/vat-validation.html).

### Step 1: Set up customer tax classes

1. On the _Admin_ sidebar, go to **Stores** > _Taxes_ > **Tax Zones and Rates**.
2.  Ensure that there is a customer tax class that is appropriate to use with the VAT.

    For this example, ensure that there is a customer tax class named Retail Customer. If Retail Customer does not exist, click Add New and add it.

### Step 2: Set up product tax classes

1. On the _Admin_ sidebar, go to **Stores** > _Taxes_ > **Tax Rules**.
2. Click **Add New Tax Rule**.
3. Expand ![](https://docs.magento.com/user-guide/v2.3/images/images/btn-expand.png) the **Additional Settings** section.
4. Under _Product Tax Class_, click **Add New Tax Class**.
5. Enter the **Name** of the new tax class and click the checkmark to add the new class to the list of available product tax classes and create three new classes:
   * `VAT Standard`
   * `VAT Reduced`
   * `VAT Zero`
6. Click Save Class for each new class that you add.

### Step 3: Set up tax zones and rates

1.  On the _Admin_ sidebar, go to **Stores** > _Taxes_ > **Tax Zones and Rates**.

    For this example you can remove the U.S. tax rates, or leave them as they are.
2.  Click Add New Tax Rate and add new rates as follows:

    **VAT Standard**

    | Tax Identifier:    | VAT Standard   |
    | ------------------ | -------------- |
    | Country and State: | United Kingdom |
    | Rate Percent:      | 20.00          |

    **VAT Reduced**

    | Tax Identifier:    | VAT Reduced    |
    | ------------------ | -------------- |
    | Country and State: | United Kingdom |
    | Rate Percent:      | 5.00           |
3. Click Save Rate for each rate.

### Step 4: Set up tax rules

A tax rule is a combination of a customer tax class, a product tax class, and a tax rate.

1. On the _Admin_ sidebar, go to **Stores** > _Taxes_ > **Tax Rules**.
2.  Add new tax rules as follows:

    **VAT Standard**

    | Name:               | VAT Standard      |
    | ------------------- | ----------------- |
    | Customer Tax Class: | Retail Customer   |
    | Product Tax Class:  | VAT Standard      |
    | Tax Rate:           | VAT Standard Rate |

    **Vat Reduced**

    | Name:               | VAT Reduced      |
    | ------------------- | ---------------- |
    | Customer Tax Class: | Retail Customer  |
    | Product Tax Class:  | VAT Reduced      |
    | Tax Rate:           | VAT Reduced Rate |
3. Click Save Rule for each rate.

### Step 5: Apply tax classes to products

1. On the _Admin_ sidebar, go to **Catalog** > **Manage Products**.
2. Open a product from your catalog in edit mode.
3. On the _General_ page, find the **Tax Class** option and select the **VAT Class** that applies to the product.
4. When complete, click Save.

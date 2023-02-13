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

## ~~Customer Information~~ <a href="#customer-information" id="customer-information"></a>

#### ~~Customers > All Customers > Edit~~

### ~~**Addresses**~~

#### Configure > Customers > Customer Configuration > Create New Account Options <a href="#configure--customers--customer-configuration--create-new-account-options" id="configure--customers--customer-configuration--create-new-account-options"></a>

<figure><img src="../.gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure>

|                                                                   |                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| ----------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Show VAT Number on Storefront                                     | Determines if the customer VAT Number field is included in the Address Book that is available in the customer account.                                                                                                                                                                                                                                                                                                                                     |
| Default Value for Disable Automatic Group Changes Based on VAT ID | VAT ID is an internal identifier for the VAT Number of the customer when used in VAT Validation. During [VAT Validation](https://docs.magento.com/user-guide/v2.3/tax/vat-validation.html), Magento confirms that the number matches the [European Commission](https://ec.europa.eu/taxation\_customs/vies/#/vat-validation) database. Customers can be automatically assigned to one of the four default customer groups based on the validation results. |

\

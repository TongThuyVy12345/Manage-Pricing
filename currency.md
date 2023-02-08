# Currency

Original Link:[https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/currency/currency-configuration.html?lang=en](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/currency/currency-configuration.html?lang=en)\
[https://experienceleague.adobe.com/docs/commerce-admin/config/general/currency-setup.html?lang=en](https://experienceleague.adobe.com/docs/commerce-admin/config/general/currency-setup.html?lang=en)

## Currency configuration <a href="#currency-configuration" id="currency-configuration"></a>

Before setting up individual currency rates, you must first set the scope of the base currency. It is set to global by default, which applies the base currency setting to the entire store hierarchy. If you have a multisite Adobe Commerce or Magento Open Source installation, you can manage multiple base currencies by setting the scope to the website level.

You also specify the currencies that you accept and which currency you want to use for the display of [prices](https://experienceleague.adobe.com/docs/commerce-admin/catalog/products/pricing/catalog-price-scope.html?lang=en) in your store. In the following diagram, the scope of the base currency is set at the website level, so each website can have a different base currency.

![Currency scope diagram](https://experienceleague.adobe.com/docs/commerce-admin/assets/scope-currency-config.svg?lang=en)

### ON THIS PAGE

* [Step 1: Choose the accepted currencies](currency.md#step-1-3a-choose-the-accepted-currencies)
* [Step 2: Configure the import connection](currency.md#step-2-3a-configure-the-import-connection)
* [Step 3: Configure the scheduled import settings](currency.md#step-3-3a-configure-the-scheduled-import-settings)
* [Step 4: Update the currency rates](currency.md#step-4-3a-update-the-currency-rates)
* [Step 5: Customize currency symbols (optional)](currency.md#step-5-3a-customize-currency-symbols-optional)

#### Step 1: Choose the accepted currencies <a href="#step-1-3a-choose-the-accepted-currencies" id="step-1-3a-choose-the-accepted-currencies"></a>

1. On the _Admin_ sidebar, go to **Stores** > _Settings_ > **Configuration**.
2. In the upper-left corner, set **Scope** to the store view where the configuration applies.
3. In the left panel under _General_, choose **Currency Setup**.
4.  Expand ![Expansion selector](https://experienceleague.adobe.com/docs/commerce-admin/assets/icon-display-expand.png?lang=en) the **Currency Options** section and set the following options:

    * **Base Currency** — Set to the primary currency that you use for online transactions.
    * **Default Display Currency** — Set to the currency that you use to display pricing in the store view.
    *   **Allowed Currencies** — Select all currencies that you accept as payment in the store view. Make sure to also select your primary currency.

        For multiple currencies, hold down the Ctrl key (PC) or the Command key (Mac) and click each option.

    ![General configuration - currency options](https://experienceleague.adobe.com/docs/commerce-admin/assets/currency-setup-currency-options.png?lang=en)

    For a detailed description of each of these configuration settings, see [Currency Options](https://experienceleague.adobe.com/docs/commerce-admin/config/general/currency-setup.html?lang=en) in the _Configuration Reference Guide_.
5.  When prompted to refresh the cache, click _Close_ ( ![Close box](https://experienceleague.adobe.com/docs/commerce-admin/assets/icon-close-x.png?lang=en) in the upper-right corner of the system message.

    You can [refresh the cache](https://experienceleague.adobe.com/docs/commerce-admin/systems/tools/cache-management.html?lang=en) later.
6.  Define the scope of the base currency:

    * In the left panel, expand **Catalog** and choose **Catalog** underneath.
    * Scroll down and expand ![Expansion selector](https://experienceleague.adobe.com/docs/commerce-admin/assets/icon-display-expand.png?lang=en) the **Price** section. (This section only appears if the scope is set as **Store View:** _Default config_.)
    * Set **Catalog Price Scope** to either `Global` or `Website`.

    ![Catalog configuration - price options](https://experienceleague.adobe.com/docs/commerce-admin/assets/catalog-price\_c1.png?lang=en)

#### Step 2: Configure the import connection <a href="#step-2-3a-configure-the-import-connection" id="step-2-3a-configure-the-import-connection"></a>

1. Scroll to the top of the page.
2. In the left panel, expand **General** and choose **Currency Setup**.
3.  Configure your currency service connection:

    There are two service options: _fixer.io_ and _Currency Converter API_

    *   To connect to the [fixer.io service](https://fixer.io/):

        * Expand ![Expansion selector](https://experienceleague.adobe.com/docs/commerce-admin/assets/icon-display-expand.png?lang=en) the **Fixer.io** section.
        * Enter your fixer.io **API key**.
        * For **Connection Timeout in Seconds**, enter the number of seconds of inactivity to allow before the connection times out.

        ![General configuration - currency setup - Fixer.io options](https://experienceleague.adobe.com/docs/commerce-admin/assets/config-general-currency-setup-fixerio.png?lang=en)

    | Field                         | [Scope](https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html?lang=en#scope-settings) | Description                                                                                                                           |
    | ----------------------------- | ----------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------- |
    | API key                       | Global                                                                                                                        | The key used to access the conversion service through your fixer.io account. For more information, see [fixer.io](https://fixer.io/). |
    | Connection Timeout in Seconds | Global                                                                                                                        | Determines the number of seconds of inactivity before a Fixer.io session times out. Default value: `100`                              |

    *   To connect to the Currency Convertor API service:

        * Expand ![Expansion selector](https://experienceleague.adobe.com/docs/commerce-admin/assets/icon-display-expand.png?lang=en) the **Currency Convertor API** section.
        * Enter your Currency Convertor **API key**.
        * For **Connection Timeout in Seconds**, enter the number of seconds of inactivity to allow before the connection times out.

        ![General configuration - currency setup - Currency Converter API options](https://experienceleague.adobe.com/docs/commerce-admin/assets/currency-setup-converter.png?lang=en)

    | Field                         | [Scope](https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html?lang=en#scope-settings) | Description                                                                                                       |
    | ----------------------------- | ----------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------- |
    | API key                       | Global                                                                                                                        | The key used to access the conversion service. For more information, see Currency Convertor API.                  |
    | Connection Timeout in Seconds | Global                                                                                                                        | Determines the number of seconds of inactivity before a Currency Converter session times out. Default value:`100` |

#### Step 3: Configure the scheduled import settings <a href="#step-3-3a-configure-the-scheduled-import-settings" id="step-3-3a-configure-the-scheduled-import-settings"></a>

1.  Continuing with Currency Setup, expand ![Expansion selector](https://experienceleague.adobe.com/docs/commerce-admin/assets/icon-display-expand.png?lang=en) the **Scheduled Import Settings** section.

    ![General configuration - currency scheduled import settings](https://experienceleague.adobe.com/docs/commerce-admin/assets/currency-setup-scheduled-import-settings.png?lang=en)

| Field                 | Scope      | Description                                                                                                                                                    |
| --------------------- | ---------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Enabled               | Store View | Determines if scheduled import is enabled for currency rates. Options: `Yes` / `No`                                                                            |
| Service               | Store View | Specifies the service that provides the data for the scheduled import. Default value is `fixer.io`                                                             |
| Start Time            | Store View | Indicates the start time by hour, minute, and second, based on a 24-hour clock.                                                                                |
| Frequency             | Store View | Determines how often the scheduled import takes place. Options: `Daily` / `Weekly` / `Monthly`                                                                 |
| Error Email Recipient | Store View | Identifies the email address of each person who is notified by email about scheduled import errors. For multiple recipients, separate each entry with a comma. |
| Error Email Sender    | Website    | Identifies the store contact that appears as the sender of the error email notification. Default sender: `General Contact`                                     |
| Error Email Template  | Website    | Specifies the template that is used as the basis of the error email notification. Default template: `Currency Update Warnings`                                 |

2. To automatically update currency rates, set **Enabled** to `Yes`.
3. Set the update options:
   * **Service** — Set to the rate provider. The default value is `Fixer.io`.
   * **Start Time** — Set to the hour, minute, and second that the rates are updated according to the schedule.
   * **Frequency** — To determine how often the rates are updated, set to one of the following:
     * `Daily`
     * `Weekly`
     * `Monthly`
   *   **Error Email Recipient** — Enter the email address of the person who is to receive email notification if an error occurs during the import process.

       To enter multiple email addresses, separate each with a comma.
   * **Error Email Sender** — Set to the store contact that appears as the sender of the error notification.
   * **Error Email Template** — Set to the email template used for the error notification.
4. When complete, click **Save Config**.
5.  When prompted to update the cache, click the **Cache Management** link and refresh the invalid cache.

    ![System message - refresh the invalid cache](https://experienceleague.adobe.com/docs/commerce-admin/assets/msg-cache-management\_c1.png?lang=en)

#### Step 4: Update the currency rates <a href="#step-4-3a-update-the-currency-rates" id="step-4-3a-update-the-currency-rates"></a>

The currency rates must be updated with the current values before they go into effect. Follow the instructions to update the rates manually or to import the rates automatically.

#### Step 5: Customize currency symbols (optional) <a href="#step-5-3a-customize-currency-symbols-optional" id="step-5-3a-customize-currency-symbols-optional"></a>

Manage Currency Symbols gives you the ability to customize the symbol associated with each currency that is accepted as payment in your store.

![Currency symbols](https://experienceleague.adobe.com/docs/commerce-admin/assets/stores-currency-symbols.png?lang=en)

1.  On the _Admin_ sidebar, go to **Stores** > _Currency_ > **Currency Symbols**.

    Each currency that is currently enabled for your store appears in the _Currency_ list.
2. Make the changes that you need to the list:
   * Enter a custom symbol for each currency that you want to use, or select the **Use Standard** checkbox for each currency.
   * To override the default symbol, clear the _Use Standard_ checkbox and enter the symbol that you want to use.

> It is not possible to change the alignment of the currency symbol from left to right.

3. When complete, click **Save Currency Symbols**.
4.  When prompted to update the cache, click the **Cache Management** link and refresh any invalid cache.

    ![System message - refresh the invalid cache](https://experienceleague.adobe.com/docs/commerce-admin/assets/msg-cache-management\_c1.png?lang=en)


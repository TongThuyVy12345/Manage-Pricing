---
description: Data transfer
---

# Import tier prices

## Import tier prices <a href="#import-tier-prices" id="import-tier-prices"></a>

Rather than entering [tier prices](https://experienceleague.adobe.com/docs/commerce-admin/catalog/products/pricing/product-price-tier.html?lang=en) manually for each product, it can be more efficient to [import](https://experienceleague.adobe.com/docs/commerce-admin/systems/data-transfer/import/data-import.html?lang=en) the pricing data. Before you begin, create a sample file of exported tier price data that you can use as a template.

![Example storefront - tiered pricing](https://experienceleague.adobe.com/docs/commerce-admin/assets/storefront-tier-pricing-water-bottle.png?lang=en)

### Step 1: Export the tier price data <a href="#step-1-3a-export-the-tier-price-data" id="step-1-3a-export-the-tier-price-data"></a>

The following example exports tier pricing data for a single product. Then, you can use the exported data as a template for bulk imports of tier price data. To learn more about exporting advanced pricing data, see [Advanced pricing data](https://experienceleague.adobe.com/docs/commerce-admin/systems/data-transfer/data-attributes-product.html?lang=en#advanced-pricing-attributes).

![Product tiered pricing](https://experienceleague.adobe.com/docs/commerce-admin/assets/price-tier-customer-group-discount.png?lang=en)

#### Tier pricing <a href="#tier-pricing" id="tier-pricing"></a>

1. On _Admin_ sidebar, go to **System** > _Data Transfer_ > **Export**.
2. Under _Export Settings_, set **Entity Type** to `Advanced Pricing`.
3. In the **Entity Attributes** grid, scroll down to the SKU attributes and do the following:
   *   For tier prices that are based on a discount percentage, enter the SKU of each product to be exported, separated by a comma.

       ![Data export - product SKUs](https://experienceleague.adobe.com/docs/commerce-admin/assets/price-tier-export-sku.png?lang=en)
   * For tier prices that are based on a fixed amount, enter the SKU of each product.
   * Scroll down and click **Continue**.
4.  Locate the export file at the downloads location for your web browser and open the file.

    ![Example - exported customer group discount tier price data](https://experienceleague.adobe.com/docs/commerce-admin/assets/price-tier-customer-group-discount-export.png?lang=en)

#### Exported tier price data <a href="#exported-tier-price-data" id="exported-tier-price-data"></a>

The following columns are included in the exported data:

* `sku`
* `tier_price_website`
* `tier_price_customer_group`
* `tier_price_qty`
* `tier_price`
* `tier_price_value_type`

You use the exported data as a template for importing tier price data.

### Step 2: Update the data <a href="#step-2-3a-update-the-data" id="step-2-3a-update-the-data"></a>

1.  Update the tier price data for each product, as needed.

    Any products without tier price updates can be deleted from the CSV file. There is no need to reimport products that have not changed.
2. **Save** the updated CSV file.

> The size of an import file cannot be larger than 2 MB.

### Step 3: Import the updated data <a href="#step-3-3a-import-the-updated-data" id="step-3-3a-import-the-updated-data"></a>

1. On _Admin_ sidebar, go to **System** > _Data Transfer_ > **Import**.
2. Under _Import Settings_, set **Entity Type** to `Advanced Pricing`.
3. Set **Import Behavior** to `Add/Update`.
4. Under **File to Import**, click **Choose File** and select the file that you prepared to import from your directory.
5. In the upper-right corner, click **Check Data**.
6.  If the file is valid, click **Import**.

    Otherwise, correct each problem with the data that is listed in the message, and try to import the file again.

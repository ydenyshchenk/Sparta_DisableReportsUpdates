# Sparta_DisableReportsUpdates disables logging product views to `report_viewed_product_index ` table
## WARNINGS:
- It stops updates of 'report_viewed_product_index' tables by disabling observers:
```
<?xml version="1.0"?>
<config xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:noNamespaceSchemaLocation="urn:magento:framework:Event/etc/events.xsd">
    <event name="catalog_product_compare_remove_product">
        <observer name="reports" disabled="true" />
    </event>
    <event name="customer_login">
        <observer name="reports" disabled="true" />
    </event>
    <event name="customer_logout">
        <observer name="reports" disabled="true" />
    </event>
    <event name="catalog_controller_product_view">
        <observer name="reports" disabled="true" />
    </event>
    <event name="sendfriend_product">
        <observer name="reports" disabled="true" />
    </event>
    <event name="catalog_product_compare_add_product">
        <observer name="reports" disabled="true" />
    </event>
    <event name="catalog_product_compare_item_collection_clear">
        <observer name="reports" disabled="true" />
    </event>
    <event name="sales_quote_item_save_before">
        <observer name="reports" disabled="true" />
    </event>
    <event name="wishlist_add_product">
        <observer name="reports" disabled="true" />
    </event>
    <event name="wishlist_share">
        <observer name="reports" disabled="true" />
    </event>
</config>
```
- using *Sparta_DisableReportsUpdates* is on your own risk

## Installation
```
git clone git@github.com:ydenyshchenk/Sparta_DisableReportsUpdates.git app/code/Sparta/DisableReportsUpdates
bin/magento module:enable Sparta_DisableReportsUpdates
bin/magento setup:upgrade
```

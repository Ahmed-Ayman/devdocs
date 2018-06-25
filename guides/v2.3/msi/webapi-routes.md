---
group: msi
version: 2.3
title: WebAPI Routes
github_link: msi/webapi-routes.md

---

Description
A Web API for Source Management is required to allow integration with external services. The Web API provides a set of endpoints that enable Create, Read, Update, and Delete (CRUD) operations on Sources by third parties.

Details
SourceInterface reference

Resource	Request method	Permissions	Payload	Response	Implementation	Description
/V1/inventory/source/:sourceCode	GET	Admin InventoryApi::source		SourceInterface	Magento\InventoryApi\Api\SourceRepositoryInterface::get	Get Single Source by identifier
/V1/inventory/source/search	GET	Admin InventoryApi::source		SourceInterface[]	Magento\InventoryApi\Api\SourceRepositoryInterface::getList	Load Sources filtered by Search Criteria
/V1/inventory/source	POST	Admin InventoryApi::source, InventoryApi::source_edit	SourceInterface	Created source_id	Magento\InventoryApi\Api\SourceRepositoryInterface::save	Create Source
/V1/inventory/source/:sourceCode	PUT	Admin InventoryApi::source	SourceInterface	SourceInterface

```xml
<?xml version="1.0"?>
<!--
/**
 * Copyright © Magento, Inc. All rights reserved.
 * See COPYING.txt for license details.
 */
-->
<routes xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
        xsi:noNamespaceSchemaLocation="urn:magento:module:Magento_Webapi:etc/webapi.xsd">
    <!-- Source -->
    <route url="/V1/inventory/source" method="GET">
        <service class="Magento\InventoryApi\Api\SourceRepositoryInterface" method="getList"/>
        <resources>
            <resource ref="Magento_InventoryApi::source"/>
        </resources>
    </route>
    <route url="/V1/inventory/source/:sourceCode" method="GET">
        <service class="Magento\InventoryApi\Api\SourceRepositoryInterface" method="get"/>
        <resources>
            <resource ref="Magento_InventoryApi::source"/>
        </resources>
    </route>
    <route url="/V1/inventory/source" method="POST">
        <service class="Magento\InventoryApi\Api\SourceRepositoryInterface" method="save"/>
        <resources>
            <resource ref="Magento_InventoryApi::source_edit"/>
        </resources>
    </route>
    <route url="/V1/inventory/source/:sourceCode" method="PUT">
        <service class="Magento\InventoryApi\Api\SourceRepositoryInterface" method="save"/>
        <resources>
            <resource ref="Magento_InventoryApi::source_edit"/>
        </resources>
    </route>
    <route url="/V1/inventory/get-sources-assigned-to-stock-ordered-by-priority/:stockId" method="GET">
        <service class="Magento\InventoryApi\Api\GetSourcesAssignedToStockOrderedByPriorityInterface" method="execute"/>
        <resources>
            <resource ref="Magento_InventoryApi::source"/>
        </resources>
    </route>
    <!-- Stock -->
    <route url="/V1/inventory/stock" method="GET">
        <service class="Magento\InventoryApi\Api\StockRepositoryInterface" method="getList"/>
        <resources>
            <resource ref="Magento_InventoryApi::stock"/>
        </resources>
    </route>
    <route url="/V1/inventory/stock/:stockId" method="GET">
        <service class="Magento\InventoryApi\Api\StockRepositoryInterface" method="get"/>
        <resources>
            <resource ref="Magento_InventoryApi::stock"/>
        </resources>
    </route>
    <route url="/V1/inventory/stock" method="POST">
        <service class="Magento\InventoryApi\Api\StockRepositoryInterface" method="save"/>
        <resources>
            <resource ref="Magento_InventoryApi::stock_edit"/>
        </resources>
    </route>
    <route url="/V1/inventory/stock/:stockId" method="DELETE">
        <service class="Magento\InventoryApi\Api\StockRepositoryInterface" method="deleteById"/>
        <resources>
            <resource ref="Magento_InventoryApi::stock_delete"/>
        </resources>
    </route>
    <route url="/V1/inventory/stock/:stockId" method="PUT">
        <service class="Magento\InventoryApi\Api\StockRepositoryInterface" method="save"/>
        <resources>
            <resource ref="Magento_InventoryApi::stock_edit"/>
        </resources>
    </route>
    <route url="/V1/inventory/stock/:stockId" method="DELETE">
        <service class="Magento\InventoryApi\Api\StockRepositoryInterface" method="deleteById"/>
        <resources>
            <resource ref="Magento_InventoryApi::stock_delete"/>
        </resources>
    </route>
    <!-- StockSourceLink -->
    <route url="/V1/inventory/stock-source-link" method="GET">
        <service class="Magento\InventoryApi\Api\GetStockSourceLinksInterface" method="execute"/>
        <resources>
            <resource ref="Magento_InventoryApi::stock_source_link"/>
        </resources>
    </route>
    <route url="/V1/inventory/stock-source-link" method="POST">
        <service class="Magento\InventoryApi\Api\StockSourceLinksSaveInterface" method="execute"/>
        <resources>
            <resource ref="Magento_InventoryApi::stock_source_link"/>
        </resources>
    </route>
    <route url="/V1/inventory/stock-source-link" method="DELETE">
        <service class="Magento\InventoryApi\Api\StockSourceLinksDeleteInterface" method="execute"/>
        <resources>
            <resource ref="Magento_InventoryApi::stock_source_link"/>
        </resources>
    </route>
    <!-- SourceItem -->
    <route url="/V1/inventory/source-item" method="GET">
        <service class="Magento\InventoryApi\Api\SourceItemRepositoryInterface" method="getList"/>
        <resources>
            <resource ref="Magento_InventoryApi::source"/>
        </resources>
    </route>
    <route url="/V1/inventory/source-item" method="POST">
        <service class="Magento\InventoryApi\Api\SourceItemsSaveInterface" method="execute"/>
        <resources>
            <resource ref="Magento_InventoryApi::source"/>
        </resources>
    </route>
    <route url="/V1/inventory/source-item" method="DELETE">
        <service class="Magento\InventoryApi\Api\SourceItemsDeleteInterface" method="execute"/>
        <resources>
            <resource ref="Magento_InventoryApi::source"/>
        </resources>
    </route>
</routes>

```

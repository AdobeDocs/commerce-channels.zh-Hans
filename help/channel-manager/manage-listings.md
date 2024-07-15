---
title: 管理列表
description: '使用Adobe Commerce和Magento Open Source的渠道管理器管理 [!DNL Commerce] 商店的销售渠道列表。'
feature: Sales Channels, Merchandising, Products
exl-id: 70999552-9ba7-4b10-a8ee-ee99bc4fe837
source-git-commit: 4670e9b25a840f86862c9cadaf9e6d3e70330b7d
workflow-type: tm+mt
source-wordcount: '713'
ht-degree: 0%

---

# 管理列表

通过渠道管理器UI管理[!DNL Walmart Marketplace]销售渠道的产品列表。

单个列表的状态表示产品在[!DNL Channel Manager]工作流中的位置，以便您可以确定后续步骤并解决任何错误。

已连接的销售渠道的![列表页面](assets/listings-dashboard-view.png){width="500" zoomable="yes"}

您可以从“列表”视图中完成以下任务。

* 查看当前列表
* 排序和筛选列表
* 添加产品
* 匹配产品
* 跟踪列表状态
* 查看具有错误状态的列表的错误描述

## 查看产品列表

1. 从管理员转到&#x200B;[!UICONTROL **营销** > **渠道经理**]。

1. 从商店列表中，选择商店条目行中的眼睛图标以打开商店视图。

1. 选择&#x200B;[!UICONTROL **列表**]。

1. 通过选择&#x200B;*列表*&#x200B;表中的任何列标题对&#x200B;*列表*&#x200B;视图进行排序。

1. 通过选择状态计数卡片之一来筛选&#x200B;*列表*&#x200B;视图。

1. 通过选择&#x200B;**刷新产品**，重置排序顺序并删除筛选器。

## 将[!DNL Commerce]产品添加到渠道管理器

通过完成以下任务为[!DNL Walmart Marketplace]渠道创建产品分类：

* [将产品从 [!DNL Commerce] 产品目录添加到 [!DNL Channel Manager]](add-products-to-channel-store.md)

* [映射目录属性](map-catalog-attributes.md#configure-product-attribute-settings)

## 匹配[!DNL Walmart]上的产品

您可以在[!DNL Walmart Marketplace]上使用产品匹配或手动上传新产品的产品列表来创建产品选件。

* **[匹配沃尔玛上的产品](connect-listings-to-marketplace.md)** — 通过更新销售相同产品的现有列表将您的渠道中的产品列表连接到[!DNL Walmart Marketplace]。 匹配条件由渠道的[属性映射配置](map-catalog-attributes.md)确定。

* **[手动上载新清单](connect-listings-to-marketplace.md#upload-new-product-listings)** — 对于与[!DNL Walmart Marketplace]上的现有清单不匹配的产品，请使用[!DNL Walmart]产品类别Excel模板批量上载产品清单。

## 列出控件和列说明

下表描述了[!UICONTROL Listings]可用的控件和列。

[!UICONTROL Listings]**的**&#x200B;控件

| **控件** | **描述** |
|----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Add Products] | 打开[!UICONTROL Admin Product Catalog]页面以选择要添加到您的[!DNL Walmart Marketplace]分类的产品，或更新产品属性以满足沃尔玛商城列表要求。 |
| [!UICONTROL Match products on Walmart] | 选择处于[!UICONTROL Draft]状态的一个或多个产品后，选择[!UICONTROL Match products on Walmart]以检查可添加到现有[!DNL Walmart Marketplace]列表的产品选件。 |
| [!UICONTROL Refresh products] | 使用最新的列表和状态更新显示。 此控件还会将列表视图重置为默认排序顺序，并删除任何筛选器。 |
| [!UICONTROL Filter by *状态*] | 通过选择列表表上方状态卡中的一个，仅显示具有特定状态的列表。 通过选择&#x200B;**[!UICONTROL Refresh products]**&#x200B;删除筛选器。 |
| [!UICONTROL Sort products] | 通过选择任何列标题来更改列表的排序顺序。 |


**列描述**

| **字段** | **描述** |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Product name] | [!DNL Commerce]商店目录中的产品的名称。 |
| [!UICONTROL SKU (Unique ID)] | [!DNL Commerce]目录中分配给产品的SKU。 |
| [!UICONTROL  Quantity] | Adobe Commerce或Magento Open Source中可用的库存数量。 |
| [!UICONTROL Price] | [!DNL Commerce]商店目录中的产品价格。 目录价格更新将同步到渠道管理器，然后发送到[!DNL Walmart Marketplace]，以便列出的项目显示当前价格。 |
| [!UICONTROL Status] | 指示[!DNL Commerce]订单工作流中的当前订单状态。 当您将产品成功添加到[!DNL Channel Manager]以及匹配市场上的产品时，状态会更新。 如果操作失败，列表会显示错误状态。 修复错误后，[!DNL Channel Manager]将重试操作并更新状态。 |
| [!UICONTROL Error Description] | 为状态为`[!DNL Error]`的产品提供其他错误信息。 |

### 关于列表状态

在列表工作区中，“状态”标签显示产品在[!DNL Channel Manager]工作流中的位置，以便您确定后续步骤并解决错误。 清单可以具有以下状态标签：

* **[!UICONTROL Draft]** — 识别尚未[提交到 [!DNL Walmart] 以匹配](connect-listings-to-marketplace.md#match-products)的产品。

* **[!UICONTROL Processing]** — 标识在[!DNL Walmart Marketplace]上提交进行匹配的产品。 在[!DNL Walmart]返回HTTP状态消息以指示匹配是否成功或发生错误之前，产品仍处于&#x200B;*正在处理*&#x200B;状态。 在[!DNL Walmart Marketplace]上完成匹配操作最多可能需要30分钟。

* **[!UICONTROL Match]** — 标识[!DNL Walmart]上成功匹配的产品。

  当产品属性值（例如UPC代码）与现有[!DNL Walmart Marketplace]列表中的UPC值匹配时，就会发生匹配。 当产品匹配时，Commerce产品选件将会添加到现有列表中。

  查看[[!UICONTROL Walmart Marketplace Seller Account Items]](https://seller.walmart.com/items-and-inventory/manage-items)仪表板以查看更新的产品列表并验证产品详细信息、价格和库存数量。

* **[!UICONTROL Match - Match in Stage]** — 标识[!DNL Walmart]上匹配的产品，在[!DNL Walmart Marketplace]存储区上线之前无法连接。 [!DNL Walmart Marketplace]商店上线时，具有此状态的产品会自动连接。

* **[!UICONTROL Error]** — 标识与现有[!DNL Walmart Marketplace]列表不匹配的产品。

* **[!UICONTROL Error description]** — 提供有关列表错误的详细信息。

  解决此错误后，请重新提交产品以进行匹配。 请参阅[产品匹配错误疑难解答](connect-listings-to-marketplace.md#troubleshoot-product-match-errors)。

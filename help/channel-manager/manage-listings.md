---
title: 管理列表
description: 管理 [!DNL Commerce] 与Channel Manager一起存储，用于Adobe Commerce和Magento Open Source。
exl-id: 70999552-9ba7-4b10-a8ee-ee99bc4fe837
source-git-commit: 41a6afec60edbb23492627bd8e80632d3c952caf
workflow-type: tm+mt
source-wordcount: '695'
ht-degree: 0%

---

# 管理列表

从管理连接渠道的产品清单 [!UICONTROL Listings] 在渠道存储视图中。

使用 *[!UICONTROL Listings]* 工作区以管理 [!DNL Commerce] 在沃尔玛市场上出售的产品。 单个列表的状态指示产品在 [!DNL Channel Manager] 工作流，以便您确定后续步骤并解决任何错误。

![连接的销售渠道的列表页面](assets/products-submit-for-matching.png)

## 查看列表

1. 从管理员中，转到 [!UICONTROL **营销** >渠道> **渠道管理器**].

1. 从“渠道商店”列表中，在商店登入行中选择铅笔图标以打开商店视图。

1. 选择 [!UICONTROL **列表**].

## 将商务产品添加到渠道管理器

完成以下任务，为Walmart Marketplace渠道创建产品分类：

* [将产品从您的商务产品目录添加到渠道管理器](add-products-to-connected-channel.md)

* [配置产品匹配](map-product-attributes-for-matching.md#configure-product-attribute-settings)

## 将产品发布到沃尔玛

您可以使用产品匹配或通过手动上传新产品的产品列表，在Walmart Marketplace上创建产品选件。 有关说明，请参阅 [向Walmart Marketplace发布列表](publish-listings-to-marketplace.md) 如以下主题中所述：

* **[在沃尔玛匹配产品](publish-listings-to-marketplace.md)** — 将渠道中的产品清单发布到 [!DNL Walmart Marketplace] 通过更新销售同一产品的现有列表。 匹配条件由 [属性映射配置](map-product-attributes-for-matching.md) 频道。

* **[手动上传新列表](publish-listings-to-marketplace.md#upload-new-product-listings)-** — 对于与Walmart Marketplace上现有列表不匹配的产品，请使用Walmart产品类别Excel模板批量上传产品列表。

## 列出控件和列描述

下表介绍了可用的控件和列 [!UICONTROL Listings].

**控件[!UICONTROL Listings]**

| **控制** | **描述** |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Refresh products] | 更新显示的最新列表和状态。 |
| [!UICONTROL Add Products] | 打开 [!UICONTROL Admin Product Catalog] 页面选择要添加到 [!DNL Walmart Marketplace] 分类，或更新产品属性以满足Walmart Marketplace的列表要求。 |
| [!UICONTROL Match products on Walmart] | 选择一个或多个处于“草稿”状态的产品后，选择“在沃尔玛中匹配产品”以检查可添加到现有产品的产品选件 [!DNL Walmart Marketplace] 列表。 |


**列描述**

| **字段** | **描述** |
|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Product name] | 从 [!DNL Commerce] 存储目录。 |
| [!UICONTROL SKU (Unique ID)] | 用于匹配市场上产品的映射属性。 此字段名称会因为 [!DNL Channel Manager] 列表。 在这种情况下，产品匹配操作将使用 [!DNL Commerce] 目录 [!DNL Walmart Marketplace]  列出的SKU值与 [!DNL Commerce] 产品属性。 |
| [!UICONTROL  Quantity] | Adobe Commerce或Magento Open Source中可用的库存量。 |
| [!UICONTROL Price] | 产品价格 [!DNL Commerce] 存储目录。 目录价格更新将同步到渠道管理器，然后发送到 [!DNL Walmart Marketplace]  让所列项目显示当前价格。 |
| [!UICONTROL Status] | 指示 [!DNL Commerce] 订单工作流。 成功将产品添加到 [!DNL Channel Manager] 以及当您匹配市场上的产品时。 如果操作失败，则列表会显示错误状态。 修正错误后， [!DNL Channel Manager] 重试操作并更新状态。 |


### 关于列表状态

在列表工作区中，状态标签显示产品在 [!DNL Channel Manager] 工作流，以便您确定后续步骤并解决错误。 列表可以具有以下状态标签：

* **[!UICONTROL Draft]** — 标识尚未 [已提交 [!DNL Walmart] 匹配](publish-listings-to-marketplace.md#match-products).

* **[!UICONTROL Processing]** — 标识在 [!DNL Walmart Marketplace]. 产品仍保留在 *处理* 状态，直到 [!DNL Walmart] 返回指示匹配是否成功或是否出错的HTTP状态消息。 在 [!DNL Walmart Marketplace].

* **[!UICONTROL Match]** — 标识成功匹配的产品 [!DNL Walmart].

   例如，当产品属性值 — UPC代码与现有[!DNL Walmart Marketplace] 列表。 当产品匹配时，商务产品选件会添加到沃尔玛的现有列表中。

   检查 [[!UICONTROL Walmart Marketplace Seller Account Items]](https://seller.walmart.com/items-and-inventory/manage-items) 功能板，以审核更新的产品列表并验证产品详细信息、价格和库存数量。


* **[!UICONTROL Error]** — 标识与现有产品不匹配的产品 [!DNL Walmart Marketplace] 列表。 通过将鼠标悬停在 *错误* 状态标签。

   解决错误后，请重新提交产品以进行匹配。 请参阅 [产品匹配错误疑难解答](https://docs.google.com/document/d/1bEbCyVLXJQQsbZvEwetJvZKWQJOKoiw5Ia1uB4Bs4uo/edit#heading=h.sz6eji8z9vzy).

* **[!UICONTROL Error - Match in Stage]** — 标识与 [!DNL Walmart] 在 [!DNL Walmart Marketplace] 存储处于实时状态。 当 [!DNL Walmart Marketplace] 商店上线。

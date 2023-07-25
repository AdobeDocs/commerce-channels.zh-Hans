---
title: 管理列表
description: '''管理销售渠道列表 [!DNL Commerce] 通过Adobe Commerce和Magento Open Source渠道管理器进行存储。'
feature: Sales Channels, Merchandising, Products
exl-id: 70999552-9ba7-4b10-a8ee-ee99bc4fe837
source-git-commit: 4670e9b25a840f86862c9cadaf9e6d3e70330b7d
workflow-type: tm+mt
source-wordcount: '715'
ht-degree: 0%

---

# 管理列表

管理产品列表 [!DNL Walmart Marketplace] 销售渠道（通过渠道管理器UI）。

单个清单的状态表示产品在 [!DNL Channel Manager] 工作流，以便您确定后续步骤并解决任何错误。

![连接的销售渠道的列表页面](assets/listings-dashboard-view.png){width="500" zoomable="yes"}

您可以从“列表”视图中完成以下任务。

* 查看当前列表
* 排序和筛选列表
* 添加产品
* 匹配产品
* 跟踪列表状态
* 查看具有错误状态的列表的错误描述

## 查看产品列表

1. 从管理员转到 [!UICONTROL **营销** > **渠道管理器**].

1. 从“商店”列表中，选择商店条目行中的眼睛图标，以打开商店视图。

1. 选择 [!UICONTROL **列表**].

1. 排序 *列表* 通过选择 *列表* 表格。

1. 筛选 *列表* 通过选择状态计数卡之一进行查看。

1. 通过选择，重置排序顺序并删除筛选器 **刷新产品**.

## 添加 [!DNL Commerce] “产品”到“渠道管理器”

为创建产品分类 [!DNL Walmart Marketplace] 完成以下任务以访问渠道：

* [从添加产品 [!DNL Commerce] 产品目录到 [!DNL Channel Manager]](add-products-to-channel-store.md)

* [映射目录属性](map-catalog-attributes.md#configure-product-attribute-settings)

## 匹配产品日期 [!DNL Walmart]

您可以在上创建产品选件 [!DNL Walmart Marketplace] 使用产品匹配或手动上传新产品的产品列表。

* **[匹配沃尔玛的产品](connect-listings-to-marketplace.md)** — 将产品列表从渠道连接到 [!DNL Walmart Marketplace] 更新销售相同产品的现有列表。 匹配条件由以下条件确定 [属性映射配置](map-catalog-attributes.md) 用于您的频道。

* **[手动上传新列表](connect-listings-to-marketplace.md#upload-new-product-listings)** — 对于与上的现有列表不匹配的产品 [!DNL Walmart Marketplace]，使用 [!DNL Walmart] 用于批量上传产品清单的产品类别Excel模板。

## 列出控件和列说明

下表介绍了可用于的控件和列 [!UICONTROL Listings].

**控件[!UICONTROL Listings]**

| **控制** | **描述** |
|----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Add Products] | 打开 [!UICONTROL Admin Product Catalog] 选择要添加到您的中的产品的页面 [!DNL Walmart Marketplace] 分类，或者更新产品属性以满足沃尔玛商城的列表要求。 |
| [!UICONTROL Match products on Walmart] | 在中选择一个或多个产品后 [!UICONTROL Draft] 状态，选择 [!UICONTROL Match products on Walmart] 检查可添加到现有产品的选件 [!DNL Walmart Marketplace] 列表。 |
| [!UICONTROL Refresh products] | 使用最新的列表和状态更新显示。 此控件还会将列表视图重置为默认排序顺序并删除任何筛选器。 |
| [!UICONTROL Filter by *状态*] | 通过选择“列表”表格上方的状态卡之一，仅显示具有特定状态的列表。 通过选择删除筛选器 **[!UICONTROL Refresh products]**. |
| [!UICONTROL Sort products] | 通过选择任何列标题来更改列表的排序顺序。 |


**列描述**

| **字段** | **描述** |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Product name] | 来自的产品名称 [!DNL Commerce] 存储目录。 |
| [!UICONTROL SKU (Unique ID)] | 在中分配给产品的SKU [!DNL Commerce] 目录。 |
| [!UICONTROL  Quantity] | Adobe Commerce或Magento Open Source中可用的库存数量。 |
| [!UICONTROL Price] | 产品价格来自 [!DNL Commerce] 存储目录。 目录价格更新将同步到渠道管理器，然后发送到 [!DNL Walmart Marketplace]  以便列出的项目显示当前价格。 |
| [!UICONTROL Status] | 指示中的当前订单状态 [!DNL Commerce] 订单工作流。 当您将产品成功添加到时，状态会更新 [!DNL Channel Manager] 以及匹配市场上的产品。 如果操作失败，列表会显示错误状态。 修复错误后， [!DNL Channel Manager] 重试操作并更新状态。 |
| [!UICONTROL Error Description] | 提供产品的其他错误信息，包括 `[!DNL Error]` 状态。 |

### 关于列表状态

在列表工作区中，状态标签显示产品在 [!DNL Channel Manager] 工作流，以便您确定后续步骤并解决错误。 清单可以具有以下状态标签：

* **[!UICONTROL Draft]** — 标识尚未使用的产品 [已提交至 [!DNL Walmart] 进行匹配](connect-listings-to-marketplace.md#match-products).

* **[!UICONTROL Processing]** — 标识提交以供匹配的产品 [!DNL Walmart Marketplace]. 产品保留在 *正在处理* 状态，直到 [!DNL Walmart] 返回一个HTTP状态消息，指示匹配是否成功，或者是否出现错误。 匹配操作最多可能需要30分钟才能在 [!DNL Walmart Marketplace].

* **[!UICONTROL Match]** — 标识匹配成功的产品 [!DNL Walmart].

  当产品属性值（例如UPC代码）与现有中的UPC值匹配时，就会发生匹配 [!DNL Walmart Marketplace] 列表。 当产品匹配时，Commerce产品选件会添加到现有列表。

  查看 [[!UICONTROL Walmart Marketplace Seller Account Items]](https://seller.walmart.com/items-and-inventory/manage-items) 用于查看更新的产品列表和验证产品详细信息、价格和库存数量的仪表板。

* **[!UICONTROL Match - Match in Stage]** — 标识匹配的产品 [!DNL Walmart] 在2008年12月31日之前 [!DNL Walmart Marketplace] 商店已上线。 当满足以下条件时，具有此状态的产品将自动连接： [!DNL Walmart Marketplace] 商店上线。

* **[!UICONTROL Error]** — 标识与现有产品不匹配的产品 [!DNL Walmart Marketplace] 列表。

* **[!UICONTROL Error description]** — 提供有关列表错误的详细信息。

  解决此错误后，请重新提交产品以进行匹配。 参见 [产品匹配错误故障诊断](connect-listings-to-marketplace.md#troubleshoot-product-match-errors).

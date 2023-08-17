---
title: 将产品添加到渠道管理器
description: '''创建产品分类 [!DNL Walmart Marketplace] 通过将产品从目录添加到在Channel Manager中配置的销售渠道来进行销售。'
feature: Sales Channels, Merchandising, Products
exl-id: 00932df7-bdc7-42a1-b269-88dffcc918bc
source-git-commit: 8a1f95cdb8817cfcc6ffa96b584c66e680a1c282
workflow-type: tm+mt
source-wordcount: '344'
ht-degree: 0%

---


# 将产品添加到 [!DNL Channel Manager]

要将产品添加到 [!DNL Walmart Marketplace] sales channel ，从 [!DNL Commerce] 产品目录并将其导入 [!DNL Channel Manager].
导入过程可能需要30分钟或更长时间，具体取决于您选择的产品数量。

## 先决条件

**[映射目录属性](map-catalog-attributes.md)** — 在 [!DNL Channel Settings] 配置，至少映射一个属性 [!DNL Commerce] 产品目录到其中一个所需的沃尔玛产品标识符 — GTIN、ISBN、ISSN、UPC、EAN。

## 列表要求

[!DNL Commerce] 产品清单必须具有以下必需的属性配置：

- **[!UICONTROL Connect to Channel Manager]** 属性已启用

- 为所需的Walmart属性提供有效值。

   - 至少一个与所需的产品属性之一匹配的产品属性 [!DNL Walmart Marketplace] 产品标识符 — GTIN、ISBN、ISSN、UPC、EAN。

   - 产品价格指定到最多两位小数，例如 `9.99`

   - 产品重量指定到最多两位小数，例如 `1.25`

>[!TIP]
>
>有关优化销售渠道列表的其他信息，请参阅 [Walmart Marketplace列表质量优化指南](https://marketplace.walmart.com/wp-content/uploads/2020/09/WMP_listing_quality_optimization_guide.pdf).

## 添加产品

1. 在连接的销售渠道商店中，选择 **添加产品** 以打开产品目录。

   ![将产品添加到Sales Channel商店](assets/add-initial-products-to-connected-channel.png){width="600" zoomable="yes"}

   目录将在新选项卡中打开。

1. 在目录产品网格中，选择要销售的产品 [!DNL Walmart Marketplace].

   ![将产品发送到Sales Channel商店](assets/select-products-from-catalog.png){width="600" zoomable="yes"}

1. 启用 **[!UICONTROL Connect to Channel Manager]** 选定项目的属性。

   - 从 **[!UICONTROL Actions]**，选择 **[!UICONTROL Update attributes]**.

   - 滚动到 **[!UICONTROL Connect to Channel Manager]** 属性并启用它。

   - 验证产品属性是否至少包含所需产品属性之一 [!DNL Walmart Product IDs].

   - 选择 **[!UICONTROL Save]**.

     此时将显示确认消息。

     ![产品从目录导入到销售渠道确认消息](assets/product-import-from-catalog-confirmation.png){width="400"}

     如果消息指示已计划更新，请使用 [队列:consumers:开始](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/start-message-queues.html) [!DNL CLI] 命令立即处理更新。

     ```bash
     $ bin/magento queue:consumers:start product_action_attribute.update
     ```

1. 导入操作完成后，通过返回到，验证您添加的产品 [!DNL Channel Manager] 并选择 **[!UICONTROL Listings]**.

   最初，产品位于 *草稿* 状态。 选择 **[!UICONTROL Refresh products]** 以更新表。

1. 通过选择更新视图以显示添加到渠道管理器的新产品 **[!UICONTROL Draft]** 状态卡。

   ![产品已导入连接的销售渠道](assets/products-in-marketplace-sales-channel.png){width="400" zoomable="yes"}



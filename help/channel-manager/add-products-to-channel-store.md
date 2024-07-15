---
title: 将产品添加到渠道管理器
description: '通过将目录中的产品添加到在Channel Manager中配置的销售渠道，为 [!DNL Walmart Marketplace] 销售创建产品分类。'
feature: Sales Channels, Merchandising, Products
exl-id: 00932df7-bdc7-42a1-b269-88dffcc918bc
source-git-commit: 0087d60791cf00e4ed2bffe992447ee8e592fd9b
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 0%

---


# 将产品添加到[!DNL Channel Manager]

要将产品添加到[!DNL Walmart Marketplace]销售渠道，请从[!DNL Commerce]产品目录中选择它们并将其导入到[!DNL Channel Manager]。
导入过程可能需要30分钟或更长时间，具体取决于您选择的产品数量。

## 先决条件

**[映射目录属性](map-catalog-attributes.md)** — 在[!DNL Channel Settings]配置中，至少将一个属性从[!DNL Commerce]产品目录映射到所需的沃尔玛产品标识符 — GTIN、ISBN、ISSN、UPC、EAN。

## 列表要求

[!DNL Commerce]产品清单必须具有以下必需的属性配置：

- 已启用&#x200B;**[!UICONTROL Connect to Channel Manager]**&#x200B;属性

- 为所需的Walmart属性提供有效值。

   - 至少有一个产品属性与所需的[!DNL Walmart Marketplace]产品标识符之一(GTIN、ISBN、ISSN、UPC、EAN)匹配。

   - 产品价格指定到最多两位小数，例如`9.99`

   - 产品权重指定到最多两位小数，例如`1.25`

>[!TIP]
>
>有关优化销售渠道列表的其他信息，请参阅[Walmart Marketplace列表质量优化指南](https://marketplace.walmart.com/wp-content/uploads/2020/09/WMP_listing_quality_optimization_guide.pdf)。

## 添加产品

1. 在连接的销售渠道商店中，选择&#x200B;**添加产品**&#x200B;以打开产品目录。

   ![将产品添加到销售渠道商店](assets/add-initial-products-to-connected-channel.png){width="600" zoomable="yes"}

   目录将在新选项卡中打开。

1. 从目录产品网格中，选择要在[!DNL Walmart Marketplace]上销售的产品。

   ![将产品发送到销售渠道商店](assets/select-products-from-catalog.png){width="600" zoomable="yes"}

1. 为所选项目启用&#x200B;**[!UICONTROL Connect to Channel Manager]**&#x200B;属性。

   - 从&#x200B;**[!UICONTROL Actions]**&#x200B;中选择&#x200B;**[!UICONTROL Update attributes]**。

   - 滚动到&#x200B;**[!UICONTROL Connect to Channel Manager]**&#x200B;属性并启用它。

   - 验证产品属性是否至少包含一个必需的[!DNL Walmart Product IDs]。

   - 选择&#x200B;**[!UICONTROL Save]**。

     此时将显示确认消息。

     ![产品从目录导入到销售渠道确认消息](assets/product-import-from-catalog-confirmation.png){width="400"}

     如果消息指示已计划更新，请使用[`queue:consumers:start`](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/start-message-queues.html) [!DNL CLI]命令立即处理更新。

     ```bash
     $ bin/magento queue:consumers:start product_action_attribute.update
     ```

1. 导入操作完成后，通过返回[!DNL Channel Manager]并选择&#x200B;**[!UICONTROL Listings]**&#x200B;来验证您添加的产品。

   最初，产品处于&#x200B;*草稿*&#x200B;状态。 选择&#x200B;**[!UICONTROL Refresh products]**&#x200B;以更新表。

1. 选择&#x200B;**[!UICONTROL Draft]**&#x200B;状态卡，更新视图以显示添加到渠道管理器的新产品。

   ![产品已导入到连接的销售渠道](assets/products-in-marketplace-sales-channel.png){width="400" zoomable="yes"}



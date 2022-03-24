---
title: 将产品添加到渠道商店
description: 通过将产品从目录添加到销售渠道，为Marketplace销售创建产品分类
source-git-commit: 905bedaf1eacdc45b2b7f222e7703e1f7b3dfd9c
workflow-type: tm+mt
source-wordcount: '254'
ht-degree: 0%

---


# 将产品添加到渠道商店

在渠道管理器中，从 [!DNL Commerce] 沃尔玛市场销售目录。

要将产品同步到销售渠道，所选产品必须具有以下属性配置：

- **[!UICONTROL Publish to Channel Manager]** 属性已启用

- 必须至少有一个产品属性与 [必需的Walmart Marketplace属性](map-product-attributes-for-matching.md)-GTIN、ISBN、ISSN、UPC、EAN

保存选择后，渠道管理器会将产品数据导入渠道。 此过程最多可能需要30分钟。

## 将产品添加到销售渠道

1. 打开与渠道管理器商店关联的产品目录。

   从连接的销售渠道商店中，选择 **添加产品**.

   ![将产品添加到连接的渠道](assets/add-initial-products-to-connected-channel.png)

   目录将在新选项卡中打开。

1. 从目录产品网格中，选择要在Walmart Marketplace上销售的产品。

   ![将产品发送到连接的渠道](assets/select-products-from-catalog.png)

1. 启用 **[!UICONTROL Publish to Channel Manager]** 属性。

   - 从 **[!UICONTROL Actions]**，选择 **[!UICONTROL Update attributes]**.

   - 滚动到 **[!UICONTROL Publish to Channel Manager]** 属性并启用该属性。

   - 验证产品属性是否至少包含一个所需的Walmart产品ID。

   - 选择 **[!UICONTROL Save]**.

   此时将显示确认消息。

   ![产品从目录导入到销售渠道确认消息](assets/product-import-from-catalog-confirmation.png)

   如果消息指示已计划更新，则使用 [队列:consumers:开始](https://devdocs.magento.com/guides/v2.4/config-guide/cli/config-cli-subcommands-queue.html) [!DNL CLI] 命令立即处理更新。

   ```bash
   $ bin/magento queue:consumers:start product_action_attribute.update
   ```

1. 返回至 [!DNL Channel Manager].

   导入操作完成后，从 **[!UICONTROL Listings]**. 最初，产品位于 *草稿* 状态。 选择 [!UICONTROL Refresh products]**更新表。

   ![导入连接销售渠道的产品](assets/products-in-marketplace-sales-channel.png)

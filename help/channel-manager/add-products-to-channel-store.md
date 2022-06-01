---
title: 将产品添加到销售渠道商店
description: 为 [!DNL Walmart Marketplace] 通过将产品从目录添加到销售渠道进行销售
exl-id: 00932df7-bdc7-42a1-b269-88dffcc918bc
source-git-commit: e3b12c9ce1ad4b5be17284e98956a773d7ccca24
workflow-type: tm+mt
source-wordcount: '247'
ht-degree: 0%

---


# 将产品添加到销售渠道商店

将产品同步到 [!DNL Walmart Marketplace] “销售渠道”中，您可以从 [!DNL Commerce] 产品目录，并将其导入渠道管理器。 所选产品必须具有以下属性配置：

- **[!UICONTROL Publish to Channel Manager]** 属性已启用

- 必须至少有一个产品属性与 [必需 [!DNL Walmart Marketplace] 属性](map-catalog-attributes.md)-GTIN、ISBN、ISSN、UPC、EAN

从导入产品的流程 [!DNL Commerce] 渠道管理器最多可能需要30分钟或更长时间，具体取决于您选择的产品数量。

## 添加产品

1. 从连接的销售渠道商店中，选择 **添加产品** 打开产品目录。

   ![将产品添加到销售渠道商店](assets/add-initial-products-to-connected-channel.png)

   目录将在新选项卡中打开。

1. 从目录产品网格中，选择要销售的产品 [!DNL Walmart Marketplace].

   ![将产品发送到销售渠道商店](assets/select-products-from-catalog.png)

1. 启用 **[!UICONTROL Publish to Channel Manager]** 属性。

   - 从 **[!UICONTROL Actions]**，选择 **[!UICONTROL Update attributes]**.

   - 滚动到 **[!UICONTROL Publish to Channel Manager]** 属性并启用该属性。

   - 验证产品属性中是否至少包含一个必需的 [!DNL Walmart Product IDs].

   - 选择 **[!UICONTROL Save]**.

      此时将显示确认消息。

      ![产品从目录导入到销售渠道确认消息](assets/product-import-from-catalog-confirmation.png)

      如果消息指示已计划更新，则使用 [队列:consumers:开始](https://devdocs.magento.com/guides/v2.4/config-guide/cli/config-cli-subcommands-queue.html) [!DNL CLI] 命令立即处理更新。

      ```bash
      $ bin/magento queue:consumers:start product_action_attribute.update
      ```

1. 完成导入操作后，请通过返回 [!DNL Channel Manager] 选择 **[!UICONTROL Listings]**.

   ![导入连接销售渠道的产品](assets/products-in-marketplace-sales-channel.png)

   最初，产品位于 *草稿* 状态。 选择 **[!UICONTROL Refresh products]** 以更新表。


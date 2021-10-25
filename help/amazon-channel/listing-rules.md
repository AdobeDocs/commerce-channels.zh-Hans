---
title: 上市规则
description: 使用上市规则可确定作为Amazon Marketplace列表发布的商务目录产品。
redirect_from: /sales-channels/asc/ob-listing-rules.html/sales-channels/asc/ob-listing-preview.html/sales-channels/asc/listing-rule-preview.html
exl-id: b28a625b-64cf-4119-98bb-f1ea33043c8f
source-git-commit: 632157839130461869345724bdfc03b306a4f613
workflow-type: tm+mt
source-wordcount: '953'
ht-degree: 0%

---

# 上市规则

您可以访问用于存储在 [存储仪表板](./amazon-store-dashboard.md).

上市规则定义规则，以确定Amazon销售渠道发布到Amazon的产品。 这些规则提供了许多选项，可用于创建简单到复杂的规则，以将产品作为列表包含或排除。 每个规则都包含设置产品列表资格要求的条件。

您的上市规则会持续与 [!DNL Commerce] 目录。 添加新 [!DNL Commerce] 符合上市规则所设资格要求的产品，将自动处理以在Amazon上市。

- 如果您希望将所有产品发布到Amazon列表，请勿为您的上市规则定义任何条件。

- 如果要限制发布到Amazon的目录产品中的哪些产品，可定义列表规则条件。 定义Amazon上市规则的条件与定义 [购物车价格规则](https://docs.magento.com/user-guide/marketing/price-rules-cart.html){target=&quot;_blank&quot;}。

- 如果您的上市规则排除某个产品，则该产品的资格状态将更改为 `Ineligible`. 不合格的产品不会发布到Amazon。

- 如果Amazon上已列出不符合条件的产品，并且您将Amazon列表与 [!DNL Commerce] 目录产品，Amazon列表的数量将更改为 `0` 以防止产品销售。 Amazon列表可以 [手动删除](./end-listings-manually.md).

数量和资格状态的更改会影响所有在市场上共享Amazon销售商SKU的列表，这些市场中存在的商店在同一地区销售(定义如 _[!UICONTROL Amazon Marketplace Country]_时段 [存储集成](./store-integration.md))。 但是，对共享 [!DNL Amazon Seller SKU] 在某个地区，不会影响该产品在其他国家/地区的Amazon列表。

![上市规则](assets/ob-listing-rules.png)

## 配置列表规则设置

1. 单击 **[!UICONTROL Listing Rules]** 在商店仪表板上。

1. 为要在Amazon上列出的产品的资格定义所需的条件。

请参阅 [示例：定义条件](./ob-define-condition-example.md).

| 字段 | 描述 |
|---|---|
| [!UICONTROL Websites] | 可用选项取决于 [网站](https://docs.magento.com/user-guide/stores/websites-stores-views.html){target=&quot;_blank&quot;}，您已在 [!DNL Commerce] 配置。 为Amazon上列出的合格产品选择网站。 只能选择一个网站，因为每个网站需要在Amazon销售渠道中创建唯一的Amazon商店。 |
| [!UICONTROL Conditions] | 用于定义 [!DNL Commerce] 您的Amazon地区产品资格的属性。 请参阅 [示例：定义条件](./ob-define-condition-example.md). |

## 条件工作区

单击条件中任何以粗体显示的区域可查看各种选项。

- 如果所选网站中的所有产品均符合条件，请勿添加条件。
- 有一组复杂的后端进程可直接与Amazon的系统通信。 根据您尝试列出的项目数以及Amazon系统可能有多忙（例如“黑色星期五”），您的项目可能需要一些时间才能在Amazon上列出。

有关条件的更多信息，请参阅 [描述条件](https://docs.magento.com/user-guide/marketing/price-rules-cart.html){target=&quot;_blank&quot;}。

## 列出规则预览

在修改列表规则的条件定义时，您可以单击 **[!UICONTROL Preview Changes]** 以应用规则更改并查看列表受到的影响情况。 在保存列表规则更改之前，在此列表预览功能中验证您的列表。

您的Amazon列表将根据您的规则和定义的条件进行比较。 然后，您可以查看：

- 哪些产品会根据您当前的 [!DNL Amazon Seller Central] 帐户
- 哪些产品从不合格状态移回合格状态
- 哪些产品属于新的Amazon列表，并会从您的合格添加到您的Amazon列表 [!DNL Commerce] 产品

列表预览功能允许您预览潜在的Amazon列表，并对列表规则进行任何必要的调整。

您的潜在Amazon列表会在 _[!UICONTROL Listing Preview]_页面：

- **[!UICONTROL Ineligible Listings]**  — 根据您当前的上市规则及条件，所列产品不符合Amazon上市资格。

   不合格的产品不会发布到Amazon。 如果Amazon上已列出不符合条件的产品，并且您将Amazon列表与 [!DNL Commerce] 目录产品，Amazon列表的数量将更改为 `0` 以防止产品销售。 要手动删除列表，请参阅 [结束Amazon列表](./end-listings-manually.md). 此处未列出不符合Amazon要求的产品。 这些产品列在 [“不活动的列表”选项卡](./inactive-listings.md).

- **[!UICONTROL Eligible Listings]**  — 根据您当前的上市规则及条件，所列产品符合Amazon上市资格，并符合Amazon要求。 此列表包含您现有的可导入的Amazon列表(如果您 **导入第三方列表** 设置为 `Import Listing` in [列表设置](./third-party-listing-settings.md))。

- **[!UICONTROL New Listings]**  — 列出的产品包括 [!DNL Commerce] 根据您当前的上市规则和条件，对新符合Amazon上市资格的产品进行编目，并创建和发布新的Amazon列表。

### 查看列表预览

1. 单击 **[!UICONTROL Listing Rules]** 在商店仪表板上。

1. 查看或添加 [列表规则](./listing-rules.md).

1. 修改 [列出规则条件](./ob-define-condition-example.md).

1. 单击 **[!UICONTROL Preview Changes]**.

1. 在 _[!UICONTROL Ineligible Listings]_,_[!UICONTROL Eligible Listings]_&#x200B;和 _[!UICONTROL New Listings]_选项卡。

1. 如果您的列表符合您的预期，请单击 **[!UICONTROL Save and close]**.

   如果列表未按预期显示，请单击 **[!UICONTROL Back]** 并修改您的规则和条件，直到列表符合您的预期。

![列出规则预览](assets/amazon-listing-rule-preview.png)

### 列出预览记录

| 字段 | 描述 |
|--- |--- |
| [!UICONTROL Product ID] | 分配给 [!DNL Commerce] 目录产品。 |
| [!UICONTROL Thumbnail] | 显示主产品图像的缩略图。 |
| [!UICONTROL Name] | 在 [!DNL Commerce] [产品网格](https://docs.magento.com/user-guide/catalog/products.html){target=&quot;_blank&quot;}。 |
| [!UICONTROL Type] | 在 [!DNL Commerce] 产品网格。 |
| [!UICONTROL Attribute Set] | 用作产品模板的属性集的名称，在 [!DNL Commerce] 产品网格。 |
| [!UICONTROL SKU] | 分配给产品的唯一库存单位，在 [!DNL Commerce] 产品网格。 |
| [!UICONTROL Visibility] | 指示产品在中可见和管理的位置 [!DNL Commerce] 产品网格。 选项：<ul><li>`Not visible individually`</li><li>`Catalog`</li><li>`Search`</li><li>`Catalog, Search`</li></ul> |
| 状态 | 指示在 [!DNL Commerce] 产品网格。 选项： `Enabled` / `Disabled` |

![列出预览工作流](assets/listing-preview-flowchart.png)
